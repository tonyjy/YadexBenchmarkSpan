# YadexBenchmarkSpan

System.Span<T> is a value type representing a continuous memory region for a collection of value type objects. It works like an array of value type <T>. Span<T> is a ref struct. Ref struct can only exist in stack and can't be the fields. Span can be used to access heap, stack, and unmanaged memory.

  - Supports type check by compiler
  - Boundary check at runtime
  - Indexer and Enumerator

Why should developers care?

  - Avoid overhead of allocation
  - Avoid overhead of memory copy
  - Avoid overhead of garbage collection 

What real-world problems can Span<T> solve?
  
  - Microsoft Search Engine Bing is written in .NET Core. The performance of Bing has improved by 34% after using Span<T>.
  - Iterating a collection of value types (simple types, struct, enum), such as byte[], involves memory copy because value type by default is pass-by-value.
  - String.Substring could be used to carve out just the piece that’s interesting to them, but that’s a relatively expensive operation, involving a string allocation,  memory copy, and garbage collection. 
  - Coding with raw pointer is dangerous because it has no strong-type and boundary-check in runtime.  
  - Same logic has to be implemented for different memories, such as heap, stack, and native code (unmanaged memory, interop).
  

Author: Tony Jiang

https://tonyjy.blogspot.com/
