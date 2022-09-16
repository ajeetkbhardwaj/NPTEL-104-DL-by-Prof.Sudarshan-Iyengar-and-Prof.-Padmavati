## Module_1 : Biological Neurons


. Hello everyone ah welcome to lecture one of

CS7 015, which is the course on ***deep learning.***

ah In today's lecture is going to be a bit non technical we are not going to cover any

technical concepts or we only going to talk about ***a brief or partial history of deep learning***

ah.

So, we hear the terms ***artificial neural networks, artificial neurons*** quite often these days.

And I just wanted you take you through the journey of where does all these originate

from and this history contains several ah spans across several fields, not just computer

science we will start with biology then talk about something in physics then eventually

come to ***computer science*** and so on right . So, ah with that lets start ah .

So, just some acknowledgments and disclaimers , I have taken lot of this material from the

first people, which I have mentioned on the bullet and there might still be some errors

because its dates as black as 1871.

So, maybe I have got some of the facts wrong . So, feel free to contact me if you think

some of these portions need to be corrected and it would be good if you could provide

me appropriate references for these corrections .

So, let us start with the first chapter, which is on biological neurons as I said its spans

several fields, will start with biology . And we will first talk about the brain and

ah neurons within the brain . So, way back in 1871 1873 around that time, ah Joseph von

Gerlach actually proposed that ah the nervous system our nervous system is a single continuous

network as opposed to a network of many discrete cells right.

So, his idea was that this is one gigantic ah cell sitting in our nervous system and

its not a network of discrete cells.

And this theory was known as the reticular theory right .

And around the same time there was the some ah breakthrough or some ah ah some progress

in staining techniques, where Camillo Golgi discovered that a chemical reaction, that

would allow you to examine the neurons ah neurons or the nervous tissue right.

So, he was looking at this ah nervous tissue using some staining technique and by looking

at what you see in this figure on the ah right hand side the yellow figure, even he concluded

that this is just once single cell and not a network of discrete cells right.

So, he was again a proponent of reticular theory.

So, this is about Camillo Golgi . And then interestingly ah Santiago Kayal he

used the same technique which Golgi proposed, and he studied the same tissue and he came

up with the conclusion that this is not a single cell this is actually a collection

of various discrete cells, which together forms a network . So, it is a network of things

as opposed to a single ah cell there right . So, that is what his theory was; and this

was eventually came to be known as the neuron doctrine.

Although this was not a ah consolidated in the form of a doctrine by Kayal, that was

done by this gentleman . So, he coined the term neuron . So, now, today when you think

about art here about artificial neural networks or artificial neurons, the term neuron actually

originated way back in 1891 and this gentleman was responsible for coining that.

And he was also responsible for consolidating the neuron doctrine . So, already as you saw

on the previous slide ah Kayal had proposed it, but then over the years many people bought

this idea and ah this guy was responsible for consolidating that into a neuron doctrine.

Interestingly he is not only responsible for coining the term neuron, he is also responsible

for coining the term chromosome . So, two very important terms were coined by this one

person right . So, now here is a question right . So, around

1906, when it was time to give the Nobel prize ah in medicine, what do you think which of

these two proponents?

Say there are two theories one is reticular theory, which is a single cell and then there

is this neuron doctrine which is a collection of cells or collection of neurons that a nervous

system is a collection of neurons . So, what do you think which of these two guys who are

proponents of these two different theories, who would have got the actual Nobel Prize

for medicine . So, interestingly ah it was given to both

of them . So, till 1906 in fact, way later till 1950 also this debate was not completely

set ah settled and then the committee said ok both of these are interesting pieces of

work, we yet do not know what really actual what the situation is actually , but these

conflicting ideas have a place together and so, the Nobel Prize was actually given to

both of them, and this led to a history of ah a some kind of controversies between these

two scientists and so on.

And this debate surprisingly was settled way later in 1950 and not by progress in biology

as such but by progress in a different field .

So, this was with the advent of electron microscopy . So, now, it was able to see this at a much

ah better scale and by looking at this under a microscope it was found that actually there

is a gap between these neurons and hence its not a one single cell, its actually a collection

or a network of cells with a clear gap between them or some connections between them, which

are now known as synapses right.

So, this was when the debate was settled . So, now why am I talking about biology why

am I telling you about ah biological neuron and so on right.

So, this is what we need to understand . So, there has always been interested in understanding

how the human brain works from a biological perspective at least.

And around this time the debate was more or less settled that we have this our brain is

a collection of many neurons and they interact with each other, to help us do a lot of complex

processing that we do on a daily basis right right from getting up in the morning and deciding

