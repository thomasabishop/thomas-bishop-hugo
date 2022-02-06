---
date: 2021-11-27
title: "Informal definitions of key concepts in propositional logic"
categories: ["Logic"]
tags: ["propositional logic"]
---

This post is the first of a series on propositional logic that introduces the foundational logical concepts of validity, soundness, truth, falsity, possibility and indeterminacy. These concepts are defined here informally and will receive formal articulation in later posts.

## What is propositional logic?

The chief unit of propositional logic is the _proposition_. It is typically said that the sentences of a language _express_ propositions. In natural languages, propositions are expressed via declarative sentences: a statement that _such and such is the case_. For example, in English: _snow is white_, _London is the capital of the United Kingdom_, _John is travelling to Stockholm_ etcetera. Whilst this is true it is important not to assume that a proposition reduces to its expression by a given sentence. There are numerous examples of why this assumption proves problematic. For example, _il pleut_ and _it is raining_ express the same proposition but do so via different sentences in different languages. Similarly the semantically ambiguous English sentence _Two cars were reported stolen by the police yesterday_ expresses two possible propositions (the police reported the car stolen, the police stole the car) that are left underdetermined by the surface grammar of the sentence. For simplicity we will talk about propositions exclusively in terms of sentences but it is important to note that the two are not straightforwardly interchangeable.

