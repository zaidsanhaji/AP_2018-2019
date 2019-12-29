# Design Patterns

## Strategy Pattern

> Summary:

Abstract class
Specific classes which extend the abstract class
Interfaces for main functions
Classes which implement a main function and specify it
Abstract class has all main functions as a property
When created, specific class takes 2 variables which fill in the properties of abstract class

> Example:

Abstract class Duck
Class Subduck extends Duck
Interface Behavior
Behavior-classes implements Behavior
Duck has property of each Behavior
Duck sets Behavior in constructor via properties
Subduck constructor takes variable of each behavior and sends them to parent-class Duck


## Observer Pattern

> Summary:

Interface Observer (update)
Interface Observable (list of observers, add/remove observers)
Class DATA implements Observable (contains data, keeps track of observers)
Class DISPLAY implements Observer (displays data, updates data)

> Example:

Interface Observer (update)
Interface Observable (list of observers, add/remove observers)
Class WeatherData implements Observable (contains data, keeps track of observers)
Class ForecastDisplay implements Observer (displays data, updates data)

## Singleton Pattern

> Summary:

Class with private constructor and static method that always returns the same static uniqueInstance

> Example:

Class ChocolateBoiler with private constructor and static method getInstance that always returns the same static uniqueInstance, plus extra methods.

## Decorator Pattern

> Summary:

Abstract class item
Specific classes which extend item
Abstract class condiments (things you can add to the item)
Specific condiment classes which extend the condiments abstract class, having a beverage as a parameter

> Example:

Abstract class Beverage
Specific classes Decaf, DarkRoast, HouseBlend, Espresso
Abstract class CondimentDecorator
Specific condiment classes Milk, Soy, Whip and Mocha, having a beverage as a property
Main: make new beverage, then add condiment by making a new condiment with the beverage as parameter.

## Command Pattern

> Summary:

Interface ‘Command’: execute & undo methods
Class item: functionalities -> methods
Item has a few commandclasses which binds Command methods to item functionalities
Remote class which can set new commands and call existing commands

> Example:

Interface ‘Command’: execute & undo methods
Class Light: methods ‘On()’ and ‘Off()’
LightOnCommand (execute() -> On()) and LightOfCommand (execute() -> Off()). Undo does the opposite of execute.
Remote has a list with commands. You can add commands with the ‘setCommand(Command command, int slot)’-method and then execute them with the ‘buttonWasPressed(int slot)’-method.