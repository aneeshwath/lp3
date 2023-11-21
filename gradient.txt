cur_x=3
rate=0.01
precision=0.00001
previous_step_size=1
max_iters=1000
iters=0
df=lambda x:2*(x+5)
while previous_step_size>precision and iters<max_iters:
    prev_x=cur_x
    cur_x=cur_x-rate*df(cur_x)
    previous_step_size=abs(cur_x-prev_x)
    iters=iters+1
    print("Iterations",iters,"\nX value=",cur_x)
print("local minima at",cur_x)