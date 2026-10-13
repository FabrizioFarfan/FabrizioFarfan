<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:FF6B5B,100:FFA633&height=200&section=header&text=Hi,%20I%27m%20Fabrizio%20Farfan&fontSize=42&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Full-Stack%20and%20Mobile%20Developer&descAlignY=58&descSize=18" alt="header"/>

<p align="center">
  <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=FF6B5B&center=true&vCenter=true&width=600&lines=Backend+in+Java+%C2%B7+Kotlin+%C2%B7+Spring+Boot+%E2%98%95;Native+apps+for+iOS+%2B+Android+%F0%9F%93%B1;Real-time+multiplayer+with+WebSockets+%F0%9F%8E%AE;From+hospitality+to+tech+%F0%9F%8D%BD%EF%B8%8F%E2%86%92%F0%9F%92%BB" alt="Typing SVG"/></a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=FabrizioFarfan&label=Profile%20views&color=FF6B5B&style=flat" alt="profile views"/>
</p>

<p align="center">
  <em>From hospitality to tech — now shipping real products end-to-end: APIs, web dashboards, native apps and an online game 🚀</em>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/fabrizio-farfan-42b4a0256/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:farfanfabrizio96@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <a href="https://eazy-fidelity.com"><img src="https://img.shields.io/badge/Eazy_Fidelity-live-22c55e?style=for-the-badge" alt="Eazy Fidelity live"/></a>
</p>

---

## 🔥 What I'm building

### 🏋️ EazyFit — *training app with friends, coaches & live feed*
> 📱 iOS + Android · 🟢 API live

Workout timers, friend groups, 1:1 coaching and a real-time social feed — one backend, two native apps.

- 🧩 **Modular monolith** (`identity` / `fitness` / `social`) — modules talk only through interfaces, never share entities. Built to split into microservices by *moving* modules, not rewriting them.
- 🔄 **Offline-first idempotent sync** — the local Room id travels as `client_id`, so re-uploading a workout never duplicates it.
- ⚡ **Real-time over WebSocket** — one JWT-authenticated socket per user; events fire only `AFTER_COMMIT`, so nobody gets notified about data that rolled back.
- 🔐 **Auth done right** — short access token + rotating, revocable refresh token, role claims + `@PreAuthorize`, Sign in with Apple/Google verified against the providers' JWKS.
- 🔔 **Push via FCM HTTP v1** with a service account (not the legacy API).

`Kotlin 2.0` `Spring Boot 3.4` `MySQL 8.4` `Flyway` `WebSocket` `Jetpack Compose` `Hilt` `Room` `SwiftUI` `Firebase` `nginx` `systemd`

---

### 🎟️ Eazy Fidelity — *digital loyalty stamp cards* · [eazy-fidelity.com](https://eazy-fidelity.com)
> 🟢 API + dashboard live · 📱 apps in development

"Buy 10, get the next one free" — but in your phone, for every shop you visit.

- 🛡️ **Anti-fraud QR** — the customer shows a signed token that lives **60 seconds** with a `typ=scan` claim; the security filter only accepts `access`, so a screenshot is never a session.
- 📒 **Stamps as a ledger** — nothing is ever deleted, only reverted (`reverted_at / by / reason`). Every stamp records *who* gave it and *where*, because loyalty fraud is almost always internal.
- 👥 **5 roles, one per account**, with store-level access checks on every stamp.
- 📊 **Metrics computed, not stored** — straight from the ledger, no counters to drift; days cut in the **business's timezone**, not UTC.
- 📲 **Kotlin Multiplatform** — models, HTTP client and session written once for Android & iOS.

`Java 17` `Maven` `Spring Boot 3.4` `MySQL 8.4` `Flyway` `JWT` `React 19` `TypeScript` `Vite` `Tailwind 4` `TanStack Query` `KMP` `Ktor` `Compose` `SwiftUI`

---

### 🌶️ Eazy Chill — *online party game, Mario Party style*
> 🛠️ In development · playable

2–8 players, points battle royale, real-time minigames.

