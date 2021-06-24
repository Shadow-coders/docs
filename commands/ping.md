---
description: Ping pong!
---

# ping

## usage

```bash
<prefix>ping
```

### returns

```bash
> Pong < WS PING >
> latency <DATE.now in ms - MESSAGE.CREATEDSTAMP>
```

## Example:

![](../.gitbook/assets/unnamed.png)

## code

```javascript
module.exports = {
	name: 'ping',
	description: 'Ping!',
	execute(message, args, client) {
		message.channel.send('> Pong ' + client.ws.ping + ' \n > latency: ' + `${Date.now() - message.createdTimestamp}` );
	},
};
```

