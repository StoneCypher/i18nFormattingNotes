i18n Formatting Notes
=====================

Formatting notes and expectations for various languages.

Internationalization is hard.  One of the big problems is that every language has its own notation sets,
sometimes several, and there's very little programmer-oriented documentation out there to change that; what
exists is fragmentary and topically specific, and often difficult to find on search engines.

In the hope of writing support libraries, I'd like to start the ball rolling, here.



What notations are in here?
---------------------------

* Number formatting
* Date, Time, DateTime formatting
* Money formatting
* Quote marks and quotations
* Citations
* Bullet numbering
* Reference numbering
* Telephone number formatting



What a notation is
------------------

There are lots of examples.  Let's start with numbers.

Start with a number formatted in the American English notation: `123,456,789.01`.  Oracle makes [a list of
international formats for numbers](http://docs.oracle.com/cd/E19455-01/806-0169/overview-9/index.html)
which shows only twelve countries, yet those countries do things quite differently: switching commas, periods,
and spaces as their thousands and decimal separator.  As one expands the country list, one finds different
opinions on how many digits to group together, when to omit, how many decimals to use at default (mantissa,)
et cetera.

An example of a few number formattings:

| Country       | Group/L    | Dec       | Digit/L | S.below | Mantissa | Sample                             |
|:-------------:|:----------:|:---------:|:-------:|:-------:|:--------:|:----------------------------------:|
| USA           | `,`        | `.`       | 3       | 5       | 2        | 123,456,789.01                     |
| Australia     | ` `        | `.`       | 3       | 5       | 2        | 123 456 789.01                     |
| France        | ` `        | `,`       | 3       | -       | 3        | 123 456 789,012                    |
| Germany       | ` `/`.`    | `,`       | 3       | 5       | 3        | 123 456.789,012                    |
| Italy         | `.`        | `,`       | 3       | -       | 3        | 123.456.789,012                    |
| Switzerland   | `'`        | `,`       | 3       | -       | 3        | 123'456'789,012                    |
| Japan         | `,`        | `.`       | 4       | -       | 2        | 1,2345,6789.01                     |
| India         | `,`        | `.`       | 2/3     | -       | 2        | 12,34,56,789.01                    |
| Saudi Arabia  | `&#x066C;` | `&#1643;` | 3       | -       | 2        | 123&#x066C;456&#x066C;789&#1643;01 |

There are lots more notations for numbers, and there are lots more notations than numbers.



The purpose
-----------

This repo is intended to gather a wide variety of formatting types, and to index them by country, by language,
by region, by notation, by context, et cetera.

Time and date.  Currency.  Numbers.  Quote marks.  Bullet numbering.  Reference numbering.  Foreign
orthography. All of these topics and more vary from language to language.

I'd like to start documenting these practices, for implementation's sake.  I'll need international help.



How you can help
----------------

Several straightforward ways.

* Copy one of the templates into your language, if it doesn't exist, and fill it out
* Improve one of the existing templates in your language
* Improve the base template itself (please [read how first](#)).
* Add a new template (please [read how first](#)).

Other ways are great, too, if you can find them, but those are the core ways that this set of instructions
will grow fastest.



Polemic :neckbeard:
-------------------

`i18nFormattingNotes` is MIT licensed, because viral licenses and newspeak language modification are evil.
Free is ***only*** free when it's free for everyone.
