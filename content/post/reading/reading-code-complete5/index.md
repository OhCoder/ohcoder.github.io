---
title: "读《代码大全（第二版）》笔记（五）"
date: 2013-04-07
slug: reading-code-complete5
image: title.jpg
categories:
  - reading
tags:
  - programming
---

本书的第五部分讲的主题为 **代码改善**。

这一部分总共包括七章，从软件开发的不同阶段以及不同角度进行了描述，当然了，中心就是 **代码改善** 代码的构建、开发者测试、调试、重构以及代码的调整等不同方面进行了讲述。 

下面还是对每一章内容做一个简要的总结。

## 第二十章——软件质量概述

顾名思义，从本章的题目中也可以看出，本章主要是对软件质量做了一个概括，大概描述了一下软件质量都包括哪些方面。

关于软件质量的特性，书中描述说，软件同时拥有外在的和内在的质量特性。软件的外在特性包括(Page.463~Page.464)，

* 正确性(Correctness)       
* 可用性(Usability)         
* 效率(Efficiency)      
* 可靠性(Reliability)       
* 完整性(Integrity)         
* 适应性(Adaptability)          
* 精确性(Accuracy)          
* 健壮性(Robustness)        
  

软件的内在特性包括(Page.464~Page.465)
* 可维护性(Maintainability)         
* 灵活性(Flexibility)       
* 可移植性(Portability)         
* 可重用性(Reusability)     
* 可读性(Readability)       
* 可测试性(Testability)     
* 可理解性(Understandability)           
  

对于外在特性，一部分特性有互相重叠，但有不同的含义，在不同场合侧重点也不一样。相应的，内在特性也是如此。而且内在特性和外在特性之间也不能完全割裂开。关于这一点，我觉得也是很显然的事情，内在的状态会对外在形成影响，外在的表现又会对内在提出要求。

随后，书中说到在哪些方面可以改善软件质量(Page.466~Page.467)。

* 软件质量目标      
* 明确定义质量保证工作          
* 测试策略      
* 软件工程指南          
* 非正式计数复查            
* 正式计数复查      
* 外部审查          
  

接下来，书中列举了一些数据，用来表明不同质量保障技术的效能。我觉得吧，这些数据看看就可以了，因为作者那个年代的移动互联网基本上还没成型，所以这些数据我觉得对于移动互联网并不一定适用，反而对于传统的大型桌面应用可能更适用一些，不过不管怎么说，对于移动互联网这个新型行业而言，去其糟粕，取其精华就好，死搬硬套要不得。

下面说到什么时候应该进行质量保证工作，书中的观点是说，从软件开始构建这个工作就开始了，我觉得这个观点很好，因为构建软件是一项工程，分为不同的阶段，哪一个阶段都应该保证质量，而且越早引入缺陷越晚发现，成本就越高，所以说质量保证工作从前期准备阶段就开始了。随后书中有这样一句话，我产生了一点感想，

>(Page.475)...，因此把时间投入到前期工作中，能让程序员在后期工作中节省更多的时间。这一方法的最终效果是软件的缺陷更少，开发时间更短，成本也更低。

看到这段话之后，我觉得对于做移动互联网开发来说，或许不太合适，因为目前很多移动互联网开发方面的应用属于试探性的开发方式，基本上测试、设计以及开发是交织在一起的。但是抛开这一点不谈，我觉得这句话从侧面也说明了一点，对于传统桌面应用来说，这种方法是在尽可能的压缩编码时间，说句大白话就是把所有设计都做好，编码只是个体力活。很明显，这种方式可以降低编写代码的出错率，保证了软件的质量，从另一方面，我也意识到，软件开发的设计阶段真的很重要。当然了，对于移动互联网的开发来说，这种方式实施起来未免会觉得有些教条。

## 第二十一章——协同构建

本章对结对编程做了介绍，及其好处。随后对代码审查的方法进行了描述，并对如何做审查做了说明，最后还介绍了几种其他类型的协同开发方法。

