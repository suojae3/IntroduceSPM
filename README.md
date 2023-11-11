# Getting to Know Swift Package Manager

<br/>

#

## How to use it?

![Untitled](Getting%20to%20Know%20Swift%20Package%20Manager%20e0d9f8f071004a4eb7d72826e4801379/Untitled.png)

- SwiftPM consists of four command line tools, and at the top level Swift Command.

<br/>

![Untitled](Getting%20to%20Know%20Swift%20Package%20Manager%20e0d9f8f071004a4eb7d72826e4801379/Untitled%201.png)

- Switch to that directory and we will run Swift Package init with the type executable

<br/>

![Untitled](Getting%20to%20Know%20Swift%20Package%20Manager%20e0d9f8f071004a4eb7d72826e4801379/Untitled%202.png)

- We have the Package.swift manifest file, which describes the structure of the package.
- We get a basic README. You have the Sources directory with a subfolder for our helloworld target. And the main.swift file for our executable.

<br/>

![Untitled](Getting%20to%20Know%20Swift%20Package%20Manager%20e0d9f8f071004a4eb7d72826e4801379/Untitled%203.png)

- A package consists of three major parts; dependencies, targets and products. And we'll look into each of these in more detail in the following.
- A target describes how to build a set of source files into either a module or a test suite.

<br/>

![Untitled](Getting%20to%20Know%20Swift%20Package%20Manager%20e0d9f8f071004a4eb7d72826e4801379/Untitled%204.png)

- SwiftPM uses llbuild as its underlying build engine. llbuild is a set of libraries for building build systems. And it's built around a general purpose and reusable build engine.
- This provides us with ability to do fast as well as correct incremental builds. And is also used by Xcode's new build system. It is also the part of the Swift open source project.

<br/>

![Untitled](Getting%20to%20Know%20Swift%20Package%20Manager%20e0d9f8f071004a4eb7d72826e4801379/Untitled%205.png)

- Developing software in isolation with all dependencies explicitly declared ensures that even packages with complex requirements can be reliably built and used in different environments.
- We also leverage build sandboxing so that nothing can write to arbitrary locations on the file system during the build.

<br/>

![Untitled](Getting%20to%20Know%20Swift%20Package%20Manager%20e0d9f8f071004a4eb7d72826e4801379/Untitled%206.png)

- SwiftPM also supports testing. This is based on the XCTest framework that you're already familiar with. We support parallel testing, so that you can get your test results faster.

<br/>

![Untitled](Getting%20to%20Know%20Swift%20Package%20Manager%20e0d9f8f071004a4eb7d72826e4801379/Untitled%207.png)

- One such feature is edit mode, which allows overwriting all transitive occurrences of a specific package, with a locally checked out copy so that temporary edits can be made, and changes to transitive dependencies can be tested without having to forward all packages in the graph upfront.
