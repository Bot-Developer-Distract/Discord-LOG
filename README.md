# discord-logs

```js
client.on("messageReactionAdd", (messageReaction, user) => {
   const channel = client.channels.cache.get("1029684021636108338")
    channel.send(`A reaction has been Added to a message ${messageReaction.emoji} has been added to a message by \`${user.tag}\``)
})
```

```js
client.on("inviteCreate", (invite) => {
    const channel = client.channels.cache.get("1031079881334853672")
    channel.send(`An invite has been created by ${invite.inviter.tag}. The code is ${invite.code}`)
})
```

```js
client.on("messageUpdate", (oldMessage, newMessage) => {
    const channel = client.channels.cache.get("1031079881334853672")
    channel.send({ embeds: [ new EmbedBuilder()
    .setColor("Blue").setDescription(`oldMessage : \`${oldMessage.content}\`\n\n newMessage: \`${newMessage.content}\``)]})
})
```

```js
client.on("voiceStateUpdate", (oldState, newState) => {
    const channel = client.channels.cache.get("1031079881334853672")
    channel.send(`${newState.member}'s voice state has been updated`)
})
```

```js
client.on("webhookUpdate", (channel) => {
    const cha = client.channels.cache.get("1031079881334853672")
    cha.send(`A webhook name has been updated in ${channel}`)
})
```

```js
client.on("userUpdate", (oldUser, newUser) => {
    const channel = client.channels.cache.get("1031079881334853672")
    channel.send(`${oldUser.username} has been changed to ${newUser.username}`)
})
```
