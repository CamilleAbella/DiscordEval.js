
# DiscordEval.js

⚠️THIS PACKAGE IS NOT LONGER SUPPORTED, PLEASE USE [`discord-eval.ts`](https://www.npmjs.com/package/discord-eval.ts) INSTEAD ⚠️

## Install

```
npm install discord-eval.js
```

## Syntax

```js
DiscordEval( code, message )
```

**code** :  

> The code that you emulate  
> **Type** : String  

**message** :  

> The message from which the code comes  
> **Type** : Message  

## Example

Here is the minimum required for your Eval command to work. **Think of securing access because a malicious Eval can be devastating for your PC !**

```js
const DiscordEval = require('discord-eval.js')
const Discord = require('discord.js')
const client = new Discord.Client()

client.login("token")

client.on('message',async function(message){
	if(message.content.startsWith("js")){
		let code = message.content.replace("js","").trim()
		await DiscordEval(code,message)
	}
})
```