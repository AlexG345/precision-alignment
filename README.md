# Precision Alignment Tool
Originally written by Wenli, previously maintained by TweaK.

Adapted calculations from client-sided to server-sided by Summer

The original tool relied on using client-sided prop positions to make constraints on an entity server sided. This may not seem like an issue however, in multiplayer, significant digits are cut to save bandwidth so if you move a prop 0.0001 on the server, its position will update, but the clients will not, because the change is not significant enough. This error leads to inprecise constraints being made with PA in multiplayer. My fix has/will move all math related to WorldToLocal & LocalToWorld from client, to server so that positioning is just as accurate as in singleplayer.