what do we want to do today, taking decisions performing computations and various complex

things that our brain is capable of doing right .

Now, the interest is in seeing if we understand how the brain works, can we make an artificial

model for that right.

So, can we come up with something which can simulate how our brain works and what is that

model, and how do we make a computer do that or how do we make a machine do that.

So, that is why I started from biological neurons to take the inspiration from biology.

## Module_2 : From Spring to Winter AI


 And now , what we will get into ah in the

next chapter is, we will start talking about artificial intelligence . And this is titled

as from the spring to the winter of a i . So, I am going to talk about when was this boom

in a I started? or when is that people started thinking and talking about a, I seriously

? And what eventually happened to the initial boom? and so, on right.

So, let us start with 1943 . Whereas, I saying that there was a lot of interest in understanding

, how does a human brain work ? And then come up with a computational or a mathematical

model of that . So Mcculloch Pitts , one of them was a neuroscientist and the other one

was a logician right, no computer scientists or anything at that point of time .

And they came up with this extremely simplified model , that just as a brain takes a input

from lot of factors right. So now, suppose you want to decide whether you want to go

out for a movie or not . So, you would probably think about , do you really have any exams

coming up that could be our factor X 1 . You could think about is a weather good to go

out is it raining would it be difficult to go out at this point . Would there be a lot

of traffic is it a very popular movie and hence tickets may not be available and so

on right . So, being kind of presses all this information

you might also look at things like the reviews of the movie, or the IMDB rating of the movie

and so on . And based on all these complex inputs , it applies some function and then

takes a decision yes or no . That ok , I want to probably go for a movie .

So, this is an overly simplified model of, how the brain works is? and what this model

says is that , you take inputs from various sources and based on that you come up with

the binary decision right. So, this is what they proposed in 1943 . So now, we have come

to an artificial neuron . So, this is not a biological neuron this is how, you would

implement it as a machine right. So, that was in 1943 .

Then along and then this kind of led to a lot of ah boom ah in our interest in artificial

intelligence and so on. And I guess around 1956 ah, in a conference the term artificial

intelligence was a formally coined and within a 1 or 2 years from there Frank Rosenberg

came up with this Perceptron model of ah doing computations or what Perceptron model of what

an artificial neuron could be ? And we will talk about this in detail later

on. The course and not tell you what these things are as of? Now just think of the a

new model was proposed and this is what he had to say about this model right. So, he

said that , the Perceptron may eventually be able to learn , make decisions and translate

languages . Do you find anything odd about this statement yeah? So, learn and make decisions

make sense, but why translate languages ? Why is so specific ? Why such a specific interest

in languages ? Right . So, that you have to connect back to history

right. So, this is also the period of the cold war and there was all those. Always a

lot of interest. A lot of research and translation was actually fueled by the world war and evens

that happened after that; Where these ah countries which were at loggerheads with each other.

They wanted to understand what the other country is doing? But they did not speak each other's

language . That is why , there was a lot of interest from espionage point of view or from

spying and so on to be able to translate languages. And hence, that specific require and lot of

this research would have been funded from agencies, which are interested in these things

right, and the defence or war or something ok .

So, and this work was largely done for the navy and this is an ah this is an extract

from the article written in New York times. Way back in 1957 or 58 , where it was mentioned

that the embryo often this Perceptron is an embryo of an electronic computer. That the

navy expects will be able to walk, talk, see, write, reproduce itself and be conscious of

it is existence . So, I am not quoting something from 2017 or

18. This is way back in 1957 58. Why I am that is why I like the history part of it

. So, recently there is a lot of ah boom or a lot of ah hype around , a I that a I will

take over a lot of things will take our jobs. It might eventually ah , we might be colonized

by a I agents and so on . So, I just want to emphasize that , I do not

know whether, that will happen or not , but this is not something new we have been talking

about the promise of a I as far back. Since, 1957 1958 right, this not something new that

people are talking about. Now , it is always been there and to what extend , this promise

will be fulfilled is yet to be seen . And of course, as compared to 1957 58 , we

have made a lot of progress in other fields which have enabled . A I to be ah much more

successful than it was earlier for example, we have much better compute power . Now we

have lots of data now and all thanks to the internet, and other things that you can actually

crawl tons and tons of data and then try to learn something from a data or try to make

the machine learn something from it right. So, we have made a lot of progress in other

aspects where, which a I is now at a position. Where, it can really make a difference ? But

just wanted to say that, these are not things which I have not been said in the past . It

has always been the day has always been considered to be very promising and perhaps a bit hyped

