## Design Patterns

## [Python Design Patterns: -01- Introduction (medium)](https://medium.com/@mrfksiv/python-design-patterns-01-introduction-54e681aaf2d0)

1. The Singleton
2. The Factory and Abstract Factory
3. The Adapter
4. The Facade (not yet published)

## [DESIGN PATTERNS in PYTHON](https://refactoring.guru/design-patterns/python)
	
	
### Creational Patterns	

  - Simple Factory
	
  - Factory Method
	
  - Abstract Factory
	
  - DAO Factory
	
  - Builder
	
  - Prototype
	
  - Singleton
	
### Structural Patterns	
	
  - Adapter
	
  - Bridge
	
  - Composite
	
  - Decorator
	
  - Facade
	
  - Flyweight
	
  - Proxy

### Behavioral Patterns	
	
  - Chain of Responsibility
	
  - Iterator
	
  - Memento
	
  - State
	
  - Template Method
	
  - Command
	
  - Mediator
	
  - Observer
	
  - Strategy
	
  - Visitor

### [Design Patterns in Python - stack abuse](https://stackabuse.com/design-patterns-in-python/)
  

```diff
Q : 簡單工廠與工廠方法之間的差異?他們看起來類似，差別在於，在工廠方法當中，傳回Pizza(Product)的類別是次類別，能解釋一下嗎?

A : 工廠方法的次類別的確看起來像簡單工廠． 要注意的是，簡單工廠把所有的事情，在一個地方都處理完了； 
+ 然而工廠方法確立的是一個框架，讓次類別決定要如何實踐．

比方說，在工廠方法當中，orderPizza()方法提供了一般的框架，以便建立比薩，
orderPizza()方法依賴工廠方法來建立具象類別，並產生出實際的比薩．
可藉由繼承PizzaStore(Creator)類別，決定實際製造出的比薩是什麼．

而簡單工廠的做法，雖然可以將物件的建立給封裝起來，但是不具備工廠方法的彈性，
- 因為簡單工廠不能改變正在建立的產品！
```

  
<table>
<!-- Row 1 : This is for Columns-->
<tr>
<th>Design Patterns</th>
<th></th>
<th>Refactoring</th>
<th>GeeksforGeeks</th>
<th>NF技術客</th>
<th>github</th>
<th>others</th>
<td>notes</td>
</tr>

<!-- Row : Creational Patterns -->
<tr>
<td><em>Creational Patterns</em></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>

<!--
<!-- Row n of ___________Patterns - [Some_Kind_of_Design_Pattern] 
<td><img src="" height="50" width="75"></td> <!-- side bar : logo 
<td>Some_Kind_of_Design_Pattern</td>
<td>
<a href="">UML</a> &nbsp;&nbsp;&nbsp;
<a href="">code</a> &nbsp;&nbsp;&nbsp;
</td> <!-- Column 1 : Refactoring 
<td><a href=""> ref </a></td> <!-- Column 2 : GeeksforGeeks 
<td><a href=""> ref </a></td> <!-- Column 3 : NF技術客 
<td><a href=""> ref </a></td> <!-- Column 4 : github 
<td><a href=""> ref </a></td> <!-- Column 5 : others 
<td><a href=""> notes </a></td> </td> <!-- Column 6 : notes 
</tr>
-->


<!-- Row 1 of Creational Patterns - Simple Factory -->
<tr>
<td>hard code; client 直接使用工廠方法</td> <!-- side bar : logo -->
<td>Simple Factory</td>
<td></td> <!-- Column 1 : Refactoring -->
<td><a href="https://www.geeksforgeeks.org/factory-method-python-design-patterns/">ref</a></td> <!-- Column 2 : GeeksforGeeks -->
<td></td> <!-- Column 3 : NF技術客-->
<td><a href="https://github.com/faif/python-patterns/blob/master/patterns/creational/factory.py">ref</a></td> <!-- Column 4 : github-->
<td><a href="https://blog.csdn.net/huobanjishijian/article/details/79151351">ref</a></td> <!-- Column 5 : others -->
<td rowspan="4">
  <a href="https://blog.csdn.net/u011654843/article/details/99692401?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task"> ref </a> &nbsp;&nbsp;&nbsp;
  <a href="https://nbviewer.jupyter.org/github/jshuang0520/design_pattern/blob/master/factory_family.ipynb"> note </a> &nbsp;&nbsp;&nbsp;
  <a href="https://www.youtube.com/watch?v=ub0DXaeV6hA"> factory2 </a> &nbsp;&nbsp;&nbsp;
  <a href="https://www.youtube.com/watch?v=xbjAsdAK4xQ"> factory3 </a> &nbsp;&nbsp;&nbsp;
  <a href="https://github.com/bethrobson/Head-First-Design-Patterns/tree/master/src/headfirst/designpatterns"> Head First Python code </a> &nbsp;&nbsp;&nbsp;
  <a href="https://carsonwah.github.io/factory-design-pattern.html"> 3 patterns </a> &nbsp;&nbsp;&nbsp;
