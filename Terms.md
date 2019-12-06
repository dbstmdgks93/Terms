# Terms

## Interleave (인터리브)

인터리브는 성능을 높이기 위해 [데이터](http://www.terms.co.kr/data.htm)가 서로 인접하지 않도록 배열하는 방법이다. [하드디스크 드라이브](http://www.terms.co.kr/HDD.htm)에 대해 인터리브를 설명한다면, 그것은 디스크 상의 [섹터](http://www.terms.co.kr/sector.htm)가 구성되는 방법을 가리킨다. 

1 : 1 인터리빙에서, 섹터들은 각 [트랙](http://www.terms.co.kr/track.htm)을 따라 차례대로 배치된다. 

2 : 1 인터리빙에서, 섹터들은 서로 엇갈려서 번호가 연속되는 섹터들은 사이에 끼여있는 섹터들에 의해 분리된다. 즉, 하드디스크의 섹터번호와 배치 순서를 보면 1 : 1에서는 0, 1, 2, 3 의 순서로 배치되는 데 반해, 2 : 1에서는 하나씩 건너뛰어서 0, 4, 1, 5, 2, 6, 3, 7 ... 의 순서로 배치된다.

인터리빙의 목적은 디스크 드라이브를 좀더 효율적으로 만들기 위한 것이다. 디스크 드라이브는 한번에 오직 한 개의 섹터만을 [액세스](http://www.terms.co.kr/access.htm)할 수 있으며, 디스크는 읽기/쓰기 헤드의 바로 아래서 끊임없이 돌고 있다. 이것은 드라이브가 다음 섹터에 액세스할 준비가 되는 시간에, 디스크는 이미 그 섹터를 지나쳐 갈수 있다는 뜻이다. 만약, 데이터 파일이 하나 이상의 섹터에 걸쳐있고, 그 섹터가 차례대로 배열되어 있다면, 드라이브는 그 파일의 나머지 부분을 액세스하기 위해 한 바퀴를 그냥 기다려야할 것이다. 만약 그 대신에 섹터들이 엇갈려 있다면, 디스크는 연속적인 섹터를 액세스하기 위한 완전한 위치에 가 있게 될 것이다.

최적의 인터리빙율은 디스크 드라이브의 속도, [운영체계](http://www.terms.co.kr/OS.htm) 그리고 응용프로그램 등에 달려있다. 가장 좋은 인터리빙율을 알아내기 위한 유일한 방법은 여러 가지 요소들과 여러 가지 [응용프로그램](http://www.terms.co.kr/application.htm)들로 시험해보는 것이다. [메모리](http://www.terms.co.kr/memory.htm)도 역시 인터리브될 수 있다.

출처 : http://www.terms.co.kr/interleave.htm

경고 : SIFT meets CNN 논문을 읽다가 찾아보았는데 이게 논문에서 나온 단어와 같은 의미인지 아직 파악되지 않았음

## ANN(approximate nearest neighbor)

최근접 이웃탐색. 
https://en.wikipedia.org/wiki/Nearest_neighbor_search#Approximate_nearest_neighbor
https://brunch.co.kr/@goodvc78/15
https://www.slideshare.net/erikbern/approximate-nearest-neighbor-methods-and-vector-models-nyc-ml-meetup
https://github.com/spotify/annoy

ANN 연산은 brute force할 때 Vector의 개수만큼 유사도 비교 연산을 필요로 한다. 그런데 Vector의 수가 1M이 넘어가기 시작하면 서버로 때우기 힘들어진다. 그리고 Vector가 현재 일반적인 사비스에서 100~1000차원이 되기 때문에 데이터 규모에 따라 연산량이 폭발한다.

그래서 github.com/spotify에서는 100%는 아니지만 높은 정확도로 근접벡터를 찾아주는 오픈소스 Annoy(Approximate Nearest Neighbors Oh Yeah) 라는걸 만들었다고 한다.



