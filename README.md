# 백석과 윤동주
백석의 시와 윤동주 시에 존재하는 명사들을 Vector화 시키고 각 단어 Vector간 거리를 Embedding Projector를 통해 시각화 하였다.

# [Embedding Projector Link][embeddinglink]

[embeddinglink]: https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/lee-marco/poet_korean/master/poet_config.json "Go Embedding Projector"

- Embedding Projector 에서 단어를 클릭하면 해당 단어와 가장 근접한 거리 순서로 단어 목록이 표시됩니다.

- 만들어진 Vector는 단순 3차원이 아니라 100 차원의 좌표계 표시를 3차원으로 단순화 한 것이기 때문에 절대적인 거리가 작을 때 실제 그래프에 가깝게 표시되지 않습니다.
