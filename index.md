## Updating UI

Updating UI is the process of re-drawing User Interface API whenever data changes within an application.

Usually applications gather data from various sources such as databases and draw them onto the monitor in a user-friendly way. 
Back in the day's applications even had to draw these interfaces on various operating systems with 2d graphical APIs that provided functions to draw shapes such as rectangles, circles. 
Those shapes are composed to form components such as labels, buttons, input texts and various different ones to display data in a format that can easily be read and understand by an application user.
Those 2D API created vertices and textures send to the graphics cards and then being displayed by the monitor.

Luckily over time, the process had become much easier. 
Modern operating systems offer components to developers that can be used rather than being stuck with a 2D API that is pretty bare metal and forces everyone to recreate such functionality.
 
Especially when we think about user interaction to cause changes to the data we display we come to a question. 
How do we maintain the displayed data to be always up to date towards our data from our data sources and how do we do it in a responsive way?

What sounds like a rather trivial problem is in fact pretty difficult when developers need to implement it.

In fact, there seem to be so many concerns, that there are tons of ways how this is being handled. 
However, we need to look very deep into the UI frameworks to understand how they are functioning.

Looking at today's approaches from various communities such as the web community with Angular or React or the whole Cross-platform community with tools such as Flutter & NativeScript its definitely 
the right time to re-explore computer science history.

There is definitely space for improvement learning and exchanging concepts from the good old days of computer history and leverage synergies by adapting new patterns or applying proven patterns to the new
web technologies. 
So let's start with a short history of UI interfaces. 

### Short history of UI interfaces

Apple is being known for a company always creating the best user experiences when it comes to user interaction and personal devices. 
Steve Jobs has been the creator of the whole personal computer history in a time when computer were heavy machines only optimized to commercial 
use within companies.

Even though Apple did not invent the concept of a User Interface for computers (actually it was invented by Xerox PARC, a research institute), Apple made it popular with "Apple Lisa" from 1983.
Still, today's concept of UI development does not come from this early stage. 

Steve Jobs seemed to reach his full potential after he left Apple and founded a company called NeXT. The computers that NeXT produced were too expensive to be a commercial success, but 
when Apple had its commercial crisis without Steve Jobs, he returned and integrated NeXT software and tools for UI development into macOS.

Since then the concepts of UI development sustain for macOS, OSX, iOS, watchOS, and iPadOS (i like marketing these days). 
Various other computer manufacturers and software developers have been inspired since then by what Apple created and integrate these concepts. 

It's impressive that the concepts created back in the time still hold valid until today despite all the disruptions that user interfaces had such as touch devices, mobile phones, and screens of various sizes including watch or TV and even VR/AR. 
The concepts barely changed, the implementations did though.

So what does all of this have to do with updating UI and displaying data changes to users?

We'll have to understand that UI is being composed of various components and how this is being done so let's start to take a look at how Apple implemented it.

### OSX, Quartz, CoreGraphics, UIKit/AppKit

Both iOS and macOS contains a stack of graphical frameworks. Those frameworks are the actual implementation of the user interface concepts from back in the time.
So lets take a look on their purpose and how they are functioning:

| Framework | Purpose |
-----------------------
| Quartz | Quartz is an image processing framework. It provides functionality to draw images and optimize quality by applying filters such as Anti-aliasing or half-pixel rendering. Quartz actually consists of the Quartz Compositor which actually acts as a window server and Quartz2D which provides image operations in order to draw images to any output device such as a graphics card. Also Quartz uses an internal component called Quartz Extreme to utilize hardware acceleration for tasks that run best on accelerated graphics hardware. |
| CoreGraphics | CoreGraphics is the 2D library of Apples Ecosystem. It is capable of drawing shapes such as circles, rectangles and utilized Quartz to optimize the image quality and process these optimizations in the most effective way. |
| UIKit/AppKit | UIKit and AppKit contain a set of already created components utilizing the drawing capabilities of CoreGraphics. In addition UIKit and AppKit contain the interaction handling with these components for eg. Touch Handling for UIKit or MousePointer handling for AppKit |



