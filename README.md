# Android-Code-Standard-Demo

This sample app is based on Android app architecture and kotlin coroutine with MVVM pattern, android architecture components.

**Architecture components**
- The architecture of the application is based on MVVM - https://developer.android.com/topic/architecture

**Major Highlights**
- MVVM Architecture
- Jetpack
- Kotlin
- Retrofit
- Coroutines

**Libraries we used**
- Coroutine - Threading
- Material - Design components
- ViewModel
- LifeCycle
- AndroidX
- DataBinding
- LiveData
- Retrofit - Networking
- SDP 
- Glide - Image Loading 
- GSON - Json Parsing 

**Project**
- Our project structure looks like this 
- We have seperate package for diffrent modules 
- It's easy to maintain & find files by seperating in diffrent packages  

![image](https://user-images.githubusercontent.com/131871156/234808417-8de5d012-8cc8-45ac-9b0f-41996d2ec86d.png)

**References**
- ViewModel https://developer.android.com/topic/libraries/architecture/viewmodel
- LiveData https://developer.android.com/topic/libraries/architecture/livedata
- Coroutine https://developer.android.com/kotlin/coroutines
- DataBinding https://developer.android.com/topic/libraries/data-binding

**Common Purpose Class / files / Methods**
- We have created many methods / Classes that are used multiple times, so instead of declaring them in all classes we just can declare companion object & use it wherever we need
- e.g. Checking Internet connection before calling API 

**Custom Views**
- We have created custom view for Edittext, Button, Textview controls 
- So we don't need to write same properties in xml for each view to customize it 
- Another advantage is, if there is any change we just need to change in common class & it will be reflected at all places

**Naming rules**
- Package and class naming rules in Kotlin are quite simple
- Names of packages are always lowercase and do not use underscores (org.example.project). Using multi-word names is generally discouraged, but if you do need to use multiple words, you can either just concatenate them together or use camel case (org.example.myProject)
-Names of classes and objects start with an uppercase letter and use camel case

**Function names**
- Names of functions, properties and local variables start with a lowercase letter and use camel case and no underscores
- Exception: factory functions used to create instances of classes can have the same name as the abstract return type

**Property names**
- Names of constants (properties marked with const, or top-level or object val properties with no custom get function that hold deeply immutable data) should use uppercase underscore-separated names

**Safe variable declarations**
- Always use a non-nullable type whenever possible
- Always declare variables as val unless you have a specific reason to use var
- Also use immutable collections instead of mutable ones
- If you need to declare a variable before assigning it a value instead of nullable declare it as lateinit
- If you find yourself doing this check if you should instead refactor your code to a lambda declaration to initialize the value instead
  e.g. val x = { when (y) { … } }
- Use safe calls and elvis operator with nullable variables
  https://kotlinlang.org/docs/reference/null-safety.html#safe-calls
- Do not use !! to force null pointer exceptions

**Properties and data classes**
- Declare class variables as public and use property access instead of setters and getters
- Variables declared as var can get both get and set externally and val is read only.
- You can still define an explicit setter or getter for a variable id you need to, for example, do some computation on the value and still use the property access syntax on the calling side
  https://kotlinlang.org/docs/reference/data-classes.html
- Data classes should be used extensively and declared with the keyword data
- Declaring a class as a data class reduces significant amount of boilerplate
- All parameters from the primary constructor will be declared as properties
  equals(), hashcode(), copy(), toString() (and componentN() (for destructuring)) functions will be generated
  E.g. data class User(val name: String, var age: Int) is a complete data class implementation
- Data classes come with a build in copy function that can be used to create a copy with value changes
  https://kotlinlang.org/docs/reference/data-classes.html#copying

**Opening a sample in Android Studio**
- To open the samples in Android Studio, begin by checking out main branch, and then open the root directory in Android Studio.


