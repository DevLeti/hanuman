---
layout: post
cover: 'assets/images/tree.jpg'
title: 텐서플로우 - 상수
date: 2018-08-04 12:54:00
tags: tensorflow_tutorial
author: DevLETi
---


```
A genius is just a talented person who does his homework. - Thomas A. Edison

천재란 자신에게 주어진 일을 하는 재능 있는 사람일 뿐이다. - Thomas A. Edison
```


## 텐서플로우에 들어가기전!
<hr />

저는 이 글을 작성하는 목적이 세가지가 있습니다. 첫번째로 마크다운 작성 문법에 익숙해지려는 것과, 텐서플로우의 기초를 이해하려고 하는 것, 그리고 중국어를 잊지 않는 것 입니다. 매 글은 참고된 사이트가 있으며, 만약 더욱 명확하고 정확한 설명이 필요하시다면 참고된 사이트를 들어가주세요. 중국어는 틀린 문장이 있을 수 있습니다. 만약 잘못된 문장이 있다면 부담없이 알려주시길 바랍니다.<br>

( br 쓰고 hr 썼는데 이건 html문법 아닌가?)

## 进去tensorflow前！
<hr />

我有三个目的。第一是习惯markdown文法，第二是学习tensorflow的基础文法，第三是防止忘掉汉语。每个说明有参考网站，如果要深的说明，请看看参考网站！
（因为我是外国人，几个句子可能是病句。如果我的句子有问题[比如：生词错误，语法错误等等]，请告诉我！)

想吃炒面..T-T


<h3>오늘의 내용 </h3>

<ol>
<li>상수 정의방법</li>
<li>구동방법(session, run)</li>
</ol>

<h3>内容</h3>

<ol>
<li>常量 定义方法</li>
<li>启动方法(session, run)</li>
</ol>


<h2>코드 / 程序代码</h2>
```
import tensorflow as tf

import os
os.environ['TF_CPP_MIN_LOG_LEVEL'] = '2' # 경고문 무시 / 无视警告

a = tf.constant(5)
b = tf.constant(10)
c = tf.constant(20)

d = a+b+c

sess = tf.Session() # Session의 첫 S는 대문자!! Session的 最初S是大字！！
result = sess.run(d)
print(result)
```

<h2>상수 정의방법 / 常量定义方法 </h2>

```
tf.constant(value, dtype=None, shape=None, name='Const', verify_shape=False)
```

value : 상수의 값 / 赋值(=一个数) <br>
dtype : datatype, tf.float32 같이 실수, 정수의 데이터 타입을 정의한다 / 定义常量的元素类型 <br>
shape :<br>
행렬의 차원을 정의한다. shape = [3, 3] 으로 정의해주면, 이 상수는 3x3 행렬을 저장하게 된다.<br>
定义矩阵的次元，如果shape = [3, 3], 这常量是3x3矩阵。<br>
name : name은 이 상수의 이름을 정의한다.(이후 설명) / 定义常量的名字(以后说明)<br>

<h2>구동방법 / 启动方法 </h2>

```
sess = tf.Session() # Session의 첫 S는 대문자!! Session的 第一个S是大字！！
result = sess.run(d)
```

구동을 하고 싶다면, 구동을 하는 공간인 session을 정의해야 한다. 구동은 session.run()을 통해 한다.<br>
如果想启动，先要定义session（启动的空间）。后用session.run()。


참고/参考 : <a title="cf_site_1" href="http://bcho.tistory.com/1150">[조대협의 블로그]</a>