also right. So, that is about 1957 58 . Then now , what we talk about ? What is all

the for the past 8 to 10 years? At least ah when we talk about a I talking about deep

learning ? And that is what this course is about largely about deep learning . I am not

saying that other and what deep learning ah is largely about? If I want to tell you in

a very layman nutshell term is . It is about a large number of artificial neurons connected

to each other in layers and functioning towards achieving certain goal right.

So, this is like a schematic of what a deep neural network or a feed forward neural network

would look like . Now this is again not something new which is up in the last 8 to 10 years.

Although , people have started discussing it a lot in the last 8 to 10 years . Look

at it way back in 1965 68 opposed something which looked very much like a modern deep

neural network or a modern feed forward neural network .

And in many circles, he is considered to be one of the founding fathers of modern deep

learning right . So ah , that is about that right. From 1943 to 1968 , it was mainly about

the springtime for a I and what I mean by that ? That everyone was showing interest

in that. The government was funding a lot of research in a I and people really thought

that a I could deliver a lot of things on a lot of for various applications, health

care defence and so on . And then around, 1969 an interesting paper

came out by these 2 gentlemen ah Minsky and Papert . Which essentially outlined some limitations

of the Perceptron model and we will talk about these limitations later on in the course.

In the second or third lecture , but for now I will not get into a details of that , but

what it is said that it is possible that a Perceptron cannot handle some very simple

functions also. So, you are trying to make the Perceptron

learn some very complex functions. Because, the way we decide how to watch a movie is

a very complex function of the inputs that we considered , but even a simple function

like x or is something which a Perceptron cannot be used to model that is what this

paper essentially showed . And this led to severe criticism for a I and

then, people started losing interest in a I and lot of government funding actually subsided

after 1969 . All the way to 1986 actually this was the

a I winter of connectionism. So, there was very little interest in connectionist a I

. So, there are 2 types of a I one is symbolic a I and the other is connectionist a I. So

whatever, we are going to study in this course about neural networks and all . That probably

falls in connectionist a I paradigm and there was no interest in this and people . I mean

hard to get funding and so on for these 17 to 18 years .

And that was largely triggered by this study that was done by Minsky and Papert and interestingly

they were also often misquoted and what they had ah actually said in that papers. So, they

had said a single Perceptron cannot do it . They In fact, said that a multi-layer network

of Perceptrons can do it , but no one focused on the second part that, a multi-layer network

of Perceptron people started pushing the idea that a Perceptron cannot do it . And hence,

we should not be investigating it. And so, on right, so that is what happened for a long

time and this known as the winter ah the first winter .

Then around 1986 actually came ah this algorithm which is known as back propagation . Again

this is an algorithm which we are going to cover in a lot of detail in the course ah

in the 4th or 5th lecture . And this algorithm actually enables to train a deep neural network

right ah. So, deep network of neurons is something that you can train using this algorithm .

Now, this algorithm was actually popularized by at Rumelhart and others in 1986, but it

is not ah completely discovered by them , this was also around in various other fields . So,

it was there in ah I think in systems analysis or something like that . It was being used

for other purposes in a different context and so on . And Rumelhart other and others

in 1986 were the first to kind of popularize it in the context of deep neural networks

. And this was a very important discovery because,

even today all the neural network, so most of them are trained using back propagation

right . And of course, there have been several other advances , but the core remains the

same that you use back propagation to train a deep neural network right.

So, something this was discovered almost 30 years back is still primarily used for training

deep neural networks. That is why, this was a very important ah paper or ah breakthrough

at that time ; and around the same time . So, again interestingly, so back propagation ah,

is used in conjunction with something known as gradient descent ; Which was again discovered

way back in 1847 by Cauchy and he was interested in using this to compute the orbit of heavenly

bodies rights. That is something that people care about at

that time today of course, we use it for various other purposes one of them being discovering

cats and videos or even for medical imaging or for describing ah . Whether ah, ah certain

have of cancer is being depicted in a X ray or things like that there is a lot of other

purposes for which , deep neural networks and hands ah .

And hence ah, back propagation gradient descent and other things are being used for it, but

again these are not very modern discoveries these are dated way back 30 years and even

gradient descent is almost 150 years and so on right; So, that is ah what I wanted to

emphasize . And around the same time in 1990 or 1989 there

is this another interesting theorem which was proved which is known as the universal

approximation theorem . And this is again something that we will cover in the course

ah in the third lecture or something like where we will talk about the power of a deep

neural network right. So, again the importance of this or why this

theorem was important? will become clear later and when we cover it in detail , but for now

