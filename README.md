import discord
from discord.ext import commands

bot = commands.Bot(command_prefix='[')

@bot.event
async def on_ready():
    print(">> Bot is online <<")

@bot.command()
async def Misaka(ctx):
   await ctx.send('https://static.zerochan.net/Misaka.Mikoto.full.2877627.png')

@bot.command()
async def Uiharu(ctx):
   await ctx.send('https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/07dfd8f3-7bf8-4fad-b39a-f6c66911adc6/d60yi57-c483c247-cf4d-4baa-a2ea-abb65d012815.gif?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOiIsImlzcyI6InVybjphcHA6Iiwib2JqIjpbW3sicGF0aCI6IlwvZlwvMDdkZmQ4ZjMtN2JmOC00ZmFkLWIzOWEtZjZjNjY5MTFhZGM2XC9kNjB5aTU3LWM0ODNjMjQ3LWNmNGQtNGJhYS1hMmVhLWFiYjY1ZDAxMjgxNS5naWYifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6ZmlsZS5kb3dubG9hZCJdfQ.Y4T5NXthG0sYkgexOGpdteHzw6sq2UFMQcGWdvuGrwo')

@bot.command()
async def PADORU(ctx):
   await ctx.send('https://media.tenor.com/images/9e38efb026f755e38c69cd6f9ba514d8/tenor.gif')

@bot.event
async def on_message(msg):
    if msg.content == '還在靠北? 禦坂網絡癱瘓了哦':
        await msg.channel.send('還在靠北? 禦坂網絡癱瘓了哦')

@bot.event
async def on_message(msg):
    if msg.content == '10032':
        await msg.channel.send('??')

@bot.event
async def on_message(msg):
    if msg.content.endswith('dc'):
        await msg.channel.send('FAG')
        await bot.process_commands(message)

@bot.event
async def on_message(msg):
    keyword = ['AC', 'Abel', 'dc', 'FAG', '14', '18', '32', '64']
    if msg.content in keyword and msg.author != bot.user:
        await msg.channel.send('FAG')
        
@bot.event
async def on_member_join(member):
    channel = bot.get_channel(749245371443839056)
    await channel.send(f'水啦!!{member} ...出現了!!')

@bot.event
async def on_member_remove(member):
    channel = bot.get_channel(749245445020188672)
    await channel.send(f'{member}離開了這個美好的世界,我們懷念他QAQ')

@bot.command()
async def ping(ctx):    
    await ctx.send(f'{round(bot.latency*1000)} (ms)')

bot.run('NzQ5MjE5ODU1MDkzNDY1MTI5.X0ozXQ.0PUz1acsmoicltHPZyg3AYJNFV4')
