---
layout: post
title: My summer research project at the University of Birmingham
date: 2023-11-07 16:11:00-0400
inline: false
related_posts: false
---

# News

* I made a presentation on this project on Oct. 31, 2023, at the School of Mathematics of the University of Birmingham.

<hr>

> <p>Today’s Nobel Peace Prize, awarded to Narges Mohammadi, is an important reminder that the rights of women and girls are facing a strong pushback, including through the persecution of women human rights defenders, in Iran and elsewhere.</p>
> <p>This Nobel Peace Prize is a tribute to all those women who are fighting for their rights at the risk of their freedom, their health and even their lives.</p>
> <p>António Guterres, Secretary-General of the United Nations, on 6 October 2023<br>
> Source: <a href="https://www.un.org/sg/en/content/sg/statement/2023-10-06/secretary-generals-statement-the-2023-nobel-peace-prize">Secretary-General's statement on the 2023 Nobel Peace Prize</a></p>

# Overview

This project was conducted under the supervision of [Professor Rowland Seymour](https://www.rowlandseymour.com/) of the School of Mathematics of the University of Birmingham, and supported by the 2023 Summer Undergraduate Research Bursary of the School. We focused in particular on comparative judgment sparse data about human rights, primarily on the risk of violence against women and girls. 

# Details

Comparative judgment, which involves getting a set of judges to compare a set of players, is a useful and intuitive technique for data that has long been proposed but used only within a limited range. As other forms of survey data, data used for comparative judgment are frequently placed subject to the questioning of reliability. This project focused on the Bradley-Terry model for assessing binary judgments. 

$$
\text{Logit}\left(\pi_{ij}\right) = \lambda_i-\lambda_j
$$

$$
Y_{ij} \sim \text{Binomial}\left(n_{ij},\pi_{ij}\right)
$$

As the main theme of it indicates, this project sought to summarize and explore the relationship between different approaches to assess the reliability of data, especially, scale separation reliability (SSR) and split halves.  

$$
\text{SSR} = \frac{G^2}{1+G^2}, \text{ where } G=\frac{\sigma_{\lambda}}{\text{RMSE}}
$$

We found that, SSR is associated to the Pearson correlation coefficient from split halves within one round when the internal consistency of the two subsets is high. Also, by lowering the hierarchy of the split halves and excluding players with large variances, traditional data reliability methods could still be applied to sparse data. 

We also proposed new methods of the assessment, one of which can be integrated into the model fitting process and improve modelling accuracy while the other one is excessively computationally inexpensive. The first one involved clustering according to the variance of the judges (interpreted as representation of quality) and imposing weights thereafter in the modelling, under the assumption of normal distributions — the nature of logistic regressions by the central limit theorem. The second one directly compare the decisions by the judges in matrices, avoiding the computationally expensive model fitting tasks. 

We focused the empirical analysis on the application to sparse data addressing issues related human rights such as forced marriage and deprivation, and concluded the high level of reliability of these data. We sincerely hope that our research can pave the way for future use of comparative judgment in wider range, especially in tackling human rights abuses, including female genital mutilation, human trafficking, online child sexual exploitation and abuse, deprivation and forced marriage. 

# Examples of Human Rights Abuses

* **Female genital mutilation**: Female genital mutilation involves removal or other injuries to the female genital organs for nonmedical reasons. See [World Health Organization (WHO) page](https://www.who.int/news-room/fact-sheets/detail/female-genital-mutilation).
* **Forced marriage**: Forced marriage is a form of modern slavery that was estimated to affect 22 million people, or nearly one of every 150 people in the world. See [the International Labour Organization (ILO), Walk Free, and the International Organization for Migration (IOM) page]( https://www.walkfree.org/reports/global-estimates-of-modern-slavery-2022).
* **Human trafficking**: Human trafficking is a crime that involves compelling or coercing a person to provide labor or services, or to engage in commercial sex acts. See [U.S. Department of Justice page](https://www.justice.gov/humantrafficking/what-is-human-trafficking).
* **Online child sexual exploitation and abuse**: Online child sexual exploitation and abuse involve using information and communication technology as a means to use the child as an object for sexual needs. See [U.N. Economic and Social Commission for Asia and the Pacific report](https://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=E2DC58C89012864145C37E78191B4BA2?doi=10.1.1.510.3821&rep=rep1&type=pdf). 

# Related Links

* [The Bradley-Terry model. ](https://doi.org/10.1093/biomet/39.3-4.324)
* [The BradleyTerry2 package in R. ](https://github.com/hturner/BradleyTerry2)
* [The Bayesian Spatial Bradley-Terry model. ](https://doi.org/10.1111/rssc.12532)
* [The BSBT package in R. ](https://github.com/rowlandseymour/BSBT)