关于结对编程，说实话，我没有实践过，也不知道是什么样的一种感受，不过倒是可以想象一下，呵呵。对于成功运用结对编程的关键点，书中提到了几点(Page.483~Page.484)，

* 用编码规范来支持结对编程          
* 不要让结对编程编程旁观        
* 不要强迫在简单的问题上使用结对编程            
* 有规律地对结对人员和分配地工作任务进行轮换        
* 鼓励双方跟上对方的步伐        
* 确认两个人都能够看到显示器        
* 不要强迫程序员与自己关系紧张的人组对      
* 避免新手组合      
* 指定一个组长          
  

其实对于这些关键点，我想联想一下都能理解其中的意思，无非都是以人为中心提出的一些建议，让两个结对编程的人能够默契，避免沟通上的一些不畅快。其实我觉得上面这些都不是问题，你想啊，如果一个是MM一个是GG，那么我觉得这些都不是问题鸟，哈哈。开个玩笑，轻松一下。

对于详查(正式审查)，书中提出了一些方法。比如说，详查人员需要哪些角色。说白了，其实就是代码的 <code>review</code>，然后大家坐在一起开会探讨。对于其中的角色，文中列出了五种(Page.486)，

* 主持人        
* 作者      
* 评论员(reviewer)      
* 记录员            
* 经理          
  

<code>主持人</code>其实就是管理详查这个事儿的，保证一定的进度。<code>作者</code>就是码农本人。<code>评论员</code>就是审查代码的人，<code>记录员</code>就是记录问题的人。<code>经理</code>就不用多说了，就是软件项目的负责人。文中有一条建议我觉得是保证顺利实施的关键一点，

>(Page.487)类似的，无论在任何情况下，详查的结果都不应当作为员工表现的评估标准，这种杀鸡取卵的行为不可取。在详查中被检验的代码仍处于开发阶段。对员工表现的评价应当基于最终产品，而不是尚未完成的工作。

关于参与这种审查的人数，作者建议一般不少于三人。随后对具体实施审查的方法进行了描述，这里就不多说了，感觉操作性很强，干巴巴的口头描述实在是有点枯燥。

最后在其他类型的协同开发实践中，作者提到<code>走查</code>。对于走查，引用书中的一段话描述，

> (Page.492)走查是一种很流行的复查方式，这个词的定义很随意，其流行在于某种程度上，人们把任何形式的复查都称为“走查”。

## 第二十二章——开发者测试

本章的一开始，介绍常见的测试方式，并给出了简要的解释(Page.499~Page.500)。

* 单元测试(Unit testing)是将一个程序员或者一个开发团队所编写的，一个完整的类、子程序或者小程序，从完整的系统中隔离出来进行测试。            
* 组件测试(Component testing)是将一个类、包、小程序或者其他程序元素，从一个更加完成的系统中隔离出来进行测试，这些被测试代码涉及到多个程序员或者多个团队。      
* 集成测试(Integration testing)是对两个或更多的类、包、组件或者子系统进行的联合测试，这些组件由多个程序员或者开发团队所创建。这种测试通常在有了两个可以进行测试的类的时候就应该尽快开始，并且一直持续到整个系统开发完成。      
* 回归测试(Regression testing)是指重复执行以前的测试用例，以便在原先通过了相同测试集合的软件中查找缺陷。        
* 系统测试(System testing)是在最终的配置下(包括同其他软硬件系统的集成)运行整个软件。以便测试安全、性能、资源消耗、时序方面的问题，以及其他无法在低级集成上测试的问题。          
  

关于测试的类型，通常分为两大类：黑盒测试(black-box testing)和白盒测试(white-box,或者玻璃盒glass-box)测试。

对于开发者测试来说，书中提到了几种推荐的方法(Page.503)。

