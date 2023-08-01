import discord
from discord.ext import commands

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='/', intents=intents)

@bot.event
async def on_ready():
    print(f'We have logged in as {bot.user}')

@bot.command()
async def hello(ctx):
    await ctx.send(f'Привет! Я бот {bot.user}!')

@bot.command()
async def creator(ctx):
    await ctx.send(f'Я бот созданый Abama_Cursed!')

@bot.command()
async def roblox(ctx):
    await ctx.send(f'Урааааа роблокс!')

@bot.command()
async def plak(ctx):
    await ctx.send(f'https://tenor.com/view/%D0%BF%D0%BE%D0%BF%D0%BB%D0%B0%D1%87%D1%8C-%D0%BF%D0%BB%D0%B0%D0%BA%D1%81%D0%B0-gif-25360320')

bot.run("token")
