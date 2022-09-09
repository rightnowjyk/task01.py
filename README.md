# task01.py
from cs1robots import *

def turn_right(robot):
    for i in range(3):
        robot.turn_left()
    

def move_n_times(robot, n):
    for i in range(n):
        robot.move()
        
create_world(7, 7)

hubo = Robot(orientation='N')
hubo.set_trace("blue")
hubo.set_pause(0.1)

for i in range(3):
    move_n_times(hubo, 6)
    turn_right(hubo)
    hubo.move()
    turn_right(hubo)
    move_n_times(hubo, 6)
    hubo.turn_left()
    hubo.move()
    hubo.turn_left()
    
move_n_times(hubo, 6)
