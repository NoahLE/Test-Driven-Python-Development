# Test-Driven Python Development

This is the source code from Harry Percival's book [Test-Driven Python Development](https://www.obeythetestinggoat.com/).

## Getting set up

Make sure `Python 3.6.X` is installed.

From the root directory, install the requirements file using `pip install -r requirements.txt`.

## Notes

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
