---
layout: post
title: "Understanding DeepFakes"
date: 2021-04-28
modified: 2021-04-28
tags: [deepfakes, media-forensics, artifical-intelligence]
categories: jekyll update
image1: ../assets/img/understanding-deepfakes/FakeHumans.png
image2: ../assets/img/understanding-deepfakes/VAE.png
---

> **Disclaimer**: The following article was featured in the 4th Edition of 
> [Turning Magazine](https://www.turningmagazine.com/). You can subscribe 
> [here](https://www.turningmagazine.com/subscribe/) to get a personal copy of the 4th edition.

In 2019, over 14,000 videos on the internet were identified as **DeepFakes** and in December 2020, this number 
skyrocketed to nearly 85,000. Starting out as a niche technology and used by only AI researchers and tech hobbyists, 
Deepfakes have slowly gained viral popularity in the internet community. With new techniques outperforming the ones that 
came before, it’s clear that this mysterious technology is here to stay. Now, whether it’s for the good of humanity or 
otherwise, that’s still up for debate. Some say that ignorance is bliss, but not when it comes to dealing with Deepfakes. 
To realize the future of Deepfakes, we should learn how this technology came into existence. With the power to question 
our own eyes and ears, it is imperative that we understand the potential of this technology - the good and the bad.


<figure>
<img src="{{ page.image1 }}" alt="Fake Humans with StyleGANv2">
<figcaption>Generated via https://thispersondoesnotexist.com</figcaption>
</figure>


Deepfakes are widely recognized as a form of synthetic media created via Deep Learning. Deep Learning models are broadly 
split into two categories: **Discriminative** and **Generative**. While discriminative models learn the distinguishing 
features of different classes of data, generative models learn the underlying (latent) distribution of data. 
Cracking the code of this latent information in data is what gave birth to Deepfakes. Although the group of generative 
models is not small, the credit for creating Deepfakes goes to **Variational AutoEncoders (VAEs)** and **Generative 
Adversarial Networks (GANs)**. VAEs use an Encoder network to learn the latent distribution of the data it receives, 
and a Decoder network to generate the best approximation of the original data based on the learned latent distribution. 
This approximation improves over multiple training cycles. GANs, on the other hand, are VAEs on steroids. They use an 
additional discriminative neural network called the Discriminator which guides the Generator (VAE) network. This results
in a far superior approximation of the latent distribution and, in turn, yields better generation results. Given the 
success of GANs, models like StyleGAN are capable of generating high quality face portraits of non-existent (fake) 
humans.

<figure>
<img src="{{ page.image2 }}" alt="VAE: Under the Hood">
<figcaption>VAE: Under the Hood</figcaption>
</figure>

In the context of synthetic media found on the internet, Rossler et al. (2019) [[1]](./#reference) classify Deepfakes into two 
categories: **Facial Identity Manipulation** and **Facial Expression Manipulation**. Facial identity manipulation, also 
called _Face Swapping_, transfers the face of a “source” person to a “target” person while maintaining the facial 
movements of the original target face. Created as an open-source project in 2017, it quickly went viral on Reddit and 
laid the foundation of the exponential rise in the number of Deepfakes over the internet; a majority of which use the 
face swapping technology. On the other hand, facial expression manipulation, also called _Facial Reenactment_, retains 
the face of the “target” person but transfers the facial movements of the “source” person.

In 2020, a mobile app named “Reface App” emerged and commodified face swapping by allowing anyone to create a DeepFake 
with a few clicks. In the open-source community, a GitHub project named “DeepFaceLab” provides face swapping in the form 
of software which requires a GPU to create DeepFake videos. Numerous content creators on famous social media platforms 
like YouTube and TikTok are already using these services to create Deepfakes in a meme format. Such Deepfakes are fun to 
watch and really bring out the creativity of the creator. If only we lived in an ideal world. 

In 2018, Sensity, an Amsterdam-based visual threat intelligence company, identified that nearly 96% of Deepfakes 
identified on the internet are pornographic in nature. At the time, the individuals targeted by such Deepfakes were 
celebrities and public figures. This trend did not only rise over time but also took a morbid turn. In 2020, Sensity 
discovered a Telegram bot which synthetically “strips'' a person in the photograph one would send to the bot, affecting 
over 100,000 women.

As face swapping has not reached its peak performance, it is still fairly easy to identify such Deepfakes when one pays 
attention to other visual cues such as the person’s voice and context of such a video. This comes into question with 
facial reenactment techniques. Deepfakes are created to make it appear that the individual targeted is either doing or
saying something, which in reality is untrue. Similar to face swaps, such Deepfakes found on social media platforms are 
intended to be funny. Nevertheless, those with malicious intent are more than capable of using such technology to defame
anyone. Multiple cases have been reported where Deepfakes are used to destabilize governments in developing countries.

The threat of Deepfakes is very real and authorities are already working on creating laws which can protect citizens 
against such defamatory attacks. Nonetheless, this should not undermine all the good Deepfakes can do in society. We can 
use Deepfakes to create multilingual videos with accurate lip-syncing, hyper-realistic virtual avatars for AI-based 
human assistance, and even accelerate creativity of the film industry by using Deepfakes instead of traditional CGI 
techniques.

In the end, the potential use of Deepfakes lies in the hands of its user and their intent. Deepfakes can either bring 
about dystopia, fuelling the era of misinformation and fake news, or bring about utopia, creating a paradigm shift in 
how artificial intelligence can benefit the world.

> **Epilogue**: This article is Part 2 of the blog mini-series, “Seeing was Believing”. You can read 
> [Part 1: Introduction to Media Forensics](https://www.turningmagazine.com/blog/2021/01/13/seeing-was-believing-part-1/) 
> on the Turning blog website. If you want to learn more about Deepfakes, you can visit https://sensity.ai/reports/.

#### Reference

[1] Rossler, A., Cozzolino, D., Verdoliva, L., Riess, C., Thies, J., & Nießner, M. (2019). Faceforensics++: Learning to 
detect manipulated facial images. _In Proceedings of the IEEE/CVF International Conference on Computer Vision_ 
(pp. 1-11).
