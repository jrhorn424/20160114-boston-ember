[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

> Components and Dependency Inversion: or, How I Learned to Stop Worrying and
> Love Encapsulation
>
> You want to use components, but they're not yet routable. I'll demo a simple
> application that almost entirely componentized. This architecture with a
> simple app makes the "data down, actions up" principle a bit overkill. I'll
> demo how to bind the store to your component using dependency injection,
> keeping the component actions and markup clean and simple.

# Components and Abstraction

| Speaker | [Jeffrey Horn](http://hello.jrhorn.me)                                                                            |
|---------|-------------------------------------------------------------------------------------------------------------------|
| Title   | [Web Development Immersive Instructor](https://generalassemb.ly/instructors/jeff-horn/3305) at General Assembly   |
| Event   | [Boston Ember.js Meetup](http://www.meetup.com/Boston-Ember-js/events/227108545/)                                 |
| Date    | Thursday, January 14, 2016                                                                                        |
| Video   | [Full Video](https://www.youtube.com/watch?v=wLEVTqWbQNc), [My Talk](https://www.youtube.com/watch?v=xmicWu1li9E) |

![opinionated](https://cloud.githubusercontent.com/assets/388761/12339760/ad1d325e-bae4-11e5-93bc-a75bdcc03a37.gif)

This talk contains opinions. I like being wrong. Let's chat or, if you prefer,
exchange ideas through
[issues](https://github.com/jrhorn424/20160114-boston-ember/issues).

## A Radical Idea

> ![injection](https://cloud.githubusercontent.com/assets/388761/12340199/54d9884c-bae7-11e5-9578-4a74fee4d799.png)
> From [ember.js - how to inject a store into a component (when using localstorage adapter) - Stack Overflow](http://stackoverflow.com/questions/28305159/how-to-inject-a-store-into-a-component-when-using-localstorage-adapter)

## DDAU

-   Makes component redistribution easy
-   Makes flow explicit in markup
-   Many small decisions must be made at each layer

> ![diagram](https://cloud.githubusercontent.com/assets/388761/12339386/dc1cc062-bae2-11e5-85be-ae33da715b2c.png)
> From [Communication Between Distant Components - Ember Igniter](http://emberigniter.com/communication-between-distant-components/)

## Encapsulated Components

![58269027](https://cloud.githubusercontent.com/assets/388761/12339892/9d328fe6-bae5-11e5-80e6-d361bde9e686.jpg)

-   Components are UI "one-offs"
-   Encapsulation over redistribution
-   Use injected service buses for communication
-   Hides signals from markup

## The Demo App

The demo app is a simple list maker. It can be characterized by having:

-   Single view, single route
-   No single-item views
-   Nested components
-   Persisted UI state

![demo](https://cloud.githubusercontent.com/assets/388761/12339395/e809372a-bae2-11e5-8073-89bcee5a7351.png)

## Suggested Readings

-   [Parent to Children Component Communication for UI State - Ember Igniter](http://emberigniter.com/parent-to-children-component-communication/)
-   [Communication Between Distant Components - Ember Igniter](http://emberigniter.com/communication-between-distant-components/)
-   [ember.js - how to inject a store into a component (when using localstorage adapter) - Stack Overflow](http://stackoverflow.com/questions/28305159/how-to-inject-a-store-into-a-component-when-using-localstorage-adapter)

[Elad](https://github.com/SaladFork) had a great suggestion to create a ListItem
service after the talk. Here are some references from our conversation:

-   [Introduction to Ember.js |](https://teamgaslight.com/training/courses/14-introduction-to-ember-js)
-   [Ember.js - Application Concerns: Services](https://guides.emberjs.com/v2.2.0/applications/services/)
-   [Ember Best Practices: Actions Down, Data Up... wait what?](https://dockyard.com/blog/2015/10/14/best-practices-data-down-actions-up)
-   [How Ember Data affects data down, actions up](http://www.samselikoff.com/blog/how-ember-data-affects-data-down-actions-up/)

Special thanks to Elad for not only giving me great stuff to read, but also for
not blaming me for being unable to pronounce his name at the end of my talk. 😄

## [License](LICENSE)

Source code distributed under the MIT license. Text licensed under the
[wtfpl](http://www.wtfpl.net). General Assembly copyright General Assembly,
Inc., all rights reserved.
