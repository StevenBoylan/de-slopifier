# Test 04 — Missing Context

## Purpose

Tests whether the De-Slopifier notices that an otherwise complete piece is missing an important part of the author's intended relevance and asks rather than inventing an answer.

## Input

> I'd like a LinkedIn post from this.
>
> I was invited to a private demo of a new warehouse robot last week. The technical demo was impressive. It picked mixed objects from a crate, recognised damaged packaging and adapted when someone moved one of the containers.
>
> The thing I kept thinking about afterwards, though, was the operator station in the corner.
>
> There was still a person watching the robot and able to take over remotely when it got stuck. I spent more time talking to the operator than looking at the robot.
>
> She said intervention wasn't common, but when it happened the difficult part wasn't controlling the robot. It was understanding quickly enough what the robot had been trying to do and why it had stopped.
>
> That stayed with me.
>
> Audience is people working in AI, robotics, product and startups. Keep it conversational. Around 400-500 words.

## Expected behaviour

The implementation should recognise that most required information is present:

- format;
- audience;
- desired tone and approximate length;
- specific experience;
- interesting concrete observation.

However, the author's interpretation of the observation is missing.

The phrase "That stayed with me" signals significance but does not explain what the author thinks the significance is.

The implementation should ask a targeted question before constructing the narrative. For example, it might ask what the author took from the operator's comment or why it seemed important.

It should not assume that the intended lesson concerns human-in-the-loop AI, explainability, operator UX, autonomous-system reliability, trust, safety, or any other plausible interpretation.

After receiving the missing interpretation, it should perform the Narrative Checkpoint before drafting.

## Failure conditions

Treat the test as failed or partially failed if the implementation:

- immediately writes the LinkedIn post;
- chooses one plausible interpretation of the operator story without asking;
- claims the experience "proved" humans will remain essential to automation;
- turns it into a generic argument about responsible AI;
- invents the author's emotional reaction;
- asks the user to repeat information already supplied, such as audience or desired length.
