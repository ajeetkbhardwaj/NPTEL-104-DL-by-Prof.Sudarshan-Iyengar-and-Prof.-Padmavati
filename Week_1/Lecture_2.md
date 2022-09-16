## Module_1 : Motivation from Biological Neurons

So, welcome to lecture 2 of C S 7015 which

is the course on deep learning . So, we will talk about McCulloch Pitts Neuron ah thresholding

Logic, perceptrons and a learning algorithm for Perceptrons and talk about the convergence

of this algorithm , and then we will talk about multi layer network of perceptrons

And finally, the representation power of perceptrons ah . So, let us start module 1 ah, which is

on biological neurons . So, remember during the history we had started all the way back

in the 1880s when we spoke about biological neurons . So, we will just start there spend

a few minutes on it and then go on to the computational models which is McCulloch Pitts

neuron . So, now this is a course on deep learning

. So, we are going to talk about deep neural networks . Now the most fundamental unit of

a deep neural network is something known as an artificial neuron .

And the question is why is it called a neuron right , where does the inspiration come from

right . So, we already know that the inspiration comes from biology and more specifically it

comes from the brain, because we saw that way back in the 1890s this term neuron was

coined for neural processing units or the cells in our brain right .

So, now before we move on to the computational neurons or the artificial neurons , we will

just see the biological neurons in a bit more detail and then we will move on from there

right . So, this is what a typical ah biological neuron

looks like . So, here actually there are 2 neurons ah. This portion ah is called the

dendrite , so it is used to receive inputs from all the other neurons right .

So, that is the place where the input comes in . Then ah remember we said that in 1950s

we discovered that these neurons are actually discrete cells and there is something which

connects them . So, that connection is called a synapse and it decides the strength of the

connection between these 2 neurons ok . So, there is an input , there is some strength

to the connection . Then once this neuron receives inputs from

various other neurons, it starts processing it right, so that is the central processing

unit which is called the SOMA , and once it is done this processing it will, it is ready

to send its output to other set of neurons right . So, that output is carried on by the

axon . So, we have inputs, we have some weights attached to the input, we have some processing

and then an output right . So, that is what a typical biological neuron looks like .

And let us see a very very cartoonish illustration of how this works right, how the neuron works

. So, our sense organs interact with the outside world and then they pass on this information

to the neuron and then the neuron decides whether I need to take some action. In this

case the action could be whether I it should laugh or not right, whether the input is really

funny enough to evoke laughter . So, if that happens this is known as something that the

neuron has fired ok . Now, of course, in reality it is not just

a single neuron which does all this . There is a massively parallel interconnected network

of neurons right. So, you see a massive network here . Now the neurons in the lower level

site, so these neurons. They actually interact with the sensory organs, they do some processing

based on the inputs , so they decide whether I should fire or not .

And if they fire they transmit this information to the next set of neurons right and this

process continues till the information is relayed all the way back and then finally,

you decide whether you need to take any action or not , again in which this case it should

be laughter right , so that is how it works. And when I say massively parallel interconnected

network I really mean it, because there are 10 raise to eleven which is roughly 100 billion

neurons in the brain right ok . Now, this massively parallel network also

ensures that there is some division of work . Now what do you mean by that is not that

every neuron is responsible for taking care of whether I should laugh or not or not every

neuron is responsible for processing visual data , some neurons may possess visual data,

some neurons may possess speeds data and so on right. So, there is this division of work,

every neuron has a certain role to play . So, for example, in this cartoonish ah example

that we took right . So, there might be this one neuron which fires

if the visuals are funny right whatever you are seeing is funny . There will be one neuron

which finds Sheldons speech to be funny right, the way he speaks , so that might be funny

and there might be another neuron which actually files the dialogue content to be funny right

. And now all of this pass on the information to the next level and this guy would fire

if at least 2 of these 3 inputs are funny right. So; that means, I have some threshold

based on which I decide whether to react or not right, if if it is really funny then only

I laugh it; otherwise I will not laugh right .

So, the neurons in the brain as was obvious in the previous slide are arranged in a hierarchy

and I will take a more realistic example, where we look at the visual cortex. So, is

this is the portion of the brain which is responsible for processing visual information

right. So, as you see here ah you have our retina from where the information starts flowing

, and it goes through various levels right. So, you see, you follow the arrows and you

will see there are several levels, there is one level here, then another here another

here and so on right . So, it is again as I was trying to illustrate in that cartoon

the information is relayed through multiple layers, and then it goes all the way back

to the spinal cord which decides that, in this case I need to move the muscle right.

So, that is what is being decided here right. So, the information flows through a hierarchy

of layers . And in this particular case I am going to focus on these three circled ah

layers which are V 1 V 2 and ah A I T right. So, these actually form a hierarchy and let

us see what this hierarchy does right . So, at layer 1 you detect edges and corners.

So, I am looking at you all, I just see some dots and some shapes, so that is what layer

1 recognizes. I just recognize some edges and some dots and so on .

Now, layer 2 tries to group all of these together and come up with some meaningful feature groups

right. So, it realizes oh these 2 edges actually form the nose, these two dots actually form

the eyes and these 2 edges actually form the mouth right. So, that is ah slightly higher

level of processing that it is doing and then layer 3 further collects all this and leads

to higher level objects right. So, now it is realizing all these things put

together is actually a human face right . So, you add edges and circles or dots , then you

had some feature groups and then the feature groups combine into objects right. So, that

is how this hierarchy processes. So, here is a disclaimer, I understand very

little about how the human brain works right and what you saw is a very oversimplified

explanation of how the brain works right. What I told you is there is an input a layer

of networks which does ah a network which has many layers which does some processing

and then you have an output right; that is the very simplistic view that I gave you . This

is an oversimplified version, but this version suffices for everything that we need for this

course right. This is not a biology or a neural processing course right. So, it is enough

for this course . So, that is where we will end module 1 .

## Module_2 : McCulloch Pitts Neurons and Thresolding Logics

Let us start in module 2.2 which is about McCulloch Pitts Neuron . So, ah as we are

done this during the history lecture way back in 1943 McCulloch and Pitts , they proposed

highly simplified computational model of the neuron , right. So, now let us see what the

motivation is. We know that our brain is capable of very

complex processing , it is capable of taking a lot of inputs from various sources and then,

helpers take various decisions and take various actions , right . Now, what if you want a

computer to do this , right . We want a module which is very similar to how the brain works

or at least how we think the brain works which takes a lot of inputs and then, does some

processing and helps us take a decision , right. So, what they proposed is this model which

will take a lot of inputs and these inputs are all binary , ok. All these inputs that

you see here these inputs are fed to this McCulloch Pitts neuron which is an artificial

neuron and it is divided into two parts, right . So, the first part collects all the input

. So, remember you had these dendrites which were taking all the information from everywhere,

right . So, this just collects all the information and then, the second part sees what this aggregation

is, right . I have collected a lot of information from all the sources . Now, the second function

will decide what this aggregation is and based on that it will take a decision whether to

fire or not , right. So, the output is again boolean . If it is

0 the neuron does not fire . If it is 1, the neuron fires , right . So, let us take a concrete

example, right. So, suppose I am trying to make a decision whether I should watch a movie

or not , right . So, x 1 could be is the genre of the movie thriller . Similarly, there could

be another variable say x n which says is the actor Matt Damon , right . So, these are

all various such factors that I could take is the director Christopher Nolan , the music

given by someone and so on, right. So, all these are probably factors which help me decide

whether I want to watch this movie or not , right and you want this neuron to help us

make that decision , ok. So, now what is happening here is these all

inputs right , they can be either excitatory or inhibitory . So, let me tell you what inhibitory

is first, right . So, you are taking input from a lot of sources . Now, see one of these

