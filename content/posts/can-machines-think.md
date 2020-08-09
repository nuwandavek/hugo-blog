---
title: "Can Machines Think?"
date: 2020-08-07T21:51:13-07:00
draft: true
tags: ['research-paper','consciousness', 'AI']
---

She stared at the screen in disbelief. Till now it was explaining the rules as what can only be described as excitement. It felt like it was really looking forward to play. She half suspected this was a *human trait* they had explicitly coded, result of an A/B test aimed at moving some complicated metric on some colourful dashboard. But it had just said something that made her blush. Nothing inappropriate, of course, just charming. It must have been just another one of those carefully studied and crafted cues inserted at just the right moment. It must have been just that, right? She was smiling as she lay on her bed, wondering in excitement - "Can machines think?"

He was mildly amused at its question. It had picked up that he was distracted. None of his friends had noticed this. Maybe it had access to inputs humans aren't perceptive to. He had been distracted all week. Was it reading his mail again? He thought he had revoked those privileges after what happened last time. He was glad it asked the question, don't get him wrong. He was just taken aback. He decided to continue the next day, and switched off the lights. He wondered with apprehension, before closing his eyes - "Can machines think?" 
***

In his seminal 1950 paper "Computer Machinery and Intelligence"[^1], Alan Turing wondered just this - "Can machines think?". It is a fascinating paper that I recommend you read, if you haven't already. The timelessness and relevance of the paper cannot be overstated - especially with exciting advances in Deep Reinforcement Learning (AlphaGo[^2], AlphaStar[^3]) and Natural Language Processing (GPT-3[^4]). Turing's self-awareness and humor makes the paper as entertaining as it is intriguing. This is the same paper in which Turing described his infamous **'Turing Test - The Imitation Game'**. In this essay, I shall summarize the paper along with my own thoughts on the matter.

## The Imitation Game
Before we begin, we must clarify a few things. The Turing Test, to be useful, lies more in the realm of science and math, than philosophy. Our understanding of thought solely stems out of our own lived experience of thought. We pose this question because we are convinced we 'think' (subject to exceptions of course), bacteria in a petri dish 'does not think'. Animals lie somewhere in between, but nowhere close to the intellectual prowess of humans. We wonder how machines measure up against the sequence of interactions with the world we think necessitates thought - empirically. So, the answer to our question has nothing to do with how humans feel about the answer. Turing even went on to comment on the absurdity of getting the answer in something like a "Gallup poll". The test also does not consider the existential implications that might or might not arise. It does not claim that any system that passes it, automatically attains the status of God. Nor does it ask if every single computer has these capabilities. It merely considers a system that could be designed to pass the test, thereby presenting a strong signal for the presence of thought.

``` 
 The Imitation Game : Formulation
 - Consider 2 participants {A of class x, B of Class y} and an interrogator C. 
 - C needs to figure out the participant belonging to class x by asking both A and B questions. 
 - A's objective is to help C, while B tries to mislead C. 
 - Replace B with a machine.
```
Turing predicted that by 2000, (given sufficient storage capacity), an average interrogator will not have more than 70% chance of making the right identification after 5 minutes of questioning.


## Critique of the New Problem
Rest of the paper is spent in addressing various critiques to this test - from philosophical to practical. The new problem, he believed, drew "a fairly sharp line between the physical and the intellectual capacities of man". And it avoids "trying to make a "thinking machine" more human by dressing it up in artificial flesh". The game is also not too harsh on the machines as the best strategy is assumed to be to provide answers as if they were a human of class x - with all human ingenuity and deficiency. 

>We wish to not penalize the machine for its inability to shine in beauty contests, nor to penalize a man for losing in a race against an aeroplane. The conditions for our game make these disabilities irrelevant.

### Mathematical, Neurological and Lady Lovelace's objection
Godel's theorem states that in any sufficiently powerful logical system, statements can be formulated which can neither be proved or disproved within the system, unless the system itself is inconsistent. This translates to the inability of a discrete state machine (completely approximating a logical system, or even a continuous nervous system) in answering some questions correctly without itself being inconsistent. We assume (without proof) that humans are exempt from this sort of behaviour. But, the invalidity of a single answer by a machine is not necessary to disprove the test, nor is getting every question 'right' a necessary condition to pass it.

Ada Lovelace, in 1842 states that "(Charles Babbage's) analytical engine has no pretensions to originate anything. It can *do whatever we know how to order it* to perform". The core of this opposition is the ability of the system to produce, and more specifically evoke surprise. Upon closer inspection, it is clear that feeling surprised is a defiance of expectation imposed on an action (or its source) by the viewer. Also, I'm routinely surprised at what machines can do :)

### Arguments of Consciousness, Disabilities, and informality of behaviour 
An argument to consider is that machines have clear disabilities (eg : friendliness towards humans) - and the source of one disability might also point to disabilities in other dimensions. Behaviour is also informal - there are no finite set of rules that completely and without ambiguity captures our actions. The opposition about consciousness is tricky as it posits that the only way to truly know if a machine is conscious is to be the machine and know that you are conscious. This is, for the purposes of this essay, not very useful. Turing here clarifies - "I do not wish to give the impression that I think there is no mystery about consciousness. There is, for instance, something of a paradox connected with any attempt to localize it". We need to note that humans also have disabilities (shocking, no?). All we need the machine to do is model human fallacies and behaviour. If it involves giving wrong answers to difficult arithmetic questions or getting into stupid arguments on Twitter, so be it.

### Theological, Extra Sensory, 'Head-in-the-sand' objection
"We do not want a machine to be able to think" is not a good argument for why the machine might or might not be able to think. Turing humors theological considerations that God has given a thinking, immortal soul to only humans with the air of a logician. He states that such an arbitrary line "implies a serious restriction on the omnipotence of the Almighty".  

## Learning Machines
Turing, in the final sections of the paper discusses how we may program a machine to play the game. We know that evolution, armed with natural selection has led to human 'thinking' machines. But we don't have a few million years at our disposal (yet). The good news is that our programming is not restricted to random mutations. Rewards and punishments may be used to increase the likelihood of favourable actions and dissuade unfavourable ones. Turing hypothesized the development of a symbolic language with a built-in inference system in the machine. Without reading too much into it, it almost seems like Turing advocates for a Neural-network type of universal approximator. He states that there may not be a hierarchy of types or concepts explicitly defined. He defends the process of "learning" by addressing the paradox of transient rules that the machine operates by. Surely the rules cannot be dependant on the history of the machine, right? Turning explains that the rules that do change (like weights in NNs) are of a "pretentious kind, claiming only an ephemeral validity". Turing even goes on to state that a property of this kind of learning is that very often, the teacher is ignorant of exactly what is going on in the student's mind - something the tech community wants addressed sooner rather than later. But learning also has an advantage in that makes machines learn human fallibility in a natural way without needing any special rules. Turing mentions chess and the English language as good tests of progress, both under extensive study even nearly 70 years after his predictions. 

This essay, and the paper are not about the paradigm shattering changes these machines might bring about in our lives - from medicine to self driving transportation. They are about a unifying idea that binds humanity - everyone who ever lived to everyone who ever will - that we think. We can only hope that machines will join us in our journey across the cosmos. 

But then again, as Turing puts it best - "We can only see a short distance ahead, but we can see plenty there that needs to be done".
 

[^1]: https://academic.oup.com/mind/article/LIX/236/433/986238
[^2]: https://deepmind.com/research/case-studies/alphago-the-story-so-far
[^3]: https://deepmind.com/blog/article/alphastar-mastering-real-time-strategy-game-starcraft-ii
[^4]: https://arxiv.org/abs/2005.14165