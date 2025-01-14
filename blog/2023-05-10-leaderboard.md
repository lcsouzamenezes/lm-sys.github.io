---
title: "Chatbot Arena Leaderboard Updates (Week 2)"
author: "LMSYS Org"
date: "May 10, 2023"
previewImg: /images/blog/leaderboard_week2/leaderboard_cover.png
---

We release an updated leaderboard with more models and new data we collected last week, after the announcement of the anonymous [Chatbot Arena](https://lmsys.org/blog/2023-05-03-arena/). We are actively iterating on the design of the arena and leaderboard scores.

In this update, we have added 4 new yet strong players into the Arena, including three **proprietary models** and one open-source model. They are:

- OpenAI GPT-4
- OpenAI GPT-3.5-turbo
- Anthropic Claude-v1
- RWKV-4-Raven-14B 

Table 1 displays the Elo ratings of all 13 models, which are based on the 13K voting data and calculations shared in this [notebook](https://colab.research.google.com/drive/1iI_IszGAwSMkdfUrIDI6NfTG7tGDDRxZ?usp=sharing). You can also try the voting [demo](https://arena.lmsys.org) and see more about the [leaderboard](https://leaderboard.lmsys.org).

<style>
th {text-align: left}
td {text-align: left}
</style>

<br>
<p style="color:gray; text-align: center;">Table 1. Elo ratings of LLMs (Timeframe: April 24 - May 8, 2023)</p>
<table style="display: flex; justify-content: center;" align="left" >
<tbody>
<tr> <th>Rank</th> <th>Model</th> <th>Elo Rating</th> <th>Description</th> <th>License</th> </tr>

<tr> <td>1</td> <td>🥇 <a href="https://chat.openai.com/" target="_blank">GPT-4</a></td> <td>1274</td> <td>ChatGPT-4 by OpenAI</td> <td>Proprietary</td> </tr>

<tr> <td>2</td> <td>🥈 <a href="https://www.anthropic.com/index/introducing-claude" target="_blank">Claude-v1</a></td> <td>1224</td> <td>Claude by Anthropic</td> <td>Proprietary</td> </tr>

<tr> <td>3</td> <td>🥉 <a href="https://chat.openai.com/" target="_blank">GPT-3.5-turbo</a></td> <td>1155</td> <td>ChatGPT-3.5 by OpenAI</td>  <td>Proprietary</td> </tr>

<tr> <td>4</td> <td><a href="https://lmsys.org/blog/2023-03-30-vicuna/" target="_blank">Vicuna-13B</a></td> <td>1083</td> <td>a chat assistant fine-tuned from LLaMA on user-shared conversations by LMSYS</td> <td>Weights available; Non-commercial</td> </tr>

<tr> <td>5</td> <td><a href="https://bair.berkeley.edu/blog/2023/04/03/koala" target="_blank">Koala-13B</a></td> <td>1022</td> <td>a dialogue model for academic research by BAIR</td> <td>Weights available; Non-commercial</td> </tr>

<tr> <td>6</td> <td><a href="https://huggingface.co/BlinkDL/rwkv-4-raven" target="_blank">RWKV-4-Raven-14B</a></td> <td>989</td> <td>an RNN with transformer-level LLM performance</td> <td>Apache 2.0</td> </tr>

<tr> <td>7</td> <td><a href="https://open-assistant.io" target="_blank">Oasst-Pythia-12B</a></td> <td>928</td> <td>an Open Assistant for everyone by LAION</td> <td>Apache 2.0</td> </tr>

<tr> <td>8</td> <td><a href="https://chatglm.cn/blog" target="_blank">ChatGLM-6B</a></td> <td>918</td> <td>an open bilingual dialogue language model by Tsinghua University</td> <td>Weights available; Non-commercial</td> </tr>

<tr> <td>9</td> <td><a href="https://github.com/stability-AI/stableLM" target="_blank">StableLM-Tuned-Alpha-7B</a></td> <td>906</td> <td>Stability AI language models</td>  <td>CC-BY-NC-SA-4.0</td> </tr>

<tr> <td>10</td> <td><a href="https://crfm.stanford.edu/2023/03/13/alpaca.html" target="_blank">Alpaca-13B</a></td> <td>904</td> <td>a model fine-tuned from LLaMA on instruction-following demonstrations by Stanford</td>  <td>Weights available; Non-commercial</td> </tr>

<tr> <td>11</td> <td><a href="https://huggingface.co/lmsys/fastchat-t5-3b-v1.0" target="_blank">FastChat-T5-3B</a></td> <td>902</td> <td>a chat assistant fine-tuned from FLAN-T5 by LMSYS</td> <td>Apache 2.0</td> </tr>

<tr> <td>12</td> <td><a href="https://www.databricks.com/blog/2023/04/12/dolly-first-open-commercially-viable-instruction-tuned-llm" target="_blank">Dolly-V2-12B</a></td> <td>863</td> <td>an instruction-tuned open large language model by Databricks</td> <td>MIT</td> </tr>

<tr> <td>13</td> <td><a href="https://arxiv.org/abs/2302.13971" target="_blank">LLaMA-13B</a></td> <td>826</td> <td>open and efficient foundation language models by Meta</td> <td>Weights available; Non-commercial</td> </tr>

</tbody>
</table>

&shy;

If you want to see more models, please help us [add them](https://github.com/lm-sys/FastChat/blob/main/docs/arena.md#how-to-add-a-new-model) or [contact us](mailto:lmsysorg@gmail.com) by giving us API access.

## Overview
Thanks to the community's help, we have gathered 13k anonymous votes. Looking at the rankings and data collected from this leaderboard update, we have a few interesting findings.

**Gaps between proprietary and open-source models**  
We do observe a substantial gap between the three proprietary models and all other open-source models. 
In particular, GPT-4 is leading the board, achieving an Elo score of 1274. It is almost 200 scores higher than the best open-source alternative on this board -- our Vicuna-13B.
After dropping ties, GPT-4 wins 82% of the matches when it is against Vicuna-13B, and it even wins 79% of the matches when it is against its previous generation GPT-3.5-turbo.

However, it is important to note that these open-source models on the leaderboard generally have fewer parameters, in the range of 3B - 14B, than proprietary models.
In fact, recent advancements in LLMs and data curation have allowed for significant improvements in performance with smaller models. 
[Google's latest PaLM 2](https://ai.google/discover/palm2) is a great example of this: knowing that PaLM 2 achieves even better performance than its previous generation using smaller model sizes, 
we remain very optimistic about the potential for open-source language models to catch up. Through our [FastChat-based Chatbot Arena](https://github.com/lm-sys/FastChat) and this leaderboard effort, 
we hope to contribute a trusted evaluation platform for evaluating LLMs, and help advance this field and create better language models for everyone.
 

**Comparing proprietary models**  
However, among the three proprietary models, we do observe, based on our collected voting results, 
that Anthropic's Claude model is preferred by our users over GPT-3.5-turbo, which is often discussed as its opponent.
In fact, Claude is highly competitive even when competing against the most powerful model -- OpenAI's GPT-4. 
Looking at the win rate plots (Figure 3 below), among the 66 non-tied matches between GPT-4 and Claude, Claude indeed wins over GPT-4 in 32 (48%) matches. Great job Anthropic team!

**Comparing open-source chatbots**  
In this update, we have added RWKV-4-Raven-14B model into the Arena thanks to the community [contribution](https://github.com/lm-sys/FastChat/issues/633). Unlike all other models, RWKV model is an RNN instead of a transformer-based model; but it performs surprisingly well!
It soon uptrends on the leaderboard and is positioned #6 on the overall leaderboard. It wins more than 50% of non-tied matches against all other open-source models except Vicuna. You are welcome to check out its [repo](https://github.com/BlinkDL/RWKV-LM) to learn more about other features like memory saving and fast inference.
Kudos to the RWKV developers.

**Fluctuations of Elo scores**  
The Elo scores of existing models can go up and down depending on the results of the new games played. This is similar to the way the Elo scores of chess players vary over time (see [here](https://en.chessbase.com/post/historical-chess-ratings-dynamically-presented)).
Since the participation of the three strong proprietary models, the Chatbot Arena has never been more competitive than ever before!
As a consequence, we observe the Elo scores of all open source models have decreased a bit. This is because open source models lose lots of pairwise matches when they are against the proprietary models.

## Detailed Results

**When does GPT-4 fail?**  
We present a few examples in which GPT-4 is not preferred by users.

<img src="/images/blog/leaderboard_week2/claude_vs_gpt4.png" style="display:block; margin-top: auto; margin-left: auto; margin-right: auto; margin-bottom: auto;"></img>
<p style="color:gray; text-align: center;">Figure 1: One example where Claude is preferred over GPT-4.</p>

In Figure 1, the user posed a tricky question that demanded careful reasoning and planning. Although both Claude and GPT-4 provided similar answers, Claude's response was marginally better as the needle was positioned on top. 
However, we observed that the outcome of this example cannot always be replicated due to the randomness of sampling.
Sometimes GPT-4 can also give the same order as Claude, but it fails at this generation trial.
Additionally, we noted that the behavior of GPT-4 differed slightly when using the OpenAI API versus the ChatGPT interface, which could be attributed to different prompts, sampling parameters, or other unknown factors.

<img src="/images/blog/leaderboard_week2/claude_vs_gpt4_fail.png" style="display:block; margin-top: auto; margin-left: auto; margin-right: auto; margin-bottom: auto;"></img>
<p style="color:gray; text-align: center;">Figure 2: One example where a user thinks both Claude and GPT-4 are wrong.</p>

In Figure 2, both Claude and GPT-4 are still struggling with this kind of tricky reasoning questions despite their amazing capabilities.

Besides these tricky cases, there are also a lot of easy questions that do not require complex reasoning or knowledge. In this case, open source models like Vicuna can perform on par with GPT-4, so we might be able to use a slightly weaker (but smaller or cheaper) LLM in place of the more powerful one like GPT-4.

**Win Fraction Matrix**  
We present the win fraction of all model pairs in Figure 3.
<img src="/images/blog/leaderboard_week2/win_fraction_matrix.png" style="display:block; margin-top: auto; margin-left: auto; margin-right: auto; margin-bottom: auto;"></img>
<p style="color:gray; text-align: center;">Figure 3: Fraction of Model A Wins for All Non-tied A vs. B Battles.</p>

**Language-specific leaderboards**  
Lastly, we present two language-specific leaderboards, by isolating the conversation data into two subsets based on the language: (1) English-only and (2) non-English. From Figure 4, we can tell that Koala is worse at non-English languages and ChatGLM-6B is better at non-English languages. This is because of the different compositions of their training data.

<img src="/images/blog/leaderboard_week2/english_vs_non_english.png" style="display:block; margin-top: auto; margin-left: auto; margin-right: auto; margin-bottom: auto;"></img>
<p style="color:gray; text-align: center;">Figure 4: The English-only and non-English leaderboards.</p>

More figures, analyses, and calculations can be found in this [notebook](https://colab.research.google.com/drive/1iI_IszGAwSMkdfUrIDI6NfTG7tGDDRxZ?usp=sharing).

## Next Steps

**Help us add more models**  
Since the launch of Chatbot Arena, we have seen growing interest from the community. Many model developers are eager to put their chatbots into the Arena and see how they perform against others.
Please help us add more models by following [this guide](https://github.com/lm-sys/FastChat/blob/main/docs/arena.md#how-to-add-a-new-model). 

**Bring your own self-hosted chatbot (BYOC)**  
We also plan to open some APIs to allow competitors to register their self-hosted chatbots and participate in the Arena.

**Area-specific Arena**  
Similar to the language-specific Arena, we will extend a single, monolithic leaderboard to more areas, and publish more functionality-specific leaderboards, 
such as writing, coding, and reasoning. In which specific area or ability do you want to see the LLMs evaluated?
Please give us feedback on [Discord](https://discord.gg/h6kCZb72G7) or [Twitter](https://twitter.com/lmsysorg).

## Acknowledgement
This blog post is primarily contributed by Lianmin Zheng, Ying Sheng, Hao Zhang, Joseph E. Gonzalez, and Ion Stoica.
We thank other members of LMSYS team (Wei-Lin Chiang, Siyuan Zhuang, and more) for valuable feedback and MBZUAI for donating compute resources.
Additionally, we extend our thanks to community contributors for their votes and model support.
