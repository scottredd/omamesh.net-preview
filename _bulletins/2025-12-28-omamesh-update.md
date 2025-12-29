---
title: "OmaMesh Update — New Year, Live Map, Discord, Channels, OTA Chess, and MeshCore Settings"
date: 2025-12-28
summary: "Live node map details, MeshBot updates, #omawx and #test channels, OTA chess, and the SF9 MeshCore settings recommendation."
---

Hi everyone,

It’s time for another OmaMesh update as we roll into the new year. A lot has been happening quietly on the air, and I wanted to share what’s new — along with a few clarifications that may help set expectations.

🗺️ Live OmaMesh Node Map (and What It Does Not Show Yet)

The OmaMesh map is live and updates automatically based on what’s actually being heard over the air:

👉 https://omamesh.net/map/

You can switch between a geographic map and a sortable node list showing:

- Node role (companion, repeater, room server)
- Last-heard timestamps
- Which nodes are visible vs hidden (no valid GPS fix)

This data is generated entirely from on-air observations — no manual curation — so it reflects what the mesh is actually doing, not what we assume it’s doing.

Important caveat: path visualization is still under construction.
The routes shown today represent observed and logged paths, not the full set of paths that may be possible at any given moment. RF conditions change constantly, and many viable routes simply haven’t been exercised or recorded yet.

In short: the map shows evidence, not limits.

📊 A Few Observations from Recent Data

Based on recent map and routing logs:

- ~60 total nodes seen recently
- ~45 nodes currently advertising valid location data
- 30+ repeaters, ~10 companions, and a small but growing number of room servers
- Coverage now extends well beyond central Omaha into surrounding towns and rural areas

Distances (conservative estimate):
Based on repeatedly observed links between nodes with stable, confirmed locations, several direct connections appear to span roughly 20–40 miles, depending on elevation, antenna placement, and local RF conditions. Longer links may be possible, but distance estimates are intentionally conservative.

Paths / hops:

- 4–6 hop paths are now routine
- 6–8 hop paths have been observed
- Longer paths may absolutely be possible — they just haven’t been reliably exercised or logged yet

As path visualization improves, these numbers will almost certainly evolve.

We're hoping to link in Lincoln soon! Does anyone want to start a LnkMesh?

🤖 MeshBot: Helpful, Experimental, and Still Evolving

MeshBot continues to evolve as a low-key helper on the mesh:

Tiny over-the-air BBS  
Users can post and read short bulletins (bbs list, bbs read, bbs new). Think of it as a minimalist corkboard that works even when nothing else does.

Weather bulletins & on-demand WX  
Periodic updates plus wx / weather replies in a concise, low-airtime format.

Polite transmissions  
MeshBot waits for quiet before speaking on busy channels, helping avoid interruptions during active conversations.

That said, MeshBot is very much a work in progress. Some features — especially those that rely on DM-style back-and-forth (like parts of the BBS) — don’t yet have the same retry and confirmation behavior that phone clients handle automatically. If something doesn’t land on the first try, it’s usually just the mesh doing mesh things.

Think of MeshBot less as infrastructure and more as an experiment you’re welcome to poke at.

There may be an opportunity for others to run MeshBot at their locations to help expand and enrich the area MeshCore scene.

🌦️ The #omawx Channel

There’s a dedicated #omawx channel for weather updates.

How it works:

- MeshBot periodically publishes short, low-airtime weather bulletins
- Anyone can request conditions with wx or weather
- Replies are rate-limited to avoid flooding or stepping on conversations

It’s designed to be useful at a glance — especially for mobile or outdoor nodes.

🧪 The #test Channel

The #test channel exists purely for experimentation.

Use it to:

- Verify routing and hop counts
- Test replies without cluttering public chat
- Watch how messages propagate across the mesh

Send test or testing and you’ll receive a structured response showing timing, hops, and (when available) routing information. It’s a safe sandbox for curiosity.

♟️ Downtown Chess Room Server

One of the more fun experiments on the mesh right now is the Downtown Chess Room Server.

Players exchange moves over the air using standard chess notation  
The room server tracks game state  
A FEN-based visualization tool can reconstruct the board and summarize moves

It’s a great example of what low-bandwidth, store-and-forward networks can do when you lean into constraints instead of fighting them.

⚙️ MeshCore Radio Settings (Important)

OmaMesh does not use default MeshCore modem settings.

Through local testing and real-world use, OmaMesh users have found that Spreading Factor 9 (SF9) performs significantly better than the default SF7, especially for multi-hop reliability.

Recommended OmaMesh MeshCore settings:

- Select USA / Canada (Recommended) preset
- Change Spreading Factor to SF9
- If running a repeater, also set Coding Rate to 8
- Save settings and reboot the device

If your node only works intermittently, only talks to very nearby nodes, or never seems to route beyond one hop, mismatched modem settings are often the reason.

ℹ️ Why SF9?

Spreading Factor controls the trade-off between speed and reliability.

Lower values (like SF7) transmit faster but are easier to lose over distance or noise.  
Higher values (like SF9) transmit more slowly but are far more tolerant of weak signals and interference.

For OmaMesh, reliability matters more than raw speed. SF9:

- Improves long-distance and multi-hop success
- Handles urban noise and imperfect antennas better
- Reduces “it works sometimes” behavior

In short: SF9 trades a bit of speed for a lot of stability, and that’s a good deal for OmaMesh.

💬 Discord (Stable Invite Links)

If you prefer coordinating off-mesh, both communities are active on Discord:

MeshCore (OmaMesh & general MC discussion):  
👉 https://discord.gg/59sbGSCEms

Meshtastic (broader MT community):  
👉 https://discord.gg/meshtastic

These invite links are non-expiring and safe to bookmark.

📡 Meshtastic vs MeshCore (Both Welcome)

Meshtastic remains active and healthy, and many people are happily running it. At the same time, more local users are experimenting with MeshCore for:

- Reliable acknowledgements
- Clearer multi-hop behavior
- Room servers and bots
- More deterministic command / reply handling

There’s no pressure to switch. Running both is common, and experimentation is encouraged.

🔭 What’s Next

A few things I’m exploring:

- Better visualization of paths and hop history over time
- More insight into long-distance and multi-hop routing
- Additional room server experiments
- Optional bridges out of the mesh — without making the mesh dependent on the internet

As always, these are experiments, not prescriptions.

If you’re new, the best way to get started is still the simplest:

- Say hi in public chat
- DM someone nearby
- Or message MeshBot with help and poke around

Thanks for being part of this strange, resilient little network. It’s been genuinely fun watching it grow.

See you on the air,  
Scott  
http://OmaMesh.net
