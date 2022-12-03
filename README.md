<h1>CPOW</h1>
<h2>Competitive Proof Of Work</h2>
<div align = left>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"> 
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white"> 
  <img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white"> 
  <img src="https://img.shields.io/badge/Blockchain-AB300?style=for-the-badge&logo=bitcoin&logoColor=white"> 
</div>

<h3>CPOW의 구조</h3>

  하나의 블록이 만들어지기 까지의 프로세스는 크게 세 개의 Round로 이루어진다. 첫Round의 채굴연산에서 첫번째로 정답을 도출한 노드는 다른 노드를 통해 검증을 받게 된다. 일반적인 PoW는 검증을 마치고 바로 체인에 블록을 올리지만, CPoW에서는 1등 노드 하나만 뽑고 끝나는 것이 아니라 참여 노드의 일정 비율만큼의 정답자를 더 받는다. 이 비율을 SNR(Survived Node Rate)라 지정했으며, 한 프로세스 내에 다음 Round로 넘어가는 과정에서 적용된다.
  
  문제를 해결한 노드들은 검증과정에서 각 노드의 선착순 배열에 들어가게 되며, 이 배열이 식(1)의 과정이 되면 해당 라운드는 종료됨과 동시에 1등노드가 블록을 생성한다. 선착순 배열에 있는 노드들을 대상으로 다음 Round에서 채굴을 진행하며, 총 세 개의 Round 동안 같은 채굴과정을 반복한다. 따라서 한 프로세스 내 총 세 개의 블록이 체결된다. 리워드는 Round 3에서 블록을 체결한 노드가 가지게 된다. 기존 PoW는 각 노드마다 해시연산 시 이전 해시 이외에 nonce만 달랐지만 CPoW는 nonce와 본인의 IP를 추가하여 각각 푸는 문제를 다르게 설계하였다
