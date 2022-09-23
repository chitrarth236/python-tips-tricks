##Pytest Notes

installation:
pip install pytest

sample functions to test
```python
def addition(a,b):
	return a + b

def is_even(input):
    if input % 2 == 0:
        return True
    return False
```


simple test
```python
import pytest

def test_addition_simple():
	assert addition(2,2) == 4
    
```

Execute tests
```python
python -m pytest
 OR
py.test

for verbose mode:
py.test -v
```


Parameterized tests
	-to combine multiple tests
	-instaed of wrting three individual test cases use this:
```python
@pytest.mark.parametrize("input,expected", [
    (2, True),
    (3, False),
    (11, False),
])
def test_is_even(input, expected):
    assert is_even(input) == expected

Skip tests
@pytest.mark.skip(reason="optional reason")
def test_addition_simple():
	assert addition(2,2) == 4
```
Use "pytest -v -rxs" to display the reason

Conditional Skip
```python
@pytest.mark.skipif(sys.version_info > (3,5), reason = "Py version is greater than 3.5")
def test_addition_simple():
	assert addition(2,2) == 4
```

Skip based on test names
this command runs all the tests which have keyword 'even'
pytest -k even

Custom markers
```python
@pytest.mark.markername1
def test_addition_simple():
	assert addition(2,2) == 4

@pytest,makr.markername2
def test_addition_simple():
	assert addition(3,3) == 6

pytest -m markername2 
#It will only run test marked as markername2
```






