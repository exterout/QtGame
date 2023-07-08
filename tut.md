1. QGraphicsScene map or world
2. QGraphicsItem
3. QGraphicsView used to visualize a scene

QGraphicsRectItem 
> by deafault it has length and width as 0, rect->setRect(0,0,100,100);

*to visualize a scene we actually have to add a view*
> we have to tell view which scene we want to visualize

 
>> we can use a pointer or ue setscene

## 2. events
> a event is anything important that happens in the lifetime of the application 
> keyPressEvent() and QKeyEevnt[this stores info about event i.e. what key is pressed]   
event propagation system [who the event is passed to ]  
QDebug [ to print code to console]
create a new custom class 
> right click the method function
___
only one Qgrap.. item can respond to a event once
```cpp
// make rect focusable
rect->setFlag(QGraphicsItem::ItemIsFocusable);
rect->setFocus(); 
```
add this to Myrect source file
> `if (event->key()==Qt::Key_Left)`
> Qgraphicsview will recive the key press and pass it to Qgraphicsscene which inturn will search for the active object inside it and pass the event to it, (here it is MyRect) this MyRect will look look in its memory functions to .. 
## 3. shoot with space bar
-make a class bullet
    
