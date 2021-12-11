---
title: mothur and QIIME
date: '2016-02-09'
slug: 2016-02-09-mothur-and-qiime
tags:
- 生物信息 BIOINFORMATICS
- 生物软件 BIO-SOFTWARE
- ecology
- mothur
- NGS
- QIIME
---


说明：mothur的官博上比较了mothur和QIIME这两个微生物生态学研究的常用软件之间存在的差异。博主略作整理，以飨读者。  
原文链接在这里：http://blog.mothur.org/2016/01/12/mothur-and-qiime

以下为原文和大意的翻译。

<div>

译者：这是mothur博客上一篇关于QIIME的文章，作者系统比较了两个工具的不同。

</div>

<div>

</div>

<div>

Despite their differences in philosophy,<span
class="Apple-converted-space"> </span>*most*<span
class="Apple-converted-space"> </span>of the differences in mothur and
QIIME are cosmetic. Both packages have been successful. Having both of
them around is good for microbial ecology. Within both packages there
are warts – inconveniences to the users and antiquated/bad ideas. Within
both packages there are strengths. If you are going to criticize someone
for their choice of software, do it for some specific point. If you are
going to campaign for mothur or QIIME, do your best to accurately
represent the strengths of your pet package.

</div>

<div>

按：尽管设计哲学不同，mothur和QIIME的大部分差异都是表现形式的不同而已。两个工具都已经非常成功。同时拥有它们是微生物生态研究之幸事。二者共存有利也有弊。如果你要苛责用户的选择，最好有针对性的指出。如果你要做一个超越二者的工具，最好准确的呈现你的专长。

</div>

<div>

</div>

When I teach workshops or field users’ questions, I am often asked what
I think of QIIME. I suspect that because I direct the development of
mothur, people are expecting me to come out with guns blazing to blow up
QIIME. In fact, people ask and then kind of step aside to avoid the
onslaught. Meh. I pause and say it’s a successful program, but that I
obviously like mothur better. After this non-answer, people then tell me
the analogies that they use to compare the two: Patagonia vs Columbia,
Mac vs. PC, or Coke vs. Pepsi are common (it’s never clear or consistent
which brand is to be preferred or why). I suppose this is fair with the
caveat that all analogies are limited. I think these analogies reflect
the point that a lot of the differences are cosmetic. Both programs were
released within months of each other in 2009 and 2010. I often get the
impression from reviewers and other software developers that mothur is a
distant second fiddle to QIIME. Yet, the Web of Science shows that
mothur has 3,410 citations and QIIME has 2,779 (as of January 8, 2016).
Although I cite these numbers in grant proposals to sway reviewers that
mothur is the leading tool used by microbial ecologists to analyze 16S
rRNA genes, citation counts really say little about quality and once you
get over a few hundred citations you’re hot stuff.

大意：人们常问我QIIME怎么样，我会说“那东西也不错”。人们就说它们就像Mac
和 PC、百事 和 可口可乐
一样。二者分别在2009和2010年发布，mothur常常被认为是小跟班。与我来讲，mothur才是主流——因为SCI数据库中引用较多，尽管引用可能并不能说明什么具体问题。

