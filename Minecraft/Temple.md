# Temple

**Category:** Minecraft  
**Tag:** minecraft  
**Points:** 25  
**Author:** QWERTZ

## Challenge Description

> The Sculkers conquered my beautiful temple... They want to destroy the holy flag, only known by the original residents of the temple...
>
> mc.pink.bayern -> Temple NPC

## Solution and Thought

### 1. Entering the Temple

First, you gotta find and click the **Temple NPC** to actually enter the challenge world.

*[Insert screenshot: Temple NPC]*

Once you enter the temple, you'll be greeted by a boss who tells you to find the **Resistor**.

*[Insert screenshot: Boss dialogue]*

So, how exactly are we supposed to find this Resistor?

### 2. Finding the Resistor

Well, you could just install a fly hack and fly around the temple mindlessly until you stumble upon something interesting.

Buuuuuut, there's a much easier way!

If you install **Wurst Client**, or any other hacked client with similar features, you'll find two particularly useful hacks.

**PlayerESP**

The first one is **PlayerESP**.

After enabling it, you'll notice something interesting: **NPCs are also considered players by PlayerESP!**

This means you can see the locations of NPCs through walls and other obstacles.

However, there's a small problem. Since there are quite a few actual players on the server, it's difficult to distinguish NPCs from real players using PlayerESP alone.

That's where the second hack comes in handy.

**NameTags**

In Wurst Client, this feature is called **NameTags**.

It basically allows you to see player name tags all the time, even through walls and from a distance. You can also adjust the settings to make the name tags much more visible.

And here's the important part: **NPCs have name tags too!**

Unlike real players, NPCs usually have names that don't look like normal Minecraft usernames.

So, by combining **PlayerESP** and **NameTags**, you can easily spot NPCs hiding around the temple.

*[Insert screenshot: PlayerESP and NameTags enabled]*

*[Insert screenshot: Wurst NameTags settings]*

And voilà! There's a **Sculk Resistor** right there!

### 3. Talking to the Resistor

Now that we've found the Resistor, all we need to do is reach it.

You can either use a fly hack to get there directly or climb up manually if you prefer doing things the legitimate way.

Once you interact with the Resistor, he'll tell you about a mysterious magic spell that nobody knows how to use.

He then gives you this strange code:

`SLQN{D_W3pso3_0i_G4unq3vv_exuqv_o1n3_i1u3}`

*[Insert screenshot: Resistor dialogue]*

Hmm... That looks suspicious.

It certainly doesn't match the flag format of this CTF, which should be `PINK{...}`.

But if you know even a little bit about classical ciphers, you'll probably recognize what's going on here.

**It's a Caesar cipher!**

### 4. Decoding the Magic Spell

A Caesar cipher is a simple substitution cipher that shifts each letter by a fixed number of positions in the alphabet.

Instead of manually trying every possible shift, we can simply use an online decoder:

[Caesar Cipher Decoder — dCode](https://www.dcode.fr/caesar-cipher)

Paste the mysterious code into the decoder:

`SLQN{D_W3pso3_0i_G4unq3vv_exuqv_o1n3_i1u3}`

*[Insert screenshot: Cipher entered into dCode]*

And guess what?

The very first result gives us:

`PINK{A_T3mpl3_0f_D4rkn3ss_burns_l1k3_f1r3}`

The cipher uses a shift of **-3**, meaning each letter is shifted three positions backward in the alphabet.

For example, `SLQN` becomes `PINK`.

That's it! We've successfully recovered the holy flag without having to search every corner of the temple!

## Flag

`PINK{A_T3mpl3_0f_D4rkn3ss_burns_l1k3_f1r3}`