# Flutter Masterclass

## Introduction

This project serves as a demo to showcase some key features to make flutter development an incredible experience

## Table of Contents

- Arquitecture
- Testing
- Native
- Configuration
- Libraries
<hr>

## Arquitecture

We follow a clean arquitecture approach that enforces seperation of concerns. This allows our code to be more readable, testable and less error-prone. Our own custom approach to the arquitecture is to have three main layers.

<img src="https://i0.wp.com/resocoder.com/wp-content/uploads/2019/08/Clean-Architecture-Flutter-Diagram.png?w=556&ssl=1" width="400" >

### Presentation

This layer holds all the logic related to the UI. It has little to no business logic and primarily serves to display views and widgets to the user and receive user interaction. By keeping this layer free from all business logic, we can safely work on UI design and not have to worry about breaking functionality. Additionaly, this also has the benefit of making the views and widgets relatively lean, thus further enhancing readability.

This layer also holds our state controllers. These controllers focus on reducing state and making calls to either a usecase or a repository.

### Domain

This layer is where the main business logic of the application resides, it is the "meat" of the app. The layer is primary split into models, repositories and use cases.

- Models: Holds the bussiness entities of the application
- Repositories: Holds the abstract class that specify what a repository implementation must fullfill. By keeping the abstraction in this layer, we can improve testability.
- Usecases: Usecases are where application specific business logic is performed. These usecases are single responsibility classes that allow our business logic to be seperated from the flutter framework.

### Data

This layer holds the repository implementations and primarily focuses on making database and API requests. By seperating this layer from the business logic, we can achieve tremendous independency from specific database and API providers, making transitions to different providers relatively easy.

<hr>

## Testing



### Unit Tests

<a href="https://flutter.dev/docs/cookbook/testing/unit/introduction"> Flutter Unit Test Documentation </a>

### Integration Tests

In flutter, Integration testing erroneusly refers to E2E Testing. It is important to understand the difference to avoid confusion

### E2E Testing

<a href="https://flutter.dev/docs/testing/integration-tests"> Flutter Integration Testing Documentation </a>

<div></div>
<a href="https://blog.codemagic.io/codemagic-flutter-integration-tests-firebase-test-lab/"> Flutter Integration Testing with Firebase Test Lab </a>


##### NOTES
Static methods in flutter cannot be mocked, if you need to mock a static method then create a wrapper class around the library.

<hr>

## Native

### Method Channels

<a href="https://flutter.dev/docs/development/platform-integration/platform-channels"> Method Channel Documentation </a>

### Event Channels

<a href="https://api.flutter.dev/flutter/services/EventChannel-class.html"> Flutter Event Channels </a>

<hr>

## Features

### Generics

<a href="https://dart.dev/guides/language/language-tour#generics"> Dart Generics Documentation </a>

<div>
Generics in dart allow us to create composable classes and functions in order to achieve improved type safety as well as avoid code duplication.    </div>

<br />

### Extensions

<a href="https://dart.dev/guides/language/language-tour#extension-methods"> Dart Extension Methods </a>

<div>Extension methods allow us to add functionality to existing libraries such as adding a custom method on the String class for custom formatting.</div>
<br />

### Mixins

<a href="https://medium.com/flutter-community/dart-what-are-mixins-3a72344011f3"> Dart Mixins </a>

<div>Mixins allow to reuse class functionality without having to extend from a base class. Dart only allows extending one base class.</div>
<br />

### Callable Classes

<a href="https://dart.dev/guides/language/language-tour#callable-classes"> Dart Callable Classes </a>

<div></div>
Implementing the call method in a class allows us to call a class like a function

<hr>

## Libraries

### GENERAL

<ul>
  <li>
    <a href="https://pub.dev/packages/intl"> Internationalization and Date Package </a>
  </li>
  <li><a href="https://pub.dev/packages/get_it"> Dependency Injection </a></li>
  <li><a href="https://pub.dev/packages/cached_network_image"> Image Caching </a></li>
  <li><a href="https://pub.dev/packages/url_launcher"> URl Launcher </a></li>
  <li><a href="https://pub.dev/packages/flutter_doten"> Environment Config </a></li>
  <li><a href="https://pub.dev/packages/dio"> Http Client </a>
  <li><a href="https://pub.dev/packages/equatable"> Equality Comparison </a>
  <li><a href="https://pub.dev/packages/flutter_launcher_icons">Launch Screen and App Icons </a></li>
  <li><a href="https://pub.dev/packages/pedantic">Linting </a></li>
  <li><a href="https://pub.dev/packages/flutter_hook"> Hooks </a> </li>
  <li>
    Mocking
    <ul>
      <li><a href="https://pub.dev/packages/mockito"> Mockito </a> </li>
      <li><a href="https://pub.dev/packages/mocktail"> Mocktail (Null Safety) </a> </li>
    </ul>

</ul>

### SUGGESTED

#### State Management

<ul>
  <li><a href="https://pub.dev/packages/provider"> Provider </a></li>
  <li><a href="https://pub.dev/packages/stacked">Stacked </a></li>
  <li><a href="https://pub.dev/packages/riverpod"> Riverpod </a></li>
  <li><a href="https://pub.dev/packages/get"> Get X </a></li>
</ul>

#### Navigation, Snackbars and Dialog

<ul>
  <li><a href="">Stacked Services </a></li>
  <li>
    Route Generation
    <ul> 
      <li><a href="https://pub.dev/packages/auto_route"> Auto Routing </a> </li>
      <li><a href="https://pub.dev/packages/stacked_generator"> Stacked Generator </a> </li>
    </ul>
  </li>
</ul>
