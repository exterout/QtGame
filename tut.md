<h1 align=center> Qt game tutorial</h1>
<p align=right><i>  - &nbsp &nbsp Nirbhay &nbsp &nbsp</i></p>
## 1.Making a Rectangle
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
- make a class bullet  
    - use QGraphicsRect, since we want it to be derivced from a rectangle, 
- we need to add bullet to scene   
    - we use a member function called scene which will return a refrence to scene MyRect is in, and then use addItem(bullet)
- ### signals and slots
    - any item that uses signals and slots has to be derived of Qobject, so we include QObject header file and use `public QObject, public QGraphicsRectItem{...`  
    and we also need to add `Q_OBJECT` macro
    - signal is just a signal and a slot that is mapped to a signal is action that will be peformed when the the signal occurs

    