it is important to understand that, what this theorem said is that if you have a deep neural

network you could basically model all types of functions continuous functions to any desired

precision. So, what it means in very layman terms is

that . If the way you make decisions using a bunch of inputs is a very, very complex

function of the input . Then you can have a neural network, which will be able to learn

this function right in many laymen terms , that is what it means .

And if I have to type it up a bit or I have to say it in a very enthused and excited manner.

I would say that basically it says that , deed neural networks can be used for solving all

kinds of machine learning problems and that is roughly what it says , but with a pinch

of salt and a lot of caveats , but that is ah what it means at least in the context of

this course ok . So, this is all around 1989 and despite this

happening right some important discoveries towards the late end of 80's, which was back

propagation universal approximation theorem . People were still not ah being able to use

deep neural networks for really solving large ah practical problems right . And a few challenges

there was of course the compute power at that time was not at a level where , ah it could

support deep neural networks . We do not have enough data for training deep

neural networks and also in terms of techniques . While back propagation is a sound technique

, it is to fail when you have really deep neural network . So, when people try it training

a very deep neural network they found that the training does not really converge the

system does not really learn anything and so on and there were certain issues with using

back propagation of the shelf at that time ah because of which it was not very successful

right. So, again despite these slight boom around

86 to 90 where some important discoveries were made ; and even follow up in 92 93 and

so on. There is still not a real big hype around deep neural networks or artificial

neural networks and at time again a slump a slow winter ah right up till 2006 .

## Module_3 : Deep Revival


When this deep revival happened, right so in 2006 a very important study was or a very

important ah contribution was made by Hinton and ah Salakhut Dinov .

Sorry if I have not pronounced it properly and they found that a method for training

very deep neural network effectively . Now, again the details of these are not important

. We will be doing that in the course at some point , but what is important take away here

is that while from 1989 to 2006 , we knew that there is an algorithm for training deep

neural networks and they can potentially be used for solving a wide range of problems

because that is what the universal approximation theorem said , but the problem was that in

practice we were not being able to use it for much , right .

It was not easy to train these networks, but now with this technique there was revived

interest and hope that now actually can train very deep neural networks for lot of practical

problems , this part of the interest again and then, people started looking at all such

of thing, right that even this particular study which was done in 2006 will actually

be very simple to something done way back in 91-93 which again ah showed that you can

train a very deep neural network , but again due to several factors may be at that time

due to the computational requirements or the data requirements or whatever I am not too

sure about that , he did not become so popular then, but by 2006 probably the stage was much

better for these kind of networks or techniques to succeed . So, then it became popular in

2006 . Then, this 2006 to 2009 people started gaining

more and more insights into the effectiveness of this discovery made by Hinton and others

which is unsupervised pre-training, right.

That is what I spoke about on the previous slide unsupervised pre-training .

They started getting more and more insights into how you can make deep neural networks

really work, right.

So, they came up with various techniques , some of which we are going to study in this course

. So, this was about how do you initialise the network better , what is the better optimization

algorithm to use, what is the better regularization algorithm to use and so on .

So, there were many things which were started coming out at this period 2006 to 2009 and

by 2009, everyone started taking note of this and again deep neural networks of artificial

neural networks started becoming popular.

That is when people realised that all this ah , all the negative things that were tied

to it that you are not able to train it well and so on helps slowly .

People have started finding solutions to get by those and maybe we should start again focusing

on the potential of deep neural networks and ah see if they can be used for large scale

practical application , right . So, this 2006 to 2009 was again a slow boom period were

people were again trying to do a lot of work to ah popularize deep neural networks and

get rid of some of the problems which existed in training them .

Now, from 2009 onwards there was this series of success is which kind of caught everyone

which made everyone to stand up and take notice , right that this is really working for a

lot of practical applications starting with handwriting recognition . So, around 2009

, these guys won ah handwriting recognition competition in Arabic and they did way better

than the computer systems using a deep neural network and then, this was a success.

So, this was an handwriting recognition and then, there was speech . So, this showed that

various existing systems , the error rate of these system could be seriously ah be significantly

reduced by using deep neural networks or plugging in a deep neural network component to existing

systems , right . So, this was handwriting and then, speech .

Then again some kind of speech recognition which was on android handwritten digit recognition

for MNIST ; this is a very popular data set which had been around since 98 and a new record

was set on this data.

So, this is the highest [acuraty/accuracy] accuracy that was achieved on this data set

around that time in 2010 , sorry and this is also the time when GPUs entered the same,

right.

So, before that all of the stuff was being done on CPUs , but then people realised that

very deep neural networks require a lot of computation and lot of this computation can

