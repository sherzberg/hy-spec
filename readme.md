hy-spec
=======

`hy-spec` is a TDD/BDD tesing framework with `rspec` roots from the lovely Ruby community. `hy-spec` is meant to be a highly readable testing framework for `Python` and by extension `hy`.

Example Usage:
--------------

Suppose you have this python code you want to test:

```python
# maths.py

def add(x, y):
    return x + y


def sub(x, y):
    return x - y
```

To test it, use this `hy` code:

```hy
# test_maths.hy

(import [maths [add sub]])

(describe "maths tests"
  (it "tests add works properly"
    (-> 5 (should= (add 3 2)))
    (-> 1 (should= (add 0 1)))
    (-> 9 (should-not= (add 1 1)))))
```
