# Test-Driven Python Development

This is the source code from Harry Percival's book [Test-Driven Python Development](https://www.obeythetestinggoat.com/).

## Getting set up

Make sure `Python 3.6.X` is installed.

From the root directory, install the requirements file using `pip install -r requirements.txt`.

Because this project has django-extensions you can run `python manage.py runserver_plus` for extra debugging functionality.

## Chapter Notes

These are caveats I found when getting going through the book. They're mostly notes to myself for future reference.

### Chapter 1

- Make sure to read [the prerequisites](https://www.obeythetestinggoat.com/book/pre-requisite-installations.html) when getting your environement set up.

### Chapter 2

- Functional tests - See the application from the user's perspective and see how it functions. It can be used to track
a user's story  throug the application. These can also be known as acceptance or end-to-end tests.
  - They should always have a followable human-readable story.
  
- Don't make comments that repeat what the code is doing

- Make sure to enable Django support if using Pycharm ![pycharm-django](docs/pycharm-enable-django.png)

- Tests are organized into classes which inherit from `unittest.TestCase`
  - All methods must start with `test_` and can contain multiple tests
  - Descriptive method names are excellent
  
 - `setUp` and `tearDown` are run after each test
 
 - [Unittest docs](https://docs.python.org/3/library/unittest.html) can be found here.
 
### Chapter 3

- Functional tests - test the application from the user's perspective (high level)

- Unit tests - test the application from the programmer's perspective (low level)

- The TDD approach is usually the following:
  1. Write a functional test
  2. Think, then write unit tests to define how the code should behave (each line of code is covered by at least one test)
  3. Write code to get the unit test to pass (then repeat steps 2 and 3)
  4. Rerun functional tests and continue testing and developing

- **Always review what you commit before you do it**

- Django's workflow is similar to this:
  - HTTP request comes in for a particular URL
  - Django uses rules to find which view function should deal with the request
  - The view processes the request and returns the an HTTP response
  
- Only solve one error at a time, don't try to over engineer solutions

- Resolving errors is usually done in the following order:
  - Look at the error
  - Look at the test that is failing
  - Look at where in the *test* code the failure is coming from
  - Look at the code which is causing the error

### Chapter 4

- Guido explaining the `any()` function [here](https://bit.ly/1iXxD18)

- Don't test constants

- When refactoring, don't change functionality

- You can set specific folders to have a content type like templates
  - This is set my right-clicking on the folder and selecting `Mark directory as`
  - ![pycharm-folders](docs/pycharm-mark-templates.png)
  
- You can use `repr(<thing>)` to get the raw value of an item

- The `resolve(<url>)` returns which view function a URL is mapped to

- Most assertX methods can be given a custom error message for more clarity

- An excellent TDD diagram [is here](https://www.obeythetestinggoat.com/book/chapter_philosophy_and_refactoring.html#simple-TDD-diagram)

- Double-loop TDD link [goes here](https://bit.ly/1iXzoLR)

- Source code for the book can be [found here](https://github.com/hjwp/book-example/)

### Chapter 5