- ⚖️ **Server is the referee** — points live on the server, nobody can cheat from their phone.
- 🎮 **Server-side simulation at 20–30 Hz** for live minigames (Bomberman-like, Smash-like, space shooter) — phones only send inputs.
- 🤖 **Seamless reconnection** — if you drop, an invisible bot plays for you; come back within 3 min with your `resumeToken` and you pick up where it left off.
- 🧪 **Same game logic in Java and C#**, kept in sync with cross-language tests on shared seeds — 39 tests, including a full match over WebSocket.

`Unity 6` `C#` `UI Toolkit` `Java 17` `Spring Boot` `WebSocket` `MySQL`

---

### 📖 EpicTales · [epictales.blue](https://epictales.blue)
> 🟢 Live

My first full-stack app: authentication, file uploads and content management.

---

## 💻 Tech Stack

**⚙️ Backend**<br/>
![Java](https://img.shields.io/badge/Java_17-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=flat-square&logo=socketdotio&logoColor=white)
![Swagger](https://img.shields.io/badge/OpenAPI-85EA2D?style=flat-square&logo=swagger&logoColor=black)

**🗄️ Data**<br/>
![MySQL](https://img.shields.io/badge/MySQL_8-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white)
![Hibernate](https://img.shields.io/badge/JPA_/_Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white)

**🌐 Web**<br/>
![React](https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind_4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=flat-square&logo=reactquery&logoColor=white)

**📱 Mobile**<br/>
![KMP](https://img.shields.io/badge/Kotlin_Multiplatform-7F52FF?style=flat-square&logo=kotlin&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white)
![SwiftUI](https://img.shields.io/badge/SwiftUI-F05138?style=flat-square&logo=swift&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black)

**🎮 Games**<br/>
![Unity](https://img.shields.io/badge/Unity_6-000000?style=flat-square&logo=unity&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)

**🚀 DevOps**<br/>
![Linux](https://img.shields.io/badge/Linux_VPS-FCC624?style=flat-square&logo=linux&logoColor=black)
![nginx](https://img.shields.io/badge/nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)


## 🌱 Currently

- 🎮 Building server-authoritative multiplayer in Eazy Chill
- 📲 Taking Eazy Fidelity's apps to the stores
- 🤖 Integrating AI into my apps

---

<h3 align="left">Languages and Tools:</h3>
<p align="left">
  <a href="https://www.java.com" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="java" width="40" height="40"/></a>
  <a href="https://kotlinlang.org" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/kotlin/kotlin-original.svg" alt="kotlin" width="40" height="40"/></a>
  <a href="https://spring.io/projects/spring-boot" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/spring/spring-original.svg" alt="spring" width="40" height="40"/></a>
  <a href="https://www.mysql.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original.svg" alt="mysql" width="40" height="40"/></a>
  <a href="https://www.typescriptlang.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" alt="typescript" width="40" height="40"/></a>
  <a href="https://reactjs.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg" alt="react" width="40" height="40"/></a>
  <a href="https://tailwindcss.com/" target="_blank" rel="noreferrer"><img src="https://www.vectorlogo.zone/logos/tailwindcss/tailwindcss-icon.svg" alt="tailwind" width="40" height="40"/></a>
  <a href="https://developer.android.com" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/android/android-original.svg" alt="android" width="40" height="40"/></a>
  <a href="https://developer.apple.com/swift/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/swift/swift-original.svg" alt="swift" width="40" height="40"/></a>
  <a href="https://unity.com" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/unity/unity-original.svg" alt="unity" width="40" height="40"/></a>
  <a href="https://learn.microsoft.com/dotnet/csharp/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg" alt="csharp" width="40" height="40"/></a>
  <a href="https://firebase.google.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/firebase/firebase-plain.svg" alt="firebase" width="40" height="40"/></a>
  <a href="https://nginx.org" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nginx/nginx-original.svg" alt="nginx" width="40" height="40"/></a>
  <a href="https://www.linux.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/></a>
  <a href="https://git-scm.com/" target="_blank" rel="noreferrer"><img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/></a>
</p>

---

<p align="center">
  <em>"From creating memorable guest experiences to building memorable user experiences" ✨</em>
</p>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:FFA633,100:FF6B5B&height=120&section=footer" alt="footer"/>
