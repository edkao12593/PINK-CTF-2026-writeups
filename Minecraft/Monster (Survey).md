# Monster (Survey)

**Category:** Minecraft  
**Tag:** minecraft  
**Points:** 25  
**Author:** QWERTZ

## Challenge Description

Thanks for participating in PINK+ CTF!

**But... something isnt right???**

Please note that this challenge doesnt count as a tie breaker.

The challenge also provides a link to a Google Forms survey.

## Solution and Thought

### 1. A Surprise Minecraft Challenge

So, this is the last Minecraft challenge of PINK+ CTF!

Interestingly, it was released on the **second day of the competition**, without any warning.

But compared to the other Minecraft challenges, this one is actually pretty easy.

First, you need to open the Google Forms link provided in the challenge description and complete the survey.

After submitting it, you'll receive the following message:

> Thanks for filling out the survey... But why is this a Minecraft Challenge? Rumors say the Guard protecting the Gate got knocked out! And someone is trying to break the Gate? You should check on it! You might need this spell against the Monster: "ANTIPINKMONSTER!"

*[Insert screenshot: Survey completion message]*

Hmm... A guard got knocked out? Someone is trying to break the gate?

And what's with that weird magic spell?

Guess we should head back to Minecraft and find out!

### 2. Finding the Monster

Once you return to the Minecraft server, you'll notice something has changed.

The guard who was previously protecting the gate is now **knocked out**, and the gate is wide open!

The layout has completely changed compared to before.

*[Insert screenshot: Changed server layout and knocked-out guard]*

After entering the gate, you'll find a sign with a strange hexadecimal code written on it.

And behind it is a pretty cool-looking **animated pink monster!**

*[Insert screenshot: The monster and the sign]*

The code on the sign reads:

```
E27D802A74858C4E2A2837F71ABFD7CB
E44A7501412442BDCF3513E2926E72DD
AEAE661BF45048683E4878146C8786A2
```

So... what are we supposed to do with this?

### 3. Figuring Out the Encryption

Remember what the survey told us?

> You might need this spell against the Monster: "ANTIPINKMONSTER!"

Well, with a little imagination, you might start to suspect that the survey actually gave us a **decryption key**, and the code on the sign is the encrypted message.

Let's take a closer look.

The spell is:

`ANTIPINKMONSTER!`

Interestingly, this string is exactly **16 bytes long**.

And you know what else uses a 16-byte key?

**AES-128!**

Now let's examine the ciphertext.

It contains 96 hexadecimal characters, which represent **48 bytes**, or exactly **three 16-byte blocks**.

That's a perfect fit for AES, which operates on 16-byte blocks.

But what mode should we use?

Since the challenge doesn't provide an IV or nonce, we can try **AES-128-ECB** first, as ECB doesn't require either.

Of course, the lack of an IV alone doesn't prove that ECB is being used, but it's a reasonable first guess for a simple CTF challenge.

And as it turns out, that's exactly what we need!

### 4. Decrypting the Ciphertext

We can use Python with the `cryptography` library to decrypt the message.

Here's the script:

```python
from cryptography.hazmat.primitives.ciphers import Cipher, algorithms, modes
from cryptography.hazmat.primitives.padding import PKCS7

ciphertext_hex = (
    "E27D802A74858C4E2A2837F71ABFD7CB"
    "E44A7501412442BDCF3513E2926E72DD"
    "AEAE661BF45048683E4878146C8786A2"
)

key = b"ANTIPINKMONSTER!"

decryptor = Cipher(
    algorithms.AES(key),
    modes.ECB()
).decryptor()

padded = decryptor.update(bytes.fromhex(ciphertext_hex))
padded += decryptor.finalize()

unpadder = PKCS7(128).unpadder()
plaintext = unpadder.update(padded) + unpadder.finalize()

print(plaintext.decode())
```

The script does three things:

1. Converts the hexadecimal string into bytes.
2. Decrypts the ciphertext using **AES-128-ECB**, with `ANTIPINKMONSTER!` as the key.
3. Removes the **PKCS#7 padding** and decodes the result into readable text.

And the output is:

```
PINK{Th3_b1g_b4d_m0nst3r_1s_cr4zy!}
```

There we go!

The decrypted message is a valid PINK+ CTF flag, and the padding is valid too, confirming that our guess was correct.

No complicated reverse engineering, no searching an enormous Minecraft world, and no ridiculous parkour required this time!

Just a survey, a suspicious magic spell, and a little bit of cryptography.

Honestly, a pretty easy and straightforward challenge compared to the other Minecraft ones.

And that's it for the Minecraft category! :3

## Flag

`PINK{Th3_b1g_b4d_m0nst3r_1s_cr4zy!}`