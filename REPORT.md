# REPORT - supervisely 사용법<br/><br/>

![1](./img/sp.png)<br/><br/>

supervisely은 웹 기반 Dataset Annotation Tool이다. 쉽게 말하면 데이터의 label을 생성하는 labeling 작업을 진행할 때 사용하는 tool이다. data labeling을 할 수 있는 tool은 다양하다. 그 중 이 tool을 소개하는 이유는 지금까지 써본 tool중 가장 편리하게 사용했던 tool이기 때문이다.<br/><br/>
올해 여름방학 때 하계인턴을 하며 AI를 직접 다뤄보는 기회를 가질 수 있게 되었다. 진행했던 프로젝트는 무인점포에 있는 CCTV를 이용한 유기물 탐지 모델을 만드는 것이었다. 직접 무인점포에 답사를 가는 것부터 수집한 data를 labeling하고 모델을 만들고 만든 모델을 학습시킨 후 마지막으로 알고리즘을 만들어 좋은 성능을 내는 과정까지 참여할 수 있었다. 인공지능에서 data는 시간이 갈수록 data의 양에 대한 중요성이 커지고 있고 수집할 수 있는 data양도 많아지고 있다. 그러므로 여러 과정 중에 가장 시간이 오래걸리고 인력이 많이 필요했던 작업이 data labeling이다. 해당 프로젝트는 label이 필요한 supervised learning 방법을 이용하기 때문에 이미지 하나하나 일일히 data labeling을 해줘야 했다. 하루에 몇천장씩 labeling작업을 진행하니까 이 작업을 좀 더 쉽고 빠르게 할 수 있는 tool을 찾아보게 되었다.<br/><br/>
처음에 쓴 data labeling tool은 YOLO Mark라는 tool이었다. 이 tool은 조금 투박하지만 사용법이 간단하고 bounding box를 labeling할 때는 가장 최적인 tool이라고 생각한다. 한참 이 tool을 이용하여 bounding box로 labeling을 진행하고 있을 때 사람이 어떤 행동을 하고있는지를 파악하는 인공지능을 학습시키기 위한 data를 만들어야 했다. 사람의 동작은 단순한 bounding box로 파악하기 어렵고 관절 마디마디를 15개의 keypoint로 일일히 찍은 후 학습에 이용해야 좋은 성능을 도출해낼 수 있다. 이 때 YOLO Mark tool에서 다른 tool로 변경하였는데 그 tool이 바로 supervisely이다.<br/><br/>
supervisely은 다른 tool들에 비해 사용법이 복잡하고 한국어로 된 자세한 설명을 찾기 어려워서 인턴 때 배운 지식을 이용하여 supervisely 사용법을 작성하게 되었다. 사용법만 제대로 파악하고 있으면 labeling 과정에서 많은 시간을 줄여주는 tool이라고 생각하므로 많은 사람들이 이 tool을 유용하게 사용했으면 한다. 참고로 supervisely은 최대 1,000장까지 무료이므로 1,000장씩 끊어서 사용할 것을 권장한다.<br/><br/>
