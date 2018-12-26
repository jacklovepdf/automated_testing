# automated_testing
the note of automated testing

## 1.常见的自动化测试

1.1 单元测试

    A single piece of code (usually an object or a function) is tested, isolated from other pieces；
    
1.2 集成测试

    Multiple pieces are tested together；
    
1.3 功能测试

    Automatic testing of the entire application, for example using a tool like Selenium to automatically run a browser.


一般来说，如果你觉得写一个单元测试比较复杂，那么很可能并不是一个单元测试；相对而言，集成测试和功能测试比单元测试更加的复杂和难以维护;


## 2.测试代码编写和运行时机

    根据测试代码编写和运行时机，可以把自动化测试划分为两种：TDD（测试驱动开发）和BDD(行为驱动开发)
    
2.1 测试驱动开放

    先写测试用例，再写代码；
    测试驱动开发的特点决定他有很高的测试覆盖率；测试驱动开发也能降低测试中出现bug的可能性；
    
    
（1）测试驱动开发的流程
    
    1.Start by writing a test;
    2.Run the test and any other tests. At this point, your newly added test should fail. If it doesn’t fail here, it might not be testing the right thing and thus has a bug in it.
    3.Write the minimum amount of code required to make the test pass;
    4.Run the tests to check the new test passes;
    5.Optionally refactor your code;
    6.Repeat from 1;

2.2 行为驱动开发；

    行为驱动开发是比较容易误解的，行为驱动开发是一组最佳实践编写好测试，BDD应该并且可以和TDD以及单元测试方法一起work；
BDD中单元测试的一个误区在于我们有时候去测试功能的实现，这意味着如果你更新函数，即使你的输入输出没有改变，你也需要去修改测试代码；
行为驱动开发不应该测试功能实现，而是测试行为；



## 总结

    单元测试告诉你应该测试什么（what）, 测试驱动开发告诉你什么时候编写测试代码（when）, 而行驱动开发告诉你该如何编写测试用例（how）;
尽管你可以单独运用某一种方法，综合运行上面方法可以相互补充，带来更大的收益；