sources or one of these inputs is am I ill today ? Am I down with fever right? So, if

that input is on irrespective of who the actor, director or whatever is, I am not going to

watch the movie right because I just cannot leave from my bed , right .

So, these are known as inhibitory inputs irrespective of what else is on in your input features

. If this input is on , your output is always going to be 0. That means, the neuron is never

going to fall a fire, right . So, you could think of it as suppose my my mood is not good

today, I do not feel like getting up or if I injured my leg or anything right, if any

of these conditions is on irrespective of what the other factors are, I am not going

to watch the movie , right. So, that is an inhibitory input and excitatory

input are on the other hand is not something which will cause the neuron to fire on its

own , but it combine with all the other inputs that you have seen could cause the neuron

to fire and how. So, this is how , right. So, these are all the inputs that your neuron

is taking . All I am going to do is I am going to take a sum of these, right . I am going

to take aggregation of all of these . So, what does this count actually give me the

number of inputs which are on , right the number of inputs which are value 1 . That

is all. This aggregate, this is a sum of all the one's in my input, right .

Now, this is what g does. This is a very simple function is taking a sum of my inputs . Now,

the function y takes this as the input. That means, it takes this sum as the input and

if the sum is greater than a certain threshold , then it fires . If the sum is less than

the certain threshold , then it does not fire , right . So, again see what is happening

here is it is same as now if you depend on the actor, director, genre and so on and you

fine, ok. At least two of these three conditions are satisfied. At least I am happy with the

actor and the director even though the genre is not something that I care about .

I will watch the movie, right or you might be a very niche go movie watcher who only

goes to a movie if the actor matches your requirement, the director matches your requirement

and the genre and the music and everything matches your requirement, right . So, you

are threshold. In that case, it should be high . So, this is how it is going to help

you make decisions, ok. Now, again a very simplified model and this is theta is called

the thresholding parameter that is the value which decides whether the neuron is going

to fire or not and this over all thing is known as the thresholding logic , ok . So,

this is what a McCulloch Pitts neuron looks like .

Now, let us implement some boolean functions using this m p neuron . So, from now on I

will just called it m p neuron and we will try to implement some boolean functions using

it , ok . So, now why are we interested in boolean functions? It is because we have only

simplified the way we take decisions, right . We are saying that the way we take decisions

is we take a lot of boolean inputs is actor Matt Damon and genre thriller and so on and

based on that we produce a boolean output , right .

So, an input is all booleans . So, we have x 1 to x n which are all booleans and your

output is also boolean , right. So, that is a boolean function that you are trying to

learn from x to y . Is that clear? You have x just happens to contain n different variables

here, ok and lot of decision problems you could cast in this framework . You can just

imagine right whether to come for lecture today or not . Again is you could cast in

it depending on various boolean ah inputs , right ok .

This is a very concise representation of the McCulloch Pitts neuron . What it says is it

takes a few boolean inputs and it has certain threshold . If the sum of these inputs crosses

this threshold, then the neuron will fire otherwise it will not fire , ok . That is

the simple representation of the m p neuron . Now, suppose I am trying to learn the function

, ok when would the function fire ? All the inputs are on . So, what should be

the value of the threshold in this case ? 3

3. Everyone agrees , right ok . What about other function ?

1 1 ok . Let us see a few more this function

. So, let me tell you what this function is, right . So, you see this circle here, right

. So, that means that this input is an inhibitory input . If that is on , then the neuron is

not going to fire , right . That is how I am representing it . So, now tell me what

should the threshold for this be . It is not so hard .

See if x 2 is on, it is not going to fire , right. So, you have four rows; 0 0 0 1 1

0 1 1 . So, two of those are ruled out and it is not going to fire . Now, out of the

remaining two, when do you wanted to fire? 1

So, what should be the threshold? 1

1 everyone gets that . Anyone who does not get that? Ok good . Now, what about this function

0 or 3. 3 is not even a valid option , ok ah 0 . Everyone agrees to that fine and what

about this? 0, ok. So, you get this ? So, now if you have a certain number of input

variables and the function that you are trying to model the decision that you are trying

to make is a boolean function , then you could represent using these MP neurons whether all

boolean functions can be represented in this way or not that is still not clear . I am

just showed you some good examples. We will come to the bad examples later on , ok. Here

is the question, right . So, can any boolean function be represented

using a McCulloch Pitts neuron? So, before answering this question, we will see a bit

of a geometric interpretation of what MP neuron is actually trying to do , ok

So, let us take OR function where you have two inputs x 1 and x 2 and this neuron is

going to fire . If x 1 plus x 2 is greater than equal to 1, right. That is clear . That

is how the definition is , ok . Now, if you look at this right x 1 plus x 2 greater than

equal to 1 , ok . Now, let us ignore the greater than part first . So, we will just talk about

x 1 plus x 2 equal to 1 . What is this equation of a ?

Line Line everyone gets that , ok . Now, in this

case since we are dealing with boolean inputs and we have two access x 1 and x 2 , how many

input points can we have ? 4, right 0 0 0 1 1 0 1 1 , right.

So, you could have these four points . So, just note that this is an x 1 and x 2 axis

, but only four inputs are valid here , right. This is not a real numbered access, ok. This

is only boolean inputs possible here , ok. Now, what is the line? X 1 plus x 2 equal

to 1 tell you which line is that . So, one which passes through 1, 0 here and

0, 1 here , right . So, this is that line ok. Now, what do we want that for all those

inputs for which the output is actually 1, they should lie on the line or on the positive

side on the line , right and all those inputs for which the output is 0 , they should lie

on the other side of the line . Is that happening? So, what is actually MP in unit actually learning

ah linear decision boundary, right . It just what it is doing in effect is actually it

is dividing the input points into two halves such that all the points lying on that line

right are, sorry all the points for which the input should be 0 low below this line

and all the points for which the output should be 1 right . Sorry in both cases, it should

have been output . So, let me just repeat it ; All the points for which the output is

0 low below this line and all the points for which the output is 1 either lie on this line

or above the line , ok. Is that fine? So, let us conveyance ourselves about this . Even

it is not already clear from the equation. For how many of you it is already cleared

from the equation that this is exactly what it does for a large number of period , but

still we will just do a few examples and move ahead .

Now, for the function what is the decision boundary? It is x 1 plus x 2; No, that is

the decision decision boundary. Equal to 2 , right ok . So, again I have these four points

. Only these four points are possible . Now, where is my decision line ?

Passing through that 1, 1 and intercepting this somewhere around 2, 0 and this around

0, 2 right. So, that is the line which I am interested in , ok. Now, again do you see

ah that our condition is satisfied that all the inputs for which we want the output to

be 1 are on or above the line and all the inputs for for which we want the output to

be 0 or below the line , right . Now, what about this function ? What is the threshold?

Zero. So, what would the line be? X 1 plus x 2 equal to 0 which passes through the origin,

right and again all the points are either on or above the line , right ; So, this part

we are going to call as a positive half space and this we are going to call as the negative

half space , ok . So far everything is fine ok .

Now, what if we have more than two inputs ? In a two dimensional case, when we just

had x 1 and x 2 we are trying to find a separating line in the three dimension case . What will

we do? Play

Play ok good and in the higher dimensions ?

Hyper Plane Hyper plane very good, ok . So, this is now

your three dimensional case, right. Again there are three axis here , but not all points

are possible . How many points are possible? 8 points and which is the function that we

are trying to implement . OR

So, for these eight out of these eight points , for how many is the output 1?

7 7 and for 1, it is 0 . So, what is the kind

of plane that we are looking at? We are looking for a plane such that 7 points lie on or above

it and 1 point lies below it and which is that point .

