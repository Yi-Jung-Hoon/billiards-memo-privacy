# Billiards Memo 개인정보처리방침 (초안 v2 — 검토 요청)

> Play Console 제출용. 국문+English 모두 포함 (리스팅 5언어 대응).
> `[TODO-본인]` = 반드시 본인이 직접 해야 하는 항목. 나머지는 코드 기준 작성됨.

## 0. 본인이 해야 할 일 (체크리스트)

- [x] `[TODO-본인-1]` 연락 이메일 확정: nobel77.lee@gmail.com (아래 전부 기입됨)
- [x] `[TODO-본인-2]` 시행일: 2026-10-13 (게시 시 실제 공개일로 수정 가능)
- [x] `[TODO-본인-3]` OpenCV 처리 방식 확정 → ② 로컬 번들로 확정 (public/opencv.js, 외부 전송 없음)
- [ ] `[TODO-본인-4]` 아래 초안을 읽고 "우리 앱이 실제로 이렇게 동작한다" 확인 (특히 1조 수집 항목, 3조 삭제 경로)
- [ ] `[TODO-본인-5]` 공개 URL 만들기 (순서는 하단 "게시 방법" 참고, 소요 10분) → URL을 Play Console > 앱 콘텐츠 > 개인정보처리방침에 등록
- [ ] `[TODO-본인-6]` Data Safety 설문 입력 (하단 표를 그대로 옮기면 됨, 소요 15분)

---

## 1. Data Safety 정리 (Console에 그대로 입력)

| Console 질문 | 답변(초안) | 근거 |
|---|---|---|
| 데이터를 수집·공유합니까? | 예 (수집만, 공유는 조건부) | 사진·파일·기기정보를 기기 내에서 다룸 |
| 수집 항목: 사진·동영상 | 예 | 자동 배치(카메라·갤러리), 썸네일 저장 |
| 수집 항목: 파일·문서 | 예 | 백업·내보내기 파일 생성 |
| 수집 항목: 기기 식별자·진단 | 예 | 로그 내보내기 시 모델·OS·배터리 포함 |
| 제3자와 공유 | 아니요 (로컬 번들로 확정, 외부 전송 없음) | `public/opencv.js` 로컬 포함 확인 |
| 수집 목적 | 앱 기능 (메모 저장·백업·문제 해결) | 서버 전송·광고·분석 목적 없음 |
| 전송 중 암호화 | 해당 없음 (자체 서버 전송 없음) | Firebase/Analytics 미사용, `google-services.json` 없음 확인 |
| 삭제 요청 | 예 — 앱 내 삭제·휴지통 비우기 + 파일 직접 삭제 + 이메일(nobel77.lee@gmail.com) 요청 | 3조 참고 |
| 13세 미만 대상 | 아니요 | 5조 |

---

## 2. 국문

**Billiards Memo 개인정보처리방침**

- 시행일: `2026-10-13`
- 사업자/문의: nobel77.lee@gmail.com

1. 수집하는 정보와 방법
   - 메모 내용(제목, 텍스트, 배치 기록, 사진): 사용자가 직접 입력·저장. 기기 내 데이터베이스(SQLite)와 파일로만 보관하며, 개발자 서버로 전송하지 않습니다.
   - 사진·카메라 이미지: 자동 배치 기능을 실행할 때만 접근합니다. 분석은 기기 내에서만 수행됩니다.
   - 백업·내보내기 파일: 사용자가 직접 실행할 때만 기기 저장소(Documents 등)에 생성됩니다.
   - 기기 정보(모델명, OS 버전, 배터리 상태): 사용자가 오류 로그 내보내기·공유를 직접 실행할 때만 로그에 포함됩니다. 자동으로 전송되지 않습니다.
   - 위치정보, 연락처, 광고 식별자: 수집하지 않습니다.
2. 이용 목적
   - 메모 기록·조회, 백업·복원, 오류 해결. 광고·마케팅·분석에 이용하지 않으며, 계정 가입도 요구하지 않습니다.
