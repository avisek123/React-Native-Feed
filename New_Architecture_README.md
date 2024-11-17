# React Native — Ultimate Guide on New Architecture in depth

The topics we learn:

- **OLD architecture**
- **OLD Architecture drawbacks**
- **New Architecture of React Native**
- **What is Codegen (Native Code Generator)**
- **What is JSI (JavaScript Interface)**
- **How can JavaScript call native methods with JSI?**
- **How JSI synchronous made it great!**
- **What is Codegen (Native Code Generator)**
- **What is Hermes Engine ?**
- **Turbo Modules**
- **Fabric (New Rendering Engine)**
- **What is Nitro Module**

Let’s dive into each of the points.

# OLD architecture

The react native code is executed over three threads:

1. **JavaScript Thread**: Executes the JavaScript bundle using a specific JavaScript engine.

2. **Native/UI Thread** : Runs native code and manages user interface operations like rendering and handling gesture events.

3. **Shadow Thread**: Calculates the layout positions of native elements before rendering.

The relationship between the JavaScript and Native threads is mediated by a component called the **Bridge**.

![React-Native-Architecture-1](https://github.com/user-attachments/assets/d0ae2efd-4966-461b-b81d-a2b1718b0a65)

# OLD Architecture drawbacks

In the old architecture, the bridge works by converting all data into a format that can be sent from JavaScript to native code.

The Bridge have some limitations:

- **It is asynchronous:** One layer sends data to the bridge and waits for the other layer to process it, even when it’s not needed.
- **It is single threaded:** JavaScript used to run on just one thread, so all calculations had to happen on that one thread.