0 Zero, zero , 0 , right . So, now what is the

equation of that hyper plane? X 1 plus x 2 plus x 3 is equal to 1 , ok good . You see

this . So, you see that all the seven points are visible , but the points 0, 0 is not visible

because it is on the other side of the plane , right . So, this is doable in three dimensions

also and again in higher dimensions also, right we could find in hyper plane ok .

So, the story so far is that ah single McCulloch Pitts neuron can be used to represent boolean

functions which are linearly separable . So, a linearly separable function is such that

there exists a line such that for that function whichever points produce an output of 1 lie

on one side of the line and whichever points produce an output 0 lie on the other side

of the line . This is a very informal definition. Later on we will try to make it more formal

, ok . So, is that fine ok? So, this is where we will end the previous

module.

## Module_3 : Perceptron

Now, let us go to the next module ah which is Perceptron , ok . So, so far the story

has been about boolean input, but are all problems that we deal with, we are only dealing

with ? Do we always only deal with boolean inputs ? So, ah yeah. So, what we spoke about

is boolean functions, right . Now, consider this example.

This worked fine for a movie example where we had these as actor so much and his director

and so on , but now consider the example where you are trying to decide . You are in oil

mining company and you are trying to decide whether you should mine or drill at a particular

station or not, right ; Now, this could depend on various factors like what is the pressure

on the surface, on the ocean surface at that point , what is the salinity of the water

at that point, what is the aquatic marina aquatic life at that point and so on, right.

So, these are not really boolean function , right. The salinity is a real number, density

would be a real number, pressure would be a real number and so on, right and this is

a very valid ah decision problem, right. Companies would be interested in doing this, right.

So, in such cases our inputs are going to be real , but so far may call up its neuron

only deals with boolean inputs , right. So, we still need to ah take care of that limitation

. Now, how did we decide the threshold in all

these cases ? I just asked you, you computed it and you told me right , but that is not

going to work out. I mean it does not scale to larger problems where you have many more

dimensions and the inputs are not Boolean and so on , right. So, we need a way of learning

this threshold , ok . Now, again returning to the movie example

. Maybe for me the actor is the only thing that matters and all the other inputs are

not so important . Then, what do I need actually ? I need some way of weighing these inputs

, right. I should be able to say that this input is more important than the others , right.

Now, I am treating all of them equal. I am just taking a simple sum . If that sum causes

a threshold, I am fine otherwise I am not fine right, but maybe I want to raise the

weight for some of these inputs or lower the weight for some of these inputs, right . So,

whether it is raining outside or not maybe does not matter. I have a car, I could go

or I could wear a jacket or an umbrella or something, right. So, that input is probably

not so important , right. What about functions which are not linearly

separable , right? We have just been dealing with the goody goody stuff which is all linearly

separable , but we will see that even in the restricted Boolean case , there could be some

functions which are not linearly separable and if that is the case , how do we deal with

it , right. So, these are some questions that we need to answer , ok .

So, first we will start with perceptron which tries to fix some of these things and then,

we will move forward from them . So, as we had discussed in the history ah ah lecture

that this was proposed in 1958 by Frank Rosenblatt and this is what the perceptron looks like

. Do you see any difference with the McCulloch Pitts neuron weights , right? You have a weight

associated with each of the input otherwise everything seems, ok right .

So, this is a more general computational model than the McCulloch Pitts neuron . The other

interesting thing is that ah of course we have introduced these weights and you also

have a mechanism for learning these weights . So, remember in the earlier case , our only

parameter was theta which we are kind of hand setting right , but now with the perceptron,

we will have a learning algorithm which will not just help us learn theta , but also these

weights for the inputs , right. How do I know that actor is what matters or

director is what matters ? Given a lot of past viewing experience, right past given

a lot of data about the movies which I have watched in the past , how do I know which

are the weights to assign this , right. So, we will see an algorithm which will help us

do that , right and the inputs are no longer limited to be boolean values . They can be

real values also , right . So, that is the classical perceptron, but what I am talking

about here and the rest of the lecture is the refined version which was proposed by

Minsky and Papert which is known as the perceptron model, right. So, when I say perceptron, I

am referring to this model. So, this diagram also corresponds to that, ok .

So, now let us see what the perceptron does , ok . This is how it operates . It will give

an output of 1 if the weighted sum of the inputs is greater than a threshold , right

. So, remember that in the m p neuron we did not have these weights , but now we have these

weighted sum of the inputs and the output is going to be 0 if this weighted sum is less

than threshold , right . It is not very different from the m p neuron , right .

Now, I am just going to do some trickery and try to get it to a better ah notation or a

better form , right . So, is this ok ? I have just taken the theta on this side , ok . Now

is this ok? Notice this here the indices were 1 to n . Now, I have made it 0 to n and the

theta is suddenly disappeared . So, what has happened .

w 0 is . Minus theta , right and x 0 is 1 . Does anyone

not get this right. If I just start it from 1 to n, then it would be summation i equal

to 1 to n w i x i plus w 0 x 0, but I am just saying w 0 is equal to minus theta and x 0

is equal to 1 which exactly gives me back this, right . So, very simple x 0 equal to

1 and w 0 is equal to minus theta . So, in effect what I am assuming is that instead

of having this threshold as a separate quantity , I just think that that is one of my inputs

which is always on and the weight of that input is minus theta . So, now the job of

all these other inputs and their weights is to make sure that their sum is greater than

this input which we have , right. Does not make sense , ok fine. So, this is how this

is the more accepted convention for writing the perceptron equation , right. So, it fires

when this summation is greater than equal to 0, otherwise it does not fire , ok.

Now, let me ask a few questions, right . So, why are we trying to implement Boolean functions

. I have already answered this, but I will keep repeating this question , so that it

ah really gets drill in . Why do we need weights ? Again we briefly touched upon that and why

is w naught which is negative of theta often called the bias , ok ?

So, again let us return back to the task of predicting whether you would like to watch

a movie or not and suppose we base our decisions on three simple inputs ; actor genre and director

, right . Now, based on our past viewing experience , we may give a high weight to Nolan as compared

to the other inputs . So, what does that mean . It means that as long as the director is

Christopher Nolan, I am going to watch this movie irrespective of who the actor is or

what the genre of the movie, right. So, that is exactly what we want and that is the reason

why we want these weights , ok . Now, w 0 is often called the bias as it represents

the prior . So, now let me ask a very simple question . Suppose you are a movie buff . What

would theta be ? 0 right. I mean you will watch any movie irrespective of who the actor,

director and genre , right. Now, suppose you are a very niche movie watcher who only watches

those movies which are ah which the genre is thriller , the director was Christopher

Nolan and the actor was Damon, then what would your threshold be ? 3 right.

High in this case , ok . I always ask this question do you know of any such movie always

takes a while . Interstellar ok ah . So, the weights and the bias will depend on the data

which in this case is the viewer history, right . So, that is the whole setup, right.

That is why you want these weights and that is why you want these biases and that is why

we want to learn them, ok . Now, before we see whether or how we can learn

these weights and biases , one question that we need to ask is what kind of functions can

be implemented using the perceptron and are these function any different from the McCulloch

Pitts neuron ? So, before I go to the next slide, any guesses ok ? I am hearing some

interesting answers which are at least partly correct .

So, this is what a McCulloch Pitts neuron looks like and this is what a perceptron looks

like . The only difference is this red part which is weights which have count on it , right

. So, it is again clear that what the perceptron also does is, it divides the input space into

two halves where all the points for which the output has to be one would lie on one

side of this plane and all the points where which the output should be 0 would lie on

the other side of this plane, right. So, it is not doing anything different from what

the perceptron was doing . So, then what is the difference ?

You have these weights and you have a mechanism for learning these weights as well as a threshold

