#Feasible region of the LP relaxation of the problem
from pylab import *
import matplotlib.pyplot as plt
import numpy as np

x = np.arange(0,6.8,0.001)
_x = np.arange(-3,5,0.001)
__x = np.arange(-3,5,0.001)

# The lines to plot
y1=(x-4)/2
_y1=(__x-4)/2

y2=(11-x)/3
_y2=(11-_x)/3

m = [0,0,0,0,1,1,1,1,2,2,2,2,3,3,3,4,4,4,5,5,6,6.8]
n = [0,1,2,3,0,1,2,3,0,1,2,3,0,1,2,0,1,2,1,2,1,1.4]
scatter(m,n, s=20 ,marker='o', c='red')
scatter(6.8,1.4, s=20 ,marker='o', c='blue')


# The upper edge of polygon (min of lines y1 & y2)
y3 = np.maximum(y1, 0)

# Set y-limit, making neg y-values not show in plot
plt.ylim(-2, 7)
plt.xlim(-1, 7.8)

# Plotting of lines
plt.plot(x, y1,color='green')
plt.plot(x, y2,color='green')

#Plotting vertical lines
plt.vlines(-1, ymin=-2, ymax=6, color='grey',linestyles='dashed',alpha='0.2')
plt.vlines(1, ymin=-2, ymax=6, color='grey',linestyles='dashed',alpha='0.2')
plt.vlines(2, ymin=-2, ymax=6, color='grey',linestyles='dashed',alpha='0.2')
plt.vlines(3, ymin=-2, ymax=6, color='grey',linestyles='dashed',alpha='0.2')
plt.vlines(4, ymin=-2, ymax=6, color='grey',linestyles='dashed',alpha='0.2')
plt.vlines(5, ymin=-2, ymax=6, color='grey',linestyles='dashed',alpha='0.2')
plt.vlines(6, ymin=-2, ymax=6, color='grey',linestyles='dashed',alpha='0.2')
plt.vlines(7, ymin=-2, ymax=6, color='grey',linestyles='dashed',alpha='0.2')

#Plotting horizantol lines
plt.hlines(-2, xmin=-1, xmax=7.5, color='grey',linestyles='dashed',alpha='0.2')
plt.hlines(-1, xmin=-1, xmax=7.5, color='grey',linestyles='dashed',alpha='0.2')
plt.hlines(1, xmin=-1, xmax=7.5, color='grey',linestyles='dashed',alpha='0.2')
plt.hlines(2, xmin=-1, xmax=7.5, color='grey',linestyles='dashed',alpha='0.2')
plt.hlines(3, xmin=-1, xmax=7.5, color='grey',linestyles='dashed',alpha='0.2')
plt.hlines(4, xmin=-1, xmax=7.5, color='grey',linestyles='dashed',alpha='0.2')
plt.hlines(5, xmin=-1, xmax=7.5, color='grey',linestyles='dashed',alpha='0.2')
plt.hlines(6, xmin=-1, xmax=7.5, color='grey',linestyles='dashed',alpha='0.2')

#Number on the axis
plt.text(.95, -.5, '1')
plt.text(1.95, -.5, '2')
plt.text(2.95, -.5, '3')
plt.text(3.95, -.5, '4')
plt.text(4.95, -.5, '5')
plt.text(5.95, -.5, '6')
plt.text(6.95, -.5, '7')

plt.text(-.25,.95, '1')
plt.text(-.25,1.95, '2')
plt.text(-.25,2.95, '3')
plt.text(-.25,3.95, '4')

#fig= plt.figure()
ax = fig.add_subplot(111)
left=0
right=7.5
low=0
high=6
# Filling between line y3 and line y4
plt.fill_between(x, y3, y2, color='grey', alpha='0.2')

arrow( left, 0, right -left, 0, length_includes_head = True, head_width = 0.15 )
arrow( left, 0, left -right, 0, length_includes_head = True, head_width = 0.15 )
arrow( 0, low, 0, high-low, length_includes_head = True, head_width = 0.15 ) 
arrow( 0, low, 0, low-high, length_includes_head = True, head_width = 0.15 ) 


# Locations to plot text
l1 = np.array((2, -1.5))
l2 = np.array((3, 3))

# Rotate angle
angle = 18
trans_angle = plt.gca().transData.transform_angles(np.array((-15,)),
                                                   l2.reshape((1, 2)))[0]

# Plot text
th1 = plt.text(l1[0], l1[1], 'x\u2081 - 2x\u2082 \u2264 4', fontsize=10,
               rotation=angle, rotation_mode='anchor')
th2 = plt.text(l2[0], l2[1], 'x\u2081 + 3x\u2082 \u2264 11', fontsize=10,
               rotation=trans_angle, rotation_mode='anchor')
th3 = plt.text(6.5, 2, '(6.8,1.4)', fontsize=10,
               rotation=0, rotation_mode='anchor')
th4 = plt.text(7.4, -.5, 'x\u2081', fontsize=10,
               rotation=0, rotation_mode='anchor')
th5 = plt.text(-.5, 5.5, 'x\u2082', fontsize=10,
               rotation=0, rotation_mode='anchor')


#Removing number on axis
plt.axis('off')

plt.grid(linestyle='dotted')
fig=plt.gcf()
fig.savefig('LPR.png', dpi = 100)
plt.show()
