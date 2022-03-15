    if (message.content.startsWith(`${prefix}off`)) {
        if (!message.member.hasPermission("MANAGE_MESSAGES"))
            return message.channel.send("**관리자 권한이 필요합니다.**");
        message.delete()
        var d = new Date();
        var currentTime = d.getHours() + "시 " + d.getMinutes() + "분 ";
        var oo1_embed = new (require("discord.js").MessageEmbed)()
        oo1_embed.setColor('ff0000')
        oo1_embed.setTitle(":red_circle:서버 오프")
        oo1_embed.setDescription('> 서버가 오프 되었습니다.\r> 서버가 온 되었다고 공지가 올라왔을때까지 기다려주세요!')
        oo1_embed.setFooter(`ICE BEAR 서버 • ${currentTime}`)
        client.channels.cache.get(CHA).send(oo1_embed)