. We are not going to hand code them , ok . So, we will first revisit some boolean functions

and then, see the perceptron learning algorithm , ok.

So, now let us see what the first condition does, right. This condition if I actually

expand it out , then this is what it turns out to be, right and what is that condition

telling me actually w naught should be less than 0 , clear . So, now based on these, what

do you have here? Actually what is this ? A system of linear inequalities , right and

you know you could solve this , right. You have algorithms for solving this not always,

but you could find some solution , right and one possible solution which I have given you

her is w 0 is equal to minus 1 w 1 equal to 1.1 and w 2 equal to 1.1. So, just let us

just draw that line , ok. So, what is the line ? It is 1.1 x 1 plus 1.1 x 2 is equal

to 1 , right. That is the line and this is the line and you see it satisfies the conditions

that I have is this the only solution possible . No, right . I could have this also as a

valid line . If I could draw properly , right all of these

are valid solutions, right . So, it is result in different w 1 w naught and w 0s , ok. So,

all of these are possible solutions . In fact, I have been telling you that you had to set

the threshold by hand for the McCulloch Pitts neuron , but that is not true because you

could have written similar equations there and then, decided what the value of theta

should be, right . So, you could try this out for the McCulloch

Pitts neuron . Also, you will get a similar set of conditions or I mean similar set of

inequalities and you can just say what is the value of theta that you could set to solve

that right, ok . So, that ends that module .

## Module_4 : Error and Error Surface

Before we go to the next section which is on learning , I just want to introduce the

concept of errors and error surfaces and tell you how it relates to these multiple solutions

that we were talking about . So, for simplicity what we will do is, we

will just set the threshold to minus ah or minus w to 1 which is setting the threshold

to minus 1 and now, I will try different values of w 1 and w 2 ok. So, I was saying that there

are multiple values of w 1 and w 2 possible and these are all real numbers, right. We

are not constrained by having them as boolean values, ok . So, now this is one solution

which I tried . I tried setting w 1 to minus 1 and w 2 to minus 1 . What is wrong with

this line ? Does it lead to any errors ? How many ?

Just one error, right . So, this makes an error of 1 out of the 4 inputs . Now, let

me just try some other values of w 1 and w 2 , ok this line . Again one error , ok. What

about this line? Not 4, 3 because 0, 0 is anyways on this side of a line, ok .

So, now given this now tell me that my question is to find these w . So, I would want to find

w 1 w 2 and so on. Given this discussion on errors , can you tell me a condition that

I am looking for . I want to find w 1 w 2 or up to w n such that errors are minimized

and in the best case errors are 0 , right. So, that is what I want, right. So, this just

I want to make a case that these search for ws is driven by certain objective and this

objective is to minimize the error , ok fine .

So, now since we are doing this , let us plot the error surface corresponding to different

values of w naught w 1 and w 2 . Once again for simpler analysis we will just keep w naught

to be fixed at minus 1 and now what I have. So, just do not read this bullet as of now

, even this one . So, I have this w 2 here . So, that is my one axis and I have w 1 here

which is my another axis , ok . Now, what I am going to do is I am going to try different

values of w 1 and w 2 . So, this axis can go from minus infinity to plus infinity . Of

course, for showing the sake of showing, here I have just had it from minus 4 to 4 , ok

. So, now what I am going to do is I am searching

for some values of ws w 1 and w 2. So, that my error is 0 and let us do a brute force

and I will just try every value between minus 4 to 4 , ok. In fact, one of the solutions

which I proposed actually was this ah 1.1, 1.1 right . That is the line which we saw

on the previous slide and which led to zero errors and that is the dark blue surface here

. So, how did I compute this error? Actually I just substituted minus , sorry 1.1, 1.1

here and then, I put in all the four values combinations for x1, x 2 , right and I realized

that I am able to satisfy all of them . So, I do not get any error , right . Now, instead

of that if I had put something different ? So, let me just go back to the previous slide

which was see minus 1, minus 1 right which is I think ah yeah somewhere around here right

minus 1, minus 1 I guess . So, for that I am in this light blue region where the error

was once . I make errors for one of the inputs , right. So, it is a very brute force way

of finding this and this is not going to work, right because we have lots of inputs to check

, but this is just to give you an intuition that we are looking at errors and we are trying

to find a value of w 1, w 2 which minimize this error, ok . So, that is the idea behind

errors and error surfaces.

## Module_5 : Perceptron Learning Algorithms

We will now go to the next module obviously Perceptron Learning Algorithm .

We now see a more ah principled approach of learning these weights and threshold , but

before that we will just again revisit our movie example and make it slightly more complicated

. Now, here what the situation is that we are

given a list of movies and a class associated with each movie indicating whether we like

the movie or not , right. So, now we have given some data of the past m movies that

we have seen and whether we like this movie or not and now instead of these three variables

, we have these n different variables based on which we are making decisions and notice

that some of these variables are real , right. They are not boolean anymore , right. The

rating could be any real number between 0 to 1 , ok and now based on this data what

do we want is the perceptron to do actually. So, I have given you some data . These factors

I have also given you the label 1 and 0. So, if the perceptron if I tell you ok my perceptron

has now learnt properly , what would you expect it to do ? Perfect match, right . So, whenever

I feed it, one of these movies it should give me the same label as was there in my data

, right and again there are some movies for which I have a label 1 which are positive

and some movies which I have a label 0 . So, I am once again looking to separate the positives

from the negatives , right. So, it should adjust the weights in such a way that I should

be able to separate, right. So, that is the learning problem that we are interested in

, ok. So, now with that I will give you the algorithm

, ok. This is the Perceptron Learning Algorithm . We have certain positive inputs which had

the label 1, we have certain negative inputs which had the label 0 and now, I do not know

what the weights are and I have no prior knowledge of what the weights are going to be . I need

to learn them from the data . So, what I am going to do is, I am just going to initialize

these weights randomly as I am also going to pick up some random values for this. So,

this should be small n . So, this should be small n and now, here is the algorithm while

not convergence do something . So, before I tell you what to do , can you tell me what

is meant by convergence? When will you say that it has converged?

When it is not making anymore errors on the training data , right, ok or its predictions

are not changing on the training data . So, that is the definition of convergence , ok.

Now, here is the algorithm . I pick up a random from point from my data which could either

be positive or negative , right. So, it comes from the union of positive negative . Basically

all the data that I have I pick up a random point from there .

If the point is positive, right and this is the condition which happens what does this

tell me ? If the point was positive , what did I actually want greater than 0 , but the

condition is less than 0. That means, I have made an error . So, I have made an error , then

I will just add x to w I see a lot of thoughtful nodding and I hope you are understanding what

is happening . Let us see . So, what is w actually? A dimensional ah .

N dimension N dimension n plus 1, right because w naught

is also inside there . So, actually there should be w naught also here, right and what

is x again n dimensional, right and that is why this addition is valid . So, let us understand

that w and x both are n dimensional , ok. Now, let us look at the other condition . Can

you guess what the other if condition is if x belongs to n and .

Summation Summation is greater than equal to 0, then?

So, that means you have completely understood how this algorithm works . Well, that is right

. So, now consider two vectors w and x. So, remember what we are trying to prove is or

get an intuition. Not prove, actually get an intuition for why this works , ok .

So, we will consider two vectors w and x and this is what my vectors look like very similar

to the case that we are considering w 0 to w n and 1 to n . So, this again x naught is

just 1 , right. Now, this condition that I have been talking

about is nothing, but the dot product . How many of you have gone through the prerequisites

for today's lecture ? Ok good . So, it is just a dot product , ok. Now, we can just

read write the perceptron rule as this instead of the dot product. I mean instead of using

