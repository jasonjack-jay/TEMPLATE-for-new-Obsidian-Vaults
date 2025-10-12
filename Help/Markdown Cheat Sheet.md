# Markdown Cheat Sheet

Ripped from [The Markdown Guide](https://www.markdownguide.org)

This Markdown cheat sheet provides a quick overview of all the Markdown syntax elements. It can’t cover every edge case, so if you need more information about any of these elements, refer to the reference guides for [basic syntax](https://www.markdownguide.org/basic-syntax/) and [extended syntax](https://www.markdownguide.org/extended-syntax/).

## Basic Syntax

These are the elements outlined in John Gruber’s original design document. All Markdown applications support these elements.

### Heading - Use one or more # + a space + your heading text

# H1
## H2
### H3
#### H4
##### H5
###### H6
####### There is no H7

### Tags - Use a # + no space + your text (with no spaces)
#done #hashtag #error #help 

### Bold

**bold text**

### Italic

*italicized text*

### Blockquote

> blockquote

### Ordered List

1. First item
2. Second item
3. Third item

### Unordered List

- First item
- Second item
- Third item

### Code

`code`

### Horizontal Rule

---

### Link - square brackets then round brackets!

[Markdown Guide](https://www.markdownguide.org) - [Basic Syntax](https://www.markdownguide.org/basic-syntax/) - [Extended Syntax](https://www.markdownguide.org/extended-syntax/)

**Try those links, or, move your cursor into this paragraph then over the links to see the formatting.** To create a link to a webpage: [text for the link](https://example.com/) - or, to **link to a page in your vault** (create a **local link**): [[Resources/some page]] - or, to link to a header in your vault (another local link): [[Resources/some page#Header]] - or, to change the text for a local link: use the | character: [[Resources/some page|this will show up instead]]

### Image

![alt text](https://www.markdownguide.org/assets/images/tux.png)

## Extended Syntax

These elements extend the basic syntax by adding additional features. Not all Markdown applications support these elements.

### Table

| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |

### Fenced Code Block

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

### Footnote

Here's a sentence with a footnote. [^1]

[^1]: This is the footnote.

### Heading ID

### My Great Heading {#custom-id}

### Definition List

term
: definition

### Strikethrough

~~The world is flat.~~

### Task List

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

### Emoji - type a : + no space + type what you want, to see a list

Example 1: That is so funny! 🤣  <- I typed a : + started typing laugh, and then selected it from the list

Example 2:
Community plug-in **Iconize** supports icon packs. **Place your cursor in this paragraph to see the codes!** You can optionally add or remove different packs. To use: Begin the icon name with the icon pack prefix - e.g. Font Awesome Regular = "far" = type a : then 'far' then start typing the icon e.g. HandSpock = :FarHandSpock: or, Lucide Icons = "li" = type a : then 'li' then start typing the icon name e.g. Handshake = :LiHandshake:


(See also [Copying and Pasting Emoji](https://www.markdownguide.org/extended-syntax/#copying-and-pasting-emoji))

### Highlight

I need to highlight these ==very important words==.

### Subscript - NON STANDARD!

'official' markdown syntax is "bracket the subscript with ~" ... but that doesn't seem to work!
H~2~O

However, we can do it by using HTML! Move your cursor into this to see how it works:
H<sub>2</sub>O

### Superscript - NON STANDARD!

Same issue!
'official' markdown syntax is "bracket the superscript with ^" ... but that doesn't seem to work!
X^2^

Here's the HTML version:
X<sup>2</sup>

