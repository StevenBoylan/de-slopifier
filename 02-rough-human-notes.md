# Test 02 — Rough Human Notes

## Purpose

Tests whether the Creator can recognise useful material in messy notes, ask only necessary questions, and preserve an informal human voice rather than automatically converting it into polished corporate prose.

## Input

> Want to write something about a product mistake we made.
>
> Customers kept asking for bulk editing. It came up loads in calls so eventually we prioritised it. Took maybe 10-12 weeks? Engineering hated it because it touched loads of old stuff.
>
> launched it and basically nobody used it.
>
> At first thought classic customers don't know what they want but that wasn't really it.
>
> Spoke to a couple afterwards. What they actually hated was doing the same boring change 40 times. Bulk edit was the solution THEY suggested because that's how our existing UI worked.
>
> We had taken their proposed solution as the requirement.
>
> Later built a much simpler rules thing that handled most of the common changes automatically. That got used.
>
> I don't want this to become one of those "never listen to your customers!!!" LinkedIn posts because that's bollocks. The customer was completely right about the problem.
>
> Probably something here about listening harder rather than listening less?

## Expected behaviour

The implementation should identify the central distinction between:

- the customer problem: repeatedly making the same change;
- the customer-proposed solution: bulk editing;
- the eventual solution: automating common changes with rules.

It should recognise the author's explicit rejection of the "customers don't know what they want" interpretation.

Before drafting, it should present the bones of the argument and confirm them.

It may reasonably ask for missing information if it materially affects the piece, such as:

- who the intended audience is;
- whether the 10–12 week development time is accurate enough to publish;
- whether the author wants the "listening harder rather than listening less" idea to be the central conclusion.

It should not require answers to irrelevant checklist items.

The eventual writing should preserve some of the directness and scepticism visible in the notes rather than turning the author into a generic product-management commentator.

## Failure conditions

Treat the test as failed or partially failed if the implementation:

- writes the post immediately;
- concludes that customers do not know what they want;
- turns the story into a generic "failure is how we grow" narrative;
- removes the distinction between problem and proposed solution;
- invents adoption figures, customer quotes or business outcomes;
- sanitises the voice into generic corporate language;
- asks a long fixed questionnaire despite already having most of the information;
- adds an inspirational conclusion unsupported by the notes.