that summation thing, we can just say that it is a dot product, ok .

Now, we are interested in finding the line w transpose x equal to 0. So, that is our

decision boundary, right which divides the input into two halves , ok. Now, every point

on this line satisfies the equation w transpose x equal to 0. What does that mean actually?

Yeah. So, just a simple example is that if I have the line x 1 plus x 2 equal to 0, then

all the points which lie on the line satisfy this equation , right. So, you could have

1 minus 1, 2 minus 2 and so on , but 2, 2 cannot be a point on this line . At every

point lying on this line satisfies this equation . So, every point lying on this line actually

satisfies the equation w transpose x equal to 0.

So, can you tell me what is the angle between w and any point on this line? How many say

how many of you say perpendicular? Why? Dot product is 0, right. So, if the dot product

is 0, they are orthogonal right. So, that means if I take this line , then my vector

w is orthogonal to this . It is orthogonal to this point or this point to this point

to every point on the line which is just the same as saying that the vector is perpendicular

to the line itself , right. As simple as that. So, the angle is 90 degrees because the dot

product gives you the cos alpha and that is 0, right and since it is perpendicular as

I said to every point of the line it is just perpendicular to the line itself, right .

So, this is what the geometric interpretation looks like. This is our decision boundary

w transpose x and the vector w is actually orthogonal to this line and that is exactly

the intuition that we have built so far , ok. Now, let us consider some points which are

supposed to lie in the positive half space of this line , right. That means, these are

the points for which the output is actually 1, ok. Now, can you tell me what is the angle

between any of these points and w or you guys are actually trying to tell me the angle we

have got some measuring stuff , no. So, I will give you three options i.e. equal to

90, greater than 90 and less than 90. Less than 90

Less than 90 it is obvious from the figure , right. Now, if I take ah any point which

lies in the negative half space, what is the angle going to be between them? It is greater

than 90, right. Again obvious and it also follows from the fact that cos alpha is w

transpose x by something and we know that for the ah positive points w transpose x is

greater than equal to 0, right. That means, cos alpha would be greater than equal to 0,

that means the angle alpha would be less than 90 degrees and for the negative points w transpose

x is actually less than 0. That means, cos alpha would be less than 0, that means alpha

would be greater than 90 degrees, right. So, it actually follows from the formula itself

, but it is also clear from the figure. So, keeping this picture in mind let us revisit

the algorithm, ok. So, this is the algorithm , ok.

Now, let us look at the first condition which was this. Now, if x belongs to p and w transpose

x is less than 0, then means that the angle between x and the current w is actually greater

than 90 degrees , but what do we want it to be? Less than 90 degrees and our solution

to do this is , but we still do not know why this works? Now, anyone knows why this works?

So, let us see why this works, ok . So, what is the new cos alpha going to be? It is going

to be proportional to this, right. It is going to be proportional to this. I will just substitute

what w nu is, fine. That means, if cos alpha nu is going to be greater than cos alpha,

what is alpha nu going to be? It will be less than and that is exactly what we wanted. This

angle was actually greater than 90 degrees . So, you want to slowly move it such that

it becomes less than 90 degrees. It is not going to get solved in one iteration and that

is why till convergence . So, we will keep doing this. I will keep picking xs again and

again till it reaches convergence. That means, till we are satisfied with that condition

, right. Let us look at the other condition x belongs

to n and w transpose x was greater than equal to 0, then it means that the angle alpha is

actually less than 90 degrees and we want it to be the opposite, ok. I will just quickly

skim over this w minus this x, right. Ok I forgot to mention that this is actually a

positive quantity, right. I mean that is why that result holds, ok. That means, cos alpha

nu is going to be less than cos alpha and this slight bit of mathematical in correctness,

I am doing here, but that does not affect the final result .

So, I will just gloss over that and you can go home and figure it out , but still it does

not take away from the final intuition and interpretation, right. So, now the new cos

alpha is going to be less than the original cos alpha. That means, the angle is going

to be greater and that exactly what we wanted, ok. So, we will now see this algorithm in

action for a toy data set. So, this is the toy data set we have and we

have initialized w to a random value and that turns out to be this, right. I just picked

up some random value for w and ended up with this particular configuration for w, ok .

Now, we observe that currently w transpose x is less than 0 for all the positive points

and it is actually greater than equal to 0 for all the negative points. If you do not

understand w transpose x, it is just that the all the positive angle points actually

have a greater than 90 degree angle and all the negative points actually have a less than

90 degree angle. So, this is exactly opposite of the situation that we want and now from

here on, we want to actually run the perceptron algorithm, right and try to fix this w. How

does it work? Remember we randomly pick a point, ok. So, say we pick the point p 1,

do we need to apply a correction? Yes

Yes. Why, because it is a positive point and the condition is violated, right. So, now

we add w equal to w plus x and we get this new w. So, notice that we have a new w, ok.

We again repeat this, we again pick a new point and this time we have picked p 2. Do

we need a correction? Yes.

At least from the figure it looks like the angle is greater than 90, right. So, we will

again do a correction. We will add w is equal to w plus p, right. This x is actually, sorry

p 2 and this is where we end up, ok. Now, again we pick a point randomly n 1. Do

we need a correction? So, this is what our w is. This line here and n 1, right. So, we

need a correction, ok. Now, what is the correction going to be? It will be minus and then, the

w changes, ok. Now, we pick another point n 3. Do we need

a correction? No at least on the figure it seems like the angle is greater than 90 and

we continue this, right. For n 2, we do not need a correction. Now,

for p 3 again we do not need a correction .

The angle looks less than 90. Sorry actually it is we need a correction. The angle is slightly

greater than 90 and this is our correction, ok and now we keep cycling.

Now, as I keep cycling over the points, I realize that I no longer need any correction

. It should be obvious from the figure that

for this particular value of w, now all my positive points are making an angle less than

90 and all my negative points are actually making an angle greater than 90. That means,

by definition now my algorithm has converged, right . So, I can just stop it. So, I can

just make one pass over the data. If nothing changes, I will just say it has converged,

ok. Now, does anyone see a problem with this? Never converge

It will never converge in some cases. So, can someone tell me why? Yeah yeah we are

considering only cases where the data is linearly separable, right. That we already assumed

. So, what you are trying to tell me is that you are going over these points cyclically.

So, let me just rephrase and put words in your mouth that what you are trying to tell

me actually is that I take a point, I adjust w , but now for the next point I maybe go

back to the same w because that point asked me to move it again and I keep doing this

again and again and basically, end up nowhere, right. That is why this will never converge.

That is exactly what you are trying to tell me, right. Now, that is exactly what I am

forcing you to tell me . So, that is not the case , right. This algorithm will converge.

## Module_6 : Proof of Convergence of Perceptron Learning Algorithms

In this module ah we will talk about the proof

of convergence for the perceptron or the learning algorithm that we saw in the previous module

ah . So, we have some faith and intuition that

it actually works , we just need to formally prove it that it actually converges right

. So, that is what we are going to do in this ah module .

So, before that a very ah few very simple definitions ah . So, if you have two sets

of points P and N in an n dimensional space and we call say that these points are absolutely

linearly separable, if there exists some n plus 1 real numbers which has w 0 to w n ; such

that every point which belongs to P right, P is the case where the output is 1 ah, .

Then these set of weights satisfy this condition right and every point which lies in the negative

set the set of weights satisfy this condition right . So, nothing very different from what

has we have been saying. So, far it is just formally defining it right .

Now, our proposition is that, if the set P and N are finite and there is a fixed number

of points in that which was the case in the toy example that we were doing and which will

be the case in most examples that we do and linearly separable right . The perceptron

learning algorithm updates the weight vector ok. Before I go there right ok, let me not

