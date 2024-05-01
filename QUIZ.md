### How does the DevBoard handle received serial messages? How does this differ from the naïve approach?

The DevBoaard handels recieved serial messaged though an interrupt which then pauses the main program execution. This differens from the naive approach which continuously polls the serial port for incoming data.

### What does `detached_callback` do? What would happen if it wasn't used?
'detahed_callback' is a function that is detached and allows the parent thread to continue executing independently of the detacked one. If it wasn't used there many not be a way to handle the completion of the detached tasks. 

### What does `LockedSerial` do? Why is it _necessary_?
'LockedSerial' ensures thread safety by making sure that only one thread can access the serial interface at a given time. This prevents data corruption and other issues that can happen when multiple threads acess the same resources at the same time. 
