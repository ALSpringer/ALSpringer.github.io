---
title: "Algorithmic Whitewashing"
layout: post
date: 2018-02-12 12:19
image: /assets/images/markdown.jpg
headerImage: false
tag:
- bias
- machine-learning
star: false
category: blog
author: aaronspringer
description: How Speech Recognition Supresses Cultural Speech
---
Whitewashing in the film industry particularly came to a head with the release of Ghost in the Shell in which Scarlett Johansson was cast to play an Asian heroine. Online communities responded strongly, [starting a petition to rescind her role as the main character]( https://www.huffingtonpost.com/2015/01/15/petition-scarlett-johansson-ghost-in-shell_n_6481288.html). [Activists declared that this was an act of 'whitewashing'](https://www.huffingtonpost.com/summer-noble/why-scarlett-johansson-st_b_6466498.html); the act of taking a culturally important story to a non-dominant group and appropriating it, thereby displacing many cultural elements by casting a white actor in a non-white role. Now imagine this act of whitewashing, but on a scale that affects millions of people daily-taking culturally important elements and instead replacing them with similar elements from the dominant culture. 

Current speech services offered by Google, Microsoft, and Amazon whitewash the speech of non-dominant groups. One of the many ways that speech interfaces err is by taking speech from different dialects and whitewashing it to Standard American English1. This whitewashing is essentially an algorithmic microagression, a user could request the song "You Da Baddest" from Cortana or Google Assistant and see the system, in real time, take their speech and attempt to change it into a more Standard American English "You're the Baddest". It's almost as if there is someone standing there and reprimanding them while they are speaking. This whitewashing can lead to errors in retrieving content created by these same cultures. The systems add insult to injury, not only did the user see their speech turned into something they never said, the intended content now cannot even be retrieved because of this transformation.

This is a form of algorithmic bias; algorithmic bias has been characterized and tied to different decisions made by teams when creating the algorithm. The way that speech recognition normally works is to attempt to turn each sound bite someone says into its corresponding text word. However, since it is very easy to miss a single word along the way, speech recognition systems take all these possible words and then look to see if it is a reasonable sentence. For example, the algorithm could make a simple error and accidentally transcribe the word 'ate' as 'hate' in the sentence 'I hate a fish yesterday'. To us, it is immediately apparent that this sentence contains an error. However, for a speech recognition system to determine this, it looks at millions of examples it has seen of sentences and phrases and quickly determines that:
1.  'I hate a fish yesterday' occurs very rarely
2.  'I ate a fish yesterday' occurs very often
3.  The audio of these two sentences are very close to each other and 'I ate a fish yesterday' is likely what was actually said.

This same phenomenon leads to algorithmic whitewashing. Other songs like 'hunnid on the drop' are whitewashed to 'hunted on the drop'. It is very likely that this occurs because the language model of the ASR being used has not been fed many examples of this non-dominant form of speech. Therefore, rather than recognizing it as a legitimate way of speaking, it attempts to find the closest parallel in Standard American English. These Standard American English parallels must occur so overwhelmingly often in the language model that even when the sentence is quite phonetically different, the algorithm still chooses to transcribe the Standard American English parallel. This bias has widespread consequences. 

Algorithmic whitewashing is cultural suppression. Language is one of the most powerful parts of culture and taking these cultural patterns of speech and replacing them with the dominant patterns of speech further suppresses already threatened cultural identities. Rather than assaulting these cultural markers, applications should be empowering these groups to speak their natural language. After all, often the cases where this whitewashing is most apparent are when users ask for culturally significant media from their own culture. We glorify these artists; we should empower the cultures that created them.


References
1. Aaron Springer and Henriette Cramer. 2018. "Play PRBLMS": Identifying and Correcting Less Accessible Content in Voice Interfaces. CHI 2018.


