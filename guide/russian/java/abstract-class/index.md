---
title: Abstract Classes in Java
localeTitle: Абстрактные классы в Java
---
Давайте обсудим абстрактные классы. Прежде чем погрузиться в этот учебник, вам лучше понять понятия классов и наследование.

Абстрактные классы - это классы, которые могут быть подклассифицированы (т.е. расширены), но не могут быть созданы. Вы можете думать о них как о **классе** интерфейсов, или как о интерфейсе с фактическим кодом, привязанным к методам.

Рассмотрим следующий пример, чтобы понять абстрактные классы: У вас есть класс Vehicle, который определяет определенные базовые функции (методы) и определенные компоненты (объектные переменные), которые должны иметь машины, чтобы их классифицировали как транспортное средство. Вы не можете создать объект транспортного средства, потому что само транспортное средство является абстрактным понятием. Однако вы можете расширить функциональность класса автомобиля, чтобы создать автомобиль или мотоцикл.
```java
abstract class Vehicle
{
  //variable that is used to declare the no. of wheels in a vehicle
  private int wheels;
  
  //Variable to define the type of motor used
  private Motor motor;
  
  //an abstract method that only declares, but does not define the start 
  //functionality because each vehicle uses a different starting mechanism
  abstract void start();
}

public class Car extends Vehicle
{
  ...
}

public class Motorcycle extends Vehicle
{
  ...
}
```
You cannot create an object of Vehicle class anywhere in your program. You can however, extend the abstract vehicle class and create objects of the child classes; 
```

Ява Автомобиль newVehicle = новый автомобиль (); // Недействительным Автомобиль car = новый автомобиль (); // действительный Автомобиль mBike = новый мотоцикл (); // действительный

Автомобиль carObj = новый автомобиль (); // действительный Мотоцикл mBikeObj = новый мотоцикл (); // действительный \`\` \`
