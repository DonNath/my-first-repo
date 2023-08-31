
class Person {
  constructor(name = "John", age = 20, energy = 100) {
    this.name = name;
    this.age = age;
    this.energy = energy;
  }
  sleep() {
    this.energy += 10;
  }
  doSomethingFun() {
    this.energy -= 10;
  }
}

class Worker extends Person {
  constructor(name, age, energy, xp = 0, hourlyWage = 20) {
    super(name, age, energy);
    this.xp = xp;
    this.hourlyWage = hourlyWage;
  }
  goToWork() {
    this.xp += 10;
  }
}

function intern(name, age, energy, xp, hourlyWage) {
  const newIntern = new Worker(name, age, energy, xp, hourlyWage);

  console.log(newIntern.name);
  return;
}

intern("Bob", 22, 110, 0, 10);

function manager(name, age, energy, xp, hourlyWage) {
  const newManger = new Worker(name, age, energy, xp, hourlyWage);

  newManger.doSomethingFun();
  newManger.doSomethingFun();
  newManger.doSomethingFun();

  console.log(newManger);
  return;
}
manager("Alice", 30, 120, 100, 30);
console.log(Worker);

Really grateful bro😊
Show quoted text
