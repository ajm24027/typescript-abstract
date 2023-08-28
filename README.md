# typescript-abstract

### Abstract Classes

As far as I can tell, Abstract classes are used to give child classes similar functionality using the extends keyword, and can have methods that are only meant for them.
They appear to look the exact same as any other class, only they use the "Abstract" keyword in it.

```typescript
abstract class VideoGame {
  protected name: string
  protected genre: string
  protected platform: string

  constructor(name: string, genre: string, platform: string) {
    this.name = name
    this.genre = genre
    this.platform = platform
  }

  abstract play(): void

  displayInfo() {
    console.log(this.name, this.genre, this.platform)
  }
}
```

Another thing is that there's this "Super" keyword that can be used to access the abstract parents class, here's a correct example:

```typescript
class Animal {
  makeSound() {
    console.log('Animal sound')
  }
}

class Dog extends Animal {
  makeSound() {
    super.makeSound() // This calls the Animal's makeSound() method
    console.log('Woof!')
  }
}
```
