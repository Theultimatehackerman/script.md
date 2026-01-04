
The Deep Dive Podcast - Episode 1
"Shadow Work & Flow States: The Neuroscience of Becoming a Hacker"
Host: 2K² (Devodero)
Guest: Afi0
Runtime: ~60 minutes
Format: Philosophy + Neuroscience + Hacking Hybrid
Release Date: January 5, 2026

## [00:00 - 02:00] COLD OPEN

**2K²:** So wait;you're telling me you found a zero-day in two hours because you were in emotional compression state?

**Afi0:** [laughs] Yeah man. It wasn't about the technique. It was about the state.

**2K²:** The state.

**Afi0:** The state. When your emotions are compressed, they don't distract you anymore. They drive you. It's like Tai Chi;control without stiffness, power without explosion.

**2K²:** That's the most Tai Chi hacker stuff I've ever heard. And they didn't pay you?

**Afi0:** Silent fix. N/A. Zero dollars.

**2K²:** [beat] We're gonna unpack that. Welcome to The Deep Dive.

---

## [02:00 - 04:30] INTRO

**2K²:** What's up everyone, this is 2K², and welcome to the first episode of The Deep Dive;a podcast where we don't just talk about hacking, we talk about the *thinking* behind hacking. The neuroscience. The philosophy. The stuff that makes you go "wait, what?"

Today I'm here with Afi0, a security researcher who approaches cybersecurity like nobody else I've met. This guy has found multiple 0-days, studies Jungian psychology, understands gamma wave states, and can explain how archetypes relate to exploit development. And somehow, it all makes sense.

Afi0, welcome to the show.

**Afi0:** Thanks for having me. Let's see where this goes.

**2K²:** So for people who don't know you;who's Afi0?

**Afi0:** I'm a security researcher from Ukraine. I do bug bounty, exploit development, vulnerability research. But really, I think of myself as someone who breaks models of thinking. The technical stuff is just a consequence of that.

**2K²:** Breaking models of thinking. That's gonna be the theme of this whole conversation, isn't it?

**Afi0:** [laughs] Probably, yeah.

---

## [04:30 - 12:00] SECTION 1: THE INSIGHT THAT CHANGES EVERYTHING

**2K²:** Alright, let's dive in. You told me something that really stuck with me. You said: "Cybersecurity is more than OWASP Top 10 and penetration testing. It's insights that change your vision of the world."

**Afi0:** Yeah, exactly.

**2K²:** Explain that. Because most people think hacking is just... learn the techniques, run the tools, find the bugs.

**Afi0:** Right, and that works to a point. But you can practice for years, watch courses, do CTFs;and if you don't have one key insight, it's all just... void. Empty action.

**2K²:** What's the insight?

**Afi0:** The system is hard if you look at it externally. But internally, it's easy. You just need to change perspective;see it from the inside out.

**2K²:** So it's not about knowing more exploits. It's about shifting how you see.

**Afi0:** Exactly. Like, probability theory, right? Where there are more API input fields, more functions, more steps in an authentication flow;that's where vulnerabilities are more likely to exist. More complexity equals more surface area for mistakes.

**2K²:** It's a search space problem.

**Afi0:** Yeah. And your job as a hacker is to have a good algorithm for searching that space. The better your algorithm;the better your mental model;the faster you find bugs with less effort.

**2K²:** This is what I call meta-learning. You're not learning techniques;you're learning how to learn. Optimizing the optimization process itself.

**Afi0:** Exactly. That's Kolmogorov complexity, right? You brought that up.

**2K²:** Yeah! So Kolmogorov complexity is basically;what's the shortest possible description of something? If you could compress all your hacking knowledge into its purest, most concise form, what would it look like?

**Afi0:** One insight. One way of seeing. Not a thousand techniques.

**2K²:** And I think that's what separates people who do well from people who struggle. The people who struggle are collecting techniques. The people who excel have internalized the *pattern* behind the techniques.

