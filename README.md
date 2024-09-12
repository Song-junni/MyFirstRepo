# MyFirstRepo
This is my first GitHub repository
\_\_author\_\_ = 'marble\_xu'

import pygame as pg
from . import setup, tools
from . import constants as c
from .states import main\_menu, load\_screen, level

def main():
  game = tools.Control()
  state\_dict = {c.MAIN\_MENU: main\_menu.Menu(),
         c.LOAD\_SCREEN: load\_screen.LoadScreen(),
         c.LEVEL: level.Level(),
         c.GAME\_OVER: load\_screen.GameOver(),
         c.TIME\_OUT: load\_screen.TimeOut()}
  game.setup\_states(state\_dict, c.MAIN\_MENU)
  game.main()
