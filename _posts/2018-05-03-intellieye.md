---
layout: post
title: IntelliEye
thumbnail: "/img/og_intellieye.png"
---

When I am not talking about information retrieval research/education, I usually talk about MOOCs in this blog. 
While IR and MOOCs seem pretty unrelated, they come together very well in the area of *Search As Learning*. 
Search though is not always necessary for MOOC research, there are plenty of other things one can explore as well.
And sometimes there is just an idea, that sounds challenging as well as interesting and we go for it.

So ... MOOCs ... 

MOOCs suffer from **retention issues**: most MOOC learners start but do not finish. 
Completion rates of **below 5%** is not a rare sights in MOOCs aiming at first year Bachelor knowledge levels.
One culprit is the lack of oversight and directions: learners need to be
skilled in self-regulated learning to monitor themselves and their
progress, keep their focus and plan their learning. Many learners
lack such skills and as a consequence do not succeed in their chosen MOOC. 

Today's MOOCs are set up in a video-centric manner and provide ample opportunities for learners to become
distracted and lose their attention without realizing it. How often have you found yourself checking your emails
or browsing the Web without consciously thinking about doing that? I have, more than once.

Here is what we did about this in our upcoming ACM Hypertext paper ([preprint](https://chauff.github.io/documents/publications/HYPERTEXT2018-zhao.pdf)):

```bibtex
@paper{Hypertext2018IntelliEye,
	author = {Tarmo Robal, Yue Zhao, Christoph Lofi and Claudia Hauff},
	title = {IntelliEye: Enhancing MOOC Learners' Video Watching Experience through Real-Time Attention Tracking},
	conference = {ACM Hypertext},
	year = {2018}
}
```


## Idea

We zoomed in on videos, as they are the most passive type to learning (just watch and listen). 
If we were able to detect online learners' loss of attention **in real-time**, we could intervene (pause the video,
make an annoying sound, etc.) and hopefully return learners' attention to the lecture video at hand. 
How can we detect anything given that our learners are spread around the world? We could use learners'
Webcam feeds. Now of course, we can't really observe learners, but we can design an *automated* method that processes
the Webcam feed and alerts learners when loss of attention is detected. To avoid false positives, we used a few
heuristics to measure inattention:

* if the browser tab/window containing the lecture video is not visible to the learner, we assume inattention;
* if a learner's face cannot be detected for some time we assume inattention unless we are observing mouse
movements at the same time (a sanity check), i.e. we employ face tracking as a robust proxy of attention tracking.

We implemented these heuristics in an open-source system we call [IntelliEye](https://github.com/Yue-ZHAO/IntelliEye), 
that embeds itself into the [edX](https://www.edx.org/) video player widget. Unlike some other MOOC platforms, 
edX allows course designers to execute custom JavaScript. After IntelliEye's deployement, 
the video player widget looks as follows:

<img src="https://chauff.github.io/img/intellieye-player.png" width="500px">



## Deployment
Such as system of course raises a lot of **privacy issues** and we were
very curious about how learners would react to such an "intervention". We deployed IntelliEye in TU Delft's self-paced MOOC
*[Introduction to Aeronautical Engineering](https://www.edx.org/course/introduction-to-aeronautical-engineering)*; 
the first time learners loaded a course page with a video player
that had IntelliEye embedded (we ran a few sanity checks to avoid IntelliEye's activation on old hardware for instance), they 
received these instructions:

<img src="https://chauff.github.io/img/intellieye-instructions.png" width="500px">

Learners were able to deactivate IntelliEye at any point in time. 

IntelliEye was deployed for ten weeks (the MOOC itself ran much longer); 
it was available for all videos within the MOOC. A total of 2,612 different learners visited the MOOC during 
the deployment period and were exposed to IntelliEye.


## Questions

We were interested in three questions:

- **Technological capabilities**: to what extent is MOOC learners' hardware capable to enable the usage of technologically 
advanced widgets such as IntelliEye?
- **Acceptance**: To what extent do MOOC learners accept technology that is designed to aid their learning but at the same 
time is likely to be perceived as privacy-invading?
- **Effect on behaviour**: What impact does IntelliEye have on learners' behaviours and actions (if any)? 

For this last question we evaluated three approaches to 'alert' the learners that have decreasing levels of annoyance built in:
- *pausing the video* when inattention is detected, 
- *ringing a bell repeatedly* when inattention is detected,
- *flashing a red border* around the video player.

Learners were randomly assigned to a single alert condition.


## Results

**78%** of our MOOC learners used hardware and software setups which are capable to support such widgets, making the
wide-spread adoption of our approach realistic, at least from a technological point of view.

**67%** of learners with capable setups was (not surprisingy) reluctant to allow the use of Webcam-based attention tracking techniques. Among those that gave us a reason for disabling (a quarter of them had tried IntelliEye at least once), most remarked that they were capable of attention tracking themselves (the literature says otherwise). Privacy was the third most popular reason for disabling IntelliEye:

<img src="https://chauff.github.io/img/intellieye-disable.png" width="500px">

Among the learners using IntelliEye we observe (i) high levels of inattention (on average one inattention episode occured every
**36 seconds**, a much higher rate than reported in previous lab studies, where attention is usually held a few minutes at least.

Learners **adapt their behaviour towards the technology**: learners in conditions that disturb (well, annoy) the learner when 
inattention occurs exhibit fewer inattention episodes than learners in a condition that provides less disturbance. Besides their behaviour though, we did not see any significant changes in their learning outcomes (also hard to measure due to the limited deployment period).

Over time we saw neither an increase nor a decrease in IntelliEye's use:

<img src="https://chauff.github.io/img/intellieye-sessions.png" width="900px">

The two main takeaway messages are really the extraordinary low attention levels (though of course this requires further research) we found and the fact that a substantial number of MOOC learners are *not* adverse to trialing such technology. 
