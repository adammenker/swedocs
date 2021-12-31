# MARKDOWN

---

## Headers
* \# text for H1
* \#\# text for H2 etc.
* ### h3
---

## Italics
* \*text\* or \_text\_
* *text*
---

## Strong/Bold
* \*\*text\*\* or \_\_text\_\_
* **text**
---

## Strikethrough
* \~\~text\~\~
* ~~text~~
---

## Horizontal Rule
* \-\-\- or \_\_\_

---

## Escape Char
* \\
* \# => \\ #
---

## Block Quote
* \> text
* > text
---

## Links
* \[text\]\(url/to/link.com \"optional title\"\)
  * optional title is displayed on hover over
* [text](google.com "google")
* can link to certain headers of same markdown file 
---

## Unordered List 
* \* text
  * tab \* to make subpoint
---
  
## Ordered List
* 1\) text1
* 2\) text2
1) text1
2) text2
---

## Code Block
* \`\`\`java
  * code
* \`\`\`
* can support multiple language syntaxes
* below example is java
``` java
  for(i = 0; i < 10; i++):
      print('text')
```
---

## Image
* \!\[text\]\(image/url\)
---

## Table
* \| category \| category \|
* \| -------- \| --------------- \|
* \| data \| data \|
* \| data \| data \|

| category | category |
| -------- | --------------- |
| data | data |
| data | data |
---

## Check List
* asterisk (*) followed by brackets ([ ])  text
  * if space in brackets box is unchecked
  * if 'X' in brackets box is checked
* [X] completed task
* [ ] uncompleted task
---

## Color Highlights
\`\`\`diff
* \- text in red
* \+ text in green
* \ ! text in orange
* \# text in gray
* \@@ text in purple (and bold)@@

\`\`\`
```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
---

## Badges
* [badges docs](https://shields.io/)
* [list of badges](https://naereen.github.io/badges/)



