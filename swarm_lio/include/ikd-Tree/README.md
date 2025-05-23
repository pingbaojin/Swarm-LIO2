# ikd-Tree
**ikd-Tree** is an incremental k-d tree designed for robotic applications. The ikd-Tree incrementally updates a k-d tree with new coming points only, leading to much lower computation time than existing static k-d trees. Besides point-wise operations, the ikd-Tree supports several features such as box-wise operations and down-sampling that are practically useful in robotic applications.



### Developers

[Yixi Cai 蔡逸熙](https://github.com/Ecstasy-EC): Data structure design and implementation

[Wei Xu 徐威](https://github.com/XW-HKU): Incorporation into LiDAR-inertial odometry package ([FAST_LIO2 Released](https://github.com/hku-mars/FAST_LIO))

More details please refer to our paper and video~



### Related paper

**Related paper** available on arxiv:

[ikd-Tree: An Incremental K-D Tree for robotic applications](https://arxiv.org/abs/2102.10808)

**Related video**: https://youtu.be/ueOunk03zxA



## Version 2

- We upgraded our **ikd-Tree** to achieve a more stable and efficient performance. More details are shown as follows:
  - Replace the queue and priority queue in STL with our code to avoid memory conflicts.
  - Fix some bugs in re-building of the previous version, which may result in information loss during the multi-thread re-building process. 
  - Add a new parameter `max_dist` to support ranged search to achieve faster nearest search in robotic applications.
  - Fix minor bugs to improve the overall performance. 

