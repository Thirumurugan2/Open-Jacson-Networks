![image](https://github.com/Thirumurugan2/Open-Jacson-Networks/assets/162677168/572b04e5-a56e-4188-80b1-9a10bc31449f)![image](https://github.com/Thirumurugan2/Open-Jacson-Networks/assets/162677168/9ce3435d-2905-40f6-8d58-4b2372ef99b3)![image](https://github.com/Thirumurugan2/Open-Jacson-Networks/assets/162677168/9f91504a-e3b7-4e10-948b-61be02d70e83)# Series Queues with infinite capacity - Open Jackson Network

## Aim :
To find (a) average number of materials in the system (b) average number of materials in the each conveyor of (c) waiting time of each material in the system (d) waiting time of each material in each conveyor, if the arrival  of materials follow Poisson process with the mean interval time 12 seconds, service time of  lathe machine in series follow exponential distribution  with service time  1 second, 1.5 seconds and 1.3 seconds respectively and average service time of robot is 7 seconds.

## Software required :
Visual components and Python

## Theory

![image](https://user-images.githubusercontent.com/103921593/203239736-7b81f599-71a8-4ae7-b63e-5d98acd9ea54.png)


## Procedure :

![image](https://user-images.githubusercontent.com/103921593/203239789-bc870dce-6727-487b-a0e2-4fc3f5114889.png)


## Experiment:
![image](https://github.com/Thirumurugan2/Open-Jacson-Networks/assets/162677168/a94b7876-d0e9-4de5-8069-3a9b4d456410)
![image](https://github.com/Thirumurugan2/Open-Jacson-Networks/assets/162677168/be83382d-538a-44e1-a8ec-aa8070780ae1)
![image](https://github.com/Thirumurugan2/Open-Jacson-Networks/assets/162677168/2a6d3ce2-b5b7-425e-ad85-8481ef08bd2e)
![image](https://github.com/Thirumurugan2/Open-Jacson-Networks/assets/162677168/c9dc46fe-47ff-48fd-9c88-7fc70566654c)



## Program
```
DEVELOPED BY : Thirumurugan R
REGISTER NO : 212223220118

arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs): "))
ser_time1=float(input("Enter the mean  inter service time of Lathe Machine 1 (in secs) :  "))
ser_time2=float(input("Enter the mean  inter service time of Lathe Machine 2 (in secs) :  "))
ser_time3=float(input("Enter the mean  inter service time of Lathe Machine 3 (in secs) :  "))
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) :  "))
lam=1/arr_time
mu1=1/(ser_time1+Robot_time)
mu2=1/(ser_time2+Robot_time)
mu3=1/(ser_time3+Robot_time)
print("-----------------------------------------------------------------------")
print("Series Queues with infinite capacity- Open Jackson Network")
print("-----------------------------------------------------------------------")
if (lam <  mu1) and (lam <  mu2) and (lam <  mu3):
    Ls1=lam/(mu1-lam)
    Ls2=lam/(mu2-lam)
    Ls3=lam/(mu3-lam)
    Ls=Ls1+Ls2+Ls3
    Lq1=Ls1-lam/mu1
    Lq2=Ls2-lam/mu2
    Lq3=Ls3-lam/mu3
    Wq1=Lq1/lam
    Wq2=Lq2/lam
    Wq3=Lq3/lam
    Ws=Ls/(3*lam)
    print("Average number of objects in the system S1 : %0.2f "%Ls1)
    print("Average number of objects in the system S2 : %0.2f "%Ls2)
    print("Average number of objects in the system S3 : %0.2f "%Ls3)
    print("Average number of objects in the overall system    : %0.2f "%Ls)
    print("Average number of objects in the conveyor S1  :  %0.2f "%Lq1)
    print("Average number of objects in the conveyor S2  :  %0.2f "%Lq2)
    print("Average number of objects in the conveyor S3  :  %0.2f "%Lq3)
    print("Average waiting time of an object in the conveyor S1 : %0.2f secs"%Wq1)
    print("Average waiting time of an object in the conveyor S2 : %0.2f secs"%Wq2)
    print("Average waiting time of an object in the conveyor S3 : %0.2f secs"%Wq3)
else:
    print("Warning! Objects Over flow will happen in the conveyor")
print("----------------------------------------------------------------------")

```


## Output
![image](https://github.com/Thirumurugan2/Open-Jacson-Networks/assets/162677168/55dacd91-f7d2-42a2-a240-433942f42cba)


## Result
The average number of material in the sysytem and in the conveyor and waiting time are successfully found

