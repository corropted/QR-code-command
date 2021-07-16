# QR-code-command
Allow you to create qr code


https://discord.gg/w6TuebW9Ys


Invite bot : https://discord.com/oauth2/authorize?client_id=806783988051476490&permissions=268435504&scope=bot
```js

//If you want to use it without 
//command handler  or if you got error join https://discord.gg/w6TuebW9Ys and dm me

//Invite  Bot https://discord.com/oauth2/authorize?client_id=806783988051476490&permissions=268435504&scope=bot
const Discord = require('discord.js');
async (client, message, args) => {
let text = (args[0])
        let qrlink = `https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=${link}`
        if (!text) 
        return message.channel.send(` Please provide text!`)

        if (text){
            const attachment = new Discord.MessageAttachment(qrlink, 'qrcode.png');

            const embed = new Discord.MessageEmbed()
            .setTitle('Successfully QR has Code!')
            .attachFiles(attachment)
            .setColor(config.embed.color)
            .setImage('attachment://qrcode.png')
            .setFooter(`requested ${message.author.tag}`)

            message.channel.send(embed)

        } else {
            message.channel.send(`Error`)
        }
```
