# Mine.js
A wonderful way to connect Minecraft players.

### Purpose
Provide the most easiest API for developers, with performance, security and integrity. This project was made by developers for use of other developers.

### Features
- Made using Node.js 8.4 and PM2
- Promise support
- Integrated DBMS and Log API  
- Support for different runtime environments
- The most easiest Minecraft Server API
- Source-scallable support
  
## API Examples

### Listeners

When a player teleports to another Location:  
```javascript
mc.on('player.teleport', async(event) => {
    const { player, from, to } = event;
    console.log('Player %s just teleported from %s to %s', from.format(), to.format());
});
```
  
Now teleporting a specific Player:   
```javascript
mc.getPlayer('wofdwid').teleport('world', { x: 20, y: 56, z: -33 }).then((result) => console.log('teleported'));

// or multiple players
mc.getPlayer('wofdwid', 'carlosjd2', ...).teleport('world', { x: 20, y: 56, z: -33 }).then((result) => console.log('multiple teleported'));
``´
