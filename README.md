# NosyNeighbour
Keeps an eye on your pesky doorcamping neighbours


## idea

Required inputs:
- Steam WEB [API key](https://steamcommunity.com/dev/apikey)
- Steam ID of player ([lookup](https://steamid.io/lookup))


- Steam [server queries](https://developer.valvesoftware.com/wiki/Server_queries) for server information
  - Generic information. `A2S_INFO` [([docs](https://developer.valvesoftware.com/wiki/Server_queries#A2S_PLAYER))](https://developer.valvesoftware.com/wiki/Server_queries#A2S_INFO)
  - Detailed information; name, score, online time. `A2S_PLAYER` ([docs](https://developer.valvesoftware.com/wiki/Server_queries#A2S_PLAYER))
- Steam [web API]([https://developer.valvesoftware.com/wiki/Steam_Web_AP](https://partner.steamgames.com/doc/webapi/IPlayerService)) for player's current info
  - Current server info
    - Used to retrieve generic server info with `A2S_INFO`
  - Recently played with player
    - Grants access to `steamid` and `playername`
    - Allows to tie to data from `A2S_PLAYER

### UI
With this information we want to establish the following:


**General info**
- Server IP
- Server name
- Player count (curr/max)
- ping

**Players info**
- Steam_ID
- name + recent names
  - if name changed -> different color
  - hover: recently played as
- online/offline
- online time
- track player (toggle)
- grid
- suspected cheater (toggle)

