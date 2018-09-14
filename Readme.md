# L4D/L4D2 SourceMod Respawn

This plugin allows server admins to respawn dead players.
 A menu which includes a list of dead human players has been introduced, it can be found in the "Player Commands" category of the "Admin Menu".

Original Authors: \
AtomicStryker & Ivailosp \
The AlliedModder page is available [here](http://forums.alliedmods.net/showthread.php?t=96249).

## Installation
Drop l4d_sm_respawn.smx into the "left4dead2/addons/sourcemod/plugins" folder

## Command Usage
`sm_respawn <player1> [player2] ... [playerN] - respawn all listed players and teleport them where you aim`\
The name of players can be partial, if multiple player name matches the pattern, the respawn fails.

## Another Admin Menu
If you want to list all players (including bots and alive players), you can add the following to your `adminmenu_custom.txt`:
```
// Custom admin menu commands.
// For more information:
//
// http://wiki.alliedmods.net/Custom_Admin_Menu_%28SourceMod%29
//
// Note: This file must be in Valve KeyValues format (no multiline comments)
//

"Commands"
{
    "PlayerCommands"
    {
        "Respawn Survivor"
        {
            "cmd"        "sm_respawn #1"
            "admin"        "sm_kick"
            "execute"    "player"
            "1"
            {
                "type"        "player"
                "method"    "name"
                "title"        "Player:"
            }
        }
    }
}
```