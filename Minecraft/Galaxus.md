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

*[Insert screenshot: Galaxus NPC]*

After that, you'll be teleported into a huge custom-made world.

And honestly, this map has a crazy amount of detail. You can really tell how much effort went into building it. TVT

### 2. Understanding the Objective

As the description suggests, this is basically a **Minecraft OSINT** challenge.

You're given a series of pictures, and your job is to locate the exact places shown in those pictures inside the custom world.

Once you're close enough to the correct location, simply type:

`/galaxus`

to mark that location as solved.

You can also use:

`/galaxusbook`

to open a book GUI that shows which locations you've already solved and lets you view the challenge pictures again.

The website linked in the description also provides a gallery of all the pictures, making it pretty convenient to check them outside the game.

*[Insert screenshot: Book GUI]*

*[Insert screenshot: Website gallery]*

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

Other NPC-related locations include:

- **Lonely Hiker**
- **Visitor from Other World**

*[Insert screenshot: Illegal Weed Farm and coordinates]*

*[Insert screenshots: Lonely Hiker and Visitor from Other World, with coordinates]*

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

Now THIS is the really useful one.

The Search feature allows you to specify a block type, and Wurst Client will highlight matching blocks through walls and other obstacles.

In fancy RGB colors too!

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

**Dragon Lair** was actually the **second-to-last** location I found.

*[Insert screenshots: A Red Mushroom, Dragon Lair, A Cozy Place, Inspirational Message, The Holy Hill, and PINK+ Treasure]*

Also, **Inspirational Message** is not inspirational at all lol.

### 6. Over the Clouds

Then there's **Over the Clouds**, which honestly doesn't require any of these fancy detection tools.

All you need to do is...

**Look up.**

Seriously.

If you're using fly hack, just fly straight upward until you reach the structure, then adjust your position a bit to find the correct spot.

And that's basically it!

I heard the intended solution involves using launch pads to get up there and completing some parkour, although I'm not sure exactly how the launch pad system works or how many there are.

But honestly, I couldn't really be bothered figuring that out while I was also dealing with the logic gate challenge at the time. :p

*[Insert screenshot: Over the Clouds]*

### 7. Getting the Flag

After you've successfully located all the places, you can open the book and claim your reward!

The flag will be sent directly to the in-game chat.

Unfortunately, for some reason, I couldn't copy it directly from the chat.

Which was a bit annoying, especially after spending all that time searching for the locations.

Hopefully they make it copyable next time!

Anyway, that's it for Galaxus!

## Flag

`PINK{G4l4xy_t00_sm4ll??}`