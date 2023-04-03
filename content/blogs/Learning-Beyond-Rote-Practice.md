---
title: "Learning Beyond Rote Practice: Embracing Failure"
date: 2023-03-10T23:29:21+05:30
draft: false
github_link: "https://github.com/kevinsadi"
author: "Kevin Sadi"
tags:
  - Math
  - Computer Graphics
  - Learning
image: /images/blogs/rote/plane.png
description: ""
toc:
---

I was never the best at math classes in early education. While I admit I was in the advanced track for all of my other classes, I found I would lag behind in my math education. I saw many of my friends take advanced Calculus or the advanced math tracks, while I struggled to wrap my head around the basics of algebra. I wouldn’t understand why I wouldn’t progress. Eventually, I reached precalculus and I was failing my exams. It was the first time I ever did not get an A, let alone fail. Stubborn as I was, I went to a local tutor and she sat down and taught me the higher level ideas of what I was learning. She would ask me guiding questions that seemed to directly target what I did not understand. Since then, in the final two years of my high school education, I came to enjoy math. I worked very hard and I found myself in the AP Calculus classes in my senior year. I now study computer graphics, a field which uses techniques entirely guided by mathematical principles. Some new game developers find math scary. I want to show some techniques I used to make math another tool in my toolkit to create interactive experiences.

Rote practice, which is also referred to as rote learning or rote memorization, refers to a technique of learning in which information is constantly repeated and drilled without necessarily understanding the underlying concepts or principles. This is what I used in my early math education. Rote practice is employed in the practice of writing a phrase from a play over and over again on a piece of paper to hope that the content will stick in the mind. This massed practice makes use of practice sessions that are long and intense. This is the same process of “cramming.”

Throughout this blog, we will instead explore the importance of embracing failure and learning from it. It’s easy to find yourself be paralyzed when you are faced with a problem you do not know how to immediately solve. It’s also easy to come to a solution that you do not entirely understand and opt to move on. There is a lot to be learned in simply attempting a problem and seeing what it is that you do not exactly understand. I try to not beat myself up about it. Instead, I breathe and consider:

* What other solutions are possible? What are the pros and cons of each solution?
* Why doesn’t my solution work?
* Where did I get stuck?
* What tools do I have that could potentially move me in the right direction?

It is okay to get stuck. If you never begin, you can never get closer to the answer. I am aware that this is advice that is constantly echoed in many circles, but I found it is easy to get stuck in one’s head regardless. At least, for me, I found I would learn this lesson in one part of life, but then forget it again when I come to apply it to another aspect of life. In this blog, I point out ways that deeper learning techniques could be applied to accomplish a computer graphics task.

# Psychological Studies and Backing

The process of strengthening our mental representations of concepts for long term memory is called consolidation. This is the process we want to target and encourage by moving away from rote and massed practice. I argue that you can strengthen this process through challenging yourself. Specifically, by spacing your practice, interleaving practice, and expanding on and testing yourself after coming to a solution. Let’s begin by discussing the importance of quizzing oneself.

### The Testing Effect:
It is very easy to have an illusion of knowing. We are always attempting to make judgements on just how much we know or don’t know something. In Daniel Kahneman’s, professor of psychology at Princeton, book “Thinking, Fast and Slow,” he describes two different systems of thinking. One is very quick, and one is very slow. The quick system of thinking is the one we find ourselves relying on most of the time through our day to day. This is the system we rely on when we make quick split second decisions like which direction to go when we walk out of our house in the morning. However, this system is very prone to mistakes. We must ensure that we are not making mistakes when we believe we know a subject matter well. Two cognitive scientists, Roediger and Karpicke, released a very influential paper in 2006 that described what they call the “testing effect.” The study found that taking a test on material you have learned significantly improves the long-term retention of that material more than just re-reading the material. This suggests that active effort with the material is more conducive to long term learning than passive rote practice.

### Interleaved, Spaced, Periodic Practice:
Next, let us discuss the importance of spaced and interleaved practice. Decades of research on memory and recall have led to the same result on what is called the “spacing effect.” This effect describes that having spaced study sessions often results in more effective learning. This can be seen by a study conducted by Cepeda et al. (2006) in which participants were asked to recall verbal phrases. They found that participants who used spaced practice on memory tasks remembered the material better than those who used massed/rote practice in 259 out of the 271 total trials. This was supported as far back as 1993 by a study by Bahrick et al. that also independently found that spaced repetition has led to better learning. They did so by testing the retrieval abilities of 27 PhDs after giving them information to memorize all at once, and also giving it to them in spaced quantities. They also discussed the importance of periodic practice in the paper. Consistently referring back and practicing the material gives more opportunities to undergo retrieval of the material, better consolidating it in the mind.

# An Example: Virtual Gardening

Let’s walk through an example in the world of Computer Graphics. We’re going to keep things relatively high-level throughout this example, but it may still be a bit confusing. I encourage you to go and attempt to create a virtual garden yourself. You can use this example to learn any tool along the way, depending on your comfort level. If you are entirely new, try to do this example in Blender. If you have some programming experience, try Processing. If you already understand graphics programming, try to follow along using OpenGL.

