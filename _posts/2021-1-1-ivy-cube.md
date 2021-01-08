---
layout: post
title: "Ivy Cube"
date: 2021-1-1 15:17:56 -0600
categories: solve algorithm commutators easy
published: true
---

# Ivy Cube

I got this on my birthday in Costa Rica. This is fairly easy to solve with intuition but I have a method to solve.

# Initial Thoughts

Corner turner. It *looks* simple. Playing around confirms it can be solved by just messing around.

# Nomenclature

Ivy cube has two types of pieces. I call them "corners" and "leaves".

![nomenclature]({{ site.baseurl }}/assets/ivy-cube/nomenclature.jpeg)


1) Orient the corners

This is relatively easy. I start with the white corners. Then there is usually just one or two corners that need some tweaking. I do this entirely intuitively. If you play around you should get a feel for how the corners move.

When the corners are solved the cube should look similar to this.

![corners solved]({{ site.baseurl }}/assets/ivy-cube/matching-corners.jpeg)

2) Solve the leaves

Obviously if you can solve the leaves without messing up the corners we're done.  I have one algorithm which swaps three leaves.

2.1) Flower Swap

I call this a flower swap (three leaves that form a flower shape)

![Flower Swap]({{ site.baseurl }}/assets/ivy-cube/flower-movement.jpeg)

![Flower Algorithm]({{ site.baseurl }}/assets/ivy-cube/mixed-leaves-algo.jpeg)

(This is my first post, hopefully my way of documenting algorithms makes sense. I think this is easier than defining the movement at the beginning then telling you "RrL'FFbL" or whatever)

Twist the corner on which I drew a green overlay "up" (send the orange leaf up). Twist the red overlay "up". Green back down. Then red down.

**You can reverse the red and green to change the direction the three leaves get swapped.**
I think of it as:

  1. corner of the leaf color I want to go 'up' first
  2. other corner up
  3. first corner down
  4. second corner down
  
You may need to do this a few times to move the leaves around until you either solve the puzzle or get to a point where doing any more swaps will start undoing your other leaves.

2.2) Triangle Swap

You may be left with a final condition which can't be solved with a flower swap. I call it a "triangle" swap. 

![Triangle Swap]({{ site.baseurl }}/assets/ivy-cube/triangle-swap.jpeg)

I'm sure I could come up with an algorithm for this. But in the spirit of lazy cubing we'll just use a Conjugate. ([RebKB has a great video on conjugates here](https://youtu.be/3WLb0VddFNg)).

In the example picture we'll take the green leaf and move it to make a flower with the orange and white leaves.

Your setup moves might be a bit different (there is more than one way to make the flower). Ideally you would memorize the setup moves so you can undo them after the algo. But on an ivy cube it's easy enough to undo the setup intuitively.

![Triangle Setup]({{ site.baseurl }}/assets/ivy-cube/triangle-post-setup.jpeg)

After the setup you can do the flower swap as normal. It won't look solved, but after undoing the setup moves you should be done!
![Triangle Post Algorithm]({{ site.baseurl }}/assets/ivy-cube/triangle-post-algo.jpeg)

# Done!
![Triangle Solved]({{ site.baseurl }}/assets/ivy-cube/solved.jpeg)