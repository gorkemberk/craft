# craft
import random
import discord
from discord.ext.commands import Bot
from discord.ext import commands

bot=discord.Client()
bot_ön=":)"
bot=commands.Bot(command_prefix=bot_ön)


@bot.event
async def on_ready():
    print("Bot çevrimiçi")
    print("isim : {}".format(bot.user.name))
    print("ID:",format(bot.user.id))
    print(str(len(set(bot.get_all_members()))) +"tane kullanıcıya çalışıyor")

@bot.command(pass_conetex=True)
async def hey(ctx):
    await ctx.send("Ben bot craft'im!")

@bot.command(pass_conetex=True)
async def slm(ctx, member:discord.Member):
    urll=["https://i.pinimg.com/originals/fc/ce/70/fcce70539f64385d24306f360ef91338.jpg"]
    embed=discord.Embed(title=ctx.message.author.name +" seni selamlıyor "+member.name)
    embed.set_image(url=random.choice(urll))
    await ctx.send(embed=embed)

@bot.command(pass_conetex=True)
async def nbr(ctx, member:discord.Member):
    urll=["https://img.wattpad.com/fe8d59ac9262f2e81165c909eb6923e9265cd321/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f776174747061642d6d656469612d736572766963652f53746f7279496d6167652f3179746b363367456574735975513d3d2d3333372e313563323438326231346434363330373134353337373431303331382e6a7067?s=fit&w=720&h=720"]
    embed=discord.Embed(title=ctx.message.author.name +" sana naber diyor "+member.name)
    embed.set_image(url=random.choice(urll))
    await ctx.send(embed=embed)




bot.run("ODMyMjE5MjU2MjAwNDk1MTI1.YHgmlA.FZ66uMuEL6pOzWkjUrzEQfxomhM")
