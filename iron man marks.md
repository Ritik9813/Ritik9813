import turtle

# Set up the screen
turtle.hideturtle()
turtle.bgcolor('black')
turtle.setup(500, 600)
turtle.title("Ironman")

# Define the pieces of the Iron Man suit
piece1 = [[(-40, 120), (-70, 260), (-130, 230), (-170, 200), (-170, 100), (-160, 40), (-170, 10), (-150, -10), (-140, 10), (-40, -20), (0, -20)],
          [(0, -20), (40, -20), (140, 10), (150, -10), (170, 10), (160, 40), (170, 100), (170, 200), (130, 230), (70, 260), (40, 120), (0, 120)]]

piece2 = [[(-40, -30), (-50, -40), (-100, -46), (-130, -40), (-176, 0), (-186, -30), (-186, -40), (-120, -170), (-110, -210), (-80, -230), (-64, -210), (0, -210)],
          [(0, -210), (64, -210), (80, -230), (110, -210), (120, -170), (186, -40), (186, -30), (176, 0), (130, -40), (100, -46), (50, -40), (40, -30), (0, -30)]]

piece3 = [[(-60, -220), (-80, -240), (-110, -220), (-120, -250), (-90, -280), (-60, -260), (-30, -260), (-20, -250), (0, -250)],
          [(0, -250), (20, -250), (30, -260), (60, -260), (90, -280), (120, -250), (110, -220), (80, -240), (60, -220), (0, -220)]]

# Set up the goto positions for each piece
piece1_goto = (0, 120)
piece2_goto = (0, -30)
piece3_goto = (0, -220)

# Set up the speed of the turtle
turtle.speed(2)

# Define a function to draw each piece
def draw_piece(piece, piece_goto):
    turtle.penup()
    turtle.goto(piece_goto)
    turtle.pendown()
    turtle.color('red')
    turtle.begin_fill()
    for i in range(len(piece[0])):
        x, y = piece[0][i]
        turtle.goto(x, y)

    for i in range(len(piece[1])):
        x, y = piece[1][i]
        turtle.goto(x, y)
    turtle.end_fill()

# Draw each piece
draw_piece(piece1, piece1_goto)
draw_piece(piece2, piece2_goto)
draw_piece(piece3, piece3_goto)

# Hide the turtle and keep the window open
turtle.hideturtle()
turtle.done()
