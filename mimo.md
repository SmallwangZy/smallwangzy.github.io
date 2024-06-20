# Power

How does the power vary in the communication system? look at the figure below:

![image-20240504173336259](https://wang-250-notes-1320145649.cos.ap-nanjing.myqcloud.com/Markdown/image-20240504173336259.png)

$P_{tx}$ is the power of the transmitted antenna, $P_{rx}$ is the power of the received antenna. This system model is a “single to single” antenna communication. $R$ is the distance between two antennas. The relation between $P_{tx}$ and $P_{rx}$:
$$
P_{rx} = \frac{P_{tx}}{4\pi R^2}
$$

but the equation above is built on the ideal condition, in reality, we need consider the influence from the gain of antenna, the equation will be checked as[^3]:
$$
P_{rx}=\frac{P_{tx}}{4\pi R^2}\frac{\lambda^2}{4\pi}G_{tx}G_{rx}
$$
$G_{tx},G_{rx}$ are the gain of transmitted antenna and received antenna respectively. 

## How to do

In summary, following to the equation, if we want to make the received power higher, we could try to:

-  Increase the bandwidth (widely used, but standard will make sure the bandwidth)
- Increase the transmitted power (ok, but there is a limit)
- Enhance the design of antenna, try to change the gain. (physically)
- MIMO: like a idea that invite more people to work rather than work harder by only one person.
- ……





# MIMO

MIMO (Multiple Input Multiple Output) has been widely used in the mobile communication. 

Taking my phone for example, there's definitely not one antenna in a cell phone, there's multiple antennas. A device usually integrate multiple antennas, but it is still a single device in the sight of user.

From a technical standpoint, MIMO actually is a **split spatially**[^1], it allows transmitter and receiver  to communicate by multiple antennas. It **involves** in three key technologies:

- spatial diversity: reliability.
- spatial multiplexing: 
- Beamforming

MIMO aims to increase the **throughput** of the communication system. MIMO is just a technology composed of spatial diversity, spatial multiplexing and beamforming.



## Spatial Diversity

spatial diversity could be divided into transmitted diversity and received diversity. 

Diversity means that multiple antennas are used to transmit or receive signals. Traditional communication use a single antenna to propagate electromagnetic wave but diversity communication use multiple antennas. 

In the spatial diversity, each received antenna should be spaced far apart to assure the irrelevance.

![image-20240504211332002](https://wang-250-notes-1320145649.cos.ap-nanjing.myqcloud.com/Markdown/image-20240504211332002.png)

The figure above shows how transmitter diversity works. it copies the same original data stream to different antenna. This is completely **different from** spatial multiplexing.

The Redundance of the data assures the quality of the communication[^2]. When one data line is faulty, the other data line can be used by the receiver, it decreases the error probability.

## Spatial Multiplexing

Spatial diversity increases the **reliability** of the system, while spatial multiplexing increases the effectivity.

![image-20240504211411188](https://wang-250-notes-1320145649.cos.ap-nanjing.myqcloud.com/Markdown/image-20240504211411188.png)

The data in the transmitter would be divided into multiple parts, each part would be transmitted by different antenna, it increases the speed of communication.

## Beamforming

Beamforming aims to enhance the gain of the signal.

Beamforming could be divided into two categories:

- Analog Beamforming.
- Digital Beamforming (Precoding)

# Precoding in MIMO

Precoding is related to the beamforming. Beamforming is a special case of precoding.[^5] There are three different precoding[^6]:

- Digital Precoding: each antenna needs a single RF chain. (costly in Massive MIMO)
- Analog Precoding only a RF chain with subsequently phase shifters.
- Digital-analog hybrid precoding.

<img src="https://img-blog.csdnimg.cn/0bc537dc7a6343b9a483deb40080eef6.png" style="zoom:50%;" />







# MU-MIMO

MU-MIMO (Multi-user MIMO). it enables AP to process the information from multiple user **at the same time.** 







# Reference

[^1]:[MU-MIMO - 华为](https://support.huawei.com/enterprise/zh/doc/EDOC1100198082)
[^2]:[Fundamentals of MIMO Communication in Wireless Systems](https://resources.system-analysis.cadence.com/blog/fundamentals-of-mimo-communication-in-wireless-systems)
[^3]:[空间分集、空间复用与波束赋形，为什么5G采用多天线MIMO技术？](https://www.bilibili.com/video/BV18h411G7AW?vd_source=a463bfbfd051c81eeb54c8a442c3acd6)

[^4]:[[小白也能看懂]MIMO技术入门，含码字，层映射，天线端口，预编码，PMI，rank，TM模式，波束赋形，空间复用，空间分集，等内  容](https://www.bilibili.com/video/BV1fT4y1A71E?vd_source=a463bfbfd051c81eeb54c8a442c3acd6)

[^5]:[波束赋形和预编码是如何关联的？(How are Beamforming and Precoding Related?)](https://www.bilibili.com/video/BV1v8411c7mg?vd_source=a463bfbfd051c81eeb54c8a442c3acd6)

[^6]:[从模拟预编码到相控阵_rf chain-CSDN博客](https://blog.csdn.net/qq_23947237/article/details/125924927)

[^7]:[MIMO: 最大分集度，自由度，空时编码](https://blog.csdn.net/fanzy_edu/article/details/122843375)
[^8]:[MIMO信道自由度和矩阵的秩的关系](https://wenku.baidu.com/view/73a03744a02d7375a417866fb84ae45c3b35c2a5.html?_wkts_=1716884852210&needWelcomeRecommand=1)

