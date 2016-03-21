# Redux.js

By [Barry Steyn](basteyn@microsoft.com)

~~

# What Is Redux?
## A Utility For Handling State Change

 * Why can't we just use MVC?

~

# MVC
## A Common pattern in frameworks

  * State stored in model
  * View and controller can cause model update
  * Not easy to understand causality relationships

~

# Why Is MVC So Bad?

There is no "centralized" control:

  >  A model can update another model, then a view can update a model, which updates another model, and this, in turn, might cause another view to update. At some point, you no longer understand what happens in your app as **you have lost control over the when, why, and how of its state**

~
# Facebook's Problem

<iframe class="stretch" src="https://www.youtube.com/embed/nYkdrAPrdcw?start=753&end=924&version=3" frameborder="0" allowfullscreen></iframe>

~~

# Flux
## Facebook's Solution

 * Flux attempts to make state mutations predictable
 * It does this by imposing certain restrictions on how and when updates can happen

~

<iframe class="stretch" src="https://www.youtube.com/embed/nYkdrAPrdcw?start=639&end=715&version=3" frameborder="0" allowfullscreen></iframe>

~~

# Flux
## Very minimal

 * Many implementations
 * Sparsely defined

~

# Redux
## Flux + Reducer = Redux

Using concepts of a **reducer** and **flux**, *Redux* was born
**Reducer** comes from the functional term *reduce* as in *map-reduce*

~

# Three Principles Of Redux

 1. **Single Source Of Truth** - there is only one store
 2. **State Is Read-Only**
 3. **Changes Are Made With Pure Functions**

~

# Well Defined
## Redux Is Well Defined

 * Allot of work has been put into Redux
 * Huge community support

~

# Elegant
## Redux Is Elegant

 * There is just one store
 * Very easy to debug errors due to predictable state changes


~~

# Redux Consists Of

 1. Actions
 2. Action Creators
 3. Reducers
 4. Store

~

# Actions

 * Payloads of information that send data from application to store
 * Are plain objects
 * Must have at least a *type* property

~

# Action Creators

 * A function that returns an action
 * Actions need to be `dispatched` in redux
 * Different from actions: This is useful for server rendering

~

# Reducers
## A reducer changes the state of a store

 * Reducer takes as input the *previous state* and *action object*
 * Produces changes the state of the store by creating a new object
 * Are **pure** functions without state and side-effects

Reducer composition makes things neat

~

# Store

 * Holds application state
 * Registers listeners
 * Handles component unsubscribe

~~

# Redux Data Flow

 1. Call an action creator
 2. Dispatch the created action to the store
 3. Redux store calls the reducers
 4. Store saves new object returned by the reducer
~

# No Race Conditions

Like Flux, Redux actions are synchronous and do not suffer from race conditions

~~

# Redux Middleware

The store can be altered with middleware

~

# Redux Middleware

 * Makes redux async
 * Hot reloading
 * Time machine
 * Logging
 * Many more...

~~

#The End
By Barry Steyn
