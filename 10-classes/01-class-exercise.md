### 1
Create the class with the `__init__` method for the following.

```
Person
======
name: str
height: int
strength: int
health_points: int = 100
---------
__str__(self) -> str
introduce(self) -> void
punch(Person) -> void
```
class Person:
    """
    Attrs:
        height (int): in cm
        name (str): First and last
        strength (int): How strong the person is 
        health_points (int): Out of 100 (everyone starts at 100)
    """
    def __init__(self, name: str, height: int, strength: int, health_points: int):
        self.height = height
        self.name = name
        self.strength = strength
        self.health_points = 100
    
    person1 = Person("Thomas Kim", "200", "200")
    print(person1.name)
    print(person1.height)
    print(person1.strength)
    print(person1.health_points)
    
    person2 = Person("Edmund Lee", "150", "300")
    print(person2.name)
    print(person2.height)
    print(person2.strength)
    print(person2.health_points)
    
    def __str__(self):
        print(person1.name)
        print(person1.health_points)
        
        print(person2.name)
        print(person2.health_points)
        
    def introduce(self):
        print(f"Hello, my name is {self.name}.")
        
    person1.introduce()
    person2.introduce()
    
    def punch(self, person):
        person.health_points -= 10
    
    person1.punch(person2)
    person2.punch(person2)
    
    def eat(self):
        self.health_points = 100
        
### 2
- Create two `Person` objects.

- Add a `__str__` (magic) method that displays the name and hp of the person.

- Print out each `Person` object.

### 3

- add an `introduce` method that will say "Hello, my name is {name}"

- Make both people objects introduce themselves.

### 4

- Add a `punch` method that will take another person as an argument, and subtract 10 from that person's hp.

- Make one `Person` object `punch` the other person object.

- Make one `Person` object punch themself.

### 5
- Add an `eat` method that, when used, will restor the health points back to 100.
