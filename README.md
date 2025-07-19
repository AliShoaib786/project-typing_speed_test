# project-typing_speed_test
ais ma hum joo haa app ki typing speed ko test kary gy   agr ais ma koi error arah haa app ais ko bhi count kary gy 


from time import *
import random as r

from numpy.ma.core import around

print(time())

def mistake(paratest,usertest):
    error=0
    for i in range(len(paratest)):
        try:
            if paratest[i] != usertest[i]:
                error=error+1
        except:
            error=error+1
    return error

def speed_time(time_s,time_e,userinput):
    time_deply=time_e-time_s
    time_R=round(time_deply,2)
    speed=len(userinput)/time_R
    return round(speed)


test=['A paragraph is self contained unit of discourse in writing dealing with particlar points or ideas',
'my name is ali shoaib','wellcome to wscube tech']
test1=r.choice(test)
print(" ******* Typing Speed *******")
print(test1)
print()
print()

time_1=time()
testinput=input('Enter :')
time_2=time()

print(' speed : ',speed_time(time_1,time_2,testinput),'word/sec')
print('Error : ',mistake(test1,testinput))
