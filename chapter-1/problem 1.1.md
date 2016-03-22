#problem 1.1
##2013301020008 方鹏程
##摘要
利用Euler方法解决一些常微分方程问题，并利用python中的matplotlib做出解的有关图像，并联系使用该画图功能，如调整线条的颜色与形状，和做些文字标注。
##正文
在利用程序计算时，选定一定的时间间隔，带入自愿落体速度公式进行计算即可。程序如下：
<pre><code>from pylab import * 
import pickle 

v = []
t = []
g = 9.8
dt = 0.1
v.append(0)
t.append(0)
end_time = 10

for i in range(int(end_time / dt)):
	tmp = v[i] - g * dt
	v.append(tmp)
	t.append(dt * (i + 1))
	print t[-1], v[-1]

plot(t,v)
plt.title("1.1_v-t")
plt.xlabel("t(s)")
plt.ylabel("v(m/s)")
show()
</code></pre>
图片如下
![](https://github.com/aquantumcat/computationalphysics_N2013301020008/blob/master/chapter-1/exercise1.1.png)

##结论
Euler方法对于解决这种简单的方程，非常方便准确。同时也学习到了用python做图的方法。
