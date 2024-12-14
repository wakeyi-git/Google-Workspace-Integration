아래는 옵시디언 플러그인에 대한 README.md 파일 예제입니다. 플러그인의 주요 정보를 사용자와 개발자에게 제공하며, GitHub에 게시할 때 유용합니다.

Google Workspace Integration

Google Workspace Integration은 Obsidian과 Google Workspace를 통합하는 플러그인입니다.
이 플러그인은 Google Calendar, Tasks, Drive와 연동하여 생산성을 향상시키는 데 도움을 줍니다.

기능

1. Google Calendar 통합
	•	노트에서 #calendar 구문을 인식하여 Google Calendar에 이벤트를 자동으로 생성합니다.

#calendar/Meeting @2024-12-15 14:00-15:00


	•	이벤트의 제목, 날짜, 시간, 설명을 지원합니다.

2. Google Tasks 통합
	•	#task 구문을 인식하여 Google Tasks에 작업을 추가합니다.

#task/Buy groceries "Milk, eggs, bread" @2024-12-20


	•	작업의 제목, 메모, 마감일을 설정할 수 있습니다.

3. Google Drive 통합
	•	노트에서 [[filename]] 형식을 인식하여 Google Drive에서 파일을 검색합니다.

Refer to the file [[project_notes]].



4. 빠른 Google Drive 접근
	•	커맨드 팔레트를 통해 Google Drive 파일 검색 및 열기:
	•	명령: Quick Access Google Drive

설치

1. 플러그인 다운로드
	1.	GitHub에서 플러그인을 다운로드합니다.
	2.	플러그인 폴더를 Obsidian 플러그인 디렉터리로 이동합니다.
	•	위치: <vault>/.obsidian/plugins/google-workspace-integration

2. 플러그인 활성화
	1.	Obsidian 설정 → 플러그인 → 커뮤니티 플러그인 → Google Workspace Integration 활성화.

3. Google API 설정
	1.	Google Cloud Console에서 새 프로젝트를 생성합니다.
	2.	OAuth 2.0 인증 정보를 생성하고 클라이언트 토큰을 복사합니다.
	3.	Obsidian 플러그인 설정에 토큰을 붙여넣습니다.

사용법

1. Google Calendar
	•	노트에 다음 형식으로 작성:

#calendar/Event Name @YYYY-MM-DD HH:MM-HH:MM


	•	예:

#calendar/Team Meeting @2024-12-15 14:00-15:00



2. Google Tasks
	•	노트에 다음 형식으로 작성:

#task/Task Title "Optional Notes" @YYYY-MM-DD


	•	예:

#task/Buy groceries "Milk, eggs, bread" @2024-12-20



3. Google Drive
	•	노트에 다음 형식으로 작성:

[[filename]]


	•	예:

Refer to [[project_notes]] for details.



4. 빠른 Google Drive 접근
	1.	커맨드 팔레트(Ctrl+P 또는 Cmd+P) 열기.
	2.	Quick Access Google Drive 명령 선택.
	3.	파일 검색 및 열기.

설정
	1.	Google API 인증 토큰
	•	플러그인의 설정 탭에서 Google API 인증 토큰을 입력합니다.
	2.	통합 활성화
	•	Google Calendar, Tasks, Drive 통합을 개별적으로 활성화/비활성화할 수 있습니다.

파일 구조

obsidian-plugin/
├── manifest.json
├── main.ts
├── settings.ts
├── google-auth.ts
├── parsers/
│   ├── calendarParser.ts
│   ├── taskParser.ts
│   ├── driveParser.ts
└── ui/
    ├── feedback.ts
    └── quickAccess.ts

기여
	1.	이 프로젝트에 기여하려면 Issues를 확인하고 제안하거나 문제를 보고하세요.
	2.	Pull Request를 통해 코드 변경 사항을 제출하세요.

라이선스

이 플러그인은 MIT 라이선스를 따릅니다.
자세한 내용은 LICENSE 파일을 참조하세요.
