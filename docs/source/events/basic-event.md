# Listening to events

## Registering your Event Listener.
### Option 1 using LoadingStages.
By adding a loading stage
EventManager to your main class you will be able to at this point register new EventListeners.
Calling the following code will allow you to do this.
```java
@LoadingStage
public void eventManager(EventManager em) {
  //this is to reference the mod.
  //eventListener means your instance of the event listener.
  em.registerEventHandler(eventListener, this);
}```
