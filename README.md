# Single server with infinite capacity (M/M/1):(oo/FIFO)
## Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 12 seconds, serivice time of lathe machine follows exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

## Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

![image](1.png)

This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.

## Procedure :

![imAGE](2.png)



## Experiment:


 
## Program
arr_time=float(input("Enter the mean inter arrival time of objects from Feeder(insecs):"))
ser_time=float(input("Enter the mean interservice time of Lathe Machine(insecs): "))
Robot_time=float(input("Enter the Additional timetaken for the Robot(insecs): "))
lam=1/arr_time
mu=1/(ser_time+Robot_time)
print("--------------------------------------------------------------")
print("Single Server with Infinite Capacity-(M/M/1):(oo/FIFO)")
print("--------------------------------------------------------------")
print("The mean arrival rateper second: %0.2f"%lam)
print("The mean service rateper second: %0.2f"%mu)
if(lam< mu):
    Ls=lam/(mu-lam)
    Lq=Ls-lam/mu
    Ws=Ls/lam
    Wq=Lq/lam
    print("Average number of objects in the system :%0.2f"%Ls)
    print("Average number of objects in the conveyor: %0.2f"%Lq)
    print("Average waiting time of an object inthesystem: %0.2f secs"%Ws)
    print("Average waiting time of an object intheconveyor :%0.2fsecs"%Wq)
    print("Probability that the system is busy: %0.2f"%(lam/mu) )
    print("Probability that the system is empty: %0.2f"%(1-lam/mu))
else:
    print("Warning!ObjectsOver flowwillhappenintheconveyor")
print("---------------------------------------------------------------")

## Output :
<img width="838" height="331" alt="image" src="https://github.com/user-attachments/assets/b5beade5-eb7e-46a2-a463-6ccd37641eb5" />

## Result :
Thus, the program has been executed successfully and the required parameters have been calculated as per the given
conditions
