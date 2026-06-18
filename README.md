# Git Branch Workflow — Mission-03 RDMS

## সংক্ষিপ্ত পরিকল্পনা

একটি GitHub repo → ৬টি branch → প্রতিটি module-এর জন্য আলাদা branch

---

## ধাপ ১ — GitHub-এ Repo তৈরি করো

1. GitHub-এ যাও → **New Repository**
2. Repository name দাও → `mission-03-RDMS`
3. ✅ **"Add a README file"** tick দাও
4. **Create repository** button চাপো

---

## ধাপ ২ — Local-এ Clone করো

```bash
cd Desktop          # যেখানে রাখতে চাও সেখানে যাও
git clone https://github.com/তোমার-username/mission-03-RDMS.git
cd mission-03-RDMS  # folder-এ ঢোকো
```

> `git clone` করলে `git init` এবং `remote add` আলাদা করে করতে হয় না।

---

## ধাপ ৩ — Module-1 Branch তৈরি ও কাজ করো

```bash
git checkout -b module-1   # নতুন branch তৈরি করো
# এখন module-1 এর files/code লেখো
git add .
git commit -m "feat: module-1 completed"
git push origin module-1
```

---

## ধাপ ৪ — Module-2 Branch তৈরি ও কাজ করো

```bash
git checkout main          # আগে main-এ ফিরে আসো
git checkout -b module-2   # নতুন branch তৈরি করো
# module-2 এর কাজ করো
git add .
git commit -m "feat: module-2 completed"
git push origin module-2
```

---

## ধাপ ৫ — Module-3 থেকে Module-6 পর্যন্ত

প্রতিটি module-এর জন্য **ধাপ ৪** repeat করো, শুধু branch name পরিবর্তন করো:

```bash
git checkout main
git checkout -b module-3
git add .
git commit -m "feat: module-3 completed"
git push origin module-3
```

```bash
git checkout main
git checkout -b module-4
git add .
git commit -m "feat: module-4 completed"
git push origin module-4
```

```bash
git checkout main
git checkout -b module-5
git add .
git commit -m "feat: module-5 completed"
git push origin module-5
```

```bash
git checkout main
git checkout -b module-6
git add .
git commit -m "feat: module-6 completed"
git push origin module-6
```

---

## দরকারি Commands — Quick Reference

| কাজ                        | Command                       |
| -------------------------- | ----------------------------- |
| নতুন branch তৈরি করো + যাও | `git checkout -b module-1`    |
| পুরনো branch-এ চলে যাও     | `git checkout module-1`       |
| main-এ ফিরে আসো            | `git checkout main`           |
| সব branch দেখো             | `git branch -a`               |
| বর্তমান branch জানো        | `git branch`                  |
| changes stage করো          | `git add .`                   |
| commit করো                 | `git commit -m "message"`     |
| GitHub-এ push করো          | `git push origin branch-name` |

---

## `git checkout` vs `git checkout -b` — পার্থক্য

| Command                    | কাজ                                | কখন ব্যবহার করবে       |
| -------------------------- | ---------------------------------- | ---------------------- |
| `git checkout -b module-1` | নতুন branch তৈরি করে + সেখানে যায় | প্রথমবার branch বানাতে |
| `git checkout module-1`    | শুধু ঐ branch-এ যায়               | branch আগেই তৈরি থাকলে |

---

## Branch Structure (চূড়ান্ত রূপ)

```
mission-03-RDMS (repo)
│
├── main
├── module-1
├── module-2
├── module-3
├── module-4
├── module-5
└── module-6
```
