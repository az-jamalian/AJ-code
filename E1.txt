from typing import Set, Tuple, List

"""Code1"""
def id_to_fruit(fruit_id: int, fruits: List[str]) -> str:
    idx = 0
    for fruit in fruits:
        if fruit_id == idx:
            return fruit
        idx += 1
    raise RuntimeError(f"Fruit with id {fruit_id} does not exist")

name1 = id_to_fruit(1, ["apple", "orange", "melon", "kiwi", "strawberry"])
name3 = id_to_fruit(3, ["apple", "orange", "melon", "kiwi", "strawberry"])
name4 = id_to_fruit(4, ["apple", "orange", "melon", "kiwi", "strawberry"])

print(id_to_fruit(1, ["apple", "orange", "melon", "kiwi", "strawberry"]))


"""Code 2"""
# You can copy this code to your personal pipeline project or execute it here.
def id_to_fruit(fruit_id: int, fruits: List[str]) -> str:
    if fruit_id < 0 or fruit_id >= len(fruits):
        raise RuntimeError(f"Fruit with id {fruit_id} does not exist")
    return fruits[fruit_id]

name1 = id_to_fruit(1, ["apple", "orange", "melon", "kiwi", "strawberry"])
name3 = id_to_fruit(3, ["apple", "orange", "melon", "kiwi", "strawberry"])
name4 = id_to_fruit(4, ["apple", "orange", "melon", "kiwi", "strawberry"])

print(name1)
print(name3)
print(name4)

