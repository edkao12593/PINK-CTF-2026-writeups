# Galaxus

**Category:** Minecraft  
**Tag:** minecraft, osint  
**Points:** 100  
**Author:** QWERTZ

## Challenge Description

 So you like Minecraft OSINT? Well then lets up the difficulty!

 https://galaxus.pink.bayern

 In-game you might need the /galaxus and /galaxusbook command

 mc.pink.bayern -> Galaxus NPC

## Solution and Thought

### 1. Entering the Challenge

Just like the other Minecraft challenges, you first need to enter the server and head to the other side to find the **Galaxus NPC**.

Right-click on it to start the challenge.

<img width="1920" height="1009" alt="2026-11-10_20 17 18" src="https://github.com/user-attachments/assets/bff38915-2b42-43ec-ab7b-d6295cda9ca8" />

After that, you'll be teleported into a huge custom-made world.

And honestly, this map has a crazy amount of detail. You can really tell how much effort went into building it. TVT

### 2. Understanding the Objective

As the description suggests, this is basically a **Minecraft OSINT** challenge.

You're given a series of pictures, and your job is to locate the exact places shown in those pictures inside the custom world.

Once you're close enough to the correct location, simply type:

`/galaxus`

to mark that location as solved,will only work if you are close to it.

You can also use:

`/galaxusbook`

to open a book GUI that shows which locations you've already solved and lets you view the challenge pictures again.

The website linked in the description also provides a gallery of all the pictures, making it pretty convenient to check them outside the game.

<img width="1207" height="917" alt="image" src="https://github.com/user-attachments/assets/1833dc38-33e0-44a8-8f0e-1f0c02a42628" />

<img width="920" height="175" alt="image" src="https://github.com/user-attachments/assets/e548a873-6a01-4f9d-bea8-1091d4587460" />

<img width="1315" height="892" alt="image" src="https://github.com/user-attachments/assets/526db132-0e48-4c12-8c6b-ecbb337fe0ef" />


Almost every picture has some kind of unique landmark, so in theory, this challenge is pretty straightforward.

Just look at the picture, find the place, stand nearby, type `/galaxus`, and repeat.

Sounds easy enough, right?

### 3. General Solving Strategy

Of course, just like in the Temple challenge, you *could* simply use fly hack and wander around mindlessly until you happen to find everything.

But this world is **MUCH bigger**, so doing that would be painful.

Let's do things a bit more efficiently.

One thing you might notice is that the world contains many different **biomes**, and each biome is built using a different block palette.

After observing the provided pictures, you'll notice that most of them seem to belong to different biomes.

So instead of searching the entire world randomly, you can narrow down each picture to its corresponding biome first.

That already saves a lot of time!

But still! Biomes themselves are pretty huge, so how do we reduce the effort even more?

### 4. Using PlayerESP and NameTags

If you've read my Temple write-up, you probably already know about two extremely useful features from **Wurst Client**:

- **PlayerESP**
- **NameTags**

And guess what? They're useful here too!

Some of the challenge pictures actually contain **NPCs**.

Since NPCs are also considered players by PlayerESP, you can spot them through walls and other obstacles.

And with NameTags enabled, you can distinguish NPCs from actual players much more easily.

So the strategy is pretty simple:

1. Identify which biome the picture belongs to.
2. Fly around that biome with **PlayerESP** and **NameTags** enabled.
3. Look for NPCs with unusual names.
4. Compare their surroundings with the provided picture.
5. Go to the correct location and type `/galaxus`.

This makes finding NPC-related locations significantly easier.

Well, except for one particularly annoying location...

**Illegal Weed Farm.**

This one isn't located inside any of the normal biomes.

Instead, it's hidden somewhere in the border ocean, basically in the middle of nowhere.

This one took me WAY too long to find, and it actually ended up being the **last location** I discovered.

<img width="1920" height="1009" alt="2026-11-07_06 47 48" src="https://github.com/user-attachments/assets/2e399509-8386-4bec-812c-662dbb98f6ac" />

Other NPC-related locations include:

<img width="1920" height="1009" alt="2026-11-07_06 26 34" src="https://github.com/user-attachments/assets/47cc7ef3-b8b4-4c9f-a5d1-ae505f043af6" />

<img width="1920" height="1009" alt="2026-11-07_06 08 41" src="https://github.com/user-attachments/assets/10c99b8a-badf-43d2-89b6-059398db31af" />

Also fun fact:you can't normally see this without hack but the npc underground have name tag of stuck! implied they are stucked instead of trying to hide or something...

<img width="1920" height="1009" alt="2026-11-07_06 33 39" src="https://github.com/user-attachments/assets/1b43fe4d-dc3e-4ee2-892b-05de7f7c8493" />


### 5. Using ChestESP and Search

