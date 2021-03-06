### Stores

As we mentioned above, Stores contain and manage your application's model and logic pertaining to a particular domain of your application. As a result an application can have many stores, each focused on a specific aspect of your domain. Stores are subscribed to the Dispatcher, our event bus, and listen to Actions that are relevant to them. The important part, is that nothing outside the store can modify the application state stored within it directly. Nothing outside the Store should know how the store manages its state, and the Store can be accessed in read-only fashion, i.e. by providing getters to the outside world.

In summary, the only way for a Store to modify the domain model of your application is by responding to an action coming through a Dispatcher.
