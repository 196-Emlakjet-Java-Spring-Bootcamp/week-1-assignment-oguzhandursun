# week-1-assignment-oguzhandursun
New Features in Java 11 and Java 17
# **New Features in Java 11**

**Launch Single-File Source-Code Programs – JEP 330**

One major change is that you don&#39;t need to compile the java source file with javac tool first. You can directly run the file with java command and it implicitly compiles.
 This feature comes under JEP 330.

Before Java 11
   $ javac HelloWorld.java
   $ java HelloWorld
After Java 11
   $ java HelloWorld.java


**String API new Methods**

Added methods such as isBlank, lines, strip, repeat String API class.

repeat(int n) method:

This method returns a new string whose value is the concatenation of this string repeated &#39;n&#39; times.

&quot;Oguz&quot;.repeat(3) -> &quot;OguzOguzOguz&quot;

isBlank() method:

This method returns true if the string is empty or contains only white spaces code points. strip(), stripLeading(), stripTrailing() methodları:

lines() method:

This method returns a stream of lines extracted from the string, separated by line terminators such as \n, \r etc.

**HTTP Client (Standard) – JEP 321**

The new HTTP client from the java.net.http package was introduced in Java 9. It has now become a standard feature in Java 11.

**Reading/Writing Strings to and from the File**

Additionally, it&#39;s now easier to read and write Strings from files.

We can use the new readString and writeString static methods from the Files class:

  **Collection to an Array**

The java.util.Collection interface contains a new default toArray method which takes an IntFunction argument.

This makes it easier to create an array of the right type from a collection:

**Local-Variable Syntax for Lambda Parameters – JEP 323**

Support for using the local variable syntax (var keyword) in lambda parameters was added in Java 11.

We can make use of this feature to apply modifiers to our local variables, like defining a type annotation:

# **New Features in Java 17**

Java 17 LTS is the latest long-term support release for the Java SE platform. JDK 17 binaries are free to use in production and free to redistribute, at no cost, under the Oracle No-Fee Terms and Conditions License, where LTS stands for long-term support. It was released on September 15, 2021.

- 306: Restore Always-Strict Floating-Point Semantics
- 356: Enhanced pseudo-Random Number Generators
- 382: New macOS Rendering pipelines
- 391: macOS/AArch64 Port
- 398: Deprecate the Applet API for Removal
- 403: Strongly Encapsulated JDK Internals
- 406: Pattern matching for Switch(Preview)
- 407: Removal RMI Activation
- 409: Sealed Classes
- 410: Removal Experimental AOT and JIT Compiler
- 411: Deprecate the Security manager for Removal
- 412: Foreign Functions &amp; memory API(Incubator)
- 414: Vector API(Second Incubator)
- 415: Context-Specific Deserialization Filters

**Category 1: Nice Developer**

1.1 Pattern matching for the switch:

It expands the expressiveness and applicability of switch expressions and statements by allowing patterns and statements by allowing patterns to appear in case labels. It also allows the historical null-hostility of the switch to be relaxed when desired.

There are two new patterns introduced as follows:

Guarded pattern: Uses pattern &amp;&amp; boolean expression for further refinement

Parenthesized pattern

1.2 Sealed Classes:

Enhances the java programming language with sealed classes and interfaces. Sealed classes and interfaces restrict which other classes or interfaces may extend or implement them.

Syntax:

public abstract sealed class Animal

permits Dog, Cat, Rabbit {...}

**Category 2: Specific Developer**

2.1 Restore Always-Strict Floating-Point Semantics:

It makes floating-point operations consistently strict.

2.2 Enhanced pseudo-Random Number Generators:

It provides a new interface type and implementations for pseudorandom number generators to make it easier to use various PRNG algorithms and to better support stream-based operations.

2.3 Strongly Encapsulated JDK Internals:

It strongly encapsulates all non-critical internal elements of the JDK

2.4 Foreign Functions &amp; memory API(Incubator):

It introduces an API by which java programs can interpret code and data outside of the java runtime.

2.5 Vector API(Second Incubator):

It introduces an API to express vector computations that reliably compile at runtime to optimal vector instructions.

2.6 Context-Specific Deserialization Filters:

It allows applications to configure context-specific and dynamic-selected deserialization filters.

**Category 3: Keeping up with Apple kinds of stuff**

3.1 New macOS Rendering pipelines:

It changed the java 2D macOS rendering pipeline for macOS to use Apple Metal API instead of deprecated Apple OpenGL API.

3.2 macOS/AArch64 Port

**Category 4: Cleaning up kinds of stuff**

4.1 Deprecate the Applet API for Removal:

Applet API will be removed as it was deprecated since JDK9 most browsers do not support it anymore.

4.2 Removal RMI Activation:

Although RMI is still used, the RMI activation mechanism is obsolete with the web technology of the last decade.

4.3 Removal Experimental AOT and JIT Compiler:

Remove the experimental java-based ahead-of-time(AOT) and just-in-time(JIT) compiler.

4.4 Deprecate the Security manager for Removal:

Deprecate the Security Manager for removal in a future release. The Security Manager dates from java 1.0. It has not been the primary means of securing client-side java code for so many years.
