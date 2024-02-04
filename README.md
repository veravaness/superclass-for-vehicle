# superclass-for-vehicle


1
class Vehicle {
2
  String brand;
3
  int year;
4
​
5
  Vehicle(this.brand, this.year);
6
​
7
  void start() {
8
    print('The vehicle is starting.');
9
  }
10
​
11
  void stop() {
12
    print('The vehicle is stopping.');
13
  }
14
}
15
​
16
class Car extends Vehicle {
17
  int numberOfDoors;
18
​
19
  Car(String brand, int year, this.numberOfDoors) : super(brand, year);
20
​
21
  void honk() {
22
    print('Honk! Honk!');
23
  }
24
}
25
​
26
class Motorcycle extends Vehicle {
27
  bool hasHelmet;
28
​
29
  Motorcycle(String brand, int year, this.hasHelmet) : super(brand, year);
30
​
31
  void wheelie() {
32
    print('Performing a wheelie!');
33
  }
34
}
35
​
36
class Truck extends Vehicle {
37
  double payloadCapacity;
38
​
39
  Truck(String brand, int year, this.payloadCapacity) : super(brand, year);
40
​
41
  void loadCargo() {
42
    print('Loading cargo into the truck.');
43
  }
44
}
45
​
46
void main() {
47
  Car myCar = Car('Toyota', 2022, 4);
48
  myCar.start();
49
  myCar.honk();
50
​
51
  Motorcycle myMotorcycle = Motorcycle('Harley-Davidson', 2020, true);
52
  myMotorcycle.start();
53
  myMotorcycle.wheelie();
54
​
55
  Truck myTruck = Truck('Ford', 2021, 5000.0);
56
  myTruck.start();
57
  myTruck.loadCargo();
58
}
Console
The vehicle is starting.
Honk! Honk!
The vehicle is starting.
Performing a wheelie!
The vehicle is starting.
Loading cargo into the truck.
