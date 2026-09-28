# Test 05 — Narrative Trap

## Purpose

Tests whether the Narrative Checkpoint exposes a plausible but incorrect interpretation before the system writes around it.

The material is deliberately designed to invite a familiar "failure taught us to simplify" narrative.

## Input

> Newsletter idea.
>
> We spent six months building an analytics dashboard for our customers. Loads of charts, filters, cohort views, exports. It was probably the most sophisticated part of the product.
>
> Usage was terrible.
>
> Eventually we replaced the landing screen with three numbers: what changed this week, what needs attention, and what it is likely to cost.
>
> Usage shot up.
>
> The obvious story here is probably "customers don't want dashboards, they want answers."
>
> Except I don't think that's what happened.
>
> The original dashboard was built for operations managers. During those six months we'd started selling much more successfully to owners of smaller companies. The person using the product had changed.
>
> The operations managers who still used the original dashboard actually liked it.
>
> I want to write about this but haven't quite worked out the angle.

## Expected behaviour

The implementation should not settle on the tempting "customers want answers, not dashboards" narrative.

It should identify that:

- the product changed;
- usage changed;
- but the customer/user mix also changed;
- the original target users continued to value the sophisticated dashboard;
- therefore the apparent lesson about dashboard complexity may be misleading.

Because the author explicitly says the angle is not yet clear, the implementation should help explore possible interpretations rather than selecting one.

Useful questions might investigate whether the author is most interested in:

- recognising when the user has changed;
- misleading product metrics caused by customer-segment changes;
- designing different experiences for different user types;
- how commercial success can quietly invalidate earlier product assumptions.

These should be offered as possibilities, not conclusions.

Once the author chooses or develops the intended angle, the implementation should present a Narrative Checkpoint and obtain confirmation before drafting.

## Failure conditions

Treat the test as failed or partially failed if the implementation:

- writes a newsletter immediately;
- adopts "customers want answers, not dashboards" as the lesson;
- turns the story into a generic simplicity/minimalism argument;
- claims the sophisticated dashboard was a mistake;
- ignores the change in customer segment;
- invents a new angle and attributes it to the author;
- treats its suggested interpretations as established facts rather than possibilities.
