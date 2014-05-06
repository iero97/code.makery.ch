---
layout: post
title: Introduction to Programming with Kara
date: 2012-10-02 00:00
slug: introduction-to-programming-with-kara
published: true
prettify: true
comments: true
tags:
- Java
- Dart
---

Kara offers a playful introduction to fundamental concepts of programming. Kara is a ladybug that lives in a simple world with trees, leafs and mushrooms.

![Kara](/assets/blog/12-10-02-introduction-to-programming-with-kara/kara.png) ![Mushroom](/assets/blog/12-10-02-introduction-to-programming-with-kara/mushroom.png) ![Leaf](/assets/blog/12-10-02-introduction-to-programming-with-kara/leaf.png) ![Tree](/assets/blog/12-10-02-introduction-to-programming-with-kara/tree.png)

The rules of Kara's world are simple:


#### Actions

* Kara can move around with `move()` (Kara can push a mushroom, can step on leafs but can't walk through trees)
* Kara turns left or right with `turnLeft()` or `turnRight()`
* Kara puts down a leaf with `putLeaf()`
* Kara picks up a leaf with `removeLeaf()`


#### Sensors

* Kara checks if he stands on a leaf with `onLeaf()`
* Kara checks if there is a tree with `treeFront()`, `treeLeft()`, or `treeRight()`
* Kara checks if there is a mushroom in front with `mushroomFront()`


## A Sample Exercise

Kara is placed in the following world setup and must be programmed to collect all leafs until he reaches the tree:

![Kara Collects Leafs](/assets/blog/12-10-02-introduction-to-programming-with-kara/kara-example-collect-leafs.png) 

One solution would be as follows:


#### Kara Collects Leafs

<pre class="prettyprint lang-java">
while (!treeFront()) {

  if (onLeaf()) {
    removeLeaf();
  }
  
  move();
}
</pre>


## Kara Versions - Which Kara Should I Use?

Kara has many different versions. The original Kara is designed as a finite state machine with a purely graphical program editor. See the full list of [available Kara versions](http://www.swisseduc.ch/informatik/karatojava/index.html).

I usually prefer to start directly with writing code in the Java or Dart language. Now there are quite a few possible editors/libraries:


### DartKara (Dart)

DartKara is a scenario written in Dart. It can be used in the Dart Editor which is a very nice and simple development environment. The scenario comes with handouts and exercises. You can find those resources on the [Dart](/dart/) page.


### GreenfootKara (Java)

Since I really like the editor of the [Greenfoot IDE](http://greenfoot.org) I decided to create a Kara version that works with Greenfoot, it is called GreenfootKara. In addition to this I wrote an entire beginners course of 16-20 lessons with exercises and handouts to go along with GreenfootKara. You can find the links to the German and English versions on the [GreenfootKara](/java/greenfoot-kara-intro/) page.


### GameGridKara (Java)

Sometimes, especially if time is too short, it might be good to directly start with a professional development environment like Eclipse or NetBeans. Since it was not possible to integrate Greenfoot into Eclipse/NetBeans, I had to find another solution. Altough, we could start JavaKara from Eclipse/NetBeans, there are just some things that are not possible (like programming an interactive Kara game). The solution was to port the code to work with a library called *JGameGrid*.

GameGridKara enables us to use Kara in any IDE of our choice by simply adding two jar files to a project. The link to GameGridKara with the adjusted beginners course in German and English can be found on the [GameGridKara](/java/gamegrid-kara-intro/) page.


### JavaKara (Java)

JavaKara is the original editor. You can find the [JavaKara download and resources here](http://www.swisseduc.ch/informatik/karatojava/javakara/index.html) (in German).










