# Intellecta API Design v1

## Authentication

POST /auth/register

POST /auth/login

POST /auth/firebase

GET /auth/me

---

## User

GET /users/profile

PUT /users/profile

GET /users/stats

GET /users/streak

---

## Subjects

GET /subjects

GET /subjects/{id}

---

## Topics

GET /topics

GET /topics/{id}

GET /subjects/{id}/topics

---

## Questions

GET /questions/random

GET /questions/topic/{id}

GET /questions/difficulty/{level}

---

## Quiz

POST /quiz/start

POST /quiz/submit

GET /quiz/result/{attemptId}

GET /quiz/history

---

## Daily Challenges

GET /daily-challenges

POST /daily-challenges/{id}/complete

---

## Achievements

GET /achievements

GET /users/achievements

---

## Worlds

GET /worlds

GET /users/worlds

POST /worlds/{id}/unlock

---

## Leaderboards

GET /leaderboards/global

GET /leaderboards/weekly

GET /leaderboards/monthly

---

## Rewards

GET /users/xp

GET /users/coins

GET /users/gems

---

## Notifications

GET /notifications

POST /notifications/token

---

## AI

POST /ai/explanation

POST /ai/hint
