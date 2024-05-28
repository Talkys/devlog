+++
title = 'The donut saga'
date = 2024-05-28T11:32:00-03:00
draft = false
+++

I'm working to make a set of donut.c programs in many languages. Turns out is way harder to install the development environment than program the donuts. Right now I have several languages:

- C
- C but optimized
- C++
- Golang
- Julia
- Pascal (the worst of all)
- Brainfuck (Not the real thing, but let's be honest here)
- Perl (really really slow)
- Python
- C#
- x86 Assembly
- Kotlin
- Java

Starting now I will report my progress here about new donuts. My next targets are Erlang, Elixir and to make a custom virtual CPU to run custom asembly and run this way (and I bet it will be faster than perl anyway).

You can check donuts [here](https://github.com/Talkys/donut)

Now. As I've made those donuts before the blog, let's take some time to review them. I used a 1000 frame execution to see the performance.

## C

The C donut is very popular, common and simple. Not really a chalenge and is my base model for other implementations.

1000 frames in 0m5,264s

## C - Optimized

This one is a int only implementation tha runs 5x faster than regular C.

1000 frames in 0m1,160s

## C++

Was the same as C, run at the same fps, so no big deal.

1000 frames in 0m5,166s

## Go

Now we're talking. The golang implementation was very easy to do as it is very very similar to C, but really messy to declare the arrays.

1000 frames in 0m9,544s

## Python

Now. This one was a mess. The lack of typing was really anoying to keep track on castings and I had to use round functions.

One of my slowest implementations.

1000 frames in 1m5,555s 

## Kotlin

Setting up the template program was way harder than coding the donut on this one. I don't really like to install a big toolchain to compile stuff, so the only option was donwloading a standalone compiler to generate a JAR file.

1000 frames in 0m9,594s

## Java

Is java, is verbose, is heavy, is boring.

1000 frames in 0m9,879s

## Julia

Julian was very fun to use, the JIT interpreter was easy to use, the program was easy to write buuuuuuuuuuut it was quite slow. I'm sure there are optimizations we can use as julia is very very fast at math, but we're measuring the same program for everyone.

1000 fames in 0m14,777s

## Pascal

This one was so bad, so bad that I don't want to touch this thing for a decade at least. First: type casting is bad. Second: Declare variables beforehand is bad. Third: Creating array types is bad. Fourth: POSIX does not exist.

1000 frames in 0m10,246s

## C#

C# is very boring, and not really that fast. I used mono instead of .NET so maybe that contributed to make it slow, but as I like tho say: Not on Linux, not on my life. So unless MS bring .NET Framework to Linux we're not using that. And .NET Core is not a desktop framework in the end.

1000 frames in 0m20,872s

## Perl

Perl was easy to do (didn't like the beforehand declaration) but not really fun to write. At least is already in my distro. Really really slow to run.

1000 frames in 1m23,243s

## Brainfuck

BF was not a real donut and I will not program it by hand. Maybe I can do a compiler to do that for me, but now, it just render static frames. As this is not a real donut I don't have a benchmark for BF.