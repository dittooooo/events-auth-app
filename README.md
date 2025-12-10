# events-auth-app （Frontend Only）

## 專案簡介

- 此專案為 React Router 練習專案。
- 使用者可進行登入、註冊，登入後可以新增、編輯和刪除活動。
- 使用 React Router 的 **loader、action、redirect、useFetcher、defer、Await、Suspense** 進行開發。
- 後端程式為課程提供，僅用於處理請求。

## 技術堆疊

### Frontend

- React + React Router
- Loaders / Actions
- Suspense + Await + defer
- Authentication
- useFetcher
- CSS Modules

### Tools

- Vite
- JavaScript ES Modules
- Git / GitHub


## 功能特色

- 登入系統

  - 使用者成功登入後會拿到 token，登出後就會清除。
  - 每次重新整理頁面時會檢查 token 是否過期，過期以後會自動登出，重新回到首頁。

- 活動管理

  - 畫面不論資料載入沒都會先出現，避免等待資料時整個卡住。
  - 不管有沒有登入，都可以瀏覽所有活動，點進某個活動就可以看它的詳細資訊。
  - 登入後可新增、編輯和刪除活動。

- 導覽列狀態
  根據登入狀態改變導覽列資訊。

- 錯誤頁面
  發生任何錯誤都會跳到這個頁面，而不是直接整個壞掉。

- Newsletter 訂閱
  表單送出後只更新自己的 UI，不會整個刷新。

## 截圖

<img width="2769" height="1473" alt="Image" src="https://github.com/user-attachments/assets/f7edd845-9c42-4308-9a20-c8839460f144" />
<img width="2801" height="1696" alt="Image" src="https://github.com/user-attachments/assets/f4da077b-7158-4f33-909d-7ba95fe15625" />
<img width="2793" height="1693" alt="Image" src="https://github.com/user-attachments/assets/2543a1e0-b0d4-4283-960a-e19b75047f2a" />

## 安裝與執行

```bash
  git clone https://github.com/dittooooo/events-auth-app.git
  cd events-auth-app/backend
  npm install
  npm start

  cd events-auth-app/frontend
  npm install
  npm start
```

## 專案架構

```bash
events-auth-app/
└── frontend/
    ├── public/
    ├── src/
    │   ├── components/
    │   │   ├── AuthForm.js
    │   │   ├── AuthForm.module.css
    │   │   ├── EventForm.js
    │   │   ├── EventForm.module.css
    │   │   ├── EventItem.js
    │   │   ├── EventItem.module.css
    │   │   ├── EventsList.js
    │   │   ├── EventsList.module.css
    │   │   ├── EventsNavigation.js
    │   │   ├── EventsNavigation.module.css
    │   │   ├── MainNavigation.js
    │   │   ├── MainNavigation.module.css
    │   │   ├── NewsletterSignup.js
    │   │   ├── NewsletterSignup.module.css
    │   │   ├── PageContent.js
    │   │   ├── PageContent.module.css
    │   │
    │   ├── pages/
    │   │   ├── Authentication.js
    │   │   ├── EditEvent.js
    │   │   ├── Error.js
    │   │   ├── EventDetail.js
    │   │   ├── Events.js
    │   │   ├── EventsRoot.js
    │   │   ├── Home.js
    │   │   ├── Logout.js
    │   │   ├── NewEvent.js
    │   │   ├── Newsletter.js
    │   │   └── Root.js
    │   ├── util/
    │   │   └── auth.js
    │   ├── App.js
    │   ├── index.js
    │   └── index.css
    │
    ├── package.json
    └── package-lock.json
```
