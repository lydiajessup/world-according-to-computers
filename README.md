# world-according-to-computers

This is my submission for [NaNoGenMo 2019](https://github.com/NaNoGenMo/2019/issues) and was also made for Allison Parrish’s Computational Approaches to Narrative class.

Inspired by the book [Autumn by Karl Ove Knausgard](https://www.penguinrandomhouse.com/books/536250/autumn-by-karl-ove-knausgaard/) (KOK) in which he writes about a different object each day (for his unborn daughter in order to share the world with her), I decided to generate a novel using this same structure but from the computer’s perspective. With this exercise, I hoped to explore the following questions: what have computers learned about the world? And what would computers tell us about the world if we asked them about it in 2019?

I decided to use the [top 100 books from Project Gutenberg from the last 30 days](https://www.gutenberg.org/browse/scores/top#books-last30) as a proxy for all the things we have collectively been teaching computers (“computers” here is also a proxy for really what should be more specific questions about individual algorithms or computational systems).

I took the top 365 nouns from these books, one for each day of the year. Then I pulled out all the sentences that included each of these words to create a “corpus” for each object. For each object I then used markovify to generate 100-200 words “about” that object (5 sentences).

KOK starts his entries about objects often with technical descriptions (followed by more narrative-type text), so I looked into adding Wikipedia descriptions using the wikipedia python library. I had hoped that I would be able to easily add the first part of the corresponding entry, but got many errors because there was not always an exact match for a wikipedia entry. I tried to instead choose the next wikipedia entry, but often this would throw disambiguation errors too or lead to a very random description (about a song for example). For now I left these cases (32/365) blank if there was not a good match and I will plant to fix these in the next phase (I think I may have to fix them by hand unless I can think of a better way to do it computationally). For the ones that matched, I included the first three sentences of the wikipedia entry.

The output doesn’t make much sense, but I do find the juxtaposition of the technical text with the generated text interesting at times when they end up connecting or reflecting each other - in particular seeing which elements carry over. I also find it a fun exercise to try to guess which novels the generated text is pulling most from and thinking about why that is. I have kept the output in the order of most common to least common nouns, which gives another kind of insight into the type of source text this uses - I think it says a lot that the most common noun is “man”. My hope with this project is that these kinds of questions can prompt deeper thinking into what we are “teaching” computers and the care and intention we put into that act.

Also a disclaimer about the output: I have not edited this or even read all of it - it is purely output based on the input corpus!

### Next Steps:
In addition to the wikipedia library problem, there is more I’d like to do on this and plan to do so for the final project for this class. This includes:
* Fixing the punctuation (there are many out of place periods, etc)
* Cleaning up some of the chapter headings etc that got mixed in from the source text
* Adding images to supplement the text
* Possibly find a way to make the text more coherent and cohesive?
* Add a concluding sentence to each?

Thank you to [Allison Parrish](https://github.com/aparrish) for teaching this class and whose python tutorials and in-person consultation I leaned on heavily and Anthony Bui who also gave feedback during the ideation process.
