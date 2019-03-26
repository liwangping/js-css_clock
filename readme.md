transition-timing-function 属性规定过渡效果的速度曲线。
cubic-bezier(n,n,n,n)	在 cubic-bezier 函数中定义自己的值。可能的值是 0 至 1 之间的数值。


const secondsDegrees = ((seconds/60)*360+90);
const minsDegrees = ((mins/60)*360+(seconds/60)*6+90);
const hoursDegrees = ((hours/12)*360+(mins/60)*30+(seconds/60)*6+90); secondHand.style.transform = `rotate(${secondsDegrees}deg)`;
minHand.style.transform = `rotate(${minsDegrees}deg)`;
hourHand.style.transform = `rotate(${hoursDegrees}deg)`;
后面的`rotate(${hoursDegrees}deg)`属于es6中的一些使用技巧可以绑定数据。改变相应元素的旋转角度。
上面的角度计算中，为了使时针的指向更为精确加上了分针的计算
setInterval(setDate,1000);定时器持续更新。