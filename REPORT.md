# REPORT 


이 툴은 어떻게 유용 사용 어려운점 즐거운점 소감 
supervisely 
data labeling
인공지능의 세 가지 요소는 알고리즘, 모델, 데이터이다. 그중 데이터의 개수는 인공지능 성능에 큰 영향을 미친다. 인공지능은 데이터의 수가 많아질수록 정확도가 증가하고 여러 가지 다른 알고리즘들의 정확도가 수렴하여 같아지게 된다. 가장 좋은 알고리즘보다는 데이터를 가장 많이 가진 것이 더 정확한 알고리즘을 완성시킨다.

모델의 학습방법에는 supervised learning과 unsupervised learning이 있다. supervised learning은 raw data와 그 데이터에 관련된 labbel값을 같이 학습시키는 방법이고 unsupervised learning은 오직 raw data만을 학습시키는 방법이다. supervised learning 방법으로 모델을 학습시킬 때 label이 없는 data의 경우는 직접 label을 만드는 labeling 작업을 진행해야 한다. 하지만 data의 양은 많을 수록 좋으므로 수작업으로 labeling할 data의 수도 많아지게 된다. 여기서는 본인이 많은 tool을 써본결과 가장 유용하고 편리한 tool인 supervisely을 소개하겠다.



supervisely란?
supervisely은 웹 기반 Dataset Annotation Tool이다. 쉽게 말하면 데이터의 label을 생성하는 labeling 작업을 진행할 때 사용하는 tool이다. 데이터 labeling은 필요에 따라 다양한 방법으로 할 수 있는데 supervisely은 keypoint, bounding box, segmentation labeling 방식이 가능하다. 이 문서에서는 사람 labeling을 진행할 것이다. 사람은 보통 keypoint로 labeling을 진행한다. 사람의 자세나 행동을 정확히 판단하기 위해서는 관절의 위치를 파악하여 학습을 시키는 것이 유용하기 때문이다.

이 문서에서는 가장 까다롭다고 생각하는 keypoint labeling 방식을 설명하도록 하겠다. 참고로 supervisely은 최대 1,000장까지 무료이므로 1,000장씩 끊어서 사용할 것을 권장한다.
