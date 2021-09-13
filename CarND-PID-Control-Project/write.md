## Results Projection

Components of PID-

P comp: - It tells about the car  that will steer propotional to cross track error(CTE). CTE is considered to mark the  deviation of the car from the center of track called as reference trajectory. 

If your car is found to be at the left of the center we will steer it back to center by moving right. But here the car overshoots when it moves to right and then it tries to move left and and it continues. This  tells that the steering value is much propotional to CTE. We estimated the P value to a low value to reduce the direct propotionality.

D comp: It tells about the rate of change of CTE. This means if the derivative is changing quickly, the car  moves quickly towards center as in case of a curve where steering values are normally higher. If the value of this component is less then we consider the oscillations are too much. To reduce the oscillations we kept the value of this component to be a bit higher

I comp:- This tells the sum of all CTE's at a point. If I component is too high, then the car oscillates too much and does not tends to pick up speed. So we choose the value of I to be really small.

## Parameters:

About Tuning Parameters:

Rise time – the time taken to move from the beginning  to the target point

Overshoot – amount that can change too much; the value considered more than the error

Settling time – the time  taken to settle back down when encountering a change

Steady-state error – the error found at the equilibrium

Stability – the “smoothness” of the speed

## Final Tuning:

P - 0.15

I - 0.0005

D - 2.0

we found out this parameters through Manual Tuning.

The way we tuned the constants is as follows:

we set Kp, Ki, and Kd to 0. This will disable them initially

we increased Kp until the error is fairly small, but it still gets from the beginning to nearly the end quickly enough. 

We increased Kd until any overshoot  may have occured minimally. But have to be careful with Kd – as too much will make it overshoot. 

We increased Ki until any error existing is eliminated. We started with a really small number for Ki, as small as 0.0001 or even smaller.

Using the rules of tuning the constants we  changed around the constants a little bit to get it working to the best performance.