3. 보관 기간 및 삭제 방법
   - 모든 데이터는 사용자 기기에만 보관되며, 별도 보관 기한을 두지 않습니다(사용자가 지울 때까지 유지).
   - 삭제 방법: ① 앱 내 메모 삭제 → 휴지통 비우기 ② 백업·내보내기 파일은 파일 앱에서 직접 삭제 ③ 처리가 어려운 경우 nobel77.lee@gmail.com으로 요청하면 안내해 드립니다.
   - 앱 삭제 시 기기 내 데이터도 함께 삭제됩니다. 단, 사용자가 따로 보관한 백업 파일은 남으므로 직접 삭제해야 합니다.
4. 제3자 제공 및 외부 라이브러리
   - 개발자 서버나 제3자에게 개인정보를 전송·공유하지 않습니다. 자동 배치용 OpenCV 라이브러리는 앱에 내장되어 있으며, 모든 처리는 기기 내에서 이루어집니다.
5. 어린이 개인정보: 만 13세(국내 만 14세 미만 아동 포함) 미만을 대상으로 하지 않으며, 아동의 정보를 고의로 수집하지 않습니다.
6. 권한 사용 안내 (안드로이드)
   - 카메라·사진: 자동 배치용 촬영·불러오기 (사용 시에만 요청)
   - 저장소: 백업·내보내기 파일 생성 (사용 시에만 요청)
   - 인터넷: 공유 기능에 사용 (자동 배치 라이브러리는 앱 내장)
7. 문의: nobel77.lee@gmail.com으로 연락하면 지체 없이 답변합니다.

---

## 3. English

**Billiards Memo Privacy Policy**

- Effective date: `2026-10-13`
- Contact: nobel77.lee@gmail.com

1. Data we handle and how
   - Memo content (titles, text, layouts, photos): entered and saved by you. Stored only on your device (SQLite/files). Never sent to our servers.
   - Photos/camera images: accessed only when you run auto-placement. Analysis runs on-device.
   - Backup/export files: created in device storage (e.g., Documents) only when you run backup/export.
   - Device info (model, OS version, battery): included in diagnostic logs only when you explicitly export and share them. Never transmitted automatically.
   - We do not collect location, contacts, or advertising IDs.
2. Purpose: note-taking, backup/restore, troubleshooting. No advertising, marketing, or analytics. No account required.
3. Retention & deletion
   - All data stays on your device until you delete it.
   - How to delete: ① delete memos in-app and empty Trash ② delete backup/export files via the file manager ③ contact nobel77.lee@gmail.com if you need help.
   - Uninstalling the app deletes on-device data. Separately kept backup files must be deleted manually.
4. Third parties & external libraries
   - We do not transmit or share personal data with any server or third party. All processing happens on-device.
5. Children: not directed at children under 13, and we do not knowingly collect children's data.
6. Android permissions
   - Camera/photos: shooting/loading images for auto-placement (requested only when used)
   - Storage: creating backup/export files (requested only when used)
   - Internet: sharing features (the auto-placement library is bundled in-app)
7. Contact: reach us at nobel77.lee@gmail.com and we will respond promptly.

---

## 4. 게시 방법 (본인 작업, 약 10분)

> 이 문서는 초안 파일이라 비공개 저장소에 있음. Play는 "로그인 없이 열리는 공개 URL"을 요구하므로 아래 중 하나를 수행.

**방법 A: GitHub Pages (권장, 무료)**
1. GitHub에서 새 public 저장소 생성 (예: `qrisma-privacy`)
2. 이 파일의 국문+English를 `index.md`(또는 `index.html`)로 올리기
3. Settings > Pages > Deploy from branch > `main` 선택 → 몇 분 후 `https://<ID>.github.io/qrisma-privacy/` 발급
4. 그 URL을 Play Console > 정책 및 프로그램 > 앱 콘텐츠 > 개인정보처리방침에 등록

**방법 B: Notion/블로그 공개 페이지**
- Notion 페이지를 "웹에 공개"로 설정한 URL도 가능. 단, 접속 차단·삭제 위험이 있어 Pages 권장.

**게시 후 확인할 것**
- [ ] 시크릿 창에서 URL이 로그인 없이 열리는가
- [ ] 이메일·시행일이 실제 기입됐는가 (`[`, `TODO` 문자열이 남아있지 않은가)
- [ ] Data Safety 답변이 이 문서 내용과 일치하는가 (불일치는 반려 사유)
