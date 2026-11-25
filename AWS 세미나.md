Claude Code Deep Dive

서울시 공공데이터?


모델 + 도구 = 에이전트(클로드 코드) / 유닉스 쉘
검색 후, 추론 모델 동작(사고 레벨)

도구, 권한, 컨텍스트를 다루는 이 실행 틀이 하네스

총 8개의 하네스 엔진이 돌아감. (없으면, 외부 데이터를 가져옴)

Skill이나 MCP는 필요한 만큼만 올려 놓고 사용 (토큰 낭비)


내 로컬에 있는 스킬을 MCP에서 쓸 수 있게 만들었음.

캐시 사용(1시간) 동안만 동작함.
Compact를 하든, 빠져 나오는게 좋음.

Cluade md 파일은 200 줄 이하로

클라우드 인프라

사내망에서 Bedrock으로 구성 되어 있음
IAM, 키 대신 SSO, 모델 고정

Setting.json을 노리는 공격은 어떻게 하나?
일부로 변경하는 경우는 없는건가?
서명을 타서 문제가 없나??
수정 못함...


AWS Configure
Access_Key를 사용하여 외부에서 사용
기본 SSO 로그인을 사용
콘솔 자격 증명
Bedrock API 키


MDM 배포 도구 (JAMF)

Deny 설정부터 걸러진다?


아래 순서로 정책 우선순위
Managed
CLI 인자
Local
Project
User


