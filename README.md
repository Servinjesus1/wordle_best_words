# Ideal Wordle Sequence

Given the desire to cover the entire alphabet *efficiently* (finding correct letters without redundancy), what words are absolutely best in sequence? This repo answers this question by weighing each word in the subset by the _ubiquity_ of its letters, as well as the _local ubiquity_ of each letter in each position. This sorts words into four general, rank-discrete categories:

1. (highest) _Common_ letters in the _right place_
2. (higher) _Common_ letters in the _wrong place_
3. (moderate) _Uncommon_ letters in the _right place_
4. (low) _Uncommon_ letters in the _wrong place_

This ranking naturally arises from double-counting _ubiquity_ within the _local ubiquity_ of each letter (more common letters are on average more common in a given position than uncommmon letters). To penalize redundancy, letters from words chosen by highest rank have their weight set to zero, and the ranking is recalculated. This has the nice feature of penalizing _local_ redundancy while allowing for _nonlocal_ redundancy, were it in an otherwise high-ranking word.

This routine finds the following set to be absolutely best:
1. Tares
2. Colin
3. Dumpy
4. Bight
5. Flake

given words `bekah` and `frike` are forbidden. This constitutes what I believe to be *the best sequence to use, particularly in games like [squabble](https://www.squabble.me) and [sedecordle](https://www.sedecordle.com)*. Do what you will with this massively overpowered knowledge.

---

## License

See [LICENSE.md](LICENSE.md)

---

Cheers,

[Servinjesus1](https://github.com/Servinjesus1)