**Afi0:** Yeah, and once you have the pattern, you don't need to memorize anything. You just see it.

**2K²:** Like intuition.

**Afi0:** Deeper than intuition. Automatism. Your unconscious brain does the work.



---

## [12:00 - 20:00] SECTION 2: BREAKING THE DEVELOPER'S MODEL

**2K²:** Let's talk about something specific. You mentioned tenant isolation bugs. Walk me through how you found one.

**Afi0:** Okay, so this was in a multi-tenant system. They had four user IDs for one user;one ID per shard. And you could just... change the org ID to a request ID from another shard and access their data.

**2K²:** Wait, that simple?

**Afi0:** That simple. Tenant isolation bypass via logic flaw.

**2K²:** And what happened when you reported it?

**Afi0:** Silent fix. N/A. They didn't want to admit the architecture was broken.

**2K²:** So this is a fundamental design error, not just a bug.

**Afi0:** Exactly. This is what I mean by breaking the developer's model. The developer trusted the wrong assumption;they assumed user IDs were always bound to the correct shard context. But they weren't.

**2K²:** And no scanner is gonna find that.

**Afi0:** No scanner, no AI, no automation. You have to understand the business logic. You have to think about what the developer *intended* versus what they *implemented*.

**2K²:** This ties into what you said about conformism and nonconformism. Most people see the system as fixed. But you see it as mutable.

**Afi0:** Yeah. Conformists inherit thinking. Nonconformists create their own models. That's the difference.

**2K²:** And that's why hackers are naturally nonconformist.

**Afi0:** Yeah, but it comes with a cost. Society calls you weird. People don't understand what you're talking about. You spend a lot of time alone.

**2K²:** But you also see things nobody else sees.

**Afi0:** Exactly. That's the trade-off.

**2K²:** You mentioned Spectre earlier. How does that fit into breaking models?

**Afi0:** Spectre is the perfect example. Everyone thought CPU speculation was a hardware feature, not a security vulnerability. The security model said: "CPUs are trusted." But Spectre showed that assumption was wrong.

**2K²:** So the vulnerability wasn't in the code;it was in the *worldview* of how CPUs work.

**Afi0:** Exactly. And once you break that model, everything changes. Suddenly you have a whole new class of vulnerabilities.

**2K²:** That's why the best vulnerabilities are the ones that make people say "wait, you can do that?"

**Afi0:** [laughs] Yeah. Like Heartbleed. Such a stupid vulnerability;use-after-free in TLS because a developer forgot to set a pointer. But it affected a third of OpenSSL installations.

**2K²:** And it's not about brilliance. It's about fundamentals done perfectly.

**Afi0:** Exactly. Security isn't about being smart. It's about discipline and seeing what everyone else missed because they were moving too fast.

---

## [20:00 - 30:00] SECTION 3: THE NEUROSCIENCE OF FLOW

**2K²:** Alright, let's talk about something wild. You mentioned finding a 0-day in two hours while you were sick, and you were in this "emotional compression state." What is that?

**Afi0:** So, when I'm in that state, my emotions aren't scattered. They're compressed;like concentrated energy. Instead of spending emotional energy reacting to things, I store it and circulate it.

**2K²:** That's Tai Chi.

**Afi0:** Exactly. Control without stiffness. Power without explosion. You use the calm as your power.

**2K²:** And in that state, you found a 0-day in two hours.

**Afi0:** Yeah. Because I wasn't thinking about it consciously. My DMN, default mode network, was off. My neocortex wasn't trying to force solutions. I was just... in flow.

**2K²:** Flow state. But you're describing something deeper than normal flow.

**Afi0:** Yeah. I call it Tretha;a blend of theta, alpha, and gamma waves happening simultaneously. It's like... synesthesia of time. You're in the past, present, and future at once.

**2K²:** That sounds like what people describe on psychedelics.

