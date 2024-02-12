# 工厂模式

工厂模式是一种常见的设计模式，用于创建对象。它的主要目的是封装对象创建的过程，使得客户端代码与具体创建逻辑解耦，提高代码的可维护性、可扩展性和灵活性。

工厂模式可分为三类：

- [[简单工厂模式（Simple Factory）]]
- [[工厂方法模式（Factory Method）]]
- [[抽象工厂模式（Abstract Factory）]]

## 使用场景

1. 需要根据某些条件来创建对象：当对象的创建过程涉及到复杂的条件判断或者需要根据不同条件创建不同类型的对象时，工厂模式非常适用。例如，根据用户的角色来创建不同类型的权限对象。
1. 需要隐藏对象创建细节：当对象的创建过程比较复杂，包含多个步骤或者需要使用其他对象来辅助创建时，可以使用工厂模式将这些创建细节隐藏起来，让客户端代码更加简洁。
1. 需要扩展或替换对象创建逻辑：如果未来可能需要添加新的产品类型或者修改现有的创建逻辑，工厂模式可以让这些修改变得更加容易，只需修改工厂类而不需要修改客户端代码。

## 解决的问题

- 解耦对象的创建和使用：工厂模式将对象的创建过程从客户端代码中分离出来，客户端只需要通过工厂来获取所需的对象，而不需要关心具体的创建细节。
- 隐藏创建细节： 工厂模式可以隐藏对象的具体创建细节，使得客户端代码更加简洁，降低了代码的复杂度和耦合度。

## 优点

- 易于扩展：工厂模式使得添加新的产品类型变得更加容易，只需修改工厂类而不需要修改客户端代码。
- 降低耦合度：客户端代码只依赖于工厂接口，而不依赖于具体的产品类，从而降低了代码之间的耦合度。
- 隐藏细节：工厂模式将对象的创建细节隐藏起来，使得客户端代码不需要关心具体的创建过程，从而降低了代码的复杂度。

## 缺点

- 增加了类的数量：工厂模式引入了额外的工厂类，可能会增加类的数量，使得代码结构变得更加复杂。
- 增加了代码的抽象程度：工厂模式引入了额外的抽象层级，可能会增加代码的理解难度。
- 不易理解：对于简单的项目或者对象创建过程比较简单的情况，使用工厂模式可能会增加不必要的复杂度。

## 工厂方法模式（Factory Method）

工厂方法模式使用场景：

当对象的创建逻辑比较复杂，不是简单的 `new` 对象而是要组合其他类对象，做各种初始化操作的时候，推荐使用工厂方法模式，将复杂的创建逻辑拆分到多个工厂类中，让每个工厂类都不至于过于复杂。

在简单工厂和工厂方法中，类只是一种分类方式。

## 抽象工厂模式（Abstract Factory）