happen very quickly on GPUs as supposed to CPUs . So, people started using GPUs for training

and that drastically reduced the training and inference time . So, that was again something

which sparked a lot of interest, right because even though these were successful , they were

taking a lot of time to train , but now the GPUs could even take care of that and this

success continued . So, people started gaining ah or getting success

in other fields like visual pattern recognition . So, this was a competition on recognising

traffic sign boards and here again a deep neural network did way better than its ah

other competitors . Then, the most popular or one thing which

made neural networks really popular was this Image Net Challenge which was around since

2008 or 2009 and before 2012 when this AlexNet was one of the participating systems in this

competition , most of the systems were non neural network based systems and this competition

was basically about ah classifying a given image into one of thousand classes, right.

So, this could be an image of a bird or a dog or a human or car, truck and so on say

you have to identify the right class of the main object in the image , right . So, in

2012 this AlexNet which was a deep neural network or a convolutional neural network

based system was able to actually outperform all the other systems by a margin of 67 percent,

right.

So, the error for this system was 16 percent and this is a deep neural network because

it had 8 layers . The next here this was improved further and

something known as ZF network propose which was again 8 layers, but it did better than

AlexNet . The next here even a deeper network with 19 layers was proposed which did significantly

better than AlexNet . Then, Google entered the scene and they proposed something which

is 22 layers and again reduced the error , then microsoft joined in and they proposed something

which had 152 layers and the error that you see here is actually better than what humans

do, right.

So, even if a human was asked to label this image because of certain law, certain noise

in the image and so on , even a human is bound to make more errors than 3.6 percent , right.

That means, even if you show hundred images to humans , he or she is bound to make go

wrong or more than three or four of these images right whether there is this system

was able to get an error of 3.6 percent over the large .

So, this 2012 to 2016 period were there was this continuous success on the Image Net Challenge

as well as successes in other fields like Natural Language Processing , Handwriting

, Recognition Speech and so on . So, this is the period where now everyone started talking

about deep learning and lot of company started investing in it . A lot of traditional systems

which were not deep neural network based was now started, people started converting them

to deep neural network based system, right.

So, translation system, speed systems, image image classification object detection and

so on, there were lot of success in all these fields using deep neural networks , right

and this particular thing that we are talking about which is image net and the success in

this was driven by something known as Convolutional Neural Networks .

## Module_4 : From Cats to Convolutional Neural Networks


 I will talk about the history of Convolutional

Neural Networks, and I call this part of history as cats and it will become obvious why I call

it so . So, ah around 1959 ah Hubel and Wiesel did

this ah famous experiment they are still I think ah you could see some videos of it on

YouTube, where ah there is this cat and there was a screen in front of it and I will screen

ah there were these lines being displayed at different locations and in different orientations

right.

So, slanted, horizontal, vertical and so on, and there are some electrodes ah ah fitted

to the cat and they were measuring trying to measure that which parts of brain actually

respond to different visual stimuli.

Let us say if you show it ah stimulus at a certain location, there is a different part

of the brain fire and so on right.

So, and one of the things of outcomes of the study was that, ah that different neurons

in brain fire to only different types of stimuli, it is not that all neurons in brain always

fire to any kind of visual stimuli that you give to them right.

So, this is essentially roughly the idea behind convolutional neural networks ah starting

from something known as Neocognitron, which was proposed way back in 1980, you could think

of it as a very primitive convolutional neural network, I am sure that most of you have now

read about or heard about convolutional neural networks , but something very similar to it

was proposed way back in 1980 . And what we know as the modern convolutional

neural networks maybe ah I think Yan Li Kun ah is someone who proposed them way back in

1989, and he was interested in using them for the task of handwritten digit recognition

and this was again in the context of postal delivery services right.

So, lot of pin codes get written or phone numbers get written on ah the postcards and

there was a requirement to read them automatically . So, that they can be the letters or postcards

can be separated into different categories according to the postcard according to the

postal code and so on right.

So, or the pin code . So, that is where this ah interest was there

and 1989 was when this convolutional neural networks were first proposed or used for this

task . And then over the years, ah several improvements

were done to that; and in 1998 this now how famous data set the emulous data set which

is used for teaching deep neural networks, courses or even for initial experiments with

various neural network based ah networks.

ah This is one of the popular data sets, which is ah used ah in this field and this was again

ah released way back in 1998 and even today even for my course I use it for various assignments

and so on . So, it is interesting that an algorithm which

was inspired by an experiment on cats is, today used to detect cats in videos of course,

among other various other things is just ah I am just jokingly saying this .

