---
title: "You : Only You can (auto-)complete you"
date: 2021-01-07T17:14:49-08:00
draft: false
tags: ['ai', 'side-projects', 'app', 'nlp']
---

GitHub Repo : [https://github.com/nuwandavek/you](https://github.com/nuwandavek/you)

*You* is an auto-completion tool that completes your sentences. It lets you train a generative model that can mimic your personal style over all your text communication. Currently, You trains on WhatsApp chat history, and offers autocomplete suggestions on WhatsApp Web via a Chrome/Firefox extension and a flask server. This can be extended to train and autocomplete on more personal communication apps (Messenger, email, Slack, Twitter, etc.). Everything runs locally and is completely private.

## Why?
Most text-based applications we use have some or the other form of aid to help us spell-check words, complete words or even complete sentences. Most primitive ones are based on simply looking up your words against a corpus, determining the most probable word and helping you complete them (spell-checks, Word docs). Intermediate tools use your own data to predict the most frequent bi-gram pairs (mobile keyboards), and advanced tools use neural networks (GMail, Google Docs). Predicting the next word (or token), however, is the most popular way of training a language model model using neural networks. The last couple of years has seen remarkable innovation in the field of NLP using neural networks from Bi-LSTMs to BERT to GPT3. We think the algorithms are already in place for tools to leverage their power and offer delightful personalized predictions - complete all your sentences. :)

We are also excited about the prospect of a language model that is tailor-made for you, across all platforms. A single model that understands how you speak to strangers over mail, colleagues over Slack, and friends over chat. We want people to be able to control and experiment with their experience and run everything locally, as much as possible - since these are after all, your personal messages only read by a handful of corporations and government agencies.

## Demo

![Chat With Rishi](https://raw.githubusercontent.com/nuwandavek/you/master/demo.gif)

## How do I run this?

Currently You works on web Whatsapp, and running You involves 3 steps 
- Training (fine-tuning) a pre-trained DistilGPT2 model on your own chats on Google Colab (or locally if you have a GPU)
- Running a flask server with the model downloaded from the above step
- Installing a Chrome/Firefox extension that talks to your server and injects the prompts to your browser

For more detailed steps, checkout the  `README` file on the [github repository](https://github.com/nuwandavek/you).

## Next Steps

We have a bunch of ToDos on the `README`. Mostly we will be experimenting with new models or with better training strategies to improve the prompts. We'll  also be working on supporting more chat and other communication applications.

This was a weekend project by [nuwandavek](https://twitter.com/nuwandavek) and [rishicomplex](https://twitter.com/rishicomplex). Do check it out, and let us know how it goes! 