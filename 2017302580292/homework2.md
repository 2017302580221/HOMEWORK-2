## P3.
### 考虑一个应用程序以稳定的速率传输数据（例如，发送方每A个时间单元产生一个/V比特的数据单元，其中4较小且固定）。另外，当这个应用程序启动时，它将连续运行相当长的一段时间。回答下列问题，简要论证你的回答：
### a.是分组交换网还是电路交换网更为适合这种应用？为什么？
### b.假定使用了分组交换网，并且该网中的所有流量都来自如上所述的这种应用程序。此外，假定该应用程序数据传输速率的总和小于每条链路的各自容M。需要某种形式的拥塞控制吗？为什么？
~~~
a.电路交换网。该程序需要长时间稳定运行，而且所需传输速率较小，相比时延不定的分组交   换，电路交换更合适。

b.不需要，传输速率总和小于链路容量。
~~~
---
## P5.
### 回顾在1.4节中的车队的类比。假定传播速度为lOOkm/h。
### a.假定车队旅行150km:在一个收费站前面开始，通过第二个收费站，并且正好在第三个收费站后面结束。其端到端时延是多少？
### b.重复（a）现在假定车队中有8辆汽车而不是10辆。
~~~
a.  每个收费站间隔75km， 传播时延为75/100km/h=45min
    每个收费站处理的传输时延为10*12s=2min
    得到总的时延是2*45+3*2=96min

b.  传播时延未变，每个收费站的传输时延变为8*12s=1.6min
    总的时延为2*45+3*1.6=94.8min
~~~
---
## P8.
### 假定用户共享一条3Mbps的链路。又设每个用户传输时要求150kbps，但是每个用户仅有10%的时间传输。（参见1.3节中关于“分组交换与电路交换的对比"的讨论。）
### a.当使用电路交换时，能够支持多少用户？
### b.对于本习题的后续小题，假定使用分组交换。求出某给定用户正在传输的概率。
### c.假定有120个用户。求出在任何给定时刻，实际有n个用户在同时传输的概率。（提示：使用二项式分布。）
### d.求出有21个或更多用户同时传输的概率。
~~~
a.用户数为3M/150k=20

b.如题，概率为10%

c.概率p(n)=10%^n*90%^(120-n)
    =0.1^120*9^(120-n)

d.此概率为1-p(0)-p(2)-……-p(20)
    =1-0.1^120*(9^120+9^119+……+9^100)
    =1-0.1^120*9^100*(1-9^21)/(1-9)
    ≈0.003
~~~
 <p align="right">刘涛<br/>2017302580292<br/>2020.03.03</p>