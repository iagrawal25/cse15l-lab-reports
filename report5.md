# Lab Report 5: Testing Commands
## Setting Up
- Today we will be testing out the _grep_ command.
- First, we will clone the repository [click here](https://github.com/ucsd-cse15l-w23/skill-demo1-data) to work with different files.

```
git clone https://github.com/ucsd-cse15l-w23/skill-demo1-data
```

```
Cloning into 'skill-demo1-data'...
remote: Enumerating objects: 237, done.
remote: Counting objects: 100% (237/237), done.
remote: Compressing objects: 100% (235/235), done.
remote: Total 237 (delta 0), reused 237 (delta 0), pack-reused 0
Receiving objects: 100% (237/237), 3.25 MiB | 5.58 MiB/s, done.
```

- Now, we have the files that we need to work with.

## Command 1

We will use _grep -o_ to count the number of occurrences of the provided pattern.. [(citation link)]([https://www.redhat.com/sysadmin/linux-find-command](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/))
```
grep -o India WhatToIndia.txt
```
- This searches for the word _India_ in the _WhatToIndia.txt_ file and returns the number of times it appears.

- Output

```
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India
India

```

Another example of the same thing:
```
grep -o France IntroFrance.txt
```
- This searches for the word _France_ in the _IntroFrance.txt_ file and returns its count.

- Output

```
France
France
France
France
France
France
France
France
France
France
France
France
France
France

```

## Command 2

_grep -n_ can be used to find the line number of a particular pattern [(citation link)]([https://www.redhat.com/sysadmin/linux-find-command](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/)). To do this, we write:
```
grep -n India WhatToIndia.txt
```
- This returns every line where the word _India_ is used. It also returns the line number in which the word appears.

- Output

```
8:        One thing the Indians enjoyed about the British was their
14:        India is still very active. Delhi in particular has very modern
36:        Fishing is very popular in India, and although it is almost
47:        marvellous way of getting away from the often madding crowd in India,
59:        the many clubs the Indians inherited from the British. Tennis lovers
64:        The most beloved sport in India, by far, is cricket.
66:        passion that appeals to the Indian people. It’s an astounding
73:        Hockey is a British import, in which the Indians have
84:        One of the many pleasant surprises in India is the way that
89:        A first encounter with Indian music is most likely to be in
113:        instrumental music, is religious and romantic in content. South Indian
116:        and without embellishment, to the more florid khyal, India’s version of
123:        Indian dance is marvelously expressive, with every gesture
137:        Indian legends in the most gorgeous costumes and elaborate makeup.
140:        eastern India is known as Odissi.
141:        Film in India, produced mainly in the cities of Chennai,
147:        stories of India’s cultural and historic past have considerable
149:        you can learn a lot about Indian people by what makes them cheer,
153:        Sen shown in Europe or North America than in India itself.
156:        to Lord Mountbatten, all have been seduced by India’s riches. It’s
158:        As in any ancient country, India’s modernizing plunge into
176:        see Indian motorists buying back spare parts stolen from their cars the
220:        Silks have long been basic to a fine Indian lady’s wardrobe
233:        the best bargain of all Indian textiles, made into tablecloths,
235:        that make life much more comfortable in the Indian heat. Indian tailors
249:        Indian diamond mines produced some of the world’s greatest gems,
259:        The essential piece of jewelry in India, however, is the
275:        to buy until your last day. The best places to buy Indian spices are

```

Another example of the same thing:
```
grep -n France IntroFrance.txt
```
- This returns every line where the word _India_ is used. It also returns the line number in which the word appears.

- Output

```
7:        For many years France was a nation of internal contrasts —
15:        escape the more frenetic life in the Ile de France; the number of
21:        France remains, however, a splendid and individualist
43:        France is blessed with an astonishing variety of landscapes:
47:        in the Côte d’Azur. All these are as typical of France as the more
75:        farmland of the Ile-de-France. And the Champagne area lies conveniently
110:        national parks and nature reserves. Evidence that France is far from
113:        France is internationally acknowledged to be a leader in
136:        France has always been a haven for foreign artists. Not by
139:        France. One of France’s greatest poets of the 20th century, Wilhelm
147:        the immigrants from France’s départements in the West Indies and from
152:        or first — homes in France; French young people are choosing to settle
156:        For the first-time visitor, France will seem at once

```

## Command 3

Now, we will use _grep -c_ to count a particular word in our file [(citation link)]([https://www.redhat.com/sysadmin/linux-find-command](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/)).
```
grep -c India WhatToIndia.txt
```
- This searches for the word _India_ in the file _WhatToIndia.txt_ and returns the count.

- Output

```
28
```

Now, we will try looking for a word in another file.
```
grep -c France IntroFrance.txt
```
- This searches for the word _France_ in the file _IntroFrance.txt_.

- Output

```
13
```

## Command 4

Now, we will use _grep -i_ to search for words. _grep -i_ ignored case distinctions in patterns and is case insensitive [(citation link)](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/).
```
grep -i LOOKOUT WhatToIndia.txt
```
- This searches for the word _LOOKOUT_ in the file _WhatToIndia.txt_.
- It ignores its case when returning the sentence where the word was found.

- Output

```
Cooks should be on the lookout for spices — chili,
```

Let's try this again with a different file.
```
grep -i PaRis IntroFrance.txt
```
- Again, this searches for _PaRis_ irrespective of the case.

- Output

```
between chic Paris and the less sophisticated provincial cities — and a
Much has changed in recent times. Paris is no longer the
the geographical center, Paris nestles in a basin ideal for industrial
While Paris is still a major destination for sightseers,
Valley, east of Paris, was selected for Europe’s first Disneyland.
l’Industrie in La Villette, on the outskirts of Paris, attracts science
the pious Breton and the pagan sophisticate of Paris.
in the international but inexorably Paris-based language of haute
```
