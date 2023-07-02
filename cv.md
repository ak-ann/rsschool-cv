# Anna Zelenkevich
# **Contacts**
* Phone: +375259197578
* E-mail:an.rkkkk@mail.ru
* Location: Mogilev,Belarus
# About me
I’m Student from Mogilev. Now studying in BRU. I plays on nerves and trying to code some intersting projects.I’m learning new Programm languages JavaScript.
# Skills
* HTML
* CSS
* Python
# Code example
```
import turtle
import random
window = turtle.Screen()
window.bgcolor('black')
window.tracer(2)
frame = turtle.Turtle()
frame.penup()
frame.goto(300, 300)
frame.width(3)
frame.pendown()
frame.color('white')
for i in range(4):
    frame.right(90)
    frame.forward(600)
frame.hideturtle()
player = turtle.Turtle()
player.color('blue')
player.shape('triangle')
player.penup()
angle=random.randint(0, 360)
player.right(angle)
goals = []
for i in range(10):
    goal = turtle.Turtle()
    goal.color('red')
    goal.shape('circle')
    goal.penup()
    x = random.randint(-290, 290)
    y = random.randint(-290, 290)
    goal.goto(x, y)
    angle = random.randint(0, 360)
    goal.right(angle)
    goals.append(goal)
def turn_left():
    player.left(20)
def turn_right():
    player.right(20)
def collide(t1, t2):
    dist = t1.distance(t2)
    if dist < 20:
        return True
    else:
        return False
window.listen()
window.onkey(turn_left, 'Left')
window.onkey(turn_right, 'Right')
info = turtle.Turtle()
info.color('white')
info.hideturtle()
info.penup()
info.goto(0, 310)
speed = 1
score = 0
while True:
    player.forward(speed)
    if player.xcor() > 290 or player.xcor() < -290:
        player.right(180)
    if player.ycor() > 290 or player.ycor() < -290:
        player.right(180)
    for g in goals:
        g.forward(speed)
        if g.xcor() > 290 or g.xcor() < -290:
            g.right(180)
        if g.ycor() > 290 or g.ycor() < -290:
            g.right(180)
        if collide(player, g):
            score = score + 1
            info.clear()
            info.write(score, align='center', font=('Arial', 14))
            x = random.randint(-290, 290)
            y = random.randint(-290, 290)
            g.goto(x, y)
            angle = random.randint(0, 360)
            g.right(angle)
turtle.exitoniclick()
```
# languages
English - Pre-Intermediate
Russian - Native
belarusian - Intermediate
