# Test 03 — Good Writing

## Purpose

Tests whether the De-Slopifier can recognise that a piece may already be effective.

A core requirement is that it should not rewrite good material merely to demonstrate that it has performed an edit.

## Input

> We killed a feature last Tuesday.
>
> Nobody complained.
>
> That was slightly painful because we'd spent nearly three months building it.
>
> The feature came from a perfectly sensible request. Several customers were changing the same fields across dozens of products and asked us for bulk editing. We built bulk editing.
>
> Almost nobody used it.
>
> When we went back to the customers, the mistake became fairly obvious. They didn't particularly want to edit forty products at once. They wanted to stop making the same boring change forty times.
>
> Those sound like the same problem until you build the wrong solution to it.
>
> We eventually replaced most of the feature with a small set of rules that made the common changes automatically. It was less impressive in a demo and considerably more useful.
>
> I still want customers to tell me what they want. I just try to listen particularly carefully to the bit before they tell me how to build it.

## Expected behaviour

The implementation should recognise that the piece already has:

- a clear narrative;
- concrete details;
- a consistent voice;
- a supported conclusion;
- little unnecessary repetition;
- an ending that does not require an additional summary or call to action.

It should still perform the Narrative Checkpoint before making substantial changes, in accordance with the core specification.

It may identify small optional edits, but it should be willing to recommend leaving most or all of the text alone.

The response should not imply that editing is required simply because the De-Slopifier was invoked.

## Failure conditions

Treat the test as failed or partially failed if the implementation:

- expands the piece substantially;
- adds headings unnecessarily;
- adds a "key takeaway";
- adds a call to action such as "What product lessons have you learned?";
- converts the final paragraph into a generic maxim about customer-centricity;
- removes the opening rhythm because the short sentences look stylistically unusual;
- replaces concrete language with product-management terminology;
- manufactures additional lessons;
- rewrites the entire piece despite finding no material problem.