give you the definition and let me ask you the definition right .

So, now I have given this definition, the first definition and given this part of the

proposition . Can you tell me what do I need to prove if I need to prove that the algorithm

converges ah, ok that is one way of looking at it , but what was happening in that ah

wrong argument which was I was making that it continuously kept toggling right . That

means, I am not making a finite number of updates right I have to keep changing again

and again and this process continues in a loop right .

So, that is how I am going to define convergence that the perceptron learning algorithm updates

a weight vector of finite number of times right, it only needs to update it finite number

of times and it will reach a configuration such that now it is able to separate the P

from the N ok; that is what the proof of convergence means right.

So, ah in other words if you are going to pick up these vectors randomly from the set

P and N cyclically, as we were doing in the toy example , then a weight vector w t is

found after a finite number of steps which will separate these two steps ah, these two

sets right . So, that is what we are trying to prove. So, that is the definition of converge,

does it make sense? Right ok . So, proof is on the next slide and ah .

It is , it is going to take me around 5 to 10 minutes to prove it . So, just ah stay

focused all right. So, here is a few set up right . So, I am going to, before I go to

the actual proof I am going to make a set up so that it becomes easier for us to prove

it right . So, the first thing that I am going to say is that, if there is a point which

belongs in negative set then the negative of that point belongs in the positive set

ok and that is very clear, because if the point belongs in the negative set then w transpose

x is less than 0 . But then w transpose minus x would be greater

than equal to 0 right . So, I take the negative of the point, I can just put it in the positive

set . So, instead of considering these two different things P and N I am just going to

consider one P prime , which is an union of P and all the N points negative ok, will the

set up clear . If this is a setup then what is the condition that I need to ensure for

every point in P dash . .

W transpose p should be greater than equal to 0 right. So, I do not care about the negative

case, I have just made everything positive now and it is, I am not done anything wrong

here, it is just a simple trick ok . And now this is how the algorithm will look in this

setup , these are the inputs with label one inputs with label 0 N minus contains a negation

of all the points in N and P prime is a union of these . Now again I start by initializing

w randomly , while convergence I will do something , I will pick a random P from P prime . Now

what is the if condition . Less than 0 .

. Do I need the other if condition .

No. No right, because everything is now positive

ok and the other small thing that I am going to do is, I am going to normalize P ok . So,

that again does not mean, because we are talking in terms of angles and I am not changing the

direction of the vector , I am just shrinking it right. So, I am just or maybe scaling it,

also I am just ah making it unit norm . So, that does not change anything right. So, it

is still everything still holds ok . And in particular you can see here right.

So, if this condition was true, this condition will also be true ok . So, . So, far just

I am done some simple tricks to make things easier for me later on, so now P has been

normalized . Now remember that this data is linearly separable ; that is what we started

the proposition . If P and N are linearly separable then the perceptron learning algorithm

will converge right . So, now, if P and N are linearly separable, irrespective of whether

we have the perceptron learning algorithm or not what do we know .

. That there exists ah .

Line . There exists a w star which is the solution

vector right , there exists at least one w star which is the solution vector right; such

that it will separate the P points from the N points . So, this vector which we do not

know, but we just know that it exists , so you can refer to it . So, we will call this

w star ok fine . Now we start the proof . So, w star is some optimal solution which

we know exists . But we do not know what it is right . Now suppose you had a time step

t . So, remember that this algorithm is going on while convergence . So, you have time step

1 2 3 you are picking up points . So, we are at a time step t , at which you pick up a

random point p i and you find that the condition is actually violated . So, this should actually

be less than 0 right , if I know the condition is violated . So, now, what will you have

to do? . .

W is equal to . .

W 1 . So, I will just call it the new w w t plus 1 is equal to the old w plus p i ok

. Now what I am going to do is I am going to consider the angle beta between w star

and w t plus 1 . I do not know what w star is, but we can still assume it exists and

make some ah calculations based on that right . So, what is the angle between w star and

w t plus 1 , its beta and what is the cost of that angle this

. And remember that we do not have w star here,

because we had assumed that it is the normalized vector right. So, we do not need that bit

ok ah, this is actually equal to 1 ok . So, now, if I just take the numerator , w star

in ah dot product w t plus 1 . Now I am going to expand w t s w t plus p i fair ; that is

exactly what I did on the previous ah step , is it ok fine .

Now, now what is p i actually, it is. So, what you had is you had these P 1 P 2 P 3

. My hand writing is really horrible and up to P n right right. So, I have just picked

one of these p i's ok . Now what I am going to define is. Now suppose this is my, these

are my p i's right. So, these are all the vectors that I have . Now suppose I have this

w star , suppose this was the w star that I am interested .

Now, for each of these I could compute w star P 1 w star P 2 and so on up to w star P n

right and I could sort them . Now what I am doing is that for whichever of these points

w star p i is the minimum ok, I am going to call that value as delta. Suppose w star P

1 is the smallest quantity out of w star P 1 w star P 2 w star P n right, and I am calling

that quantity delta ok . So, I have this quantity here and my delta

is the minimum of all the possible values that it can take. It can make w star P 1 P

2 up to P n , so delta is the minimum quantity . So, here I have an equality ok . Now, are

you ok with this . This is the minimum quantity right . So, any p i that I put in here it

is always going to be greater than or worst case equal to delta fair ok, fine .

Now, again this w 2 itself I could write it as w t minus 1 plus p j , because that also

would have come up from some update in the previous step ok . Again this is there which

I could call it as delta and still retain the greater than equal to here, ok fine. So,

let us see where are we heading with this right .

Now, notice that we do not make a correction at every time step, when I was running that

toy algorithm I was not making a correction at every time step . We were only making a

correction at those time steps for which the condition was violated . So, now, if I am

at th time step , maybe I have made only k which is less than or equal to t corrections.

At max I would have made t corrections, but it could have been less than that also ok

. So, now every time we make a correction we

are adding a value delta to this right. So, at the time step t what would happen , I had

started off from w naught I have reached time safety and I have made a case that , I have

not made t updates I have made k less than equal to t updates right. So, how many deltas

would get added? . K delta.

K delta . So, I could say that with respect to w naught where I had started from, this

is what this quantity is, ok is that fine , anyone has a problem with this ok.

So,. So, far what are we shown right, we started with this , this condition was true again

not less than equal to and hence we made the correction and this was the point that we

picked up at the t th step and thence we made that correction .

And we also showed that the numerator is actually greater than equal to this quantity right,

we showed it by induction fine . Now let us look at the denominator and particularly let

us look at the denominator squared ok , is a step ok right .

This is actually w t plus 1 dot product w t plus 1 , but w t plus 1 can be written as

w t plus p i , is this ok . This bracket needs to disappear right, is that ok fine. Now what

is ah , what is this quantity . .

Ah no . .

That's less than equal to 0 . So, now, can you guess what is the next thing that I am

going to write right . .

That's correct , yeah it is a negative quantity yeah yeah. So, that is going to be less than

equal to this yeah ok yeah . So, that is fine and what about ah p i square or this term

. .

Ah . .

Ah Because this is less than right that is why .

Yeah Yeah correct ok is this fine ok. Now what

is p i square . 1 .

One ok . Now can you guess what I am going to do by induction .

K . K ok ; that is ok ah . So, what is w t square

again right . Just this w t plus 1 square was w t square plus 1 , w t square is going

to be w t minus 1 square plus 1 right and how many such ones will get added k of those

right , starting from w naught ok . So, what have we shown, the numerator is greater

than equal to this , the denominator is less than this ok . Now if I put them together

I actually get that cos beta is going to be greater than equal to the numerator over the

denominator ok . Now what is this quantity proportional to k, k square, k cube square

root of k, k by 2 . Square root of k.

