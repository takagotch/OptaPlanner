### Optaplanner
---
https://github.com/kiegroup/optaplanner

https://www.optaplanner.org/

```java
MyRoster problem = ...;
SolverFactory<MyRoster> factory = SolverFactory
  .createFromXmlResource(".../mySolverConfig.xml");
Solver<MyRoster> solver = factory.buildSolver();

MyRoster solution = solver.solve(problem);

for (MyShift shift : solution.getShifts()) {
  assertNotNull(shift.getEmployee());
}
```

```sh
mvn clean install -DskipTests
cd optaplnner-examples
mvn exec:java
```

```
```