I have gotten this question with growing frequency over the past months
(hence this blog post) and I know that the topic recently came up over
at the<span class="Apple-converted-space"> </span>[QIIME
forum](https://groups.google.com/forum/m/#!topic/qiime-forum/vDuBwVF7rOg).
Often times the person asking the question or making the dogmatic
statement doesn’t seem to have a full appreciation for the differences
and similarities and whether the differences are really meaningful. I
frequently work with researchers to craft rebuttals to reviewers who
think that an otherwise benign paper is the battle ground for such a
debate. Take this gem, for example…

> Finally, I like mothur for some of its unique features but QIIME is
> better for others and is backed up by a very strong group of
> bioinformatics tools and researchers, in my opinion you should
> consider using QIIME in future studies.

<div>

</div>

<div>

</div>

<div>

大意：不要再问我QIIME怎么样了。我就是喜欢mothur，它有一些我钟情的因素。QIIME可能更适合你。

</div>

<div>

</div>

It’s really hard to know where to begin with that kind of statement. I
hope that this would even make the QIIME developers cringe. It would
make me cringe if the software names were switched. Sadly, this isn’t
the only example of this that I have seen. Such comments beg the
question, “Which mothur features were used in this paper that would have
been better in QIIME?” There may be some, but what is the author to do
with such a vague comment from the reviewer? How do these types of
statements help anyone? But I digress… My point is that to this reviewer
and many others the differences that they think are huge are largely
cosmetic. For example, I received feedback a year ago that someone
didn’t like using the mothur wiki site because it had a very modest
picture of my wife nursing our 4th child, John and that grossed them
out. For. Reals. Many people are QIIME or mothur people because their PI
or collaborators are, not for any deep seated philosophical
justification.

So, what are the differences? Are they meaningful or just cosmetic? Is
this all a matter of personal preference? In full disclosure, my
experience with QIIME came from a<span class="Apple-converted-space">
</span>[recent paper I wrote](https://peerj.com/articles/1487/)<span
class="Apple-converted-space"> </span>in which we compared various
clustering algorithms including those implemented in QIIME. I’ve looked
over their SOPs, talked with a number of QIIME users, and feel that I
generally have a good sense of what their strategy is about. I’m not
looking to get into a mothur vs. QIIME debate (note: the title of this
post is mothur<span class="Apple-converted-space"> </span>and<span
class="Apple-converted-space"> </span>QIIME), but if I misrepresent
something or am being unfair, please let me know and I’ll edit this
post. In what follows allow me to lay out what I see as the
similarities, differences, strengths, and weaknesses of each program. To
reduce my bias, I’ll leave it to you to determine whether any of it
matters. I’m happy to extend the list if you think I’m missing something
critical. My hope is that people getting started in the field and that
the person that forwarded that reviewer comment to me (and others with
similar reiviewers) will find the discussion useful.

Here’s a list of the topics I’ll cover that are linked so you can jump
down the list. I summarize everything at the very end with some<span
class="Apple-converted-space"> </span>concluding thoughts…

大意：好吧，我们还是来好好谈谈这个问题吧。

<div>

<div>

-   Development strategy
-   Language
-   Installation
-   Accessibility
-   Openness
-   User community
-   Method transparency

</div>

<div>

-   Reproducibility
-   Data Accessibility
-   Data visualization
-   Clustering / OTU picking
-   Illumina sequence processing
-   Classification
-   Databases

</div>

<div>

### Development strategy 开发策略

*mothur.*<span class="Apple-converted-space"> </span>When you run a
function from within mothur, you are running mothur code. When you<span
class="Apple-converted-space"> </span>[run
classify.seqs](http://www.mothur.org/wiki/classify.seqs), you are not
running the code developed by the RDP. You are running our
reimplementation of their code. We have done this with several functions
to make them operating system (OS)-independent, make them open source,
parallelize them, make them faster, generalize their application, and
expand their features. Our first draft of any function is to translate
the code from its original language to C++ and make sure we get the same
output with the same input. In some cases (e.g.<span
class="Apple-converted-space">
</span>[chimera.uchime](http://www.mothur.org/chimera.uchime)<span
class="Apple-converted-space"> </span>and<span
class="Apple-converted-space">
</span>[metastats](http://www.mothur.org/metastats)) the original
authors have made their C code open and we have directly integrated that
code into mothur. In most cases, however, you are running code that we
developed from scratch (e.g.<span class="Apple-converted-space">
</span>[chimera.uchime](http://www.mothur.org/cluster)). This strategy
has strengths (we think the code is better, more uniform, and easier to
maintain), but also has weaknesses (it can be hard to incorporate new
tools if they weren’t written in C/C++). Regardless, we seem to do a
good job of keeping current with the needs and wants of the community.

大意：mothur是从头开发。每一个mothur函数都是基于可移植的C/C++代码。这使得我们的程序可以在各个平台运行、在各种条件下快速、准确的得到一致的结果。

*QIIME.*<span class="Apple-converted-space"> </span>QIIME is essentially
a big wrapper that helps users to transition data between independent
packages. Certainly, a lot of the functionality within QIIME is written
by the QIIME developers, but much of the heavy lifting (e.g. OTU
clustering, classification) is from code written by others. In fact, you
can actually run mothur from within QIIME. It’s a very old version of
mothur, but you can use mothur to cluster sequences in QIIME. As you
might expect, the advantage of this approach is that if the developers
can write a light wrapper for a new package in Python, then it is pretty
painless to bring in other people’s software. Of course, that software
comes in warts and all and creates<span class="Apple-converted-space">
</span>[dependency hell](https://en.wikipedia.org/wiki/Dependency_hell).
When I’ve heard QIIME developers talk at conferences, one comment they
make is that they allow people to use methods the way it was originally
implemented. I get that. At the same time, if you told people that you
had to use Gosset’s original implementation of<span
class="Apple-converted-space"> </span>[Student’s
T-test](https://en.wikipedia.org/wiki/Student%27s_t-test#History)<span
class="Apple-converted-space"> </span>and it couldn’t be ported to SAS,
SPSS, R, Excel, etc. then you’d rightly be laughed at. I would be
curious to know how much dead wood exists in QIIME – I could foresee
functions that were developed by a contributor that then graduate or
lose interest and there is no one left to maintain or update the code.
The QIIME development team may have a mechanism to deal with this type
of problem, but the fact that they are using mothur v1.25, which was
released in May 2012, suggests that there is some slippage. A big part
of what we do with mothur development is to modify functions to work
with bigger and more diverse datasets and we continue to maintain
everything within mothur.

</div>

</div>

大意：QIIME则是一系列工具的“整合”。它甚至不排斥mothur，当需要mothur执行任务时，会调用mothur来完成相应的工作。QIIME实质上应该是一个“调度”工具。尽管QIIME开发人员写了很多代码，但是大部分的核心代码仍然是衍生自其它相关项目。

<div>

<div>

<div>

### Language 编程语言

*mothur.*<span class="Apple-converted-space"> </span>We write mothur in
C and C++. C and C++ are compiled languages, which means that once the
code is compiled, you don’t need another program to run it. Pretty much
everything you likely have on your computer right now is a compiled
program. There are a few reasons we do this. First, C/C++ runs much
faster than other languages including R, Python, Perl, or Java. I
suppose we could be writing it in Fortran, but I put my last punch card
in my daughter’s bicycle spokes. Most of the source code has been
written by Sarah Westcott and myself. It is an open source package that
others are free to contribute to or build upon for other applications.
It is somewhat disappointing that we haven’t had more contributions, but
then again, how many microbiologists know C or C++? If we had written it
in Python or made it an R package, we would have far more contributors.
But of course, then we’d have performance issues. We might make an R
wrapper … wait for it … mothuR, but it will just be wrapping our C++
code.

*QIIME.*<span class="Apple-converted-space"> </span>QIIME is written in
Python, which is a very powerful, popular, and well-developed language.
I look for reasons not to learn Python (I’m on team R), but deep down
know that I should learn Python. My kids are learning Python. Through
the efforts of<span class="Apple-converted-space"> </span>[Software
Carpentry](http://software-carpentry.org/),<span
class="Apple-converted-space">
</span>[Codecademy](https://www.codecademy.com/), and other groups, many
biologists are learning Python. You should definitely learn Python. For
all of these reasons, I think QIIME has gotten a lot of code
contributions from their user base. Python is also great for doing light
lifting functions like wrapping functionality and converting file
formats. It’s not so great at heavy lifting. Part of this is because it
is not a compiled language – the language itself is written in C. As an
example of this consider our aligners, which both implement the NAST
algorithm. The paper describing QIIME’s Python-based aligner,<span
class="Apple-converted-space">
</span>[pynast](http://www.ncbi.nlm.nih.gov/pubmed/19914921), states
that it can align a full-length sequence in 1.46 seconds. In contrast,
our paper describing mothur’s C++-based aligner,<span
class="Apple-converted-space">
</span>[align.seqs](http://www.ncbi.nlm.nih.gov/pubmed/20011594), could
align 15 full-length sequences per second (21.9-times faster).

大意：mothur主要用C和C++写成，是编译性语言。QIIME用Python写成，是脚本语言。所以，mothur更快。mothur胜。

<div>

### Installation 安装

*mothur.*<span class="Apple-converted-space"> </span>Because of our
overall development strategy we have worked very hard to make mothur a
standalone software package. When you download mothur, you have mothur.
All of it. You don’t have to chase down external dependencies or worry
about software licenses. The only thing you have to go get are the
databases that are required for aligning or classifying sequences. As
described above, this is possible because all of the functionality is
baked into the source code. You can get the executable binaries or the
source code from our<span class="Apple-converted-space">
</span>[project’s GitHub releases
page](https://github.com/mothur/mothur/releases/latest). You can even
download the code that we are working on for the next release through
that GitHub repository.

*QIIME.*<span class="Apple-converted-space"> </span>Installation is one
of the things that seems to drive people nuts about QIIME and to their
credit, I think their developers have worked hard to overcome these
problems. These problems are largely because of their development
strategy. If you have Python installed and are running it on your local
computer, a simple<span class="Apple-converted-space">
</span>`pip install qiime`<span class="Apple-converted-space">
</span>should suffice to install QIIME. But then you have to get all of
the guts (admittedly many of the dependencies can be installed using
an<span class="Apple-converted-space">
</span>[intaller](https://github.com/qiime/qiime-deploy). Some of the
more important guts (e.g. USEARCH) require separate downloads and may be
proprietary and require you to pay a fee. To overcome some of these
problems, the developers have created virtual machines and other
abstractions to make it easier to install. Alas, installing and running
a virtual machine on one’s computer is not trivial and results in a hit
in processing speed. Although some of the individual packages within
QIIME may be closed source and pricey, they make their source code
available through<span class="Apple-converted-space"> </span>[their
GitHub repository](https://github.com/biocore/qiime)<span
class="Apple-converted-space"> </span>like we do.

大意：mothur安装可以一蹴而就。QIIME则需要安装很多依赖，甚至有些依赖是需要你付报酬的。为了解决这个问题，QIIME有虚拟机形式可以使用。mothur胜。

<div>

### Accessibility 可移植性

*mothur.*<span class="Apple-converted-space"> </span>When we survey our
users and run workshops, we consistently find that more than half of
them are using computers that run the Window’s operating system. Guess
which operating systems most bioinformatics software packages are
designed for? Linux and Mac. It has been very important to us to make
mothur as platform-independent as possible. One advantage of rewriting
software is that we can make sure it compiles and works in Windows. For
some reason the same commands run with the same data do run a bit slower
on a Windows machine than a Mac or Linux. Because of this, we think that
people will eventually want to move towards a Linux-based cloud
solution, but we also want to meet people where they are with their
existing hardware without excluding them because of their choice of
operating system.

*QIIME.*<span class="Apple-converted-space"> </span>Considering many of
the tools wrapped within QIIME were designed to run on Linux, QIIME runs
easiest on a machine running Linux. The developers have made a Mac-based
port and as mentioned above, they have created virtual machines to run
on Windows. Difficulties installing and running virtual machines are not
trivial for people just learning bioinformatics and they will experience
hits in performance.

大意：很多人研究人员用Windows，也有人用Linux和Mac，所以我们竭尽所能使mothur可以在Win、Linux和Mac中运行。QIIME则只能在Linux中运行，开发团队提供一种变通的方法在Windows中使用QIIME（虚拟机）。尽管你可能对虚拟机毫无兴趣抑或不想承担虚拟机带来的性能损失，你还是得接受这个现实。mothur胜。

<div>

### Openness 开放性

*mothur.*<span class="Apple-converted-space"> </span>All of the
functionality of mothur is available as source code under the<span
class="Apple-converted-space"> </span>[GPL v3
License](https://github.com/mothur/mothur/blob/master/LICENSE.md). If
you want to know how mothur does something (and can read C/C++), its
right there on our<span class="Apple-converted-space"> </span>[GitHub
repository](https://github.com/mothur/mothur). I suspect that 99% of our
users have no interest in going through the source code, but it’s there.
mothur is<span class="Apple-converted-space"> </span>[free as in freedom
as well as beer](https://en.wikipedia.org/wiki/Gratis_versus_libre). You
don’t have to pay a dime to use any component of mothur if you are a
academic, garage scientist, or work for big pharma. This also goes for
our online materials and technical support.

*QIIME.*<span class="Apple-converted-space"> </span>For most purposes,
QIIME is just as free as mothur and is available under the<span
class="Apple-converted-space"> </span>[GPL v2
License](https://github.com/biocore/qiime/blob/master/COPYING.txt). The
one caveat is their use of USEARCH. Robert Edgar, the developer of
USEARCH provides the 32-bit version for free to academics and
non-profits after registering their use; however, if you’re at a
for-profit or need the 64-bit version, you’re going to have to pay for
it. This is not entirely trivial considering the primary clustering
methods in QIIME are based on USEARCH. I’ve heard that QIIME is working
towards replacing USEARCH with the free VSEARCH, but I believe this is
still in the testing stages.

大意：mothur使用 GPL V3协议发布，QIIME使用 GPL V2
协议发布。同样的自由软件，开放源代码。（译者：从版本号上看，mothur胜。）

<div>

### User community 社区

*mothur.*<span class="Apple-converted-space"> </span>As indicated by the
number of citations, both software packages have large and loyal
followings and some people actually use both on the same project. Both
groups have discussion lists, user forums, online documentation,
instructional materials, swag, and devotees. Engaging those devotees and
potential users to advance the software and surrounding resources is a
challenge for all open source software efforts. For example, take a look
at the list of co-authors on the<span class="Apple-converted-space">
</span>[mothur paper](http://www.ncbi.nlm.nih.gov/pubmed/19801464).
There are 15 names, 3 of us (Westcott, Ryabin, Schloss) wrote code and
most of the wiki (Ryabin was an undergrad). The remaining 12 co-authors
took me up on an offer to get their name on the paper if they
contributed a wiki page describing how they used mothur for their
application. These are the posts on the<span
class="Apple-converted-space"> </span>[Analysis Examples wiki
page](http://mothur.org/wiki/Analysis_examples). Unfortunately, none of
them have been updated since they were posted and having created this
mechanism to share, no one else has contributed their analysis. On a
similar note, I will regularly get emails from people telling me that
there’s a typo on the wiki. Apparently they don’t know that the point of
a wiki is that anyone can edit it! Oh well. We also have a very active
user forum where people mostly ask questions and very few people (mostly
Sarah and I) answer them. Although I’d love for more people to be
involved in this, I think the questions and answers do provide others a
form of very useful documentation. Ultimately, the lack of engagement is
probably more a product of culture that our users aren’t used to. We’re
open to suggestions. Still it’s pretty awesome what we’ve been able to
do over the past several years with 1.0 FTE working on mothur.

*QIIME.*[Greg Caporaso rightly
points](https://groups.google.com/forum/m/#!topic/qiime-forum/vDuBwVF7rOg)<span
class="Apple-converted-space"> </span>out that QIIME has a great
collaborative network of developers. I think a lot of this is because
they develop in Python, which a lot of people know and that the strong
computer science background of Knight, Caporaso, and the other
developers has collaboration baked into it. I also think that because
the Knight lab is heavily involved in a lot of big science projects they
have an amazing list of collaborators that go on to use QIIME, publish
in high-impact papers, and reinforce collaboration with the QIIME
developers. What can I say? I’m jealous.

大意：mothur有社区、有Wiki，这些都是我们几个人在维护。QIIME则财大气粗，人多势众。Knight
（QIIME开发者）毕竟大老板，铁血真英雄。我只能嫉妒他们的这一点。

<div>

### Method transparency 方法透明度

*mothur.*<span class="Apple-converted-space"> </span>There are
currently<span class="Apple-converted-space"> </span>[145 commands in
mothur](http://mothur.org/wiki/Category:Commands). Many of these
commands implement various methods to do the same thing while generating
the same output formats. For example, the<span
class="Apple-converted-space"> </span>[cluster
command](http://www.mothur.org/wiki/cluster)<span
class="Apple-converted-space"> </span>implements three ways of
clustering sequences into OTUs. To run cluster, you first have to run a
number of other steps. Each step is a different step in the pipeline. By
making each step discrete like this, users have very fine control on the
knobs of their pipeline and they know exactly what is going on. Of
course, we give people the default parameter values and usually have
papers to backup the defaults, but people are free to alter the commands
at each step. This gives users great control, but at the same time can
be somewhat overwhelming if they feel the need to do something
different. For example, we have 8 chimera functions that each implement
a different algorithm – I would only ever suggest using<span
class="Apple-converted-space">
</span>[chimera.uchime](http://www.mothur.org/wiki/chimera.uchime).

*QIIME.*<span class="Apple-converted-space"> </span>In contrast to the
mothur approach, my experience and that of people I’ve talked with is
that most QIIME users tend to treat functions as a “black box”. If you
want to use the open reference clustering algorithm that command will
align, classify, and assign sequences to OTUs. Although it is possible
to tweak parameters for each of those steps, it isn’t always clear how.
It’s also not entirely clear how one might add steps for making sure
sequences overlap the same region or to identify and remove chimeras.

大意：mothur现在有145个函数。每个函数都会实现自己的功能，你可以随意组合、随意调整参数，并总能得到相应的结果。QIIME则像一个黑盒，你并不清楚它内部在干些什么，调用了那些命令，设置了那些参数。这些你都不能像在mothur中一样随心所欲。

<div>

### Reproducibility 再现性

*mothur.*<span class="Apple-converted-space"> </span>An ongoing problem
in science that has recently gotten a lot of important attention has
been the ability to reproduce work of other scientists. One place where
we can hopefully make progress on this is in the world of computational
analysis. I should be able to take your data and reproduce a figure from
your paper. Sadly this isn’t always possible or as easy as we think it
should be. As a reviewer I see this problem frequently where people will
say they used mothur/QIIME to analyze their data. Um… there are an
infinite number of permutations of functions and parameter values that
one could use. Help? We have worked to help users make their results
more reproducible by outputting log files and posting SOPs. Over the
last two years we have also worked really hard to put<span
class="Apple-converted-space"> </span>[all of our data and code
online](https://github.com/SchlossLab)<span
class="Apple-converted-space"> </span>for others to reproduce. There are
currently two primary tools that people use – Jupyter (previously
IPython Notebooks) and R Markdown documents. We have created a<span
class="Apple-converted-space"> </span>[mothur
hook](https://github.com/SchlossLab/ipython-mothurmagic)<span
class="Apple-converted-space"> </span>for use with IPython notebooks and
are developing hooks for use with R Markdown documents. I personally
prefer R Markdown because I can embed results in my text to write a
paper. In contrast, Jupyter is a notebook, which is useful for
demonstrating how you did an analysis and the results, but isn’t really
able to produce a manuscript ready to submit. Needless to say this is an
area of active development.

*QIIME.*<span class="Apple-converted-space"> </span>Likely because of
its strong roots in Python, the QIIME developers are making great use of
Jupyter to demonstrate how to use QIIME and disseminate their methods.
My understanding is that QIIME v2.0 will make extensive use of this
format.

大意：一篇论文可能告诉你他用了mothur或者QIIME进行了分析，而你事实上并不能重复出相应的结果，因为太多的细节是缺失的，比如命令行的参数等等。mothur和QIIME都在尽可能的把命令和数据同时提供出来，以便后来人重复出相应的结果。

<div>

### Data Accessibility 数据可获取性

*mothur.*<span class="Apple-converted-space"> </span>Related to the
previous point, analyses cannot be reproducible if the data are not
available. Previously, submitting 16S rRNA gene sequences to NCBI’s
Sequence Read Archive (SRA) has been a pain in the tuckus. This resulted
in labs posting data to their personal websites or to 3rd party sites
such as MG-RAST. I’m guilty of the former, although we’re working to
correct this. The problem with these approaches is that often people are
not depositing their raw data (i.e. sff and fastq files), only their
processed data and may not be depositing their metadata. Also, although
the SRA is difficult to search and access, it is a breeze to use
compared to MG-RAST. To overcome this problem, we worked with the
curators at the SRA to develop the<span class="Apple-converted-space">
</span>[make.sra command](http://www.mothur.org/wiki/make.sra), which
helps to<span class="Apple-converted-space"> </span>[simplify the
process](http://www.mothur.org/wiki/Creating_a_new_submission). This
feature has been live since March 2015 and has been widely used by
microbial ecologists. These are low estimates, but as of the beginning
of January there have been 86 submission from 61 studies containing 6367
runs representing 116 GBp submitted using make.sra. There really is no
excuse at this point to use anything but the SRA for depositing raw
sequence data. We are also in the process of developing an sra.info
command that will convert data out of SRA format.

*QIIME.*<span class="Apple-converted-space"> </span>As an alternative to
the SRA, the developers of QIIME also developed<span
class="Apple-converted-space"> </span>[QIITA](http://qiita.ucsd.edu/).
QIITA is an online database for storing and analyzing 16S rRNA gene
sequence data. The goal appears to involve applying a common pipeline to
datasets so that they can be compared. This makes use of the open and
closed-reference clustering algorithms that are critiqued below. It also
provides researchers with the ability to deposit raw data. I recently
tried to access the Earth Microbiome Project (EMP) data that was used in
one of their<span class="Apple-converted-space"> </span>[open-reference
clustering papers](http://www.ncbi.nlm.nih.gov/pubmed/25177538). I
failed. There was no obvious way to download large number of files like
one can with the SRA. When I asked some of the EMP researchers for help,
it was clear QIITA is still under development and that it really isn’t
designed to do what I wanted. My understanding is that they are in the
process of uploading the data to either the European Nucleotide Archive
(ENA) or the SRA.

大意：问题在于SRA存储的是原始数据，你不能得到其它的相关信息，它远非一个完整的信息。鉴于此，mothur开发了一个make.sra的命令用以生成sra并在其中嵌入相关的必要信息。QIIME曾建立了一个QIITA服务来自行组织16S
rRNA的基因序列。不过现在好像有点坚持不下去了。orz。

<div>

### Data visualization 数据可视化

*mothur.*<span class="Apple-converted-space"> </span>We initially
attempted to develop functions that would build heatmaps and venn
diagrams as SVG files. Although these data visualization tools are
useful, I don’t feel like we did a great job of making the output from
these functions as elegant as they could be. After experimenting a bit,
we decided we would never be able to generate figures as nice as one
could in R or Python using the extensive codebase that has been
developed there. Instead, we focus on outputting data in formats that
people can manipulate in other packages. To that end, all of our output
files are text files and we can output a shared file as a BIOM-formatted
file for integration with other microbial ecology tools that use that
format.

*QIIME.*<span class="Apple-converted-space"> </span>I applaud the QIIME
developers efforts to build data visualization tools for analyzing
microbial ecology data. I’m not personally a big fan of their black
background ordinations or 2D depictions of 3D ordinations. The demos
I’ve seen do a nice job of showing how users can re-color points in
ordinations by metadata. Of course, this is something you can also do in
R, but you need to know R first.

大意：mothur曾试图直接输出可视化结果，但后来放弃了。目前，我们主张通过数据交换来使用其它相应的工具（R等）来完成可视化。QIIME这一点做的非常好（此处应有掌声）。这一点QIIME胜。

<div>

### Clustering / OTU picking 聚类/OTU选取

*mothur.*<span class="Apple-converted-space"> </span>We got started with
creating DOTUR, which was the first open source tool for assigning
sequences to OTUs. The plan for mothur was to make DOTUR able to process
454 data, but then we got to having so much fun… mothur currently
implements hierarchical clustering algorithms in the<span
class="Apple-converted-space"> </span>[cluster
command](http://www.mothur.org/wiki/cluster)<span
class="Apple-converted-space"> </span>including the average (the
default), weighted, nearest, and furthest neighbor. We also have<span
class="Apple-converted-space">
</span>[cluster.split](http://www.mothur.org/wiki/cluster.split), which
is a way of dividing your data by taxonomy and then clustering. The
output of cluster.split is the same as cluster, but it is faster and can
be parallelized. We have done<span class="Apple-converted-space">
</span>*a lot*<span class="Apple-converted-space"> </span>of
benchmarking to show that the average neighbor clustering algorithm
gives the best clusters. It may be slower than other methods, but the
data suggest it is consistently the best approach. You can read those
papers<span class="Apple-converted-space">
</span>[here](http://www.ncbi.nlm.nih.gov/pubmed/26664811)<span
class="Apple-converted-space"> </span>and<span
class="Apple-converted-space">
</span>[here](http://www.ncbi.nlm.nih.gov/pubmed/21421784).

*QIIME.*<span class="Apple-converted-space"> </span>As mentioned above,
you can run an old version of mothur from within QIIME. Looking at their
papers and online documentation, it is clear they want people to use
their greedy de novo or their open reference OTU assignment commands,
which are both based on USEARCH. In our<span
class="Apple-converted-space"> </span>[2015
paper](http://www.ncbi.nlm.nih.gov/pubmed/26664811)<span
class="Apple-converted-space"> </span>that benchmarked a diverse
collection of clustering algorithms, we showed that in some cases their
distance-based greedy clustering algorithm could be as good as the
average neighbor algorithm. However, we point out myriad problems with
their open and closed reference clustering algorithms. It is very hard
for me to encourage people to use these algorithms in QIIME. A common
rejoinder is that some datasets are too large for the average neighbor
algorithm. Our experience has been that this is<span
class="Apple-converted-space"> </span>[more a product of sequencing
error](http://blog.mothur.org/2014/09/11/Why-such-a-large-distance-matrix%3F/)<span
class="Apple-converted-space"> </span>than anything else. As we point
out in that paper, speed and memory usage are important, but cannot be
used as the basis to say one method is better than another when there
are clear differences in OTU quality. High quality clustering is a
problem that will continue to plague us as datasets grow, even if they
have a very low sequencing error rate.

大意：mothur更快，还支持并行处理。

<div>

### Illumina sequence processing Illumina序列的处理

*mothur.*<span class="Apple-converted-space"> </span>The<span
class="Apple-converted-space"> </span>[make.contigs
command](http://mothur.org/wiki/make.contigs)<span
class="Apple-converted-space"> </span>is our method of assembling paired
sequence reads into contigs. If your reads fully overlap then it is
possible to use this command with the<span
class="Apple-converted-space"> </span>[rest of the
pipeline](http://mothur.org/wiki/MiSeq_SOP)<span
class="Apple-converted-space"> </span>to get an error rate below 0.02%.
This is easily an order of magnitude lower than what we have seen other
groups describe. Actually, very few other groups (any?) are sequencing
mock communities to report an error rate. You can find the<span
class="Apple-converted-space"> </span>[wetlab
protocol](https://github.com/SchlossLab/MiSeq_WetLab_SOP)<span
class="Apple-converted-space"> </span>at our GitHub repository. This
approach and the bioinformatics benchmarking was<span
class="Apple-converted-space"> </span>[published at
AEM](http://www.ncbi.nlm.nih.gov/pubmed/23793624). Even with the advance
in Illumina’s MiSeq technology to paired 300 nt reads, we are sticking
with the paired 250 nt reads to sequence the V4 region because<span
class="Apple-converted-space"> </span>[the new chemistry
sucks](http://blog.mothur.org/2014/09/11/Why-such-a-large-distance-matrix%3F/).

*QIIME.*<span class="Apple-converted-space"> </span>Greg Caporaso was
the first author on the<span class="Apple-converted-space">
</span>[original
method](http://www.ncbi.nlm.nih.gov/pubmed/20534432)<span
class="Apple-converted-space"> </span>describing how to sequence 16S
rRNA genes on an Illumina machine. Unfortunately, much of their
benchmarking consisted of showing it was possible and that they got
similar results to 454 data. They didn’t actually report error rates.
In<span class="Apple-converted-space"> </span>[subsequent
work](http://www.ncbi.nlm.nih.gov/pubmed/22170427), they suggested that
it is possible to make comparisons with single reads or using HiSeq
data. From our work and experience, we know that these data are very
noisy and problematic. If you want to distinguish very different
communities, use HiSeq data, if you are looking at more similar
communities, you need high quality data. With this as background, it
really isn’t clear what QIIME proposes for assembling reads into contigs
or how it compares to what we’re doing with make.contigs. Their primary
tutorial uses their<span class="Apple-converted-space"> </span>[Moving
Pictures of the Human
Microbiome](http://www.ncbi.nlm.nih.gov/pubmed/21624126)<span
class="Apple-converted-space"> </span>dataset and is disseminate as
a<span class="Apple-converted-space"> </span>[Jupyter
notebook](http://nbviewer.ipython.org/github/biocore/qiime/blob/1.9.1/examples/ipynb/illumina_overview_tutorial.ipynb).
Interestingly, that tutorial does not mention what to do with paired
reads. Other parts of their website discuss assembly, but it isn’t clear
to the typical user how the output fits in with the rest of the
pipeline. They indicate that a paper is forthcoming so hopefully they’ll
expand on this in the future and be able to compare their results to
ours.

大意：二者都有一些工具来处理短序列。但目前缺乏可比性。

译者：由于Illumina的读长太短，并不适合进行rRNA测序（由于序列相似性太高，难以正确的拼接）。MiSeq可以做到300nt。这需要测序技术的进步，即读长的提高。如果有朝一日读长可以达到1500bp，基本达到了16S
rRNA的全长了。那分析就更加完整和方便了。

<div>

### Classification 分类

*mothur.*<span class="Apple-converted-space"> </span>Taxonomic
classification of sequences is handled within the<span
class="Apple-converted-space"> </span>[classify.seqs
command](http://www.mothur.org/wiki/classify.seqs). The default method
is to use the<span class="Apple-converted-space"> </span>[naive Bayesian
classifier](http://www.ncbi.nlm.nih.gov/pubmed/17586664)<span
class="Apple-converted-space"> </span>that was originally developed by
the RDP team. We also enable researchers to use the k-Nearest Neighbor
algorithm based on distance, blast, and kmer-based distances. The naive
Bayesian classifier uses a pseudo-bootstrapping procedure to generate a
confidence score. The RDP website uses 80%, by default cluster.seqs does
not apply a threshold although our SOPs all tell people to use 80%. The
next release of mothur (v1.37.0) will use 80% as the default threshold
for classify.seqs.

*QIIME.*<span class="Apple-converted-space"> </span>The default
classification method in QIIME is to use USEARCH to find the closest
match in a reference database using the<span
class="Apple-converted-space"> </span>[assign\_taxonomy.py
script](http://qiime.org/scripts/assign_taxonomy.html). This appears to
be a quasi nearest neighbors algorithm and if you use the defaults, then
it requires 2 of the 3 top matches to have the same classification. I
haven’t seen this approach published or validated anywhere. This would
appear to be problematic since many taxa in the references only have one
representative – so you would never get a sequence to classify to that
taxon. I would also worry about the problems<span
class="Apple-converted-space"> </span>[we saw with using
USEARCH](http://www.ncbi.nlm.nih.gov/pubmed/26664811)<span
class="Apple-converted-space"> </span>for database searching and closed
reference clustering – basically, classification will change with the
order of the database sequences. QIIME also provides the naive Bayesian
classifier as an option in this script. As the default threshold, they
require a confidence score of 50%. Although the original paper suggests
a threshold of 80%, the RDP site curiously suggests 50% for short
sequences; however, this makes no sense since your confidence should not
vary with sequence length. In our own unpublished analyses, quality of
assignment is proportional to the confidence score.

大意：mothur给你更多、更可靠的选择。

<div>

### Databases 数据库

*mothur.*<span class="Apple-converted-space"> </span>For whatever
reason, when I talk with people about the differences between mothur and
QIIME, one of the things people think makes a<span
class="Apple-converted-space"> </span>*huge*<span
class="Apple-converted-space"> </span>difference between the packages is
the databases we use. Supposedly, I like RDP and QIIME likes greengenes.
Given that QIIME ships with greengenes, I suspect that the QIIME
developers do like greengenes; however, we have no particular affinity
for the RDP taxonomy. We use it in the SOP because it is smaller and
easier to work with. I try to make it clear that you can use the RDP,
SILVA, or greengenes for classification. We actually make the<span
class="Apple-converted-space"> </span>[three reference taxonomies
publicly available](http://mothur.org/wiki/Taxonomy_outline). When it
comes to alignment database, I do think the only way to go is to use a
reference alignment based on the SILVA database. As I tell people, the
alignment within the variable regions in the greengenes alignment looks
like the person was somewhat drunk at the time while the SILVA alignment
looks like it was done by Germans. Oh wait… :) This isn’t a matter of
personal conjecture, we actually quantified the difference in an<span
class="Apple-converted-space"> </span>[earlier
paper](http://www.ncbi.nlm.nih.gov/pubmed/20011594)<span
class="Apple-converted-space"> </span>and then<span
class="Apple-converted-space"> </span>[looked again
recently](http://blog.mothur.org/2015/08/04/No-greengenes-hasnt-improved/)<span
class="Apple-converted-space"> </span>and found the same thing. As the
database curators update their databases, we also update the references.
I don’t know that they change much, but people get vexed when we don’t
keep up with the Joneses.

*QIIME.*<span class="Apple-converted-space"> </span>QIIME comes
prepackaged with the greengenes database from 2013. This is a nice
feature, because it limits the difficulties of keeping track of things.
This also makes for bigger downloads. The QIIME commands appear to allow
people to use their own database if they aren’t interested in the
greengenes database. There are two important points to make with regard
to QIIME’s use of databases. First, as I’ve mentioned elsewhere in this
posting,<span class="Apple-converted-space"> </span>[USEARCH is
sensitive to the
ordering](http://www.ncbi.nlm.nih.gov/pubmed/26664811)<span
class="Apple-converted-space"> </span>of the sequences in your
reference. As we showed in that paper, for whatever reason, the default
ordering of the greengenes database produces high error rates and could
be substantially improved by randomizing the sequences before using
USEARCH. Second, To build trees for used for phylogenetic approaches,
they use sequences that are aligned to the greengenes alignment that I
described above. This is somewhat disconcerting as the the poorly
greengenes-aligned sequences<span class="Apple-converted-space">
</span>[artificially increases the
distances](http://blog.mothur.org/2016/01/12/mothur-and-qiime/(http://www.ncbi.nlm.nih.gov/pubmed/20011594))<span
class="Apple-converted-space"> </span>between sequences. But, as<span
class="Apple-converted-space"> </span>[their documentation
indicates](http://qiime.org/scripts/filter_alignment.html)<span
class="Apple-converted-space"> </span>“FILTERING ALIGNMENTS WHICH WERE
BUILT WITH PYNAST AGAINST THE GREENGENES CORE SET ALIGNMENT SHOULD BE
CONSIDERED AN ESSENTIAL STEP (caps in original)”. This filtering is no
doubt necessary to remove the poorly aligned variable regions. In
the<span class="Apple-converted-space"> </span>[same
publication](http://www.ncbi.nlm.nih.gov/pubmed/20628621), we showed
that applying filters like the traditional Lane mask significantly mutes
the differences between sequences. Although I agree that such filtering
is necessary for building phylogenies where you are trying to propose
new lineages of taxa, it seems mistaken to filter when you are looking
for differences between sequences. It really would be nice to see them
remove so much emphasis on the greengenes database and make the SILVA
references alignment the prepackaged default instead.

大意：mothur使用的是RDP数据，QIIME使用的是greengenes数据。除此之外，常见的rRNA数据库还有SILVA等。mothur中你可以选择任一个数据库分析，QIIME则“太”钟情于greengenes了。我觉得用SILVA会更好的。

<div>

### Conclusions 总结

I hope that you have found this comparison to be useful. As much as
possible, I have tried to be balanced in my critiques of<span
class="Apple-converted-space"> </span>*both*<span
class="Apple-converted-space"> </span>mothur and QIIME. Hopefully, you
will find that most of the differences between the two programs are
pretty cosmetic. The more substantive difference are in aspects of the
programs that are admittedly under active development. One of the things
that absolutely drives me crazy is when people say they like program X
because it gives them “good results”. I am unclear what that means.
Unless you have objective criteria or know the correct answer, you can’t
be certain that you have “good results”. Be honest to admit that you use
program X because you just like it better for cosmetic reasons or have
some actual data to suggest that it is better. Of course, if X happens
to be QIIME, please let me know – my group uses mothur and we want to
make sure we’re using the best software possible. I know you want the
same thing. Finally, I really appreciate the input that I received from
a number of people that I asked to review this review before I posted
it. I worked very hard to remove any snark, cynicism, sarcasm, etc to
provide as balanced a review as possible. These people have held me to
this goal and I appreciate their feedback.

大意：我尽量做到公正评价。（译者：但mothur毕竟是真爱。）

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

 