</td> 
</tr>


<!-- Row 2 of Creational Patterns - Factory Method -->
<tr>
<td><img src="https://refactoring.guru/images/patterns/cards/factory-method-mini-2x.png" height="50" width="75"> 1個產品，每個產品多個類型; client call 某一個 ConcreteCreator 使用工廠方法把產品做出來，回到 AbstractCreator 做product.doStuff()(doStuff()裡面一系列的prepare(),bake(),cut(),box()就是商業邏輯)</td> <!-- side bar : logo -->
<td>Factory Method</td>
<td>
<a href="https://refactoring.guru/design-patterns/factory-method">UML</a> &nbsp;&nbsp;&nbsp;
<a href="https://refactoring.guru/design-patterns/factory-method/python/example#lang-features">code</a> &nbsp;&nbsp;&nbsp;
</td> <!-- Column 1 : Refactoring -->
<td></td> <!-- Column 2 : GeeksforGeeks -->
<td><a href="https://notfalse.net/3/ioc-di#IoCDI-vs-Factory-Method-Pattern">ref</a></td> <!-- Column 3 : NF技術客-->
<td></td>  <!-- Column 4 : github--> 
<td><a href="https://blog.csdn.net/huobanjishijian/article/details/79151351">ref</a></td> <!-- Column 5 : others -->

</tr>

<!-- Row 3 of Creational Patterns - Abstract Factory -->
<td><img src="https://refactoring.guru/images/patterns/cards/abstract-factory-mini-2x.png" height="50" width="75"> 多個產品，每個產品多個類型 </td> <!-- side bar : logo -->
<td>Abstract Factory</td>
<td>
<a href="https://refactoring.guru/design-patterns/abstract-factory">UML</a> &nbsp;&nbsp;&nbsp;
<a href="https://refactoring.guru/design-patterns/abstract-factory/python/example#lang-features">code</a> &nbsp;&nbsp;&nbsp;
</td> <!-- Column 1 : Refactoring -->
<td><a href="https://www.geeksforgeeks.org/abstract-factory-method-python-design-patterns/"> ref </a> </td> <!-- Column 2 : GeeksforGeeks -->
<td><a href=""> ref </a></td> <!-- Column 3 : NF技術客 -->
<td><a href="https://github.com/faif/python-patterns/blob/master/patterns/creational/abstract_factory.py"> ref </a></td> <!-- Column 4 : github -->
<td>
<a href="https://blog.csdn.net/huobanjishijian/article/details/79151351"> ref </a>
<a href="https://medium.com/design-patterns-with-python/hihih-2ce4b45624d6"> medium </a>
<a href="https://github.com/miguelalba-old/hfdp-python/blob/b35a06a6168bc8b8601d04d7e4f7f33e92d56ea8/factory/pizzaf.py#L147"> pizza code </a>
</td> <!-- Column 5 : others -->

</tr>

<!-- Row 4 of Creational Patterns - DAO Factory -->
<tr>
<td><img src="https://gerardnico.com/_media/lang/java/daoabstractfactorypattern.jpg?ezimgfmt=rs:752x431/rscb1/ng:webp/ngcb1" height="50" width="75"> Aiming to minimize the direct dependency between:
1. application code
2. data access code </td> <!-- side bar : logo -->
<td>DAO Factory</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>
<a href="https://www.oracle.com/technetwork/java/dataaccessobject-138824.html"> J2EE </a> &nbsp;&nbsp;&nbsp;
<a href="https://www.roseindia.net/tutorial/java/jdbc/dataaccessobjectdesignpattern.html">ref2</a> &nbsp;&nbsp;&nbsp;
<a href="https://www.youtube.com/watch?v=1ui5yVMivTo">youtube</a> &nbsp;&nbsp;&nbsp;
<a href="https://gerardnico.com/lang/java/dao">DataBlog</a> &nbsp;&nbsp;&nbsp;
<a href="https://www.baeldung.com/java-dao-pattern">DaoInJava</a> &nbsp;&nbsp;&nbsp;
</td> <!-- Column 5 : others -->

</tr>

<!-- Row 5 of Creational Patterns - Builder -->
<tr>
<td></td>
<td>Builder</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>

<!-- Row 6 of Creational Patterns - Prototype -->
<tr>
<td></td>
<td>Prototype</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>

<!-- Row 7 of Creational Patterns - Singleton -->
<tr>
<td></td>
<td>Singleton</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>

</table>

---

## Discussion

## [Python Design Patterns: For Sleek And Fashionable Code](https://www.toptal.com/python/python-design-patterns)

## [Design Patterns in Python - GOF](https://legacy.python.org/workshops/1997-10/proceedings/savikko.html#gof)

---
## Others

[Python Design Patterns Tutorial - Home Page](https://www.tutorialspoint.com/python_design_patterns/index.htm)