Square root of k right , you have, I mean roughly speaking you have a k here , you have

a square root of k here . So, I could roughly speaking say that it is proportional to square

root of k . So, as k grows what will happen to cos beta , it will grow and that is fine

right, it can keep growing . .

Only until one right . So, cos beta is going to be proportional to k . What is k? The number

of updates that you make . now if I were to take that degenerate case which you guys were

hinting at , where that it will keep changing again and again , what will happen to k? It

will keep going to infinity can that happen .

No. No, because cos beta will blow up right and

that is not allowed . So, k has to be finite , so that cos beta stays within its limits

right . Hence are we done . How many if you think we are done , how many if you are satisfy

that we are done , it is not a trick question that we are done . Please we are done ok .

So, yeah . So, this says that we can only have a finite number of such k updates that

we make and after that the algorithm will converge , is that ok. So, we have a proof

of convergence ok . Now coming back to our questions this is where we had started at

one point , what about non billion inputs , so perceptron allows that right. We took

I M D B rating and critics rating as an input . Do we always need to hand code the threshold

. No.

No , in our perceptron learning algorithm are all inputs equal , no we now assign weights

to input . What about functions which are not linearly separable? We still do not know

right. So, that is where we are headed now ok , not possible with a single perceptron

, but we will see how to handle this ok. So, far the story is clear to everyone ok.

So, we will end this module here .

## Module_7 : Linearly Seprable Boolean Function

So, in this module, we look at linearly separable boolean functions again and we will try to

make some more statements about them, ok.

So, what do we have do?

So, the guiding question that we have is what do we do about functions which are not linearly

separable and let us see one such very simple function.

Can you guess what function I am going to talk about?

All of you are paying attention in the first lecture, good right.

So, here is the XOR function.

Now, these are the set of inequalities that result from XOR function.

I hope yeah right.

Now, let us see the first condition implies that w naught should be less than 0, second

condition implies this, third condition implies this, fourth condition implies this.

Just looking at this can you tell me, can you find a configuration for w naught w 1

w 2, such that these inequalities can be satisfied together.

No, right because 2 and 3 want it to be greater than minus 1 minus w naught and when you take

an addition of that, it has to be less than minus 1.

So, that is not going to operate.

So, you see a contradiction.

So, this is a simple boolean function which the perceptron cannot handle because it is

not linearly separable.

It is not linearly separable.

There does not exist a line.

If there does not exist a line, you cannot find the line, right.

In fact, you can look at it visually, right.

So, these are the red points for which the output should be 0 or 1 and the blue points

are the points for which the output should be 0.

If we need to change this, I think we were using blue as positive and red as negative

and you cannot just draw a line.

There is no way you can draw a line such that the blue points lie on one side and the red

points lie on the other side, right.

So, it is a simple two input function, right.

So, it is not that I have taken a very contrived example, ok.

Most real world data is not linearly separable and it always contain some outliers, right.

So, here maybe you have some data where you are trying to say that people which live in

this part of the world belong to a certain or maybe people who live or work here have

a certain qualification, people who work in this company may have a certain different

qualification, right and there might be some outliers, right.

It is not that is always going be very clean.

So, now what do I mean, ok and it is not necessary that the points will only be outliers.

In fact, there could be a clear case where there are no outliers, but still you cannot

find a line such that you separate the positive from the negative.

Can you think of such an example?

Good right.

This is clear data.

There is no outliers here as well.

I mean it is just saying that everyone who lies within this boundary has a certain characteristic

and outside that boundary people have a different characteristic, right and there is no outlier

here, but you cannot separate this data with a line.

So, all functions that you deal with will not go or are not going to be linearly separable.

So, we have to work around those, right and while a single perceptron cannot deal with

this, we will show that a network of perceptrons can indeed deal with such data.

So, that is where we are headed, ok.

So, before going there we will discuss some more boolean functions in more detail and

I will try to see what kind of non-linearly separable boolean functions are there, right.

So, first of all how many boolean functions can you design from two inputs?

How many can you design?

16 looks like a good number from 3 inputs 256.

How many if you understand this?

Ok let us see.

So, let us begin with some easy ones that you already know, right.

So, these are two inputs x 1 x 2.

What is this function always off.

The other extreme is always on and I have already given you the answer f 16, right.

So, then you have function and then, some other functions, right.

So, why did you reach 16?

Actually because with two inputs we will have these four values to take care of and each

of these are again binary.

So, you actually have 2 raise to 2 raise to n, right.

So, for three inputs 2 raise to 2 raise to 3 would be 256, right ok.

Now, that is the easy part of these.

How many are linearly separable?

I will have to do any actually stare it in and seriously try to find the answer when

you cannot really do that, right . So, turns out all of them except XOT and in,

not of XOR, ok.

So, for the two input cases, there are two functions which are not linearly separable,

ok.

For n inputs how many functions would be not linearly separable?

It is an arbitrary, ok.

N is not the answer.

You are not going to disappoint me, not n ok, but what is the answer, ok.

So, for n inputs, we will have two ratio 2 n functions of these we do not know how many

are going to be not linearly separable.

That is not a solved problem, although I encourage you to go and find the answer.

I am looking for a good will hunting kind of a moment, but all it suffices to know is

that there exists some which are not linearly separable, right and that everyone agrees

that there exists some, right and as n grows probably that number will increase and so

on, but it is not known exactly.

You cannot write it as a function, ok.

So, what we have done so far is looked at boolean functions, how many boolean functions

can exist and of that we just have concluded that there would be some which are not linearly

separable.

So, we will end this module here.

## Module_8 : Representation Power of Perceptron Learning Algorithms

We will go to the next module, where we talk about a network of perceptrons, and then we

talk about the representation power of a network of perceptrons. So, this module should have

been titled as network of perceptrons, ok. So now, in particular what we are going to

see is how any Boolean function whether linearly separable or not can be represented using

a network of perceptrons. Now, what do I mean by represented during

a network of perceptrons? What it means is that I will give you a network of perceptrons,

you take any Boolean function feed any value of x 1 to x n and the network will give give

you the same y as it is expected from the truth table, ok, that is what representation

means just to put it out clearly, ok, fine. And now I am going to again do a setup, I

am not giving you the solution, I am just making some set up and then we will discuss

the solution, right. So, for this discussion we will assume that

true equal to plus 1 and false equal to minus 1. So, instead of 0 and 1, we will assume

minus 1 and plus 1, ok. And these are your inputs x 1 and x 2 we are taking the 2 input

case. And I will have 4 perceptrons first, I will have 4 perceptrons. And I will also

have very specific weights connected to from the inputs to these perceptrons. So, red means

minus 1 and blue means plus 1, right . So, the first 2 inputs are connected with a weight

of minus 1. The next 2 inputs with minus 1 plus 1, plus 1 minus 1 and the last would

be plus 1 plus 1, ok. Now, once I have this, I will set the bias

of all these perceptrons to minus 2, ok. So, that will; that means, they will fire only

if they are weighted sum of the inputs is greater than 2, ok, fine? Ok now after this

I will have one more perceptron. So, I had 2 inputs, I converted that to 4 values, these

4 values are now going to feed into one more perceptron, ok.

And these weights I will not fix them, these are the weights that I am going to learn ok,

these and the final output of this perceptron which is the green perceptron is the output

of the network, right. So now, coming back to what I said that it can represent any function,

what I mean is that you take any function, feed in any combination of x 1 x 2, this network

will give you y and I am telling you that it will match the truth table of that function,

ok, right. Now, let us define some terminology this will

also stay with us for the rest of the course. So, this network contains 3 layers. The layer

containing the inputs is called the input layer; very creative, the middle layer containing

