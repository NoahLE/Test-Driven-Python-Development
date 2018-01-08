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
 
  