* 对每一项相关的需求进行测试，以确保需求都已经被实现。          
* 对每一个相关的设计关注点进行测试，以确保设计已经被实现。      
* 用基础测试(basis testing)来扩充针对需求和设计的详细测试用例。     
* 使用一个检查表，其中记录着你在本项目迄今为止所犯的，以及在过去的项目中所犯的错误类型。            
  

这些测试方法，我觉得还是需要根据实际情况去掌握吧，因为我觉得这些方法主要还是针对于大型桌面软件来说的，对于如今的移动互联网来说，我觉得仅能起参考价值。

对于先写测试还是后写测试，作者推荐还是先写测试。文中说，

> (Page.503)首先写测试用例可以将从引入缺陷到发现并排除缺陷之间的时间缩减至最短。

对于开发者测试，文中提到了一些局限性，这些局限性对于我来说，我觉得还是蛮准的(Page.504)。

* 开发者测试倾向于“干净测试”        
* 开发者测试对于覆盖率有过于乐观的估计      
* 开发者测试往往回忽略一些更复杂的测试覆盖率类型            
  

在测试技巧这一节，文中提到几种测试类型。例如，
* (Page.505)结构化基础测试。
* (Page.509)数据流测试。        
  

本章后面提到了几种测试支持工具。
* (Page.524)Diff工具        
* (Page.524)测试数据生成器      
* (Page.526)覆盖率监视器        
* (Page.526)数据记录器/日志记录器           
* (Page.526)符号调试器          
* (Page.527)系统干扰器      
* (Page.527)错误数据库      
  

说实在的，好多测试工具都木有接触过。算是长姿势，开眼界了。

## 第二十三章——调试

首先，对于调试在软件质量中扮演的角色，引用文中的一句话说是，

> (Page.536)同测试一样，调试本身并不是改进代码质量的方法，而是诊断代码缺陷的一种方法。

在效率低下的调试方法中，作者列举了几种常见的调试方法，在调试之魔鬼指南类型中，作者列举了几种常见错误的调试方法(Page.539)，

* 凭猜测找到缺陷        
* 不要把时间浪费在理解问题上        
* 用最唾手可得的方式修正错误                
  

我估计很多码农都有过这种想法吧，尤其是在压力大，时间紧迫的时候，哈哈。另外，作者还提到一种方式，叫迷信式调试。描述迷信式调试的这一段作者很幽默，一起欣赏下，
>(Page.539~Page.540)撒旦已慷慨地将地狱的某个部分租给那些在调试时怨天尤人的程序员了。每个团队里都也许有这样一个程序员，他总会遇到无穷的问题：不听话的及其，奇怪的编译器错误，月圆时才会出现的编程语言的隐藏缺陷，实效的数据，忘记做的重要改动，一个不能正常保存程序的疯狂的编辑器——你怎么描述这种行为好呢。这就是“迷信式编程(programming by superstition)”。

看到这一段，让我想起酷壳上一篇名为<a href="http://coolshell.cn/articles/2058.html" target="_blank">《各种流行的编程风格》</a>的文章。好吧，我中枪了...
在关于编译器给出语法错误方面，文中介绍了几种调试的方法(Page.549)，

* 不要过分信任编辑器信息中的行号        
* 不要迷信编译器信息            
* 不要轻信编译器的第二条信息        
* 分而治之          
* 找出没有配对的注释或者引号        
  

在修正错误的时候，文中给出了几种建议(Page.550~554)，
* 在动手之前先要理解问题        
* 理解程序本身，而不仅仅是问题      
* 验证对错误的分析          
* 放松一下          
* 保存初始的源代码      
* 治本，而不是治标          
* 修改代码时一定要有恰当的理由          
* 一次只做一个改动          
* 检查自己的改动            
* 增加能暴露问题的单元测试          
* 搜索类似的缺陷            
  

## 第二十四章——重构

