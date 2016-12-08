## Challenges

1. Create an `Plant` constructor.

  ```js
  function Plant(name, age, color) {
    this.name = name;
    this.age = age;
    this.color = color;
  }
  ```

3. Create a `Tree` constructor with the same properties as `Plant` (bonus if you use the `call` method). Trees should also have a property called `isHardwood`.

  ```js
  function Tree(name, age, color, isHardwood) {
    Plant.call(this, name, age, color);
    this.isHardwood = isHardwood;
  };
  ```

4. Implement prototypal inheritance with `Tree` as a subclass of `Plant`.

  ```js
  Tree.prototype = new Plant;
  Tree.prototype.constructor = Tree;
  ```

5. Create a new instance of `Tree`!

  ```js
  oak = new Tree("Oak", 3, "brown", true);
  //=> Tree {name: "Oak", age: 3, color: "brown", isHardwood: true}
  ```

6. Check if the tree you just created is an `instanceof` `Tree`. How about an `instanceof` `Plant`?

  ```js
  oak instanceof Tree
  //=> true

  oak instanceof Plant
  //=> true
  ```
