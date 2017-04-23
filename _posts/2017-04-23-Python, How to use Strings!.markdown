---
layout: post
title:  "Python, How to use Strings!"
date:   2017-04-23 01:02:20 +0900
categories: Python
---
The code below shows how to print a string backwards.

{% highlight Python %}
school = "sunrin"
x=len(school)-1
while x >= 0:
    print(school[x])
    x-=1

#=> prints 'n
#=> i
#=> r
#=> n
#=> u
#=> s' to Shell.
{% endhighlight %}

This time we're gonna slice the string and print the parts we want to.

{% highlight Python %}
s = "sunrin high"
print(s[0:5])
print(s[3:8])
print(s[-1])

# The Result is
#=> sunri
#=> rin h
#=> h
{% endhighlight %}

Now lets find a certain character inside a string. And if I find it the result will be true.

{% highlight Python %}
print('S' in 'Sunrin')

# The Result is
#=> True
{% endhighlight %}

The code below appends an element to an array. This has nothing to do with strings tho.

{% highlight Python %}
num = [1, 2, 4, 5];
print(num)
num.append(6)
print(num)
num.insert(0, 10)
print(num)
num.remove(10)
print(num)
num.remove(num[2])
print(num)

# The Result is
#=> [1, 2, 4, 5]
#=> [1, 2, 4, 5, 6]
#=> [10, 1, 2, 4, 5, 6]
#=> [1, 2, 4, 5, 6]
#=> [1, 2, 5, 6]
{% endhighlight %}

Here are some problems to solve with the concepts above. With the answers.

Problem 1. Print any string in an array randomly

{% highlight Python %}
import random
quotes = ["개같이 벌어서 정승같이 쓴다", "개 눈에는 똥만 보인다", "개는 잘 짖는 다고 좋은 개가 아니다"]
print(random.choice(quotes))
{% endhighlight %}

We need to import the random library and use choice to choose anything inside an array. Inside the Array there are a few string elements.


Problem 2. Input numbers and print the average of those numbers.(Using the array)

{% highlight Python %}
num = []
i = 0
sum = 0
while i < 5:
    num.append(eval(input("숫자 입력: ")))
    sum += num[i]
    i+=1
print("평균: ",sum/len(num))
{% endhighlight %}

Problem 3. Say there is a dice, Roll that 1000 times and print the counts of how much each number came out(1~6).

This one's pretty tricky!

{% highlight Python %}
import random
counters = [0, 0, 0, 0, 0, 0]
x=0
while x <= 1000:
    value = random.randint(0,5)
    counters[value] = counters[value]+1
    x+=1

x=0
while x < 6:
    print("주사위가 ",(x+1),"인 경우는 ", counters[x])
    x+=1
{% endhighlight %}
