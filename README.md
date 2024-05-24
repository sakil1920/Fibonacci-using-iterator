# Fibonacci-using-iterator

class Fibonacci:
def **init**(self, max_value):
self.max_value = max_value
self.a, self.b = 0, 1

    def __iter__(self):
        return self

    def __next__(self):
        if self.a > self.max_value:
            raise StopIteration
        current = self.a
        self.a, self.b = self.b, self.a + self.b
        return current

max_value = 100
fib_item = Fibonacci(max_value)

for num in fib_item:
print(num)