## Module_5 : Faster, Higher & Stronger 


So, now ah . So, this is what the progression

was right that, in 2006 people started ah or the study by Hinton and others led to the

survival, and then people started realizing the deep neural networks and actually we use

for lot of practical applications and actually beat a lot of existing systems .

But there are still some problems and we still need to make the system more robust, faster

and ah even scale higher accuracies and so on right.

So, in parallely while there was lot of success happening from 2012 to 2016 or even 2010 to

2016. In parallel there will also a lot of research to find better optimization algorithms

which could lead to better convergence better accuracies .

And again some of the older ideas which were ah proposed way back in 1983. Now this is

again something that we will do in the course . So, most of the things that I am talking

about we are going to cover in the course. So, we are going to talk about the image the

challenge, we are going to talk about all those networks the winning networks that I

had listed there Alex net z f net Google net and so on .

We are going to talk about Nesterof ah gradient descent ah which is listed on the slide. And

many other ah better optimization methods which were proposed starting from 2011. So,

there was this parallel resource happening while people were ah getting a lot of success

using traditional neural network, they are also interested in making them better and

robust and lead for lead to faster convergence and better accuracies and so on .

So, this led to a lot of interest in coming up with better optimization algorithms, and

there was a series of these proposed starting from 2011 . So, Adagrad is again something

that we will do in the course, RMS prop, Adam Eve and many more it is a many new algorithms

I have been proposed, and in parallel a lot of other ah ah regularization techniques or

weight initialization strategies have also been proposed for example, Batch normalization

or Xavier initialization and so on . So, these are all things which were aimed at making

neural networks perform even better or faster and even reach better solutions or better

accuracies and so on, this all that we are going to see in the course at some point or

the other.

## Module_6 : The Curious Case of Sequences


So, I was talking about successes in ah image , speech , pattern recognition even natural

language processing and so on . So, the interesting thing here is about sequences, right.

So, I will talk about sequences now . Sequences are everywhere when you are dealing

with data . So, you have time series which is like say the stock market ah trends or

any other kind of a series , time series , then you have speech which is again a series of

phonemes or you have music , you have text which is a series of words , you could even

have videos which are the series of images, right , one frame, each image, each frame

can be considered to be an image and so on right .

So, in speech data one peculiar characteristic of speech data is that every unit in the sequence

interacts with other units , right.

So, words on their own may not mean much , but when you put them together into a sentence,

they all interact with each other and give meaning to the sentence, right and the same

can be said about music or speech or any kind of sequence data , right.

So, all these ah elements of the sequence actually interact with each other .

So, there was a need for models to capture this interaction and this is very important

for natural language processing because in natural language processing, you deal with

sequence of words or all your texts or sentences or documents or all sequences of words, right

. So, that is very important and the same in the case of speech also .

So, if you take up any deep learning paper, nowadays it is very likely that you will come

across the term Recurrent Neural Network or LSTMS which are long short term memory cells

and so on, right.

So, this is also something which was proposed way back in 1986 , right.

So, a recurrent neural network is something which allows you to capture the interactions

between the elements of your sequence . I had said at a very layman ah level , but of

course, you are going to see this in much more detail in the course and this was also

not something new even though you hear about it a lot in the past 3 to 4 years , the first

recurrent neural network and what you see here is exactly a very similar to what we

are going to cover in the course was proposed way back in Jordan by Jordan in 1986 .

Its variant was proposed by Elmen in 1990 , right.

So, this is again not a very new idea . This has existed for some time , but now there

are various ah factors because of which it has been possible to now start using them

for a lot of practical applications . As I said one, you have a lot of compute time and

the other you have a lot of data and the third is now the training has stabilized a lot because

of these advances which I was talking about in terms of better optimization algorithms

, better regularization , better weight initialization and so on .

So, it has become very easy to train these networks for real world problems at a large

scale , right . So, that is why they have become very popular and hear about them on

a regular basis , but it is again something which was done way back .

So, from 1999 to 1994, actually people also looking at various problems will be training

neural networks and recurrent neural networks , so that this problem which is known as exploding

and the vanishing gradient problem which is again something that we will see in the course

Unreasonable Detail . We have this problem and it is very difficult.

You train recurrent neural networks for longer sequences, right.

So, if you have a very long sequence or a time series, you cannot really train a recurrent

neural network to learn something from that .

To overcome these problems around 1997 , Long Short Term Memory cells were proposed and

this is again something that we will cover in the course and this is now almost the factor

standard used for training for a lot of work.

LSTM are used as one of the building blocks and another variants of LSTMs which are known

