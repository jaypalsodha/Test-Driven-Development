# Test Driven Development

- Test-driven development (TDD) is a software development process that relies on the repetition of a very short development cycle: 

- Requirements are turned into very specific test cases(in java we can consider small specific method), then the software is improved so that the tests pass. 

- This is opposed to software development that allows software to be added that is not proven to meet requirements.

- Test-driven development is related to the test-first programming concept

# Test-driven development cycle
1. Add a test
2. Run all tests and see if the new test fails
3. Write the code
4. Run tests
5. Refactor code

Once done, repeat the same thing again. . . .
# 1. Add a Test
- In test-driven development, each new feature begins with writing a test. 
- Write a test that defines a function or improvements of a function, which should be very succinct. 
- To write a test, the developer must clearly understand the feature's specification and requirements. 
- The developer can accomplish this through use cases and user stories to cover the requirements and exception conditions, and can   write the test in whatever testing framework is appropriate to the software environment. 
- It could be a modified version of an existing test.
- This is a differentiating feature of test-driven development versus writing unit tests after the code is written: it makes the developer   focus on the requirements before writing the code, a subtle but important difference.

# 2. Run all tests and see if the new test fails
- This validates that the test harness is working correctly, shows that the new test does not pass without requiring new code because the   required behavior already exists, and it rules out the possibility that the new test is flawed and will always pass. 
- The new test should fail for the expected reason. This step increases the developer's confidence in the new test.

# 3. Write the code
- The next step is to write some code that causes the test to pass. 
- The new code written at this stage is not perfect and may, for example, pass the test in an inelegant way. 
- That is acceptable because it will be improved and honed in Step 5.
- At this point, the only purpose of the written code is to pass the test. 
- The programmer must not write code that is beyond the functionality that the test checks.

# 4. Run tests
- If all test cases now pass, the programmer can be confident that the new code meets the test requirements, and does not break or         degrade any existing features. 
- If they do not, the new code must be adjusted until they do.

# 5. Refactor code
- The growing code base must be cleaned up regularly during test-driven development. 
- New code can be moved from where it was convenient for passing a test to where it more logically belongs. 
- Duplication must be removed. Object, class, module, variable and method names should clearly represent their current purpose and use,   as extra functionality is added. 
- As features are added, method bodies can get longer and other objects larger. 
- They benefit from being split and their parts carefully named to improve readability and maintainability, which will be increasingly     valuable later in the software lifecycle. 
- Inheritance hierarchies may be rearranged to be more logical and helpful, and perhaps to benefit from recognized design patterns. -  -  - There are specific and general guidelines for refactoring and for creating clean code.
- By continually re-running the test cases throughout each refactoring phase, the developer can be confident that process is not           altering any existing functionality.
- The concept of removing duplication is an important aspect of any software design. In this case, however, it also applies to the         removal of any duplication between the test code and the production code—for example magic numbers or strings repeated in both to make   the test pass in Step 3.

# Repeat
- Starting with another new test, the cycle is then repeated to push forward the functionality. 
- The size of the steps should always be small, with as few as 1 to 10 edits between each test run. 
- If new code does not rapidly satisfy a new test, or other tests fail unexpectedly, the programmer should undo or revert in preference   to excessive debugging. 
- Continuous integration helps by providing revertible checkpoints. 
- When using external libraries it is important not to make increments that are so small as to be effectively merely testing the library   itself, unless there is some reason to believe that the library is buggy or is not sufficiently feature-complete to serve all the     needs of the software under development.


# Refactoring
- Refactoring is a systematic process of improving code without creating new functionality that can transform a mess into clean code and   simple design.

## Clean code
The main purpose of refactoring is to fight technical debt. It transforms a mess into clean code and simple design.

Nice! But what’s clean code, anyway? Here are some of its features:

### Clean code is obvious for other programmers.
- And I’m not talking about super sophisticated algorithms. Poor variable naming, bloated classes and methods, magic numbers -you name it- all of that makes code sloppy and difficult to grasp.

### Clean code doesn’t contain duplication.
- Each time you have to make a change in a duplicate code, you have to remember to make the same change to every instance. This increases the cognitive load and slows down the progress.

### Clean code contains a minimal number of classes and other moving parts.
Less code is less stuff to keep in your head. Less code is less maintenance. Less code is fewer bugs. Code is liability, keep it short and simple.

### Clean code passes all tests.
- You know your code is dirty when only 95% of your tests passed. You know you’re screwed when you test coverage is 0%.

Clean code is easier and cheaper to maintain!
