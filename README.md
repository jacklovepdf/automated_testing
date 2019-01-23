# automated_testing
the note of automated testing

## 1.常见的自动化测试

1.1 单元测试

    A single piece of code (usually an object or a function) is tested, isolated from other pieces；
    单元测试的主要作用是把一个复杂的应用拆分为一个个代码片段或者小的功能模块（通常是一个对象或者功能函数）分别进行独立测试；独立表征了测试单元是不依赖网络，数据库等任何外界其它条件（必要的时候，可以mock）;
    
1.2 集成测试

    Multiple pieces are tested together；
    集成测试是把多个小的功能模块整合起来一起进行测试；
    
1.3 功能测试

    Automatic testing of the entire application, for example using a tool like Selenium to automatically run a browser.
    对整个应用进行自动化测试，例如使用Selenium这样的工具自动运行一个浏览器；

一般来说，如果你觉得写一个单元测试比较复杂，那么很可能并不是一个单元测试；相对而言，集成测试和功能测试比单元测试更加的复杂和难以维护;


## 2.测试代码编写时机；

    TDD（测试驱动开发）是一种编写测试代码的方法论，主要特点：先写测试用例，再写代码；
    
2.1 测试驱动开放

    测试驱动开发的特点决定他有很高的测试覆盖率；测试驱动开发也能降低测试中出现bug的可能性；
    https://codeutopia.net/blog/2016/10/10/5-step-method-to-make-test-driven-development-and-unit-testing-easy/
    
（1）测试驱动开发的流程
    
    1.Start by writing a test;
    2.Run the test and any other tests. At this point, your newly added test should fail. If it doesn’t fail here, it might not be testing the right thing and thus has a bug in it.
    3.Write the minimum amount of code required to make the test pass;
    4.Run the tests to check the new test passes;
    5.Optionally refactor your code;
    6.Repeat from 1;

## 3.测试代码的方法；
    
    根据模块（代码片段）的行为而不是实现来编写测试代码；

    行为驱动开发是比较容易误解的，行为驱动开发是一组最佳实践编写好测试，BDD应该并且可以和TDD以及单元测试方法一起work；
    BDD中单元测试的一个误区在于我们有时候去测试功能的实现，这意味着如果你更新函数，即使你的输入输出没有改变，你也需要去修改测试代码；
    行为驱动开发不应该测试功能实现，而是测试行为；


## 4.测试代码运行器（test runner）

1. Karma
    
    Karma并不是一个测试框架，也不是一个断言库；Karma只是启动一个http服务并且生成测试运行的html文件；   

2. jest
    
## 5.单元测试框架

5.1 mocha


5.2 


## 6.断言库


## 7.关于前端自动化测试
    
    由于前端的自动化测试成本较高，导致很大场景下，成本抵不上收益，导致前端自动化测试很多时候止于尝试；自动化测试就是通过自动化脚本将一个又一个测试用例串起来，每个测试用例都要模拟环境、模拟输入、然后断言输出。
前端自动化最难的地方就是模拟环境、模拟输入和断言输出了！

7.1 模拟环境

    首先前端代码是跑在不同的终端环境上的，纯粹的使用某台机子的运行环境进行模拟是无法发现真正存在的问题。所以我们的测试用例必须跑在真实的环境下，这里面包括不同的机器：Android、ios、pc、macbook；不同的系统：window10、window8、linux、mac；不同的运行载体：IE、safari、chrome、firefox、Opera、Android webview、UIWebview、WKWebview；不同网络环境：WiFi、4G、3G、offline

7.2 模拟输入

    前端的输入不好模拟，在PC上有鼠标click，double Click、drag、mouseDown、mouseOver、input等等，在mobile上有swipe、tap、scroll、摇一摇、屏幕翻转等。相对于后端的单元测试，前端的输入种类繁多，每一种模拟起来都十分复杂，而且很多bug隐藏在几种连贯的输入之后才会复现。

7.2 断言输出

    前端的断言不是简单的判断值是否相等，很多情况是即使值相等、效果完全不一样。很多展示效果更是不能通过简单的断言来检测，比如区域是否能滑动，输入时键盘是否正确弹起等。


## 总结

    单元测试告诉你应该测试什么（what）, 测试驱动开发告诉你什么时候编写测试代码（when）, 而行驱动开发告诉你该如何编写测试用例（how）;
    尽管你可以单独运用某一种方法，综合运行上面方法可以相互补充，带来更大的收益；
