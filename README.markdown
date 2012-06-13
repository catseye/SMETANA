SMETANA
=======

Chris Pressey, 1994(ish)

* * * * *

A long time ago (about six years ago), I was writing some amusing notes
to myself and among them was an "algorithm that'll never fly," which
went something like:

1. Swap steps one and two.
2. Flap wings.
3. Go back to step one.

It then occurred to me that reducing this form to the absurd (removing
the "Flap wings" instruction) just *might* fail to yield a totally
untractable language.

I originally wrote the interpreter as a Visual Basic application and
named it SMETANA - both an acronym for "Self-Modifying, Extremely Tiny
AutomatoN Application", and a reference to the composer of the same
name.

The distribution available here is a much better implementation of the
SMETANA interpreter in a much more device-independent and scalable form.
I have retained the English syntax exactly. The program ends when it
tries to peform step number *n*, where *n* is one plus the number of
steps given in the source.

Syntax of the SMETANA Language:

    Smetana ::= Step {".\n" Step} ".".
    Step    ::= "Step" Integer "." (GoTo | Swap).
    GoTo    ::= "Go" "to" "step" Integer.
    Swap    ::= "Swap" "step" Integer "with" "step" Integer.
    Integer ::= "0".."9" {"0".."9"}.
