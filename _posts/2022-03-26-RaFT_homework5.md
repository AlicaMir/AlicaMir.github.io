---
layout: post
title: ТКиП - Поля частных и факториальность колец многочленов
tags: Скуридин
#categories: 
---

## Домашнее задание по Теории колец и полей №5

### Задание 1

Пусть $$I \subset R$$ - идеал кольца $$R$$. Доказать: $$\frac{R[x]}{IR[x]} \cong \frac{R}{I}[x]$$

Рассмотрим канонический эпиморфизм $$\pi: R \rightarrow \frac{R}{I}$$. Продолжим его на кольцо многочленов $$\widehat{\pi}: R[x] \rightarrow \frac{R}{I}[x]$$ по правилу $$a_0 + a_1x + ... \mapsto \pi(a_0) + \pi(a_1)x + ...$$. $$\text{Ker}\ \widehat{\pi} = \{a_0 + a_1x + ... \in R[x] \mid \forall i:\ a_i \in I\} = IR[x]$$. По теореме о гомоморфизме $$\frac{R[x]}{IR[x]} \cong \frac{R}{I}[x]$$.

$$I \subset R$$ прост $$\Leftrightarrow\ \frac{R}{I}$$ - область целостности $$\Leftrightarrow\ \frac{R}{I}[x]$$ - область целостности $$\Leftrightarrow\ \frac{R[x]}{IR[x]}$$ - область целостности $$\Leftrightarrow\ IR[x] \subset R[x]$$ прост.

$$(2) \subset \mathbb{Z}$$ максимален, так как $$\mathbb{Z}$$ - ОГИ и 2 - прост. Но $$(2) \subsetneq (2, x) \subsetneq \mathbb{Z}[x]$$, поэтому $$(2)$$ не максимален в $$\mathbb{Z}$$.

Пусть $$IR[x] \subset R[x]$$ максимален, тогда $$\frac{R[x]}{IR[x]}$$ - поле. По доказанному изоморфзиму тогда $$\frac{R}{I}[x]$$ - поле. В частности ОГИ. По задаче 3 из ДЗ 2 тогда $$\frac{R}{I}$$ - поле, что равносильно тогму, что $$I \subset R$$ максимален. 

### Задание 2. 

#### Докажите, что полем частных Z[i] является поле Q[i] = {a + bi | a, b ∈ Q}

Воспользуемся эквивалентным определением поля частных: Пусть дана область целостности R и она вложена в поле Q отображением i. Q - поле частных R, если для любого поля F и гомоморфизма $$\phi: R \rightarrow F$$ существует единственный гомоморфизм $$\psi: Q \rightarrow F$$, так что $$\psi \circ i = \phi$$.

Естественно вложение $$\mathbb{Z}[i] \rightarrow \mathbb{Q}[i]$$. Пусть задано поле F и гомоморфизм $$\phi: \mathbb{Z}[i] \rightarrow F$$, а также $$\frac{a}{b} + \frac{c}{d}i \in \mathbb{Q}[i]$$. Домножим $$(\frac{bd}{1} + \frac{0}{1}i)(\frac{a}{b} + \frac{c}{d}i) = \frac{da}{1} + \frac{cb}{1}i$$

Поскольку $$\psi$$ гомоморфизм, то $$\phi(bd + 0i)\psi(\frac{a}{b} + \frac{c}{d}i) = \psi((\frac{bd}{1} + \frac{0}{1}i)(\frac{a}{b} + \frac{c}{d}i)) = \psi(\frac{da}{1} + \frac{cb}{1}i) = \phi(ad + cbi)$$. Так как F - поле, то $$\psi$$ однозначно определяется через $$\phi$$ следующим образом: 

$$\psi(\frac{a}{b} + \frac{c}{d}i) = \phi(bd)^{-1}\phi(ad + cbi)$$

Таким образом, $$\text{Quot}\ \mathbb{Z}[i] = \mathbb{Q}[i]$$.

### Задание 3.

#### 1) 

$$p$$ не ассоциирован с $$q$$, при этом оба элемента неразложимы. Тогда выполнено $$q \nmid p$$ и $$p \nmid q$$, иначе бы нарушились вышеперечисленные свойства.

Поэтому их НОД ассоциирован с 1: остаток $$r$$ делит и $$p$$, и $$q$$, но поскольку $$p$$ неразложим, то любое его делящее число либо с ним ассоциировано (тогда по транзитивности $$p \sim q$$ - противоречие), либо $$r \sim 1$$. Таким образом, $$(p, q) = (1) = R$$, так как R - ОГИ (дз 3, задание 3). А значит $$\forall a \in R: a \in (p, q)$$, поэтому $$\exists \ b, c \in R: a = bq + cp$$, поэтому в $$\text{Quot}\ R$$ выполнено равенство $$\frac{a}{pq} = \frac{b}{p} + \frac{c}{q}$$.

#### 2)

Рассмотрим кольцо $$\mathbb{Z}[x]$$. Оно факториально, но не ОГИ. Его поле частных - поле рациональных функций $$Z(x)$$. Рассмотрим его элемент: $$a = 1, p = 2, q = x$$. Покажем, что не существует $$b, c \in \mathbb{Z}[x]$$, таких что $$\frac{1}{2x} = \frac{b}{2} + \frac{c}{x}$$.

Действительно, тогда бы было выполнено соотношение $$1 = bx + 2c$$, откуда по соображениям степени равных многочленом $$b = 0$$, а $$\text{deg} \ c = 0$$, т.е. $$c \in \mathbb{Z}$$. Но уравнение $$1 = 2c$$ не имеет решения в целых числах. Поэтому результат пункта 1 неверен для факториальных, но не ОГИ колец. 

### Задание 4

Так как $$(g)_K \subset (f)_K$$, то существует $$q \in K[x]$$, т.ч. $$g = fq$$.  Так как $$(cont_g) \subset (cont_f)$$, то существует $$c \in R$$, т.ч. $$cont_g = cont_fc$$. Пусть $$cont_q = \frac{A}{B}$$, тогда 

$$cont_gB\widehat{g} = cont_fA\widehat{f}\widehat{q}$$  

$$cont_fcB\widehat{g} = cont_fA\widehat{f}\widehat{q}$$ 

$$cB\widehat{g} = A\widehat{f}\widehat{q}$$ 

По лемме Гаусса, т.к. $$\widehat{g}$$ и $$\widehat{f}\widehat{q}$$ примитивны (второй как произведение примитивных), а $$cB$$ и $$A$$ - константы, следует: $$\widehat{g} \sim \widehat{f}\widehat{q}$$. Домножим на $$cong_g$$: 

$$g \sim cont_g\widehat{f}\widehat{q}$$

$$g \sim cf\widehat{q}$$

Поэтому $$f \mid g$$, а значит $$(g) \subset (f)$$.