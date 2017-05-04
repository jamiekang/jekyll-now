---
layout: post
title: Jekyll로 GitHub에 blog 만들기
use_math: true
date: 2017-04-28 03:22:31
categories: 
- Keep Learning
tags: 
- Jekyll
- GitHub
- Blog
---

GitHub로 블로그를 옮기면서 WordPress, 티스토리 등의 블로그 플랫폼과 다른 환경에 새로 알아야할 것이 많았습니다. 기억을 위해 간단히 정리해 봅니다.


> ![Algorithm1]({{ site.baseurl }}/media/2017-04-29-generative-adversarial-nets-algorithm1.png)

요약하면, stochastic gradient descent (SGD) 계열의 알고리즘을 적용해 minibatch 단위로 Discriminator $D(x)$와 Generator $G(z)$를 번갈아 가며 training 시킵니다. 일반적으로 $D(x)$가 $G(z)$보다 빨리 성장하는 경향이 있습니다. 그런 경우, $G(z)$가 아직 미숙한데 $D(x)$가 너무 결과를 잘 판별해 버리면 $G(z)$가 쉽게 죽어버립니다. 두 모델이 균형 있게 성장하도록 많은 튜닝이 필요합니다. 

현재까지 알려진 GAN의 장단점은 아래와 같습니다.
- 장점
	- 결과물의 quality가 좋다: VAE등 기존 연구 대비 선명
	- 출력이 빨리 나온다: PixelRNN등 픽셀 단위 출력 대비
- 단점
	- training이 unstable하다.
	- 정량적 quality 측정 기준 미비: 사람의 주관적 판단에 의존
	- oscillation: 오래 training해도 더 이상 수렴 못하는 현상
	- mode collapsing 문제: 비슷비슷한 결과물이 나오는 현상

최근 GAN의 인기는 앞서 언급한 Arjovsky의 [WGAN](https://arxiv.org/pdf/1701.07875v1.pdf), Radford의 [DCGAN](https://arxiv.org/abs/1511.06434), Chen의 [InfoGAN](https://arxiv.org/abs/1606.03657) 등 다양한 후속 연구에 힘입은 바가 큽니다. 이에 대해서는 다른 포스팅에서 더 다뤄보도록 하겠습니다.


**References**
- Stack Overflow의 [Jekyll tagged questions](https://stackoverflow.com/questions/tagged/jekyll)
- GitHub Help의 [Adding a Jekyll theme to your GitHub Pages site](https://help.github.com/articles/adding-a-jekyll-theme-to-your-github-pages-site/)
- Adam Pritchard의 [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

