# Latency Protection

This mod is an attempt to prevent players from glitching through protected nodes. By recording position every 20 seconds (This can be changed in settings) and teleporting them on any protection interaction. If a player interacts with a protected node the position will not be recorded for an extra cycle. Before recording a position, the player’s avg_jitter is checked to make sure the player is not lagging out.

The timer for when to record a player position.
``` lua
latency_protection.timer = 20
```

The max jitter a player can have before refusing the position update.
``` lua
latency_protection.jitter_max = 1.5
```
