---
title: "When the Machine Learns Our Mistakes: Bias, Fairness, and the Human Cost of AI"
date: 2026-10-29
draft: false
description: "How algorithmic bias emerges in AI, why fairness is more than accuracy, and what fairer AI governance could look like."
image: "/images/bias-fairness-ai.jpg"
tags: ["AI Ethics", "Bias", "Fairness"]
---

Artificial intelligence is often presented as a neutral judge. Unlike a tired human manager or a prejudiced official, a machine, we are told, simply follows the data. It does not have favourites, bad days, or hidden motives. That promise is powerful, especially in high-stakes decisions about jobs, loans, policing, and healthcare. Yet the promise is also misleading. AI systems do not fall from the sky. They are trained on data collected from human societies, built by human teams, and deployed inside human institutions. When those societies, teams, and institutions contain inequality, AI can learn that inequality, hide it behind technical language, and then apply it at a scale no single human could match.

This blog post explores bias and fairness in AI. It argues that fairness cannot be reduced to a single accuracy score, and that building fairer AI requires more than better code. It requires clear principles, honest testing, human oversight, and a willingness to ask whether a system should be used at all.

## What algorithmic bias really means

In class, we learned that an algorithm is a finite set of instructions that takes an input and produces an output. In machine learning, the instructions are not written by hand in the same way as a recipe. Instead, the system learns patterns from examples. That is why the data matters so much.

One of the six ethical concerns of algorithms discussed in class is misguided evidence. This happens when a system is trained on biased or unrepresentative data, and then treats a pattern in that data as if it were the truth. A related concern is inconclusive evidence: an algorithm may act on a correlation without a solid causal reason. For example, a credit-scoring system might lower a score because of a pattern it found, even if that pattern does not explain why a person is actually a credit risk.

Bias, then, is not only a technical error. It is a social problem that has been turned into data, and then turned back into decisions. If past hiring favoured men, a hiring model trained on past hiring will tend to favour men. If past policing focused more heavily on certain neighbourhoods, a predictive policing model trained on arrest records may predict more crime in those same neighbourhoods. The system is not inventing prejudice from nothing. It is learning it, repeating it, and giving it the appearance of objectivity.

## A hiring tool that learned the past too well

A well-known real-world example is Amazon's experimental hiring tool. Amazon began work on the tool in 2014, training it on resumes submitted to the company over the previous ten years. Because most of those resumes came from men, reflecting the male-dominated technology workforce at the time, the model learned to associate successful candidates with male patterns in language and experience. According to reporting on the case, it downgraded resumes that contained the word "women's", as in "women's chess club", and penalised graduates of all-women's colleges.

Amazon scrapped the tool in 2018 after it could not reliably correct the bias. Importantly, the company said the tool was never used to make actual hiring decisions; the problem was caught during internal testing. That detail matters, because it shows both a failure and a safeguard. The failure was that a system designed to be efficient reproduced a familiar inequality. The safeguard was human review and testing before deployment. Without that testing, qualified women could have been screened out quietly, at scale, without ever knowing why.

This case also illustrates the principle of justice. Justice in AI ethics means being fair and working to eliminate discrimination, not simply treating everyone through the same process. A process can be identical for every applicant and still be unfair if the training data, the features, or the definition of success already favours one group.

## When facial recognition fails unevenly

A second example comes from facial recognition. In 2018, Joy Buolamwini and Timnit Gebru published "Gender Shades", a study of commercial gender-classification systems from IBM, Microsoft, and Face++. They found that the systems performed far worse for darker-skinned women than for lighter-skinned men. Error rates were as high as 34.7 percent for darker-skinned women, compared with less than 1 percent for lighter-skinned men.

These numbers are not a small technical gap. They show how error can be distributed unfairly. If a system is described as 95 percent accurate overall, that average can hide the fact that it works well for one group and poorly for another. This is why fairness researchers distinguish between group fairness, which asks whether groups receive similar outcomes, and individual fairness, which asks whether similar people are treated similarly. It is also why situational fairness matters: fairness must be judged in the real situation, not only in a mathematical model.

Facial recognition also raises the problem of inscrutable evidence. Many modern models are black boxes, meaning even experts cannot easily explain why a particular decision was made. If a medical AI recommends a treatment but doctors cannot explain why, trust and informed consent are weakened. The same problem applies when a person is flagged by a facial recognition system, denied a benefit, or stopped by police. Without explainability, it is difficult to challenge a decision, correct a mistake, or hold anyone responsible.

That leads to a further concern: traceability. When an algorithm causes harm, who is responsible? The developer who built it, the company that deployed it, the organisation that bought it, or the person who relied on its output? If responsibility is unclear, accountability disappears. This is why the principle of explicability is so important. Explicability means that AI systems should be understandable, and that we should be able to say who is accountable when something goes wrong.

## Fairness is not just accuracy

