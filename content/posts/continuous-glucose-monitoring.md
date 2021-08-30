---
title: "Not-so-Sweet News : Experiments with a CGM"
date: 2021-08-29T17:13:10-07:00
draft: true
---

Data, Code, Analysis: [https://github.com/nuwandavek/spiky](https://github.com/nuwandavek/spiky).

I love food. This, on the surface, is a pretty trite statement. But I don't mean I love food the same way one says "oh you're going to love this!" and show you a mediocre video of a silly dance to which you reply "LOL". Everyone involved in this interaction including the dancers in the video know you did not laugh out loud. I mean that I feel a loss of self-control the same way I feel with respect to matters of my poor, poor heart. It is agonizing to not open the fridge when I'm thirsty and know that there are delicious drinks one door pull away. It is frustrating to say no to a cup full of sunshine and butterflies on ice-cream-fridays. And it sucks to say enough. Matters of the heart, much? So naturally, I bought a Continuous Glucose Monitor (CGM).

{{< figure src="/images/cgm/cgm-1.jpeg" title="Micro-chipped by the govt! :O " width="80%" >}}

## What is a CGM?
A CGM measures your blood glucose levels, which is extremely useful for diabetics. Procuring this device in the US without a prescription was as difficult and trying as anything to do with healthcare here. Almost all startups that are working on metabolic health with CGMs use Abbott' Libre Freestyle line of sensors (with their custom sticker of course). Levels Health has a ton of literature on the correlation of [glucose levels with metabolic health](https://www.levelshealth.com/blog/the-ultimate-guide-to-metabolic-fitness), [and](https://www.levelshealth.com/blog/the-ultimate-guide-to-metabolic-health-and-cancer) [also](https://www.levelshealth.com/blog/what-is-glucose) [on the various thresholds](https://www.levelshealth.com/blog/what-should-my-glucose-levels-be-ultimate-guide) [of glucose](https://www.levelshealth.com/blog/optimal-diet). But here are the main takeaways : 
- Very high/low blood sugar is bad (correlated with heart disease, cancer, and generally a shitty and short life)
- Spikes in glucose are bad
- High mean (especially fasted) glucose is bad

Stable, low-but-safe glucose levels is an ideal to aim for. I wore the CGM for ~10 days and did a bunch of experiments to see how different foods affect my glucose levels. I have not studied biology since the 10th grade, so the things I found were extremely fascinating (and probably already well known to others with a basic bio background). [Here's a notebook I made to analyze the data.](https://github.com/nuwandavek/spiky).

{{< figure src="/images/cgm/cgm-2.png" title="Spiky behaviour" width="100%">}}

## Insights : The Bad
- Sugar is **BAD**. It results in the largest spikes, and the largest falls. Also, sugar elevates the mean blood sugar level - your post-sugar-mean is much higher than the pre-sugar-mean even after the spike has ended. I had cake one evening (for science, of course), which resulted in an increase of ~40 points and a decrease of ~30 points. That's a movement of nearly 70 points in one hour! * shudders *
- Potatoes are bad :(. This was the most heartbreaking discovery. Potatoes cause an increase in blood glucose that lasts longer than any other food I consumed. 
- Alcohol is bad, especially at night. It causes huge variations overnight and is also linked with bad sleep.
- Diet Coke is bad! This one was fascinating! Turns out that our pancreas preempt any glucose spikes using our senses and start generating insulin. So, when the sweet tasting diet soda brings no glucose, our body experiences a sugar crash. Diet soda is also associated with low self control wrt. other sugary drinks.
- My blood glucose is fairly good, if I don't consume the above things. It crosses the lower limit than it does the higher limit - which I read is a function of shock of drastic dietary changes. I hope that stabilizes over time. 
{{< table "table table-dark table-striped table-bordered">}}
|    | date       |   time_over_max |   time_under_min |   time_normal |
|---:|:-----------|---------------------------:|----------------------------:|-------------------------:|
|  0 | 2021-08-16 |0%    |                        1.15% |                    98.85% |
|  1 | 2021-08-17 |0.79% |                       13.34% |                    85.87% |
|  2 | 2021-08-18 |4.9%  |                        4.44% |                    90.66% |
|  3 | 2021-08-19 |2.43% |                        0%    |                    97.57% |
|  4 | 2021-08-20 |0%    |                        0%    |                   100%    |
|  5 | 2021-08-22 |1.16% |                        0%    |                    98.84% |
|  6 | 2021-08-23 |0%    |                        3.59% |                    96.41% |
|  7 | 2021-08-24 |0%    |                       43.38% |                    56.62% |
|  8 | 2021-08-25 |0%    |                       62.44% |                    37.56% |
{{< table />}}
![Some Text](/images/cgm/cgm-3.png)

## Insights : The Good
- There's a spike in glucose every morning when I wake up! It turns out that your body wants you wake up with energy and enthusiasm and pumps you up with glucose (Aww). Working out, hence, is a great way to expend this glucose and ensuring that one does not consume excess calories post workout due to glucose depletion.
- Yoghurt is a superfood! When I had non-fat-Greek yoghurt with protein powder and strawberries, my blood glucose barely rose! This is my go to snack now and a really great substitute for ice cream!
- I do not consume any breakfast and fast till lunch (some version of IF). This period (9am - 12pm) seems to be the most stable glucose time, especially on days I work out! Look at those flat lines! 
![Some Text](/images/cgm/cgm-4.png)

## Conclusion
My sensor stopped working on Day 11 when I went swimming in the ocean. This experiment was extremely useful in anchoring how *bad* certain foods are, and in benchmarking them against other foods. A lot more people at office are doing these experiments now, and we hope to gain a better understanding when we have more data. I am still skeptical how useful monitoring glucose is, long term, but it definitely shocks you into better dietary habits. Take care of yourself, (hopefully not so) sweet child o' mine. 

