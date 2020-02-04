# SwiftUI-Notes
[Markdown Reference](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

This repo contains all the important reference for swiftUI Learning

#@State
It is one source of truth for any view in swiftUI. Views are volatile i.e they are ment to be changed according to every user actions. To persist a view we SwiftUI have ***@State*** which a persistant storage created by SwiftUI on views behalf. @State property wrapper tells the system, the view depends on the property value and need to be updated everytime it is changed, Hence on every runtime change on the state property are recognized and triggers a re-rendering of only the portion of view which uses the state property.

```SwiftUi
 @State var isBlue: Bool = true
```

Now @State wrapped property should be owned by the Top most one view
To pass the State wrapper to child view we use @Binding

#@Binding
@Binding property wrapper tells the system the property has read/write access to value without ***Ownership***. 
>Note:- Binding properties have their values passed in from parent view as a binding,Hence default value for the property is not needed

To create binding we pass State property reference by using ***$*** prefix.

```SwiftUi
 @State var isBlue: Bool = true
 
 var body : some View{
    ChildView(showColor: $isBlue)
 }
```

in childView we define 

```SwiftUi
 @Binding var showColor: Bool
```


## References 
[SwiftUI @State and @Binding](https://dev.to/thetealpickle/swiftui-state-and-binding-23j5)
[@ObservedObject, @State and @EnvironmentObject](https://www.hackingwithswift.com/quick-start/swiftui/whats-the-difference-between-observedobject-state-and-environmentobject)


#Heading

# H1
## H2
### H3
#### H4
##### H5
###### H6

Alternatively, for H1 and H2, an underline-ish style:

Alt-H1
======

Alt-H2
------

#Emphasis

Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~

#Lists

1. First ordered list item
2. Another item
⋅⋅* Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
⋅⋅1. Ordered sub-list
4. And another item.

⋅⋅⋅You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
⋅⋅⋅Note that this line is separate, but within the same paragraph.⋅⋅
⋅⋅⋅(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

* Unordered list can use asterisks
- Or minuses
+ Or pluses

#links

[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs and URLs in angle brackets will automatically get turned into links. 
http://www.example.com or <http://www.example.com> and sometimes 
example.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com


#Code

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
```python
s = "Python syntax highlighting"
print s
```
 
```
No language indicated, so no syntax highlighting. 
But let's throw in a <b>tag</b>.
```



