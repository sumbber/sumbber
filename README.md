import discord
from discord.ext import commands

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='$', intents=intents)

@bot.event
async def on_ready():
    print(f'We have logged in as {bot.user}')

@bot.command()
async def hello(ctx):
    await ctx.send(f'Привет! Я бот {bot.user}!')

@bot.command()
async def heh(ctx, count_heh = 5):
    await ctx.send("he" * count_heh)
@bot.group()
async def cool(ctx):
    
    if ctx.invoked_subcommand is None:
        await ctx.send(f'No, {ctx.subcommand_passed} is not cool')
@cool.command(name='bot')
async def _bot(ctx):

    await ctx.send('Yes, the bot is cool.')


bot.run("MTEzMjI3Nzc1MjQwMjI4ODc1MA.GneukO.2eBq3DeNKkgb2jy1ju-eC3AqAFncpv0jtanX9g")
