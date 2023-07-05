# hierst_painting.import turtle as turtle_module

import random
tim = turtle_module.Turtle()
turtle_module.colormode(255)
tim.speed("fastest")
tim.penup()




color_list = [(237, 227, 216), (222, 161, 74), (19, 43, 84), (135, 63, 85), (166, 65, 47), (224, 234, 229),
              (240, 198, 72), (32, 110, 139), (57, 49, 35), (123, 38, 59), (192, 135, 156), (22, 86, 61), (60, 132, 76),
              (223, 87, 45), (150, 184, 173), (228, 174, 190), (190, 101, 130), (143, 164, 182), (28, 66, 57),
              (167, 203, 198), (59, 72, 41), (74, 154, 89), (35, 47, 102), (56, 29, 47)]
tim.setheading(225)
tim.forward(300)
tim.setheading(0)
number_of_dots = 100
for dot_count in range(1, number_of_dots+1):
    tim.dot(10, random.choice(color_list))
    tim.forward(50)

    if dot_count % 10 == 0:
        tim.setheading(90)
        tim.forward(50)
        tim.setheading(180)
        tim.forward(500)
        tim.setheading(0)


screen = turtle_module.Screen()
screen.exitonclick()

