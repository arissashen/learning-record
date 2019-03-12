### 软件测试方法

#### 等价类划分法

属于黑盒测试  
将不能穷举的测试过程进行分类  
**注意：（求和的例子）一个框输入正确的值，一个框输入错误的值，才能更容易确定是哪个输入框出现错误的值**

步骤  
>先确定有效等价类和无效等价类  
>有效等价类即题目条件（边界值、中间随意一个值）  
>无效等价类先划分与条件相反的情况，再找到特殊情况（中文、英文、特殊符号、空格、不输入、被和谐词）  
>>正整数-->小数、**负数**

#### 边界值

找到有效等价类和无效等价类的边界点，对边界点数据专门进行测试
>对边界值（0、100）及**边界值两边**的数（-1、1、99、101）分别进行测试  
>>数字和字母组合-->数字和字母组合、纯数字、纯字母  

#### 因果图法

步骤  
>找到所有输入条件并编号  
>找到所有输出条件并编号  
>找到所有输入、输出的制约关系

#### 判定表

组成
>条件桩：所有条件  
>动作桩：所有输出  
>条件项：针对条件桩的取值  
>动作项：条件项的各种取值情况下的输出结果  

步骤
>列出所有条件桩和动作桩  
>填写条件桩和动作桩中的项目  
>简化判定表  




