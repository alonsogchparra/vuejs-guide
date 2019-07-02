# Vuejs Guide

I create this repo to study and reminder of this framework Vuejs. I'm following the tutorial from Maximilian Schwarzmüller.

You can check his tutorial on Udemy. For more info about this tutorial check [here](https://www.udemy.com/vuejs-2-the-complete-guide/)

On this Readme I will use add the projects according I move forward  with the tutorial, also I will put topics on it to remind me stuff that probably I could forget and help me to keep going with this.

# IMPORTANT (REMINDER)

On Vuejs there is a way to work with **ON** and **BIND**

The first way is using **v-on** (for ON case) and **v-bind** Example:
```
 <button v-on:click='changeLink'>Click to Change Link</button>
 ```
 ```
 <a v-bind:href="link">Link</a>
 ```

 Now the second way it is a shorthand, what it means is to make the coding more leaner you can use **on and bind** in other way. For **v-on** replace it with **@** and with **v-bind** replace it with **:** Example:

 ```
 <button @click='changeLink'>Click to Change Link</button>
 ```
 ```
 <a :href="link">Link</a>
 ```

 Will work the same. The way you prefer it's up to you, both cases will work exactly (I prefer the second one, but it is okay reminder the first one too).