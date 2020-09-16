# 백석과 윤동주
백석의 시와 윤동주 시에 존재하는 명사들을 Vector화 시키고 각 단어 Vector간 거리를 Embedding Projector를 통해 시각화 하였다.

# [Embedding Projector Link][embeddinglink]

[embeddinglink]: https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/lee-marco/poet_korean/master/poet_config.json "Go Embedding Projector"

- Embedding Projector 에서 단어를 클릭하면 해당 단어와 가장 근접한 거리 순서로 단어 목록이 표시됩니다.

- 근접 결과 목록 중 단어 하나를 클릭하면 해당 클릭 단어와 가장 유사한 단어 목록으로 변경되어 표시됩니다.

- 만들어진 Vector는 단순 3차원이 아니라 100 차원의 좌표계 표시를 3차원으로 단순화 한 것이기 때문에 절대적인 거리가 작을 때 실제 그래프에 가깝게 표시되지 않습니다.

- 우측의 Search를 통해 특정 단어를 검색하여 유사한 단어를 찾을 수 있습니다.

# File
- poet_vectorize.ipynb : 백석과 윤동주의 시에서 명사만 추출하여 vector화 한 후 파일로 저장하는 코드

- poet_korean : 벡터화 완료된 결과가 저장되어있는 파일

- poet_korean_metadata.tsv : Embedding Projector로 시각화를 위한 명사 메타데이터 저장 파일

- poet_korean_tensor.tsv : Embedding Projector 시각화를 위한 명사의 Vector 값 저장 파일

- poet_config.json : Embedding Projector에서 위의 두 파일을 읽어오기 위한 설정 파일

# 활용 명령어
- 벡터화 완료된 결과 파일에서 메타데이터와 벡터값 파일을 생성하기 위해 아래의 명령어를 실행
><pre><code>python -m gensim.scripts.word2vec2tensor -input "poet_korean" -output "poet_korean"</code></pre>
