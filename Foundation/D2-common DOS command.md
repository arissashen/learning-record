## DOS命令

### 第一部分  

time 
>显示当前计算机的本地时间  

ctrl+c 
>退出当前正在执行的命令  

shutdown /s /t 1800 
>设置自动关机（单位：s）  

shutdown /a 
>取消之前设置的自动关机  

cls 
>清屏  

### 第二部分 

ping 网址
>用于检查当前的网络是否是通的    
>可以得到当前被访问网页的ip地址 

ipconfig -all  
>列出当前计算机的所有网卡信息  
>>ip地址：用于在一个网络内唯一的标识当前计算机（一台计算机的ip地址可以变）。  
>>最早的ip地址为ipv4（已枯竭），现在使用ipv6  
>>mac地址：即物理地址，它是被 烧入 ROM的。用来在全世界唯一标识一台计算机（理论上每台计算机的mac地址是唯一的）。

### 第三部分 

盘符名称: 
>用于切换盘符  
>>根目录：具体的某个盘符的一级目录   
>>**cd只能切子目录，不能切盘符（即无法跨盘符操作）**

cd ..  
>用于返回上一级

cd /  
>用于返回根目录

dir  
>用于列表展示某个目录下的内容

md 路径
>用于创建目录  
>>**创建的是文件夹，而不是某文件**

echo 内容>文件名  
>echo qweasd>f:\test\aa\test.txt    
>通过这种方法间接得到一个文件

rd 路径  
>用于用于删除空目录

rd /s 路径  
>用于删除目录

del 文件名  
>用于删除文件  
>>del 目录  或  del 文件名
>>用于删除该目录下的所有文件，**但该目录下文件夹还存在**  

copy 被复制文件的路径 [目的路径[\重命名]]
>copy aa\qwe.txt **bb\asd.txt** 将该目录下aa文件夹内的qwe.txt文件复制到**该目录下bb文件夹，并重命名为asd.txt**  

move 被剪切文件的路径 目标路径