It is tempting to think that fairness will follow automatically if we collect more data or improve accuracy. More data can help, but only if the data is representative and carefully chosen. A larger dataset that repeats the same imbalance will simply teach the model the same lesson more confidently. Similarly, a system can become more accurate on average while still failing the people who are already most at risk.

Fairness also involves autonomy. People should retain meaningful control over decisions that affect their lives. Recommendation systems, hiring tools, and risk scores can shape behaviour in subtle ways, nudging choices, narrowing opportunities, and normalising surveillance. Protecting autonomy therefore means giving people clear information, real choices, and a way to opt out or appeal. Privacy-preserving techniques, such as differential privacy and federated learning, can help, but they are not a substitute for consent and control.

Two other principles from the unified framework for AI ethics help here. Beneficence asks whether AI is doing good, not merely avoiding obvious harm. Nonmaleficence asks whether it is doing no harm, including harm to privacy and security. A hiring system that is fast and cheap is not automatically good if it quietly excludes qualified candidates. A facial recognition system that is convenient is not automatically good if it exposes some groups to greater risk of misidentification.

## Soft ethics, hard ethics, and governance

So how should we respond? In class, we distinguished between hard ethics and soft ethics. Hard ethics refers to formal, legally binding rules, such as laws, regulations, and compliance requirements. Examples include data protection rules like the GDPR in Europe, and newer laws such as the EU AI Act. Soft ethics refers to what organisations should do beyond the law, through self-regulation, codes of conduct, and internal governance.

Neither approach is enough on its own. Laws are essential, but they can be slow, general, or difficult to enforce across borders. A company might follow the letter of the law in one country while testing a controversial system in a country with weaker oversight. In class, this was called ethics dumping: conducting ethically questionable work where oversight is less rigorous, and thereby creating double standards for digital rights.

Soft ethics can fill some of these gaps, but only if it is real. There are five risky ways to be unethical that we studied: ethics shopping, ethics blue washing, ethics lobbying, ethics dumping, and ethics shirking. Ethics shopping means selecting principles for public relations while ignoring them in practice. Ethics blue washing means presenting a company as more ethical than it actually is. Ethics lobbying means using ethics talk to delay binding regulation. Ethics shirking means avoiding responsibility by blaming users, complexity, or regulators, while continuing to profit.

A genuine soft-ethics approach looks very different. It includes:

- Regular bias audits of training data and model outputs
- Representative and balanced datasets, and fairness-aware training methods
- Model cards and datasheets that document a model's purpose, limitations, and intended use
- Ethical impact assessments before deployment, similar to environmental impact assessments
- Independent audits, clear accountability structures, and diverse design teams
- Human oversight for high-risk decisions, especially in hiring, healthcare, policing, and criminal justice
- Explainable AI tools, so that people affected by a decision can understand and challenge it

These practices do not guarantee fairness, but they make fairness testable. They turn vague claims about ethics into evidence that can be checked, questioned, and improved.

## What fairer AI would look like in practice

Imagine a company that wants to use AI in hiring. A fairer process would start before any model is trained. The company would ask what "a good candidate" really means, and whether past hiring data reflects that definition or simply reflects who had access to opportunity in the past. It would test the system on different groups, not only on average performance, and it would keep a human in the loop for final decisions. If the system could not explain its recommendations, or if its errors fell unevenly on one group, the company would pause deployment rather than treating speed as success.

The same logic applies to facial recognition in public spaces. Before deployment, an ethical impact assessment should ask who benefits, who bears the risk of error, whether consent is meaningful, and whether there is a less intrusive alternative. If the answer is that one community bears most of the risk while another gains most of the benefit, that is not a technical detail. It is an ethical failure.

This approach also connects to AI for social good. The seven principles for AI for social good that we studied include incremental deployment, safeguards against manipulation, privacy protection and consent, situational fairness, and explanations in plain language. Together, they point to a simple idea: deploy slowly, test in real contexts, protect the people affected, and explain decisions in words they can understand.

## Conclusion

Bias in AI is not a mystery, and it is not inevitable. It comes from data that reflects unequal histories, from models that learn patterns without understanding causes, from black-box systems that cannot explain themselves, and from institutions that deploy those systems without clear accountability. The Amazon hiring tool and the Gender Shades study show the same lesson from different directions: a system can appear efficient and accurate while still being unfair.

Fairness, therefore, is a practice, not a feature. It requires justice in how outcomes are distributed, autonomy in how people are treated, explicability in how decisions are explained, and accountability when harm occurs. It requires both hard ethics, in the form of law and regulation, and soft ethics, in the form of honest governance, auditing, and restraint. Most of all, it requires humility: the willingness to test our tools, listen to the people most affected by them, and sometimes decide not to automate a decision at all.

If AI is going to shape who gets a job, who is recognised by a camera, who receives care, and who is trusted by institutions, then fairness cannot be an afterthought. It must be part of how we design, test, and govern these systems from the start. That is not only a technical challenge. It is a human one, and it is one we cannot afford to get wrong.