Alright, so we've taken care of the NPC-related pictures.

But what about the ones that **don't have any NPCs**?

Well, after observing the pictures a bit more carefully, I noticed something interesting.

Almost every remaining picture contains blocks that don't really belong in their respective biome.

And this is where two more Wurst Client features come in handy:

- **ChestESP**
- **Search**

**ChestESP**

This one is pretty simple.

It highlights chests through walls and terrain.

If a picture contains a chest, you can use ChestESP to locate it much more easily.

**Search**
<img width="714" height="90" alt="image" src="https://github.com/user-attachments/assets/90a5b6f1-4793-4b10-b302-07ba2661910e" />

Now THIS is the really useful one.

The Search feature allows you to specify a block type, and Wurst Client will highlight matching blocks through walls and other obstacles.

<img width="437" height="311" alt="image" src="https://github.com/user-attachments/assets/c6116bf2-773b-4750-add7-9b1d8e4a1dab" />

In fancy RGB colors too!
<img width="1920" height="1009" alt="2026-11-10_19 32 20" src="https://github.com/user-attachments/assets/6be9d8fa-56ac-4adf-9f4e-bbba2745d3ac" />

So here's what you can do:

1. Look at the challenge picture and determine its biome.
2. Identify a block in the picture that doesn't naturally belong in that biome.
3. Add that block to the **Search** feature.
4. Fly around the biome and look for the highlighted blocks.
5. Once you find something suspicious, compare the surroundings with the picture.

For example, if a picture contains a block that is completely different from the rest of the biome, searching for that block can immediately narrow down the possible locations.

This method works for the following pictures:

- **A Red Mushroom**
- **Dragon Lair**
- **A Cozy Place**
- **Inspirational Message**
- **The Holy Hill**
- **PINK+ Treasure**

**Dragon Lair** was actually the **second-to-last** location I found,partly because its similar to illegal weed farm that its in the outer border of world.

<img width="1920" height="1009" alt="2026-11-07_06 32 01" src="https://github.com/user-attachments/assets/2601eb5b-1770-4413-8cee-8c6827e9d43d" />
<img width="1920" height="1009" alt="2026-11-07_06 35 55" src="https://github.com/user-attachments/assets/80710210-183a-46b6-865e-dd83dea338ed" />
<img width="1920" height="1009" alt="2026-11-07_06 13 11" src="https://github.com/user-attachments/assets/0d0adf39-ad78-47ca-8734-b91dbf3a6490" />
<img width="1920" height="1009" alt="2026-11-07_06 21 21" src="https://github.com/user-attachments/assets/28bd9e1e-07cc-4736-982a-13c12f44e31d" />
<img width="1920" height="1009" alt="2026-11-07_06 12 04" src="https://github.com/user-attachments/assets/56d38a71-a5e9-4342-915d-e3e76b054f6b" />
Holy hill took me a bit of time to find correct angle.
<img width="1920" height="1009" alt="2026-11-07_06 27 42" src="https://github.com/user-attachments/assets/b8019914-b585-486b-b5f7-54b613a8fac4" />



Also, **Inspirational Message** is not inspirational at all lol.
<img width="532" height="252" alt="image" src="https://github.com/user-attachments/assets/fc386f18-0b99-43b7-91fe-785c6c3d2d3a" />


### 6. Over the Clouds

Then there's **Over the Clouds**, which honestly doesn't require any of these fancy detection tools.

All you need to do is...

**Look up.**

Seriously.

If you're using fly hack, just fly straight upward until you reach the structure, then adjust your position a bit to find the correct spot.

And that's basically it!
Might have to adjust location a bit but you will get it eventually.
I heard the intended solution involves using launch pads to get up there and completing some parkour, although I'm not sure exactly how the launch pad system works or how many there are.

But honestly, I couldn't really be bothered figuring that out while I was also dealing with the logic gate challenge at the time. :p


<img width="1920" height="1009" alt="2026-11-10_21 54 51" src="https://github.com/user-attachments/assets/cf404bd1-cac5-4963-9d24-6b09bbeab265" />


### 7. Getting the Flag

After you've successfully located all the places, you can open the book and claim your reward!
<img width="861" height="63" alt="image" src="https://github.com/user-attachments/assets/1ccc5f2b-f64f-41b2-8c06-87b54d40bdf2" />

The flag will be sent directly to the in-game chat.

<img width="353" height="34" alt="image" src="https://github.com/user-attachments/assets/ecde7cbd-3325-4088-a6e5-1b58ce8ee638" />

Unfortunately, for some reason, I couldn't copy it directly from the chat.

Which was a bit annoying, especially after spending all that time searching for the locations.

Hopefully they make it copyable next time!

Anyway, that's it for Galaxus!

## Flag

`PINK{G4l4xy_t00_sm4ll??}`
