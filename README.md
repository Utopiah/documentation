# Contributing guide

## Windows

### Requirements

1. Scoop
2. Hugo
3. PowerShell 5
4. .Net Framework 4.5

### Install Scoop

1. Open Windows PowerShell
2. Run

```text
  Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')
  # or shorter
  iwr -useb get.scoop.sh | iex
```

### Install Hugo

1. Open Windows PowerShell
2. Run

```text
  scoop install hugo-extended
```

## Clone documentation repository

```git
 git clone https://github.com/Stock-Knowledge-Engineering/documentation.git
```

## Add new documentation category

1. Create new folder and name it with category name use "-" for whitespace
2. Create new file inside the newly created folder and name it \_index.en.md
3. Add this inside \_index.en.md

```markdown
---

title: "Insert title here"
date: "Put unix timestamp"
icon: "Insert themify icon name"
description: "Insert description"
weight: "Insert integer number, 1 is the highest and nth is the lowest"
type: "docs"

---
```

Example

```markdown
---

title: "New Category"
date: 2018-12-29T11:02:05+06:00
icon: "ti-panel"
description: "Lorem ipsum dolor sit amet ipsum dolor sit amet ipsum dolor sit amet"
weight: 2
type: "docs"

---
```

## Add topic to category

1. Create new folder inside a category folder and name it with topic name use "-" for whitespace
2. Create new file inside the newly created folder and name it \_index.en.md
3. Add this inside \_index.en.md

```markdown
    ---
    title: "Insert title here"
    date: "Put unix timestamp"
    icon: "Insert themify icon name"
    description: "Insert description"
    weight: "Insert integer number, 1 is the highest and nth is the lowest"
    ---

    //write markdown content in the following line
```

Example

```markdown
    ---
    title: "Leaderboard"
    date: 2018-12-29T11:02:05+06:00
    description: "Lorem ipsum dolor sit amet ipsum dolor sit amet ipsum dolor sit amet"
    weight: 1
    ---

    //write markdown content in the following line
```

## Preview changes in local machine

Run

```text
  hugo server -D
```

## Publishing changes

Note: Make sure branch is always in main.

1. Git add all changes
2. Git commit all changes
3. Git push

```text
  git push origin main
```
