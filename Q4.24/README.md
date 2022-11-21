# Solution for Q2 (4.24)

## Implementation
- Two different programs are written for the implementation of this problem.
- One is a serial approach that is carried out on a single thread.
- The other is a parallel approach that makes use of the multi-threading idea to implement the different functionalities, such as generating random coordinates, checking whether they lie within the circle, and finally the estimation of pi on different threads.
- The comparision of the two approaches is given in the inferences.
- 800000000 random points were plotted in order to make the estimation.




## Conclusions
- The serial approach takes 17.233197s.
- The parallel approach takes 9.065234s.
- Hence we can see that the serial takes almost 1.9 times longer.

*Thus we can conclude that by taking a multi-threaded approah helps in faster computation*
