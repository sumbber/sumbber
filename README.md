import discord
import random
from discord.ext import commands

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='/', intents=intents)
items = {
        'бумага': '2-5 месяцев',
        'банановая кожура': 'от 2 до 5 недель',
        'пластиковая бутылка': '400 лет'
}
@bot.event
async def on_ready():
    print(f'We have logged in as {bot.user}')
@bot.command()
async def podelka(ctx)
    await ctx.send(f'https://www.youtube.com/watch?v=fHL7vMqwI2Q')
    
@bot.command()
async def a(ctx, item):
    if item in items:
        time_to_decompos = items[item]    
        await ctx.send(f'Предмет {item} разлагается {time_to_decompos}')
    else:
        await ctx.send('информация не найдена')
bot.run('MTEzOTg4NDc4OTE5Mzc4OTQ2MQ.G5rPAY.7JcPUeEmn09iAEp8yg0gJRUWTlF-tQ65HXXU2g')
