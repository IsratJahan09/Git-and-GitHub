# Team Project With Git and GitHub

# 👥 Coaching Guru App — Team Git Workflow Guide

This document outlines the Git workflow for the Coaching Guru team project using **branch-based collaboration**. The team consists of:

* 👩‍💼 **Manager** (Team Lead): Israt
* 👩‍💻 Developer: Israt (Branch: `israt`)
* 👩‍💻 Developer: Faria (Branch: `faria`)

---

## 📂 Branch Structure

| Branch        | Purpose                                |
| ------------- | -------------------------------------- |
| `main`        | 🔒 Final production-ready code (clean) |
| `development` | 🧪 Combined team work (daily tested)   |
| `israt`       | 👩‍💻 Personal working branch (Israt)  |
| `faria`       | 👩‍💻 Personal working branch (Faria)  |

---

## 🚀 Project Setup (By Manager)

```bash
git init
git add .
git commit -m "initial commit"
git branch -m main
git remote add origin https://github.com/IsratJahan09/Coaching_Guru.git
git push -u origin main
```

### 🔧 Create Development Branch

```bash
git checkout -b development
git add .
git commit -m "branch change"
git push -u origin development
```

---

## 👤 Developer Setup (Faria)

```bash
git clone https://github.com/IsratJahan09/Coaching_Guru.git
cd Coaching_Guru
npm install
npm run start
```

Create and switch to personal branch:

```bash
git checkout -b faria
git push -u origin faria   # Only once when creating branch
```

---

## ⏰ Daily Workflow

### ✅ **Before Starting Work (Both Developers)**

```bash
git checkout development
git pull origin development     # Get latest team updates

git checkout israt              # or faria   //your own branch
```

### 📂 **After Completing Work (On Your Branch)**

```bash
git add .
git commit -m "✅ Work done today"
git push origin israt           # or faria
```

> 🔁 If it's the first time pushing, use:
> `git push -u origin israt` or `git push -u origin faria`

---

## 👩‍💼 Team Leader Routine (End of Day)

```bash
git checkout development
git pull origin development

git merge israt
git merge faria

git push u origin development
```

---

## 🏁 After Project Completion

```bash
git checkout main 
git pull origin main
git merge development
git push u origin main
```

---

## ✅ Best Practices

* 🔀 Pull before pushing (`git pull origin [branch]`)       `#e.g: branch development`
* ✅ Keep `main` clean — only merge when everything is stable
* 🧪 Test code in `development`
* 🧹 Use clear commit messages with emojis:

  * ✅ Feature complete
  * 🐛 Bug fix
  * 🔧 Small update
  * 🚧 Work in progress

---

## 📌 Branch Naming Convention

| Person | Branch  |
| ------ | ------- |
| Israt  | `israt` |
| Faria  | `faria` |

---

> ℹ️ This guide ensures smooth collaboration, avoids code conflicts, and helps deliver a stable final project.
