# EnjoyAPI

Ассинхронный клиент для API EnjoyMickeyBot

Установка:





  Через GIT:

```shell
$ pip install git+https://github.com/KotypeyPyEdition/EnjoyAPI
```

Через Pypi:

```shell
$ pip install EnjoyAPI
```

Пример:

```py
from EnjoyAPI.EnjoyAPI import EnjoyAPI


from discord.ext import commands

bot = commands.Bot(command_prefix='>>')

enjoyClient = EnjoyAPI(bot, 'ваш токен тут')
@bot.command()
async def checkUser(ctx: commands.Context, userID: int):
    data = await enjoyClient.check(userID)
    await ctx.send(f'Вот данные от пользователя с ID, ```{data}```')


bot.run('тут токен бота')
```





если будут проблемы/вопросы [Issues](https://github.com/KotypeyPyEdition/EnjoyAPI/issues)
