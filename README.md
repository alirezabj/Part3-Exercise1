# Part3-Exercise1

### A:

The inheritance used in this exercise is Specialization. The reason is that the LoginScreen class extends the CommandLineApp and inherits the ask method, which allows it to prompt the user for input. Instead of changing the existing functionality, LoginScreen adds a new method called lock, which handles user login. This makes LoginScreen a specific version of CommandLineApp, which follows the is-a relationship in inheritance.

### B: 

The code partially works but has a major issue in the Hydroelectric class that prevents it from compiling. The Coal class implements the NaturalResource interface correctly by providing implementations for both amountLeft() and spend(float amount). However, the Hydroelectric class does not implement the NaturalResource interface correctly because it specifies the spend(float amount) method as private, but spend(float amount) must be public because in java interface methods must be implemented with at least the same visibility level as defined in the interface. Since the method is private in Hydroelectric, the compiler throws an error, making the code invalid.

One benefit of the code is that it follows encapsulation and code reusability by defining a common interface (NaturalResource) that can be used to represent different types of resources. Another advantage is that it enables future scalability, where new resource types can be added easily by implementing the interface. However, the main drawback is the incorrect implementation of the interface in Hydroelectric, which results in a compilation error due to the visibility mismatch of the spend method. 


### C: 

The code does not work because of a mismatch in the return type in the overridden method. In the RandomGenerator class, the generate method returns an Object, meaning it can return different types, such as Integer, String, or a generic Object. However, in RandomIntegerGenerator, the overridden generate() method returns an Integer. Therefore, since the parent method can return multiple different types, returning an integer in the subclass causes a compilation error because it does not fully override all possible return types of the parent method.

One benefit of the code is that it attempts to use inheritance and method overriding to allow different implementations of the generate method. However, a major drawback is the return type mismatch, which causes a compilation error due to the overridden method in RandomIntegerGenerator returning Integer instead of Object. Additionally, the base class RandomGenerator returns different types (Integer, String, Object), making it unsafe to use without explicit type checking or casting since it would be difficult to predict the output.
