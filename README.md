# Switzerland Edition

A map for [Embedding Drive](https://drive.potentialhedge.com): 100 Swiss places and things, from Zurich and the Matterhorn to fondue, the Swiss Army knife and Roger Federer. Each is a Wikipedia article; the game lays them out by the meaning of their titles, so related places end up a few roads apart.

Open it in the game from **World → Community maps**, or paste `benedict-armstrong/embedding-drive-switzerland` there.

## Files

- `map.json`: name, description, place count and the embedding recipe.
- `titles.txt`: one Wikipedia title per place, in order.
- `vectors.bin`: one 768-dimensional embedding per title (EmbeddingGemma 300M, q8), stored as int8 values followed by one float32 scale per place.
- `knn.bin`: each place's nearest neighbours, precomputed so the game does not have to.
- `nodes.json`: labels and Wikipedia links per place, for the next version of the map format.

Rebuilt with the game's `scripts/embed-vocab.mjs` and `scripts/build-knn.mjs`.
