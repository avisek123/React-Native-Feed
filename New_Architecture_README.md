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

Let’s dive into each of the new points.

# OLD architecture

The react native code is executed over three threads:

1. **JavaScript Thread**: Executes the JavaScript bundle using a specific JavaScript engine.

2. **Native/UI Thread** : Runs native code and manages user interface operations like rendering and handling gesture events.

3. **Shadow Thread**: Calculates the layout positions of native elements before rendering.