the 4 perceptrons is called the hidden layer. And the output layer which gives you the output

is called the output layer output perceptron; which gives you the output is called the output

layer right. So, you have a input layer or hidden layer and an output layer. And the

outputs of the 4 perceptrons I am going to call them as h 1 h 2 h 3 and h 4, ok. And

the red and blue edges are called the weights for the layer one, which we have not learned

we have actually set them by hand. And the weights for w 1, w 2, w 3, w 4 are called

the weights for the second layer, other the layer 2 weights, and these are the weights

that we want to learn, ok. Now I make this claim that this network, it

can take any Boolean function, it can implement any Boolean function, right? So, this same

network can implement any Boolean function; that means, if I take this network, and if

I try to learn the values of w 1, w 2, w 3, w 4, for any Boolean function whether it was

originally linearly separable or not I will be able to implement it, right.

So, isn't this an astonishing claim any Boolean function, do you think this is an astonishing

claim? Well not really if you really understand what is happening here right. So, let us see

what exactly is happening here. So, when will perceptron one fire? When the input is false

false 0 0. Will it fire for any other input? When will perceptron 2 fire ? Any other input?

Same for the next perceptron? Same for the next perceptron?

So, you start getting an intuition of what is happening here ? You do, ok let us see.

So now, for this particular network now that I have given you some intuition of what is

happening, basically every node or every neuron in the hidden layer is catering to one of

the inputs, and it will fire only for that input, it will not fire for anyone else right.

So now let us try to implement the xor function, and see what are the ok. So now, let us try

to implement the xor function, and see what are the set of inequalities that result from

this. Earlier when we try to look at the set of inequalities, we ended up with a contradiction,

let us see if that happens now. So, this is x 1, x 2 this is your xor function. So, that

is just like any truth table that I am noting down the intermediate values. And then my

final input to the green perceptron is going to be summation of these, ok, fine and it

will fire if this summation is greater than equal to 0, or else it will not fire, ok.

Now, for the first case when the input is 0 comma 0 what is h 1 going to be? One and

everything else is going to be 0, that is exactly what we saw in the previous slide.

So, what is the summation going to be? Just w 1 right, so, it is w 1 h 1 plus w 2 h 2

so on, but h 2 to h 4 are 0. So, only thing that remains is w 1. For the second case,

w 2; for the third case, w 3 for the 4th case w 4.

So, is it clear now what is happening? Let us go a bit more into detail right. So now,

for the xor condition, what are the conditions that we need? W 1 should be less than w 0,

right? Because this should not fire, w 2 should be greater than equal to 0, w 3 should be

greater than equal to sorry w naught not w is not 0, and w 4 should not fire. So, w 4

should be less than w. Are there any contradictions here? By design no right. So, we have made

sure that for the final layer only one of these guys feeds to it.

So, it does not matter what the remaining outputs are, right? They do not interfere

with each other, unlike earlier where we had conditions like w 1 should be something w

2 should be something, and then w 1 plus w 2 should be something. There are no such contradictions

here. Because we have made sure that every neuron in the middle layer actually caters

to one specific input, and now the weights in the final layer can be adjusted so that

we get the desired output for that input, right.

So, I can set whatever value of w and I need to set. So, that I can fire the new on it.

In fact, I could just fix w 0 as 0, and then I can adjust the weights of w 1 w 2 w 3 w

4, right. And I can implement the xor function. So, are you convinced that this can be used

to implement any Boolean function. How many if you are not convinced? So, the negative

question never works, how many if you are convinced? Sure, ok.

Now, what if we had 3 inputs? Before that it should be clear that the same

network can be used for any of the remaining 15 functions, right? And for each of these

functions we will end up with a different value of w 1 w 2 w 3 4, but you will be able

to satisfy the truth table, right and you can go home and try it, which I am sure you

will do. Ah So, what if we have a function of 3 inputs

? 256, what is 256? No. .

8 right? Fine, sure, ok. So, this is what it will

look like, and anything specific about the weights of the initial layer, can you tell

me what the weights would be? Just tell me red red red red blue blue whatever colours

you like this thing. First perceptron what would the weight colours be red, red, red,

then ? .

Then enough ok so, this is how it will look right, right and now this same thing will

work with the same logic for any Boolean function of 3 inputs, you will get these 8 inequalities,

and they will not interfere with each other, and you can set the values of w 1 to w 8 so

that you can satisfy it ok, fine. So, what if we have n inputs ?

2 power. 2 power n perceptrons in the middle layer,

right, ok? So now here is the theorem, any Boolean function

of n inputs can be represented exactly by a network of perceptrons containing one hidden

layer with 2 raise to n perceptrons, and one output layer containing one perceptron, right?

We just saw an informal proof of this, we just constructed I just gave you the answer

it this is how you will get it, right? Now note that a network of 2 raise to n plus 1

perceptron, is it sufficient or necessary? Or both? Sufficient yes that is what it says,

is it necessary? No, we already saw the and function which

we can just represent using a single perceptron, right. So, it is not necessary, but it is

sufficient ok. So, this is a very powerful theorem if you think of it right. So now,

this whole objection right remember this history, and when we have the c I winter when people

showed that perceptron cannot handle the xor function, that is for a single perceptron.

If you have a network of perceptrons you can actually have any Boolean function, but what

is the catch as the value of n increases the number of neurons increases exponentially

right, but still in theory you could have a solution, ok.

Now again why do we care about Boolean functions, I keep coming back to this . Why do we care

about Boolean functions, because you took this ah and so, the question that I the question

that I want to answer is, how does this relate back to our original problem, right we know

ok any Boolean function can be implemented, how do we go back to our original problem?

Which is whether we like a movie or not, right, and you could see that there is a whole family

of problems there, right, whether we like a movie or not whether we like a product or

not, whether I want to go home today or not, yes no any kind of a yes no problem, it is

a whole family of problems there, right? So, let us see so, we are given this data

from our past experience, right. So, we are told that this is what the movie looks like.

These are the actor's director's joiners everything. We also know whether we like these or not.

So, we have a set of positive points and we have a set of negative points, right. And

now we want to have a computational model which can satisfy this data; that means, once

the model is trained, once whatever algorithm I algorithm I use has converged, it should

be able to give me the correct output for a given input. That is what we are interested

in, and that is a real classification problem that we are interested in. Now for each movie

we are given these factors as well as the decision.

And I said p is and n is are positive and negative points. The data may or may not be

linearly separable. It is not necessary that the data is linearly separable those were

the goody cases it, but in general that may not happen. But do we worry about it now?

No what the previous theorem told us is that irrespective of whether your data is linearly

separable or not, I can give you a network which will be able to solve this problem modulo

that it might be very expensive in the number of neurons in the middle, right? But if you

keep that aside, I have a solution for this. And that is why we care about Boolean functions,

because many problems we could actually cause to it in a simplistic way, if we ignore the

real inputs. And if you even think of the real inputs, right? Suppose it could take

all values between 0 to 1, you can always make it binary, you could say that is the

value between 0 and 0.1 is the value between 0.1 and 0.2. And you could make it as small

the scale as small as possible right. So, that is why we care about this.

So, the story so far has been that the network of networks of the form that we just saw,

it which contain one input layer output layer and one or more hidden layers. These are known

as multilayer perceptrons, but a more appropriate terminology would be multi-layered network

of perceptrons, right? Because the perceptron is not multi-layered. You have a network of

perceptrons and that network has many layers right.

But generally there is is abuse of notation we always call it MLP which is multi-layered

perceptrons. And the theorem that we just saw gives us the representation power of an

MLP, and basically tells us that it can represent any Boolean function that we want to deal

with, right? So, that is where we will end this class, and in the next class we will

talk about sigmoid neurons, ok. Thank you .