as gated recurrent units and some other ah variants.

So, this is also not something new even though they have become very popular nowadays like

almost any article that you pick about to talk about , any article on deep learning,

the topic about to talk about recurrent neural networks or LSTMs or gated recurrent units

, this is not something which is new.

LSTMs had come way back in 1997 ah, but again due to various ah compute and other issues

which I said at that time, it is not so easy to use them , but by two 2014 because of these

parallel progresses which I mentioned ah in terms of optimization regularization and so

on , people are now able to use RNNs LSTMs for large scale sequence to sequence problems

and in particular a very important discovery at this time are very important ah model which

was proposed at this time which is Attention Mechanism which is ah used in a lot of ah

deep neural networks nowadays which enabled to deal with a lot of sequence prediction

problems.

For example, translation where you have given one sequence in one language and you want

to generate the equivalent sequence in another language.

So, this is known as a sequence to sequence translation problem . So, for that people

proposed a sequence to sequence attention network and this was one of the key discoveries

which then led to a lot of ah adaptation of adoption of ah deep neural networks for NLP.

A lot of research in NLP happened ah which was then driven by deep neutral networks . So,

a lot of existing algorithms which are non neural network based algorithms which are

traditionally used for NLP was slowly replaced by these deep neural network based algorithms

, ok.

Again this idea of attention itself is something that was explored earlier also ah somewhere

around 1991 or so and it was something known as Reinforcement Learning which was used for

learning this attention mechanism.

What attention basically tells you is that if you have a large sequence and if you want

to do something with this sequence, what are the important ah entities of this sequence

or elements of this sequence that you need to focus on, right.

So, this is again something that we will look at in detail in the course

## Module_7 : Beating Human at their own game


Now, since I mentioned ah r l.

So, we will go on to the next chapter which was now becoming much more ambitious with

what you can do with deep learning and people started beating humans at their own game quite

literally . So, there was this starting with Atari games

in 2015 where ah resources from deep mind show that you could train a deep neural network

to play Atari games and do much better than what humans do , right . So, that is something

that they were able to show on Atari games and then, people started looking at other

game . So, then there was this GO and this popular

ah ah tournament and which AlphaGO which is ah deep reinforcement learning based agent

was actually able to beat the reigning champion at that time AlphaGO Zero was one of the best

players of GO at that time . Then, even at poker were something known as DeepStack which

is again a deep reinforcement learning based agent which is able to beat 11 professional

poker players at this game . Then, other games like Defense of the Ancients

since on which is a much more complex strategy based game where again ah deep reinforcement

learning based agents have shown a lot of success in beating top professional players

on this game right.

## Module_8 : Madness


So, this was all happening where deep learning now started showing a lot of promise in a

lot of fields N L P, vision speech ah and again this deep reinforcement learning and

so on, which led to this complete madness starting from 2013 .

Well almost for every application the traditional methods were then ah overwritten or kind of

beaten by deep neural network based system. So, something like language modelling, which

has been around since probably 1950s or so. Now the reining ah algorithm or the or the

better algorithm for language modelling is now something which is based on deep neural

networks . Then similarly for speech recognition, lot

of work, a lot of probabilistic ah, lot of work based on probabilistic models was done

in this or in the speech ah ah area or the speech literature for the past 30 40 years

, and now all of that has been overcome by deep neural network based solutions .

Same for ah machine translation , a lot of interest in this field , a lot of companies

now have their machine translation systems based on deep neural networks as opposed to

the earlier phrase based statistical machine translations or the probabilistic models which

were used earlier ah Similarly, for conversation modelling dialogue,

a lot of new work started in dialogue post a deep learning era, where people now realize

that if you have a lot of sequences of conversations, you could actually try to train a deep neural

network to learn from this sequence and have conversations with humans. Of course, you

are nowhere close to human level conversations, we are very very far off from them, but in

limited domains these ah bots are showing some success now.

Ah same for question answering where you are given a question and you want to answer it,

either from a knowledge graph or from a document or from a image and so on .

And in the field of ah ah ah computer vision things like object detection, most of the

raining ah systems or the best performing systems, nowadays are deep neural network

based systems, a lot of advances are being made on these systems over in the last few

years . Same for visual tracking where you want to

track the same person in a video or image captioning, where you want to generate captions

for images . For example, people upload a lot of images on Facebook .

And if you want to automatically caption them or imagine you are ah on a reselling site

right, something like O L X where you upload your furniture , and you do not provide a

description from that , but can the machine already automatically generate a description

for it. So, it is easier for the human to read what that product is and so on right.

So, similarly video captioning, I given a video anyone to caption the main activity

