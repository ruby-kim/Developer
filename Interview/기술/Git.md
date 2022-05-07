# Git

<details>
  <summary><strong>Git이란?</strong></summary>
  <ul>
    <li>Git은 분산 버전 관리 시스템 (VCS)로, 프로젝트 파일의 변경 사항을 추적하는 시스템</li>
    <li>프로젝트의 변경 사항을 기록하고, 특정 시점의 버전으로 언제든 돌아갈 수 있다</li>
    <li>많은 사람들이 효율적으로 함께 작업하고, 프로젝트를 중심으로 협업할 때 사용한다</li>
  </ul>
</details>

<details>
  <summary><strong>Repository란?</strong></summary>
  <ul>
    <li>Git으로 관리하는 프로젝트 저장소</li>
    <li>Local respository: 자신의 컴퓨터에 저장된 로컬 버전의 프로젝트 저장소</li>
    <li>Remote repository: 원격 서버의 프로젝트 저장소
      <ul>
        <li>팀 협업시에 많이 사용하며, 프로젝트 코드를 공유할 수 있고 다른 사람의 코드도 확인할 수 있다</li>
        <li>로컬 버전의 프로젝트와 병합하고, 변경 사항을 적용할 수 있다</li>
      </ul>
    </li>
  </ul>
</details>

<details>
  <summary><strong>Commit이란?</strong></summary>
  <ul>
    <li>프로젝트의 현재 상태를 나타내는 체크포인트 또는 스냅샷</li>
    <li>커밋 히스토리에 필요한 만큼 커밋을 생성 할 수 있고, 커밋 내역들을 살펴보며 코드의 변경사항을 확인할 수 있다</li>
  </ul>
</details>

<details>
  <summary><strong>Branch란?</strong></summary>
  <ul>
    <li>독립적으로 어떤 작업을 진행하기 위한 개념</li>
    <li>다른 브랜치의 영향을 받지 않기 때문에 필요 시 여러 작업을 동시에 진행 할 수 있다.</li>
    <li>보통 Git Flow에 따라 feature, release, hotfix라는 접두사를 붙인다.</li>
  </ul>
</details>

<details>
  <summary><strong>Git Flow란?</strong></summary>
  <ul>
    <li>Git Flow는 Vincent Drissen이 시작한 Git 사용 방법론</li>
    <li>master, develop, 그리고 3가지의 접두사를 이용해서 운영한다:</li>
    <ul>
        <li>master: 기준이 되는 브랜치로 제품을 배포하는 브랜치</li>
        <li>develop: 개발 브랜치로 개발자들이 이 브랜치를 기준으로 각자 작업한 기능들을 병합(merge)한다.</li>
        <li>feature: 단위 기능을 개발하는 브랜치로 기능 개발이 완료되면 develop 브랜치에 합친다.</li>
        <li>release: 배포를 위해 master 브랜치로 보내기 전에 먼저 QA(Quality Assurance, 품질 검사)를 하기위한 브랜치이다.</li>
        <li>hotfix: master 브랜치로 배포를 했는데 버그가 생겼을 때 긴급 수정하는 브랜치이다.</li>
      </ul>
  </ul>
</details>

<details>
  <summary><strong>Git vs GitHub</strong></summary>
  <ul>
    <li>Git은 버전 관리 시스템으로, 시간이 지남에 따라 파일의 변경 사항을 추적하는 도구</li>
    <li>GitHub은 Git을 사용하는 프로젝트를 위한 호스팅 서비스</li>
  </ul>
</details>

<details>
  <summary><strong>Pull Request(PR)란?</strong></summary>
  <ul>
    <li>자신이 작업한 브랜치 작업 내용을 특정 브랜치에 반영해달라는 요청</li>
    <li>PR 요청 시 프로젝트 오너 또는 팀 리더에게 리뷰를 받을 수 있고, 그 과정에서 버그나 컨플릭트가 있다면 다시 수정해서 요청할 수 있다.<br> 병합되기에 아무런 문제가 없다면 머지 권한이 있는 개발자가 병합을 진행한다</li>
  </ul>
</details>

<details>
  <summary><strong>Conflicts란?</strong></summary>
  <ul>
    <li>어떤 파일의 변경 사항이 기준이 되는 특정 브랜치의 파일과 겹쳐, Git에서 어떤 버전의 코드를 선택해야 할지 모를 때 발생하는 것</li>
    <li>충돌이 발생한다면, 개발자가 직접 코드를 비교해 충돌을 해결하고 merge를 마무리 해야한다:</li>
      <ul>
        <li>1) git fetch</li>
        <li>2) git pull</li>
        <li>3) merge conflict가 있을 시 직접 수정</li>
      </ul>
  </ul>
</details>

<details>
  <summary><strong>Git Rebase란?</strong></summary>
  <ul>
    <li>일련의 커밋들을 새로운 베이스 커밋으로 옮기거나 합치는 과정</li>
    <li>rebase를 해서 git history를 정리하기 때문에 필요 내용만 확인할 수 있다. (상대 개발자 배려)</li>
  </ul>
</details>

<details>
  <summary><strong>Git merge vs rebase</strong></summary>
  <ul>
    <li>이 두 명령 다 한 브랜치에서 다른 브랜치로, 변경 사항들을 통합하기 위해 디자인 됬다.</li>
    <li>즉, 두 명령은 비슷하지만 다른 방법으로 사용되는 것이다.</li>
  </ul>
</details>

<details>
  <summary><strong>Squash vs Reward</strong></summary>
  <ul>
    <li>Squash와 Reward는 커밋 히스토리를 조정하는 기능이다.<br>사소한 커밋들이 여러번 있다면, 이 커밋을 큰 하나의 커밋으로 변경할 수 있다.</li>
    <li>squash: 커밋을 합치기</li>
    <li>reward: 커밋은 남겨두고 메시지만 수정</li>
  </ul>
</details>
