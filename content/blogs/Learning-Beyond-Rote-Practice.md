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

When browsing the internet and talking to new game developers, I have noticed math is often viewed as a barrier to creative development. In this blogpost, I want to show some techniques I’ve used to make math another tool in my toolkit to create interactive experiences. This blog post will not explain all of the math that you will likely encounter through a game development or animation journey. If you wish to start there, you can reference my list of [helpful learning resources](https://github.com/kevinsadi/Links).

However, I believe this blogpost will be helpful even if you do not yet feel comfortable with the fundamentals of the math used in game development. This blogpost reframes math to be a creative tool. Math can be leveraged to assist in visualizing what is in your mind, similar to the tools are built into your game engine of choice. Moreso, I believe it is not impossible for anyone to learn how to use math in a creative way. Furthermore, this can be expanded to overcome any barrier in the way of creating. Here, I explain the learning strategies I’ve used to help make this shift of mindset when I use math in my own projects.

# A Personal Story

I was never the best at math classes in early education. While I found the content interesting, I lagged behind my peers. I saw many of my friends follow the advanced math tracks, while I struggled to wrap my head around the basics of algebra. I wouldn’t understand why I wouldn’t progress. The content was interesting, but some concepts would not remain in my mind after an exam. Eventually, I reached precalculus and I was failing my exams. I was an overachieving child, so it shocked me to see I was doing so bad. Luckily, I was given the opportunity to go to a local tutor. She volunteered to help teach the local community for free. Once every other week she would set up a small white table in the park, and she would call over students from the park to ask their questions. 

She taught me the higher level ideas of what I was learning in my classes. She would ask me guiding questions that seemed to directly target what I did not understand. She pushed me to think outside of the context of the exact problem that I was working on. I could understand what y=x would look like on a graph. However, would I understand what that line meant? Did I understand that it was the valid solutions to that same equation? I was good at finding the patterns to solve an exact question, but it was the first time I started working outside of that boundary. I became a lot more comfortable with failure and asking questions even if I thought the would percieve the question as stupid. Since then, math started to click in the final two years of my high school education. With lots of work, I now study computer graphics, a field which uses techniques entirely guided by mathematical principles.

Until recently, despite my background in mathematics, I still viewed mathematics as a barrier to my creative journey. I recognized when math was *necessary* to accomplish a task. However, it was still difficult to apply what I’ve learned in contexts outside of where I’ve directly seen it used before. A peer recommended that I should read [“Make It Stick, The Science Of Successful Learning”](https://www.amazon.com/Make-Stick-Science-Successful-Learning/dp/0674729013) by Peter C Brown. The book called me to practice a lot of the same principles taught to me by that same tutor those years ago. From there, I started to become more creative with how I used the math that I've learned before.

# Rote Practice
Rote practice, which is also referred to as rote learning or rote memorization, refers to a technique of learning where you learn by repeating the same process without necessarily understanding the underlying concepts or principles. Rote practice is employed when writing a formula over and over with the hope of learning it. Rote practice sessions are often long and intense. This is also known as “cramming.”

The process of strengthening our mental representations of concepts for long term memory is called consolidation. This is the process we want to target and encourage by moving away from rote and massed practice. I argue that you can strengthen this process through challenging yourself. Specifically, by spacing your practice, interleaving practice, and expanding on and testing yourself after coming to a solution. Let’s begin by discussing the importance of quizzing oneself.

## The Testing Effect:
It is very easy to have an illusion of knowing. We are always attempting to make judgements on just how much we know or don’t know something. In Daniel Kahneman’s, professor of psychology at Princeton, book “Thinking, Fast and Slow,” he describes two different systems of thinking. One is very quick, and one is very slow. The quick system of thinking is the one we find ourselves relying on most of the time through our day to day. This is the system we rely on when we make quick split second decisions like which direction to go when we walk out of our house in the morning. However, this system is very prone to mistakes. We must ensure that we are not making mistakes when we believe we know a subject matter well. Two cognitive scientists, Roediger and Karpicke, released a very influential paper in 2006 that described what they call the “testing effect.” The study found that taking a test on material you have learned significantly improves the long-term retention of that material more than just re-reading the material. This suggests that active effort with the material is more conducive to long term learning than passive rote practice.

## Interleaved, Spaced, Periodic Practice:
Next, let us discuss the importance of spaced and interleaved practice. Decades of research on memory and recall have led to the same result on what is called the “spacing effect.” This effect describes that having spaced study sessions often results in more effective learning. This can be seen by a study conducted by Cepeda et al. (2006) in which participants were asked to recall verbal phrases. They found that participants who used spaced practice on memory tasks remembered the material better than those who used massed/rote practice in 259 out of the 271 total trials. This was supported as far back as 1993 by a study by Bahrick et al. that also independently found that spaced repetition has led to better learning. They did so by testing the retrieval abilities of 27 PhDs after giving them information to memorize all at once, and also giving it to them in spaced quantities. They also discussed the importance of periodic practice in the paper. Consistently referring back and practicing the material gives more opportunities to undergo retrieval of the material, better consolidating it in the mind.

# An Example: Virtual Gardening

Let’s walk through an example in the world of Computer Graphics. For this example, I assume some mathematical knowledge. This information can be found on my [helpful learning resources](https://github.com/kevinsadi/Links). I encourage you to attempt to create a virtual garden yourself. You can use this example to learn any tool along the way, depending on your comfort level. If you are entirely new, try to do this example in Blender. If you have some programming experience, try Processing. If you already understand graphics programming, try to follow along using OpenGL.

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

Congratulations on creating your own virtual garden. While we can celebrate now, it’s not time to remove all this information from your brain. *Try to quiz yourself*. I cannot stress how important quizzing yourself is to inform how much you have interalized the content. It may point out some lapses in knowledge that were not immediately apparent. When you’re done, feel free to compare your answers. I’ve also attached my [OpenGL implementation](https://github.com/kevinsadi/Links) here if you want to try to implement this exercise yourself.

### Questions:
* How many distinct vertices would you need to create a cube? Hint: a cube has 6 faces?
* How would the above question be different if we could reuse vertices? What if we can’t?
* Why might this be significant?

### Answers:
* 36 vertices. 6 vertices per face * 6 faces. We don’t reuse any points.
* It would only take 8 vertices. One for each corner of a cube.
* We have to store less data for a mesh if we have less vertices. Efficiency is everything for real-time graphics applications.

# Conclusion

Throughout this example, I attempted to point out where I was using the learning techniques outlined above instead of Rote Learning. Using effortful recall, the testing effect, and interleaved practice allowed me to be less intimidated to use these mathematical principles to create my terrain. It also helped me a lot to not be afraid to fail. When I failed, I also learned. In this way, it was exciting to fail, because I knew everytime I failed I learned. However, It is challenging to practice using these techniques instead of rote learning because they feel as though they take longer. This is okay, and it's human. 

I personally found it incredibly satisfying to see all of these lessons being shown through arbitrary problems that I encountered in computer graphics. It was a good exercise in practicing my understanding to write it out, and I encourage you to go out and play with the concepts yourself. I have included links of resources that are good to get initial understandings of the content, so that you can go on and extend and experiment with the concepts yourself later.

# Resources

* [Great site for learning graphics and openGL](https://learnopengl.com/Introduction)
* [Processing tutorials by the creator of Processing himself.](https://processing.org/tutorials)
* [The famous donut tutorial. Great resource for learning Blender.](https://www.youtube.com/watch?v=nIoXOplUvAw)