which is happening in that video. All of these ah problems are being solved using deep learning

based solutions, using a combination of something known as feed forward neural networks or convolutional

neural networks or recurrent neural networks and so on .

Visual question answering, you are given an image and a question and you want to answer

that question .Video question answering; answering questions from videos . Video summarizations;

if you are given a large video and you want to generate a trailer, a sort of a trailer

for that video contains, which kind is the most important frame for that video. Even

these systems are based on deep learning . Then this was all about classification recognition

and so on , but now people started getting more ambitious that can, we humans are very

good at creativity . So, can we use machines to be creative right to generate images . So,

now, if I have seen a lot of celebrity faces , can I generate new celebrity faces or if

I have seen a lot of bedroom images . And I am if a fireman architect . Now can

I generate new bedroom images can i, can we train a machine to generate new bed bedroom

images. So, a lot of phenomenal progress or work has happened in this field in the last

4 5 years, starting with things like generative adversarial networks, we reached an auto encoders

and so on . And people are now starting to seriously invest

into creativity that how to make machines creative , again we are far off from where

the desired output, but there is still significant progress happening in this field ah generating

audio. So, that was about generating ah images, you can generate music also ah. And this is

again about generating images and so on .

## Module_9 : Need for Sanity


So, lot of fields have adopted deep learning now and lot of State of the Art systems are

based on deep neural networks , but now what is needed is after all this madness were deep

learning has taken over a lot of ah research areas . Can we now bring in some sanity to

the proceeding , right.

So, this is really a need for sanity . Why I say that is that because there is this paradox

of deep learning . So, there is this interesting question that why does deep learning works

so well despite having a high capacity . So, the deep neural networks have a very high

capacity which means that susceptible to over fitting.

So, most of you would have done some course on machine learning . So, there you know that

over fitting is bad because you are just memorizing the training data and then, you might not

be able to do so well and attested and over fitting happens when your model has a high

capacity . So, even though deep neural networks have high capacity , why are they doing so

well . We will focus on this high capacity, but when we talk about the universal approximation

theorem and give some arguments for why deep neural networks have such a high capacity

. The other thing is they have this numerical

instability, right . So, we spoke about this vanishing and exploding gradients and again,

we will talk about this later on in the course . So, despite this training difficulties why

is it that deep neural networks performs so well and of course, they have this sharp minima

which is again ah it could lead to over fitting.

So, if you look at there is an optimization problem, it is not a need convex optimization

problem . So, it is a non convex optimization problem . So, why does it still do so well?

So, it is also not very robust . So, here is an example on the right hand side the figure

that you see . So, the first figure is actually of a panda and the machine is able to detect

this Panda with some 57 percent confidence , right . We have trained a machine for a

lot of animal images . We have shown it a lot of animal images at test time.

We show at this image.

The first image that you see on the ah right hand side and is able to classify this is

a Panda with 57 percent confidence , but now what I do is I add some very random noise.

So, that second image that you see with some very random pixels if I add it to this image

, I will get a new image , right.

So, every pixel in this image is added to this new noise image and I get the image which

is see on the third.

The third image that you see right to you and me or to any average human, this still

looks like a Panda . There is hardly any difference between this image and the original image

, but now if you pass this to the machine , all of a sudden instead of recognizing this

is a Panda, it starts to recognize it as a Gibbon and that too with 99 percent confidence

, right.

So, why is it that they are not very robust and despite this not being very robust , why

are deep neural networks so successful , right.

So, people are interested in these questions and people have started asking these questions

. There are no clear answers yet , but slowly

and steadily there is an increasing emphasis on explainability and theoretical justifications

, right . So, it is not enough to say that your deep neural network works and gives you

99 percent accuracy . It is also good to have an explanation for why that happens is it

that some components of the networks are really able to discriminate between certain patterns

and so on.

So, what is going on inside the network which is actually making it work so well , right

and hopefully this will bring in some sanity to the proceedings .

So, instead of just saying that I apply deep learning to problem x and got 99 success , we

will also make some kind of ah more scene arguments just to why this works and what

is the further promise of this and thinks like that.

So, that is roughly a ah quick historical recap of where deep learning started and where

it is today starting all the way back from advances in biology in 1871 to recent advances

till 2017 and so on deep learning, right and here are few URL.

So, you could take a look at this for a lot of interesting applications of recurrent neural

networks . Bunch of startups which have come up in this space is working on very varied

an interesting problems and here are all the references that I have used for this particular

presentation . So, that is where we end lecture 1 and I will see you again soon for lecture

2 . Thank you.
