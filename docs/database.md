# Intellecta Database Schema v1

## users

| Column | Type |
|----------|----------|
| id | UUID |
| firebase_uid | VARCHAR |
| username | VARCHAR |
| email | VARCHAR |
| avatar_url | VARCHAR |
| level | INT |
| xp | BIGINT |
| coins | BIGINT |
| gems | BIGINT |
| streak_days | INT |
| created_at | TIMESTAMP |
| updated_at | TIMESTAMP |

---

## subjects

| Column | Type |
|----------|----------|
| id | UUID |
| name | VARCHAR |
| icon | VARCHAR |
| description | TEXT |

---

## topics

| Column | Type |
|----------|----------|
| id | UUID |
| subject_id | UUID |
| name | VARCHAR |
| description | TEXT |

---

## questions

| Column | Type |
|----------|----------|
| id | UUID |
| topic_id | UUID |
| type | ENUM |
| difficulty | ENUM |
| question_text | TEXT |
| explanation | TEXT |
| source | VARCHAR |
| ai_generated | BOOLEAN |
| created_at | TIMESTAMP |

---

## question_options

| Column | Type |
|----------|----------|
| id | UUID |
| question_id | UUID |
| option_text | TEXT |
| is_correct | BOOLEAN |

---

## quiz_attempts

| Column | Type |
|----------|----------|
| id | UUID |
| user_id | UUID |
| question_id | UUID |
| selected_option | UUID |
| correct | BOOLEAN |
| xp_earned | INT |
| coins_earned | INT |
| attempted_at | TIMESTAMP |

---

## achievements

| Column | Type |
|----------|----------|
| id | UUID |
| title | VARCHAR |
| description | TEXT |
| badge_image | VARCHAR |
| xp_reward | INT |
| gem_reward | INT |

---

## user_achievements

| Column | Type |
|----------|----------|
| user_id | UUID |
| achievement_id | UUID |
| unlocked_at | TIMESTAMP |

---

## xp_logs

| Column | Type |
|----------|----------|
| id | UUID |
| user_id | UUID |
| amount | INT |
| reason | VARCHAR |
| created_at | TIMESTAMP |

---

## coin_logs

| Column | Type |
|----------|----------|
| id | UUID |
| user_id | UUID |
| amount | INT |
| reason | VARCHAR |
| created_at | TIMESTAMP |

---

## daily_challenges

| Column | Type |
|----------|----------|
| id | UUID |
| title | VARCHAR |
| description | TEXT |
| xp_reward | INT |
| coin_reward | INT |
| active_date | DATE |

---

## user_daily_challenges

| Column | Type |
|----------|----------|
| user_id | UUID |
| challenge_id | UUID |
| completed | BOOLEAN |

---

## leaderboards

| Column | Type |
|----------|----------|
| id | UUID |
| user_id | UUID |
| rank | INT |
| score | BIGINT |
| leaderboard_type | ENUM |

---

## worlds

| Column | Type |
|----------|----------|
| id | UUID |
| name | VARCHAR |
| required_level | INT |
| description | TEXT |

---

## user_worlds

| Column | Type |
|----------|----------|
| user_id | UUID |
| world_id | UUID |
| unlocked_at | TIMESTAMP |

---

# Question Types

MCQ

TRUE_FALSE

FILL_BLANK

MATCH

IMAGE_BASED

---

# Difficulty Levels

CLASS_1_3

CLASS_4_5

CLASS_6_8

CLASS_9_10

CLASS_11_12

SSC

BANKING

RAILWAY

UPSC

---

# XP Economy

Easy = 10 XP

Medium = 25 XP

Hard = 50 XP

UPSC = 100 XP

---

# Coin Economy

Easy = 5 Coins

Medium = 10 Coins

Hard = 20 Coins

UPSC = 40 Coins