**Afi0:** [laughs] Yeah, but I don't use psychedelics. This is just brain state optimization.

**2K²:** So how do you get into that state?

**Afi0:** You can't force it. It happens when you've done the work;when you've integrated your shadow, when you've removed the internal friction. Then flow becomes your default state, not something you chase.

**2K²:** Wait, let's back up. Shadow integration. Jungian psychology. How does that connect to hacking?

**Afi0:** So Jung's idea is that we have different parts of ourselves;archetypes;that operate unconsciously. The Shadow is the parts we deny or suppress. And if you don't integrate it, it controls you.

**2K²:** Like how?

**Afi0:** Like, I went through a phase where my Shadow was dominant. I had massive energy, massive drive, but I couldn't control it. It was overwhelming. For two weeks, I was terrified;fear of self, fear of nothing, fear of the Shadow itself.

**2K²:** That sounds intense.

**Afi0:** It was. But that fear was necessary. Because you can't integrate what you don't face. And once I integrated it, everything changed.

**2K²:** How?

**Afi0:** The energy was still there, but now I could control it. It wasn't chaos anymore;it was power. And that's when I found the 0-day. Because I wasn't fighting myself. I was aligned.

**2K²:** So the technical breakthrough came from a psychological breakthrough.

**Afi0:** Exactly. That's what people don't understand. Your internal state determines your external results. If you're fragmented inside, your work will be fragmented. If you're integrated, your work flows.

**2K²:** And most people never do the internal work.

**Afi0:** Most people don't even know it's possible.

---

## [30:00 - 40:00] SECTION 4: BIOHACKING THE BRAIN

**2K²:** Let's talk biohacking. Because you've studied neurochemistry, brain waves, neurobiology. How does that fit into all this?

**Afi0:** So, everything is patterns. Your thoughts aren't just abstract;they literally shape your chemistry. If you think about hugging someone, your limbic system releases oxytocin. It works with dopamine, serotonin, all the neurotransmitters.

**2K²:** So you can hack your brain through thought alone.

**Afi0:** Yeah. But most people don't realize this. They think they need nootropics or supplements to optimize. But the real optimization starts with understanding how your brain works.

**2K²:** You mentioned gamma waves earlier. What are those?

**Afi0:** Gamma waves are associated with peak insight, peak performance. When your brain is in gamma, all your neurons are firing synchronously. Your neocortex connects to your limbic system. You get crazy insights.

**2K²:** And that's what happened when you found the 0-day.

**Afi0:** Yeah. But here's the thing;you can't force gamma. It happens when you're aligned. When there's no internal conflict. When your conscious and unconscious minds are working together.

**2K²:** So it's not about pushing harder. It's about removing obstacles.

**Afi0:** Exactly. Most people are blocked by their own internal friction. They're fighting themselves without realizing it.

**2K²:** And how do you remove that friction?

**Afi0:** Shadow work. Self-integration. Understanding your patterns. Jung talked about this;when you integrate your archetypes, you stop being controlled by them. You can access their power consciously.

**2K²:** Give me an example.

**Afi0:** Okay, so the Wizard archetype. When I integrated the Wizard, I developed automatic prediction abilities. I could look at a system and just... know where the bug was. Not through analysis, but through unconscious pattern recognition.

**2K²:** That's what people call intuition.

**Afi0:** Deeper than intuition. Automatism. Like, sometimes I predict bugs and I don't even know how I know. My brain just does it.

**2K²:** That's because you've internalized so many patterns that your unconscious mind can process them faster than your conscious mind.

**Afi0:** Exactly. But that only happens after you've done the work. You can't skip to that level.

**2K²:** It's earned.

**Afi0:** It's earned.

**2K²:** You also mentioned BDNF;brain-derived neurotrophic factor. What's that about?

**Afi0:** BDNF is like growth hormone for your brain. It helps create new neural connections, strengthens existing ones. I have higher BDNF production genetically, which means I learn patterns faster.

