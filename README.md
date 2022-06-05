# Assignment 2
1. (P22, Page294)
```
a. If all the k - 1 packets have been received and acknowledged by the receiver,
   the sender’s window range will be [k, k + 4 - 1] = [k, k + 3] because it is
   sending k and the next 3 after k to have a size of 4. If the acknowledgements
   were not received by the sender, the window will be in the range
   [k - 4, k - 1].
b. If none of the acknowledgements are received by the sender, the 4 last
   packets with be sent, therefore the sender’s range will be [k - 4, k].
```

2. (P27, Page 294)
```
a. The sequence number for the second packet would be 126 + 80 = 206, the source
   port number would still be 302, and the destination port number would still
   be 80 because the packet is being send in the same direction.
b. The acknowledgement number would be for the first packet not yet received,
   i.e. 206. The source port would be 80 and destination would be 302.
c. The acknowledgement number would be for the first packet not yet received,
   i.e. 126.
d. See below:
```
![image](https://user-images.githubusercontent.com/25465133/172072786-d0d0a8c6-d7f1-4822-8ee8-b7415d5f602c.png)

3. (P32, Page296)
```
a. (.729)SampleRTT4 + (.081)SampleRTT3 + (.09)SampleRTT2 + (.1)SampleRTT1
b. 𝛼SampleRTTn + n-1Sumi=1 (1 - 𝛼)(n-i)SampleRTT(n-i)
c. It is an exponential moving average because as n approaches infinity, each
   previous data points become less impactful overall.
```

4. (P40, Page297)
```
a. TCP slow start would be in the intervals [0, 6] & [23, 26], we can see the
   exponential graph detailing this.
b. TCP congestion avoidance is operating between the interval [6, 16] & [17, 22]
   where there are relatively linear data points modeling the behavior of
   congestion avoidance.
c. After the 16th transmission, fast recovery takes place, signifying loss
   detection and not a timeout.
d. After the 24th transmission, slow start takes place, signifying a timeout,
   not loss detection.
e. The initial value of ssthresh is 32 because that is where slow start stops on
   the graph.
f. The value of ssthresh is 21 at the 18th round because it is half the value of
   the congestion window at a lost packet which is 42 in this case.
g. The value of ssthresh is 13 at the 24th round because it is half the value of
   the congestion window at a lost packet which is 26 in this case.
h. The 70th segment is sent in the 7th round. The slow start sends 63 and from
   then each segment is more, therefore the 70th is sent in the 7th.
i. The window size and ssthresh would be half of the window size before the
   loss, i.e. 4.
j. The ssthresh is still 21, however, the congestion window is now 4.
k. 1 + 2 + 4 + 8 + 16 + 21 = 52
```

5. (P44, Page298)(BONUS)
```
a. Considering no loss, it would take 6 RTTs.
b. Average: (6 + 7 + 8 + 9 + 10 + 11)/6 = 8.5
```

6. (P45, Page299)(BONUS)
```
a. Loss Rate
   W/2 + (W/2 + 1) + … + W
   = W/2Sumn=0(W/2 + n)
   = (W/2 + 1)W/2 + W/2Sumn=0n
   = (W/2 + 1)W/2 + (W/2(W/2 + 1))/2
   = (W^2)/4 + W/2 + (W2)/8 + W/4
   = (3/8)W2 + (3/4)W
   L = 1/((3/8)W2 + (3/4)W)

b. Average Rate
   L ≈ 8/3W2
   W ≈ (8/3L)1/2
   Avg = (3/4)(8/3L)1/2(MSS/RTT)
       = (3/4)(8/3)1/2(MSS/(RTT * L1/2))
       = 1.22(MSS/(RTT * L1/2))
       = 1.22*MSS/(RTT * L1/2)
```

7. (P46, Page299)
```
a. maxSize = ((1 * 106 * 150 * 10-3)/(1500 * 8) = 12.5
b. averageWindowSize = 125(.75) = 9.375
   averageThroughput = (9.375 * 1500 * 8)/(150 * 1-3) = 750
c. t = (12.5/2) * 150 * 10-3 = .9375
```