Do not worry, we will leverage our learning skills and practice generative learning as we walk through the example. The effort will add to our learning experience. Consider the case of wanting to create a virtual garden. The first step will be just to make a 2D plane in a 3D space. Try to think of what that would look like before moving on. The process of visualizing this space yourself practices effortful learning.

![2d plane in 3d space](/images/blogs/rote/plane.png)

Let’s notice that this plane has 4 points in 3D space that define it. These are the only points we need to create our 2D plane. But now, let’s add an additional constraint. Let’s consider the case where you want to create the same shape using only triangles? Can you think about how you could approach using those same points to create the same shape, but only with triangles? Often, in computer graphics, all of the 3D geometry (shapes) that you see is composed of many triangles. This is because the hardware on the computer is optimized to render (make images appear) on your screen.

![3 Points on a plane](/images/blogs/rote/3points.png)

Let’s say that we can make two triangles out of the plane. Let’s focus on 1 triangle and select corners 1, 2, and 3. We often call these points in 3D space “vertices.” We can use these 3 vertices to define a triangle in 3D space. We can have a vector point away from the face that we just created using these three points. This is called a normal vector, and it is often leveraged to create shading effects on the surface of an object that we make.

![Annotated Image](/images/blogs/rote/drawn.png)

Great! We now have a single triangle. We can apply the same idea to create a second triangle, and we have a plane. You might notice that if we wanted to make a second triangle, the points overlap. What could we do in this situation? Well, we can start off simple and just say we won’t reuse vertices. Thus, it would take 6 vertices to define the 2d plane. However, as we create larger models that use more shared triangles, this can blow up very quickly. Instead, we can assign a number to each vertex that defines the plane. Then, we can reference those numbers when we create our triangles, 3 vertices per triangle. Try to wrestle with this idea in your head and truly convince yourself of how it works. Once you have done so, come back to the rest of this. This would help practice generation and effortful learning with the content.

Now that you have convinced yourself of the concept, let’s continue on our example of creating a virtual garden. Now that we have a single plane, we can move any of our 4 vertices to create variations in elevation. However, the amount of elevation variation we can make with 4 vertices is quite limited. Thus, we need more points! We can extend the exact same idea we have above to create a larger plane of many points. This will perceptually look the exact same, but the plane we see will actually be composed of many vertices. We can take these points and use any method to make the ground look more ground-like. In this example, I just manually sculpted the plane to look like rolling hills, but there are many ways to tackle this problem. You can use real elevation data, use Perlin noise to create elevation changes procedurally, or even use Machine Learning to create these changes in elevation!

While we have the general structure of some terrain now, it’s not quite satisfying until we can see some color on our terrain. We can do this using textures. Effectively, we’ll just take any picture that we want and we can put it on top of our terrain. We can do this by assigning every single vertex an extra value. Right now, each vertex has 3 values. The three values correspond to the x coordinate, y coordinate, and z coordinate of the vertex respectively. Now, we can just attach another 2 values to each vertex. One for what x value we want to sample from an image and one for the y value we want to sample from an image. Programs like Blender and Processing handle this for us. However, for OpenGL, you will have to manually specify this yourself.

![The finished project image](/images/blogs/rote/final.png)

Congratulations on creating your own virtual garden. While we can celebrate now, it’s not time to remove all this information from your brain. Try to quiz yourself. I’m sure it’ll point out more than you expect on what might have been shaky from the explanations above. When you’re done, feel free to compare your answers. I’ve also attached my OpenGL implementation here if you want to try to implement this exercise yourself.

### Questions:
* How many distinct vertices would you need to create a cube? Hint: a cube has 6 faces?
* How would the above question be different if we could reuse vertices? What if we can’t?
* Why might this be significant?

### Answers:
* 36 vertices. 6 vertices per face * 6 faces. We don’t reuse any points.
* It would only take 8 vertices. One for each corner of a cube.
* We have to store less data for a mesh if we have less vertices. Efficiency is everything for real-time graphics applications.

# Conclusion

Here we have seen a real example of applying our learning skills while solving a new problem. I hope that this has excited you the same way it excited me when I first started practicing these skills. I feel as though it is very easy to not fully realize when we are not taking full advantage of the skills that we know can be beneficial to our long term learning. It is often difficult to consistently practice these principles as often they feel they take much longer and are less effective than massed practice. It is important to note that this feeling is natural and is very human. I encourage you to try to practice the techniques outlined in the paper, even when they feel difficult at first.

Also, I personally found it incredibly satisfying to see all of these lessons being shown through arbitrary problems that I encountered in computer graphics. It was a good exercise in practicing my understanding to write it out, and I encourage you to go out and play with the concepts yourself. I have included links of resources that are good to get initial understandings of the content, so that you can go on and extend and experiment with the concepts yourself later.

# Resources

* [Great site for learning graphics and openGL](https://learnopengl.com/Introduction)
* [Processing tutorials by the creator of Processing himself.](https://processing.org/tutorials)
* [The famous donut tutorial. Great resource for learning Blender.](https://www.youtube.com/watch?v=nIoXOplUvAw)