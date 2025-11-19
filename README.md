# How to Edit the ECSE GC Constitution

Welcome! This guide explains how to edit these bylaws even if you've never used LaTeX before. Don't worry—it's actually quite simple.

---

## 📋 Quick Start

The main document is **`main.tex`**. Open it in any text editor (VS Code, Google Docs, Notepad, etc.) and start editing!

---

## 🔍 Understanding the Structure

Think of the document like an outline:

- **Articles** = Main sections (like "Article I. Name")
- **Sections** = Subsections within articles (like "Section 1. Equal Opportunity")

---

## ✏️ Making Common Edits

### **Change the Document Title or Date**

Find this section at the top of `main.tex`:

```
\textbf{\orgname} Bylaws

Effective: November 19, 2025
```

Simply change the date to whatever you want. That's it!

---

### **Update Organization Name**

Find this section near the very top:

```
\newcommand{\orgname}{ECSE Graduate Council}
\newcommand{\orgshort}{ECSE GC}
\newcommand{\depname}{ECSE}
```

Replace these with your organization's names:
- `\orgname` = Full name (used in formal contexts)
- `\orgshort` = Short abbreviation (used in text)
- `\depname` = Department name

That's literally all you need to change. The rest of the document updates automatically!

---

### **Edit Article or Section Content**

Just find the text you want to change and edit it directly. For example:

**Before:**
```
The name of this organization shall be the \textbf{\orgname}.
```

**After:**
```
The name of this organization shall be the Super Cool \textbf{\orgname}.
```

You can ignore all the LaTeX formatting—just change the actual words!

---

## 🎯 Important Parts to Know (But Keep Simple!)

### **Creating a New Article**

To add a new article, use this template:

```
\Article{V}{Your Article Title Here}

Your content goes here. Just write normally!
```

Replace the number (I, II, III, etc.) and add your title.

---

### **Creating a New Section Within an Article**

To add a section inside an article:

```
\Sec{1. Your Section Title Here}

Your content goes here.
```

---

### **Adding a Bulleted List**

If you need a list, wrap it like this:

```
\begin{enumerate}[label=\alph*)]
    \item First item
    \item Second item
    \item Third item
\end{enumerate}
```

The `\alph*)` means bullets will show as **a)**, **b)**, **c)**. Just add more `\item` lines as needed.

---

### **Making Text Bold**

Wrap text in `\textbf{...}`:

```
\textbf{This text will be bold}
```

---

## 🛠️ Viewing Your Changes

### **Option 1: Use VS Code (Easiest)**
1. Install the "LaTeX Workshop" extension in VS Code
2. Open `main.tex`
3. Click the green "Build" button (or press keyboard shortcut shown in the extension)
4. A PDF preview appears automatically!

### **Option 2: Use Online LaTeX Editor**
1. Go to **https://www.overleaf.com**
2. Create a free account
3. Upload all files from this folder
4. Edit and see changes in real-time

### **Option 3: Don't Preview (Just Edit)**
Just edit the text and send the updated file. Someone else can compile it when needed!

---

## ⚠️ Important: Don't Delete These!

Never remove or heavily modify:

```
\documentclass[11pt]{article}
\usepackage{...}
\definecolor{...}
\titleformat{...}
```

These are the "magic" that makes the document look nice. If you accidentally delete something and the document breaks, just restore the file from backup.

---

## 🚨 Common Mistakes (And How to Avoid Them)

| Mistake | Why It's Bad | Fix |
|---------|-------------|-----|
| Deleting `{` or `}` brackets | The document won't compile | Use Ctrl+Z to undo |
| Using special characters like `&` or `#` without escaping | Causes errors | Write `\&` instead of `&` |
| Removing entire lines of formatting | Document breaks | Use Ctrl+Z to undo |
| Changing text *inside* `\newcommand{...}` | Won't work properly | Only change the content, not the structure |

---

## 📝 Step-by-Step Example: Editing Article I

**Original:**
```
\Article{I}{Name}
The name of this organization shall be the \textbf{\orgname}.
```

**What you want to change:** Add a sentence about the organization's purpose.

**After editing:**
```
\Article{I}{Name}
The name of this organization shall be the \textbf{\orgname}. 
We are dedicated to supporting our members.
```

That's it! No special formatting needed.

---

## ❓ I'm Stuck!

- **The document won't compile:** Check for missing or extra `{` `}` brackets
- **Text disappeared:** Use Ctrl+Z to undo
- **Something looks weird:** Check for typos in the text you edited
- **Still confused?** Compare your changes to the original version

---

## 💾 Saving and Sharing

1. Save your changes (Ctrl+S or Cmd+S)
2. Send the updated `main.tex` file to your team
3. Someone compiles it to PDF for official use

That's all you need to know! The bylaws editing is that simple.

---

**Happy editing! 🎉**
