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

### iOS/OSX - Quartz, CoreGraphics, UIKit/AppKit

OSX in fact was one 
