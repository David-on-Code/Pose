### Single-Stage Multi-Person Pose Machines  
#### Shuicheng Yan  
现存的方法大多是两阶段：  
one stage for proposal generation and the other for 提名生成  
allocating poses to corresponding persons 分配姿态给相应的人  
针对多人pose这方面，主流的方法分为两类:  
1) Top-Down solution。先用一个detector检测出来图像上的所有行人，然后针对每一个检测的出来的human box，做单人pose预测，总共需要2步  
2) Bottom-Up solution。先用一个cnn检测出来图像上所有人的所有关键点，再通过一个聚类算法（或者其它方法）对这些点进行区分，将同一个人的点划分到一起，最后得到所有人的关键点，总共需要2步  
论文提出的方法，一步到位,一次就可以得到多个人的pose点  
![F1](https://github.com/David-on-Code/Pose/blob/master/SPM/F1.png)



