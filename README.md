# 2022vpython

Web VPython 3.2
ball = sphere(pos = vec(5,10,0), color=color.red)
bo=box(size=vec(2,2,2), pos=vec(0,1.5,0,color=color.blue))
sc=0

box(size = vec(100,1,20))
box(size = vec(5,50,20), pos=vec(50,0,0))
box(size = vec(5,50,20), pos=vec(-50,0,0))

ball.v = vec(25,-10,0)

while True : 

    rate(200)
    k=keysdown()
    ball.pos = ball.pos + ball.v * 0.01

    if ball.pos.y <= 1.5 :
        ball.v.y = -ball.v.y
    
    if ball.pos.x <= -49.5 :
        ball.v.x = ball.v.x+1
        ball.v.x = -ball.v.x
        sc=sc+1
        print("score:"+sc)
    if ball.pos.x >= 49.5 :
        ball.v.x = ball.v.x+1
        ball.v.x = -ball.v.x
        sc=sc+1
        print("score:"+sc)
    ball.v.y = ball.v.y + -9.8 * 0.01
    
    if 'right' in k :
        bo.pos.x += 0.15
    if 'left' in k :
        bo.pos.x -= 0.15
        
    for i in range(1):
        if ball.pos.x*0.1-bo.pos.x*0.1+ball.pos.y*0.1-bo.pos.y*0.1=0:
            print("game over, your scores is" +sc)
            del ball
