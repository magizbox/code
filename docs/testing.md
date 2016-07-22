# Testing

<img src="http://elstarit.nl/wp-content/uploads/2014/08/UNIT_TEST_TDD.png" alt="" />

# 1. Definition [^1] [^2]
Test-driven development (TDD) is a software development process that relies on the repetition of a very short development cycle:

![](http://image.slidesharecdn.com/presentationontddatdd-100216123440-phpapp02/95/overview-on-tdd-test-driven-development-atdd-acceptance-test-driven-development-27-1024.jpg?cb=1266325710)

> Step 1: First the developer writes an (initially failing) automated test case that defines a desired improvement or new function,

> Step 2: Then produces the minimum amount of code to pass that test,

> Step 3: Finally refactors the new code to acceptable standards.

Kent Beck, who is credited with having developed or 'rediscovered' the technique, stated in 2003 that TDD encourages simple designs and inspires confidence.

# 2. Principles [^2]

Kent Beck defines

* Never with a single line of code unless you have a failing automated test.
* Eliminate duplication

**<span style="color: red">Red: (Automated test fail)</span>**
**<span style="color: green">Green (Automated test pass because dev code has been written)</span>**
**<span style="color: blue">Refactor (Eliminate duplication, Clean the code)</span>**

# 3. Assertions & Assert Framework

<blockquote>
  Assert that the expected results have occurred.
</blockquote>

[code lang="java"]
@Test
public void test() {
    assertEquals(2, 1 + 1);
}
[/code]

![](https://lh3.googleusercontent.com/7Al53UeVble_p8m_JytrrRgVObvFZmw-sbCT9Q4bXzY4PcCjWFVsTG6MRVZdaBlke9CoTtRkyhwGwQ=w673-h242-no)

# 4. Test Runners [^3]

![](http://blog.excastle.com/images/resharper/UnitTestRunner.png)

> When testing a large real-world web app there may be tens or hundreds of test cases, and we certainly don't want to run each one manually. In such as scenario we need to use a test runner to find and execute the tests for us, and in this article we'll explore just that.

A test runner provides the a good basis for a real testing framework. A test runner is designed to **run tests**, **tag tests** with attributes (annotations), and **provide reporting** and other features.

In general you break your tests up into 3 standard sections; `setUp()`, `tests`, and `tearDown()`, typical for a test runner setup.

The setUp() and tearDown() methods are run automatically for every test, and contain respectively:

* The setup steps you need to take before running the test, such as unlocking the screen and killing open apps.
* The cooldown steps you need to run after the test, such as closing the Marionette session.



# 5. Test Frameworks

<table>
<tr>
<td>Language</td>
<td>Test Frameworks</td>
</tr>

<tr>
<td>C++/VisualStudio</td>
<td><a href="http://magizbox.com/index.php/code/cc/test-c/">C++: Test</a></td>
</tr>
<tr>
<td>Web Service</td>
<td><a href="https://github.com/jayway/rest-assured">rest-assured</a></td>
</tr>

<tr>
<td>Web UI</td>
<td><a href="http://www.seleniumhq.org/">SeleniumHQ</a></td>
</tr>

</table>

[^1]: [Test-driven development](https://en.wikipedia.org/wiki/Test-driven_development)
[^2]: [Overview on TDD (Test Driven Development) & ATDD (Acceptance Test Driven Development)](http://www.slideshare.net/tiemoon/overview-on-tdd-test-driven-development-atdd-acceptance-test-driven-development)
[^3]: [Part 5: Introducing a test runner](https://developer.mozilla.org/en-US/docs/Archive/Firefox_OS/Automated_testing/gaia-ui-tests/Part_5_Introducing_a_test_runner)

