# 📝 Article Views I

## 🎯 Problem Description

We have a table called **Views** that tracks who looked at which article and when. The table looks like this:

| article_id | author_id | viewer_id | view_date  |
|------------|-----------|-----------|------------|
| 1          | 3         | 5         | 2019-08-01 |
| 1          | 3         | 6         | 2019-08-02 |
| 2          | 7         | 7         | 2019-08-01 |
| 2          | 7         | 6         | 2019-08-02 |
| 4          | 7         | 1         | 2019-07-22 |
| 3          | 4         | 4         | 2019-07-21 |
| 3          | 4         | 4         | 2019-07-21 |

👉 **What do the columns mean?**
- **article_id**: Which article was viewed.
- **author_id**: Who wrote the article.
- **viewer_id**: Who viewed the article.
- **view_date**: When the article was viewed.

🔍 **Important note:** If **author_id** is the same as **viewer_id**, it means the author looked at their own article!

---

## 🔥 Goal: Find Self-Viewing Authors
We want to **find all authors who viewed at least one of their own articles**.

### ✅ Output Table
Our output should look like this:

| id   |
|------|
| 4    |
| 7    |

👉 **What does this mean?**
- **4** is an author who looked at their own article.
- **7** is another author who did the same.

📌 The output should be **sorted in ascending order**.

---

## 🧠 Example Breakdown

Let’s break it down:

1️⃣ **Author 3** — Viewed by **5** and **6** → Did **NOT** view their own article ❌

2️⃣ **Author 7** — Viewed by **7** (themselves) ✅ → **Include 7**

3️⃣ **Author 4** — Viewed by **4** (themselves) ✅ → **Include 4**

✅ Final result: **4** and **7**, sorted in ascending order.

---

## 💡 How to Solve
Here’s the game plan:

1️⃣ **Check if author_id = viewer_id** — This tells us if the author looked at their own article.

2️⃣ **Select those unique authors** — We only want each author listed **once**.

3️⃣ **Sort by id (ascending)** — To make it nice and tidy!

✨ Now you’re ready to write the query and find those self-checking authors!