重构其实是一个很大的话题。本章对重构进行了简介，并从<code>特定的重构</code>，<code>安全的重构</code>以及<code>重构策略</code>三个方面做了讲解。对于什么情况下进行重构，文中给出了很多条重构的理由，找几条典型的记录下，

* (Page.565)冗长的子程序，在面向对象的编程中，很少会需要用到长度超过一个屏幕的子程序。           
* (Page.567)数据成员被设置为公用            
* (Page.568)在子程序调用前使用了设置代码(setup code)，或在调用后使用了收尾代码(takedown code)       
* (Page.569)程序中的一些代码似乎是在将来的某个时候才会用到的            
  

在特定重构一节，作者对不同层面的重构给出了相应的重构方法。具体都涉及到哪些层面，我想在此列一下，具体的方法就不说了，列出来可真就成了巨人的汗衫了(看过一点<a href= "http://book.douban.com/subject/5273955/" target="_blank">《Window程序设计》</a>那本书的同学笑了)，呵呵。
* 数据级的重构      
* 语句级的重构      
* 子程序级重构      
* 类实现的重构          
* 类接口的重构      
* 系统级重构            
  

其实，我是觉得，对于这些不同层面的重构，其原则只有一个，就是<code>KISS</code>原则。对于不同层级的重构，如果尽可能的保持<code>KISS</code>原则，应该不会有大的偏差，只不过对于不同层级的重构，应用的方法不同而已。但我觉得书中提到的这些方法主要是起到了借鉴作用，还得要具体情况具体分析，似乎这句话听起来有点像废话，其实我的意思是，任何时候都不要太教条，世间没有什么救世主，哈哈。

接下来是安全的重构。这部分主要是在提醒你，重构的时候要注意安全。其实最中心思想就是要避免在重构的过程中犯一些无法纠正的错误。关于这部分，文中也出了一些建议(Page.579~Page.581)，

* 保存初始代码          
* 重构的步伐请小些          
* 同一时间只做一项重构          
* 把要做的事情一条条列出来          
* 设置一个停车场            
* 多使用检查点          
* 利用编译器警告信息            
* 重新测试          
* 增加测试用例          
* 检查对代码的修改          
* 根据重构风险级别来调整重构方法            
  

 这些建议细细品味觉得真的很受用，不过关键还是得根据自己的实际情况落实到实处哇。

关于不宜重构的情况，文中指出，

> (Page.582)不要把重构当作先写后改的代名词。重构最大的问题在于被滥用。

我觉得可能很多人思想上就把重构当成了理所当然的补救措施，从而在开发阶段掉以轻心，降低了代码质量。另外一条是，

> (Page.582)避免用重构代替重写。

## 第二十五章——代码调整策略

关于性能问题，作者说，

> (Page.587)你可以在两个层面考虑性能问题：策略上和技术上。

虽然是从两个层面进行考虑，不过本章只是从策略层面进行了讲解。

首先，对代码调整做了简介，对其中的一些概念做了解释。例如Pareto法则，

>(Page.592)Pareto法则也就是众所周知的80/20法则。它讲述的是你可以用20%的努力取得80%的成绩。这一法则适用于程序设计之外的众多领域，它对程序优化也绝对有效。

这一点很重要。作者也用自己亲身经历的例子做了证明。很多时候，软件运行效率的低下并不是大部分代码有问题，而是一小部分代码出现了问题，只要找到那一小部分就可以对软件的优化起到决定性作用。对于优化，作者列出了一些很荒谬的观点(Page.593~Page.595)。
* 在高级语言中，减少代码的行数就可以提升所生成的机器代码的运行速度，或是减少其资源占用——错误！          
* 特定运算可能比其他的快，代码规模也较小——错误！        
* 应当随时随地进行优化——错误！          
* 程序的运行速度同其正确性同等重要——错误！          
  

对于这些错误的观点，书中展开做了解释。对于我来说，学习占主要成分，不是说这些错误我没有犯过，而是有些错误我还没有想到过...好吧，我很受伤，桑心了。