Not every sentence in a language has a propositional form. Consider for example _Áchtung!_ or _thanks_. It is not obvious that these sentences express a proposition in the manner of declarative sentences. Philosophers and linguists have called expressions that do not satisfy propositional criteria [speech acts](https://en.wikipedia.org/wiki/Speech_act). The difference between declarative sentences and speech acts (like thanking someone or issuing an order) consists in the fact that the former possess clear **truth-conditions** that reduce to a given **truth-value**. In the case of _il pleut_ the sentence is true if it is raining and false otherwise. Those are its truth-conditions. Its truth-value is the particular assignment that is made on the basis of these conditions. Assume it is not raining; in this case the truth-value of _il pleut_ is false.

Although declarative sentences are a subset of the totality of possible grammatical expressions in any natural language, they are clearly an important subset. They form the basis of all scientific and mathematical discourse and are our primary means of spreaking and reasoning about the world. The scope of propositional logic is limited to sentences that have this declarative property. There are no questions, commands or exhortations in propositional logic, only statements which may be true or false.[^1]

The purpose of propositional logic is to analyse propositions in terms of their truth conditions and to derive rules governing their proper application and combination in arguments. Equipped with these rules, we are able to demonstrate for example that an argument is valid or that it displays sound reasoning. On the other hand, the same rules will allow us to demonstrate when an argument is invalid or that it leads to contradiction.

## Arguments and consistency

Propositional logic proceeds upon two interconnected axes:

1. Analysing compound propositions in terms of their constituent parts
2. Analysing a proposition in relation to other propositions

In this post we are focused on the second axis. The first will be covered in a future post on logical connectives and truth-tables.

When we analyse a series of propositions and the relations between them we call the group a **set**. Sets possess logical **properties**. The first such property we will define is **consistency**.

{{< admonition type=tip title="Logical consistency"  >}}
A given set of propositions is consistent if and only if it is possible for each member of the set to be true at the same time. It is inconsistent just if this is not the case.
{{< /admonition >}}

The following set of propositions form an inconsistent set. Can you spot the inconsistency? [^2]
{{< admonition type=example title="Inconsistent set of propositions"  >}}

1. Anyone who takes astrology seriously is crazy.
2. Jane is my sister and no sister of mine has a crazy person for a husband.
3. Richard is Jane's husband and he checks his horoscope every morning.
4. Anyone who checks their horoscope takes astrology seriously.

{{< /admonition >}}

The set is inconsistent because it is not the case that all the propositions can be true at once. Specifically: if (1), (3), and (4) are true, (2) cannot be. Alternatively, if (2), (3) and (4) are true (1) cannot be.

Let's illuminate the first instance of inconsistency. On the one hand we assert that taking astrology seriously is crazy and we assume that checking your horoscope means that you take astrology seriously. Richard is Jane's husband and he checks his horoscope each morning. By definition then, Richard is crazy and Jane is married to him, but if I believe this, I cannot believe that my sister would not marry a crazy person. My beliefs are inconsistent.

Now, the second instance of inconsistency. Jane, my sister, is married to Richard. None of my sisters have a crazy husband. Richard checks his horoscope each day and therefore takes astrology seriously. If this is the case, I cannot believe that taking astrology seriously is crazy because otherwise my sister cannot be married to Richard.

In deconstructing the inconsistencies in the scenario of Richard and Jane we have been concerned to point out that one proposition **implies** or **follows from** another proposition. Intuitively we have been invoking the logical notion of an **argument**. This is not so different from what we mean by an argument in ordinary life. If we are arguing with someone, we believe that they are wrong about something where 'something' is a proposition and 'wrong' means _false_. For example _the prime minister is a liar_. A more logical way to put this is that we believe their beliefs about a set of propositions are inconsistent. In order to make assertions about the relative consistency or inconsistency of a set of propositions we advance arguments. This is like seeking to change the person's viewpoint by showing that their belief _A_ conflicts with their other belief _B_ or that if _A_ is true, they cannot believe _B_.

In the example above each proposition in the set has equal footing; we have not distinguished one type of proposition from any other. When we construct an argument however, we distinguish the propositions by type. We say that one or more propositions are **premises** and one proposition is the **conclusion**:

{{< admonition type=tip title="Argument"  >}}
An argument is a set of propositions comprising one or more premises and a conclusion. The conclusion is taken to be supported by the premises.
{{< /admonition >}}

Let's demonstrate how this works by making an implicit argument from previous example explicit:
{{< admonition type=example title="Argument"  >}}

1. P: Anyone who checks their horoscope takes astrology seriously.
2. P: Richard checks his horoscope.
3. C: Richard takes astrology seriously.

{{< /admonition >}}

This constitutes a logical argument because of how the propositions are arranged: we are asserting that the conclusion (C) is supported the two premises (P). We call such arguments **syllogisms**.

## Evaluation criteria for arguments

In what sense do the premises support the conclusion of an argument? What is the relation between these two types of proposition? The word 'support' is rather vague. In logic there are different ways to assess the qualility of an argument: **inductive strength** and **deductive validity**.

Consider the following argument:

{{< admonition type=example title="Inductive argument 1"  >}}

1. P: When a cat scratches itself it can mean it has fleas.
2. P: Our tabby, Carrot has been scratching himself a lot lately.
3. C: Carrot has fleas.
   {{< /admonition >}}

To ask ourselves whether this is a strong argument is to reflect on whether we have good grounds for believing the conclusion given the premises. My intuition that this is a reasonable argument but not a particularly strong one. It doesn't strain credulity but it is by no means watertight.

Contrast it with this argument:
{{< admonition type=example title="Inductive argument 2"  >}}

1. P: Every day the sun rises in the east.
2. P: The sun rose in the east today.
3. C: The sun will rise in the east tomorrow.
   {{< /admonition >}}

This strikes me as a stronger argument than the first. If you had to bet on Carrot having fleas or the sun rising in the East you would put your money on the latter although you would probably get better returns on the former. With arguments of this nature we are proceeding on the basis of likelihood. The technical term for this is **induction**: given some background context of beliefs (for instance the typical behaviour of cats and the planet) there are stronger or weaker grounds for accepting the conclusion of an argument bases on its premises.

{{< admonition type=tip title="Inductive strength"  >}}
An argument is inductively strong if and only if the conclusion is probably true given the premises.
{{< /admonition >}}

Although the arguments differ in their relative strength they are both inductive arguments. This is because they are each falsifiable. In the first case, this is obvious: Carrot might not have fleas and could be scratching for some other reason. Perhaps surprisingly, the second argument is also falsifiable. The magnetic field of the Earth could switch polarity meaning that while the Earth would not change its position relative to the sun, our compass would be inverted and therefore indicate that the sun rising in the west. This is very unlikely to happen imminently but it _will_ happen at some point in the next 10,000 years. Therefore the conclusion could prove false.

The next obvious is whether all arguments are like this. Is probability the best we can hope for? Fortunately not. Propositional logic is a deductive schema which means it aims for truths that are not falsifiable in the manner of the two examples above. It is this criterion of evaluation that we mainly interested in when we use logic as a formal discipline. This is the domain of deductive validity. Validity is our second key logical property.

{{< admonition type=tip title="Deductive validity"  >}}
An argument is deductively valid if and only if it is not possible for the premises to be true and the conclusion false.
{{< /admonition >}}

## Validity and soundness

The following syllogism is an example of a valid argument:
{{< admonition type=example title="Valid argument 1"  >}}

1. P: All fish live in the sea and only in the sea.
2. P: Cod are fish.
3. C: Cod live in the sea.
   {{< /admonition >}}

And here is an invalid argument:
{{< admonition type=example title="Invalid argument 1"  >}}

1. P: All fish live in the sea and only in the sea.
2. P: Cod are fish.
3. C: Cod live on land.
   {{< /admonition >}}

In the valid instance, there is no sense to the idea that we might accept each premise and yet deny the conclusion. In the invalid instance this is not the case: we can accept each premise and deny the conclusion. We can relate this back to the the notion of consistency. Recall that a set of propositions is consistent if and only if it is possible for each member to be true at once. With the first argument we cannot consistently accept the premises and deny the conclusion whereas in the case of the second argument we can quite consistently accept the premises and deny the conclusion since the propositions do not comprise a consistent set.

In contrast to the previous inductive arguments, with valid arguments the conclusion is supported purely in virtue of the terms used in the premises and the propositions they express. In order to assess the validity of an argument like the first it is not neccessary to aquaint oneself with cod and to study their behaviour so as to determine whether they do in fact live in the sea. All that is necessary is to understand the propositions expressed. Philosophers refer to statements of this sort as **analytic**. They are true or false 'by definition'. More specifically: the concept of the predicate is contained within the concept of the subject for example _all brothers are male_. In the case of the argument, we have defined at (P1) that fish are creatures that live in the sea so given this definition, the conclusion is bound to follow from the premises since it is just a specific instance of the general property already defined. Validity is therefore an entirely formal notion that exists over and above any facts of the matter. If I have defined 'fish' universally as sea-dwellers I cannot without inconsistency say that they are not sea-dwellers.

This is further exemplified with an argument like the following:
{{< admonition type=example title="Valid argument 2"  >}}

1. P: Manchester is the capital of the UK.
2. P: Manchester is north of Birmingham.
3. C: The capital of the UK is north of Birmingham.
   {{< /admonition >}}

Is this a valid argument? To answer this question remember that invalidity means that it is possible for the premises to be true and the conclusion false. In the strict logical sense, this is valid argument since _were_ the premises true, the conclusion would also be true. The point is that validity is a function of truth-conditions not truth-values. The truth value of the first premise and the conclusion in the above argument happen to be false but this does not affect its validity. There is no necessity to London being the capital of the UK and not Manchester. We can imagine things being otherwise which is to say that we can entertain the truth-conditions of the proposition and make judgements in accordance with it being true or false quite independently of whether it is in actuality true/false.

We can take this back to the earlier example of the invalid argument about cod: in order to judge the argument invalid it was not necessary for us to look for cod that live on land and come back empty. Rather we just had to assume that if all fish live in the sea then it must be the case that if something is a fish, it is a sea-dweller. We made no commitment to fish actually living in the sea.

Does this mean that actual truth does not matter to logic? No, it just means that validity as a property is decoupled from truth as a property although we cannot of course have a grasp of the notion of validity without possessing a prior notion of truth. A proposition being true in fact is a property it may or not possess in addition to its membership within a valid sequence of reasoning. If an argument is both valid and its premises are true in fact we say that it is a **sound** argument. This is a stronger criterion of evaluation than validity alone.

{{< admonition type=tip title="Soundness"  >}}
An argument is sound if and only if it is deductively valid and all of its premises are true.
{{< /admonition >}}
It follows from this definition of soundness that:

- an argument cannot be sound if it is not also valid
- an argument can be valid without being sound
- if an argument is sound its conclusion must be true

(The last point follows from the fact that soundness means the premises are true and validity requires that if the premises are true the conclusion must also be true.)

We have already seen examples of arguments that are valid but not sound in the Manchester example, let's close this section with an example where both premises and conclusion are true yet the argument is invalid, demonstrating that truth alone is not sufficient for soundness.
{{< admonition type=example title="Invalid argument 2"  >}}

1. P: London is the capital of the UK.
2. P: The capital of the UK is in the southern part of the country.
3. P: Cambridge is not the capital of the United Kingdom.
4. C: London is south of Cambridge.
   {{< /admonition >}}

This argument is deductively invalid because we can consistently assert the premises but deny the conclusion. Specifically: there isn't anything about the premises that makes the denial of the conclusion inconsistent. From the point of view of the premises alone, London could be north of Cambridge whilst still being in the southern part of the country.

## Logical possibility

In distinguishing the properties of logical consistency and validity we have been making much tacit use of the notion of **possibility**. This is because when we consider the validity of an argument we are assessing truth-conditions and this consists in asking ourselves what could or could not be the case: were it such that _P_, then it would be the case that _Q_. It is important to understand what possibility means in the context of logic and how it differs from what we might mean ordinarily when we use the term.

It is evident from the case of arguments that are valid but not sound that logic operates with a specialised notion of possibility. For example it has to be the case that the proposition _Every woman can levitate_ is logically possible since the following argument is valid:

{{< admonition type=example title="Valid argument 3"  >}}

1. P: Janice is a woman.
2. P: Every woman can levitate.
3. C: Janice can levitate.
   {{< /admonition >}}

But we know of course that women cannot levitate. When we assert that this is impossible we are relying on a stronger notion of possibility than logical possibility. It follows that the concept of possibility can have different degrees. The scope of the concept of possibility has been the concern of logicians and philosophers since at least the time of Plato and numerous different formulations exist. The notion that we mostly work with unreflectively in everyday life is nomological possibility. This means 'governed by the application of laws' where these laws pertain to our current understanding of the natural world as determined by physics. Levitation is therefore nomologically impossible but logically possible.

If logical possibility is not contrained by the laws of physics does it place any restrictions on what is possible? Logic applies a single restriction, the law of non-contradiction: a proposition cannot both be true and false at once. The following propositions are examples of a contradictory propositions.

{{< admonition type=example title="Contradictions"  >}}

- There is a dog that is not a dog.
- Today is Tuesday and today is not Tuesday.
- The cat that is dead is alive.
  {{< /admonition >}}

From this we can derive the following property of logical possibility:

{{< admonition type=tip title="Logical possibility"  >}}
A proposition is logically possible just if it does not imply a contradiction.
{{< /admonition >}}

## Logical truth, falsity and indeterminacy

What are the truth-conditions of a contradictory proposition? We know that a logically possible proposition such as _every woman can levitate_ could be true or false. It has to be so because we are capable of constructing valid arguments where it features as a premise and a valid argument implies the possible truth of its premises.

In the case of a contradiction there are no conditions under which it could be judged to be true. For this reason, contradictions are classified as **logically false**. This is distinct from ordinary falsity where a proposition _could_ be true but happens to be false.
Logically false propositions are universally false and could never be true. This is consistent with our previous observation of the law of non-contradiction: if a proposition cannot be both true and false at once we are saying that something _cannot be the case_ which is of course to say _is false_.

Logical falsity is therefore another property that a proposition may possess and it is a property that is possessed by all propositions that are contradictions:

{{< admonition type=tip title="Logical falsity"  >}}
A proposition is logically false if and only if it is not possible for the sentence to be true.
{{< /admonition >}}

Complementing logical falsity is **logical truth**:

{{< admonition type=tip title="Logical truth"  >}}
A proposition is logically true if and only if it is not possible for the sentence to be false.
{{< /admonition >}}

We call logically true propositions tautologies. Some examples:
{{< admonition type=example title="Tautologies"  >}}

- An apple is an apple.
- Today is Tuesday or today is not Tuesday.
- The cat is dead or alive.
  {{< /admonition >}}

The properties of logical truth and falsity are alike in their universality. Propositions that are logically true do not exclude any possibility (today is Tuesday or it is not Tuesday; there is no possible state outside of this) whereas logically false propositions exclude all possibilities (there is no scenario where today is both Tuesday and not Tuesday).

We class all propositions that are not contradictions or tautologies **logically indeterminate** propositions. This means that their truth-value is not assigned purely on the basis of the meanings of the terms of which they are comprised. _It is raining_ for example, is logically indeterminate because we cannot know its truth-value just by reflecting on the meaning of the predicate _is raining_. It may be true under certain conditions and false under others and in order to know the specific truth-value at a given moment, we must look to states of affairs beyond the sentence. The vast majority of propositions expressed in natural and formal languages are indeterminate in this manner.

## Summary

In this post we introduced propositions as descriptions of states of affairs that possess truth-conditions. We noted that propositions are expressed in language through the medium of declarative sentences and that not every expression in a language possesses a propositional form. Two key properties that pertain to sets of propositions were introduced and exemplified: consistency and validity. In addition we considered different evaluative criteria for logical arguments comparing inductive strength with deductive validity. We distinguished logical possibility from nomological possibility and explained how the law of non-contradiction places bounds on what is logically possible. Equipped with the concept of logical possibility we were able to introduce logical truth and falsity, analysing the truth-conditional form of tautologies and contradictions and noting that propositions that are neither logically true or false are logically indeterminate.

[^1]: These all being standard instances of speech acts which are resistant to truth-conditional analyses as noted above.
[^2]: This example comes from (Bergmann, Moor and Nelson, 2014).

## References

Bergmann, M., Moor, J. and Nelson, J. (2014). The logic book. Boston: Mcgraw-Hill/Connect Learn Succeed.

Wikipedia Contributors (2019). Speech-act. [online] Wikipedia. Available at: https://en.wikipedia.org/wiki/Speech_act.

‌
‌