**2K²:** So you're neuroplasticity-maxing.

**Afi0:** [laughs] Yeah, basically. But even without genetics, you can increase BDNF through learning, exercise, stress management.

**2K²:** And that's why you don't take a lot of notes.

**Afi0:** Yeah. I internalize patterns instead of storing them externally. My brain is the database.

**2K²:** That's dangerous though, right? What if you forget?

**Afi0:** If you forget, it wasn't important. The patterns that matter stay because you use them constantly.

---

## [40:00 - 50:00] SECTION 5: FROM BUG BOUNTY TO INNER PEACE

**2K²:** So you've done bug bounty for years. You've found critical vulnerabilities. And now you're saying... it's trash?

**Afi0:** [laughs] Yeah. I mean, every expert says this about their field eventually. Python developers call Python trash. JavaScript gods call JavaScript trash. When you know something deeply, you see all the problems.

**2K²:** But there's something deeper here. You're not just criticizing the field;you're saying you're done with it.

**Afi0:** Not done. Just... evolved past it. Bug bounty was about proving I could see what others couldn't. But I've proven that. Now I don't need external validation.

**2K²:** So what's next?

**Afi0:** Software development. Building things instead of breaking them. Minecraft plugins, actually.

**2K²:** Wait, seriously?

**Afi0:** [laughs] Yeah. I know it sounds weird. But when I code plugins, I feel... rest. When I do exploit development for three days with no results, I feel exhausted. But twelve hours of development? I feel energized.

**2K²:** Because it's creation instead of destruction.

**Afi0:** Exactly. And I realized;why am I spending my life in frustration when I could be creating things that make me happy?

**2K²:** This is the Steve Jobs quote, right? "If you live every day as if it were your last, you will be right someday."

**Afi0:** Yeah. That insight gave me time compression. It feels like a year passes in a minute, and suddenly I'm in 2027.

**2K²:** Time compression. Explain that.

**Afi0:** When you're aligned with your purpose, time speeds up because you're not wasting energy on friction. You're flowing. And when you're flowing, progress stacks faster than people expect.

**2K²:** That's what happens when you drop internal resistance.

**Afi0:** Exactly. Most people are fighting themselves constantly. They want to do something, but they doubt themselves, or they're chasing validation, or they're afraid of failure. All that creates drag.

**2K²:** And when you remove the drag...

**Afi0:** You move like water. No resistance. Just flow.

**2K²:** So this whole journey;from bug bounty to software development;it's really about finding peace.

**Afi0:** Yeah. I spent years chasing adrenaline, dopamine, the rush of finding bugs. But that's not sustainable. Eventually, you burn out. And I burned out five or six times.

**2K²:** Five or six times?

**Afi0:** Yeah. And each time I learned something. Until finally, I realized;I don't need to keep doing this. I can choose calm instead.

**2K²:** And calm is more productive than chaos.

**Afi0:** Way more productive. When you're calm, you're not wasting energy on emotional reactions. You can think clearly. You can see patterns. You can work twelve hours and feel rested instead of drained.

**2K²:** So the final stage isn't about being the best hacker. It's about being at peace with yourself.

**Afi0:** Exactly. And when you're at peace, the work comes naturally. You're not forcing it anymore.

---

## [50:00 - 58:00] SECTION 6: THE OUROBOROS & CYCLES OF GROWTH

**2K²:** You mentioned the Ouroboros earlier;the snake eating its own tail. What does that represent for you?

**Afi0:** Cycles. Patterns. Start and end collapsing into the same point. Life isn't linear;it's recursive. You loop through the same lessons at different levels until you finally *get* it.

**2K²:** So you don't escape the cycle. You understand it.

**Afi0:** Exactly. And once you understand it, you can control the cycles. You know when to chase dopamine and when to let the system rest. You know when to push and when to pause.

**2K²:** That's rhythm, not force.