对于下面这句话，我觉得灰常的在理，

>(Page.596)程序员应当使用高质量的设计，把程序编写正确。使之模块化并易于修改，将让后期的维护工作变得很容易。

关于这句话的理解，我觉得对于软件的优化来说，设计的重要性要大于局部的代码改动。

对于常见的影响性能的热点，书中列举了几点(Page.598~Page.599)。

* 输入/输出操作         
* 分页          
* 系统调用          
* 解释型语言            
* 错误          
  

关于性能的测量，作者给出了很理性的解答。例如，

> (Page.603)性能问题的很多方面都是违反直觉的。...经验对性能优化也没有太大的帮助。...在任何一种因素发生改变后，所有的经验之谈也会成为狗屁。除非对效果进行测量评估，否则你永远也无法确定某次优化所带来的影响。

对于这部分作者给出了自己的一个教训，

>(Page.604)我得到了一个教训，如果没有测量性能变化，那么你想当然的优化结果不过是代码变得更为晦涩难懂了。

说的很明白，对没有确实测量结果的优化，都是毫无道理的。不但如此，还让降低了代码的可读性。

## 第二十六章——代码调整技术

本章主要从代码上对优化做了讲解。首先对于逻辑判断语句提出了一些建议。

* (Page.610)在知道答案后停止判断。例如，在 <code>for</code> 循环中一旦得到结果就跳出循环，减少循环次数。         
* (Page.612)按照出现频率来调整判断顺序。例如，在 <code>if-else</code> 语句和 <code>switch-case</code> 语句中，把预计频繁出现的判断尽量排到前面。         
  

对于循环，也给出了一些建议。
* (Page.616)将判断外提。如果在循环运行时某个判断结果不会改变，你就可以把这个判断提到循环的外面，从而避免在循环中进行判断。          
* (Page.617)合并。合并(jamming)，或融合(fusion)，就是把两个对相同一组元素进行操作的循环合并在一起。此举所带来的好处就是把两个循环的总开销减少至单个循环的开销。        
* (Page.620)尽可能的减少在循环内部做的工作。        
* (Page.621) 哨兵值。当循环的判断条件是一个符合判断的时候，你可以通过简化判断来节省代码运行时间。如果该循环是一个查找循环，简化方法之一就是使用一个哨兵值(sentinel value)，你可以把它放到循环范围的末尾，从而保证循环一定能够中止。        
* (Page.623)把最忙的循环放到最内层。            
* (Page.623)削减强度。削减强度意味着用多次轻量级运算(例如加法)来代替一次代价高昂的运算(例如乘法)。          
  

在数据使用上，同样给出了一些优化的建议。
* (Page.625)使用整型数而不是浮点数。整型数的加法和乘法要比浮点数的相应运算快很多。                    
* (Page.625)数组维度尽可能少。          
* (Page.626)尽可能减少数组引用。        
* (Page.627)使用辅助索引的意思就是天假相关数据，使得对某种数据类型的访问更为高效。书中给出了两种索引方式，一种是字符串长度索引。另一种是独立的平行的索引结构。                    
* (Page.628)使用缓存机制。缓存机制就是把某些值存起来，使得最常用的值会比不太常用的值更容易被获取。              
  

对于表达式方面，也给出了同样的一些建议，不过在这里就不列举了，因为都是用一些比较长的例子，或者是条目一一列举出来的，所以我觉得这里再列举出来感觉也没啥意思。

最后，在子程序方面，也给出了一些优化的建议。

* (Page.639)将子程序重写为内联          
* (Page.640)用低级语言重写代码          
  

好啦，基本上整个这部分讲的就是这些。感觉这部分内容很杂，当然主题还是代码优化，只不过涉及到的面比较广，所以给人的感觉就比较杂。不过还好，一路看下来，并没有感到特别的云里雾里的。中心思想还是比较清晰的，脉络也比较清晰。        