**Afi0:** Yeah. And rhythm is sustainable. Force burns you out.

**2K²:** This ties into something you said about mountains. You climb one mountain, reach the peak, and then realize there's another mountain. But the next mountain isn't even formed yet.

**Afi0:** Right. Because you haven't become the person who can see it clearly. That's how growth works;climb, gain perspective, let the next challenge reveal itself as you adapt.

**2K²:** And between the mountains, there's emptiness.

**Afi0:** Yeah. That's the void. When you finish one thing and you don't know what's next. Most people panic in the void. But the void is where integration happens.

**2K²:** So emptiness isn't failure. It's preparation.

**Afi0:** Exactly. It's the space where your brain processes everything you've learned and rebuilds your model of the world.

**2K²:** And then one day, insight clicks.

**Afi0:** Yeah. Like on New Year's night. I spent all of late 2025 wanting an insight but not knowing what it was. And then on New Year's, it hit me. And everything changed.

**2K²:** What was the insight?

**Afi0:** That I don't need to keep proving myself. I can just... be. And from that being, everything else flows.

**2K²:** That's self-actualization.

**Afi0:** Maybe. I don't know what to call it. I just know it feels right.

---

## [58:00 - 60:00] CLOSING

**2K²:** Alright man, we're coming up on time. Last question: what would you say to someone who's just starting in security? Someone who's listening to this and thinking, "I want to think like Afi0."

**Afi0:** [pauses] Don't try to think like me. Think like yourself. The whole point is to develop your own model, not copy someone else's.

**2K²:** But there must be some universal advice.

**Afi0:** Okay. Two things. First: break the model. Whatever you think you know about how systems work;question it. Test it. Don't trust documentation. Don't trust experts. Trust your own experiments.

**2K²:** And second?

**Afi0:** Know yourself. Because all the technical knowledge in the world won't help if you're fighting yourself internally. Do the shadow work. Integrate your archetypes. Find your rhythm. And then the technical stuff becomes easy.

**2K²:** That's beautiful. Afi0, this has been incredible, man. Where can people find you?

**Afi0:** I'm mostly just doing my own thing. But if people want to reach out, they can find me through my Medium articles.

**2K²:** Perfect. Alright everyone, that's the first episode of The Deep Dive. If you got value from this, share it with someone who needs to hear it. We're doing something different here;not just techniques, but the *thinking* behind the techniques.

Next episode, we're going even deeper. Until then, stay curious. Push boundaries. And remember;

**Afi0:** Break the model.

**2K²:** Break the model. Peace.

---

## [OUTRO MUSIC]

---

### TIMESTAMPS FOR YOUTUBE:
- 00:00 Cold Open: Emotional Compression State
- 02:00 Introduction
- 04:30 The Insight That Changes Everything
- 12:00 Breaking the Developer's Model
- 20:00 The Neuroscience of Flow & Shadow Integration
- 30:00 Biohacking the Brain: Gamma Waves & Archetypes
- 40:00 From Bug Bounty to Inner Peace
- 50:00 The Ouroboros & Cycles of Growth
- 58:00 Closing Advice

### SHOW NOTES:
- Afi0's Medium: [Articles on Security & Biohacking]
- Mentioned Concepts:
  - Kolmogorov Complexity
  - Jungian Psychology (Shadow, Archetypes, Individuation)
  - BDNF (Brain-Derived Neurotrophic Factor)
  - Gamma Wave States
  - Spectre Vulnerability
  - Heartbleed
  - Ouroboros Symbol
  - Flow State Research

### KEY QUOTES:
- "The system is hard if you look at it externally. But internally, it's easy."
- "You can practice for years, but if you don't have one key insight, it's all void."
- "When your emotions are compressed, they don't distract you;they drive you."
- "Shadow work isn't optional. You can't integrate what you don't face."
- "The final stage isn't being the best hacker. It's being at peace with yourself."
- "Break the model. That's where the real vulnerabilities live."
