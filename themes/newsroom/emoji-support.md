+++
position = 11
author = "Hugo Authors"
title = "Emoji Support"
date = "2019-03-05"
description = "Guide to emoji usage in Hugo"
tags = ["emoji"]
image = "/images/artist.jpg"
+++

Emoji can be enabled in a Hugo project in a number of ways.
<!--more-->

The `[emojify](https://gohugo.io/functions/emojify/)` function can be called directly in templates or [Inline Shortcodes](https://gohugo.io/templates/shortcode-templates/#inline-shortcodes).

To enable emoji globally, set `enableEmoji` to `true` in your site’s [configuration](https://gohugo.io/getting-started/configuration/) and then you can type emoji shorthand codes directly in content files; e.g.

<p><span class="nowrap"><span class="emojify">🙈</span> <code>:see_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙉</span> <code>:hear_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙊</span> <code>:speak_no_evil:</code></span></p>
<br>

The [Emoji cheat sheet](http://www.emoji-cheat-sheet.com/) is a useful reference for emoji shorthand codes.

***

**N.B.** The above steps enable Unicode Standard emoji characters and sequences in Hugo, however the rendering of these glyphs depends on the browser and the platform. To style the emoji you can either use a third party emoji font or a font stack; e.g.

### Inline CSS

```html
<style>
  .emojify {
    font-family: Apple Color Emoji,Segoe UI Emoji,NotoColorEmoji,Segoe UI Symbol,Android Emoji,EmojiSymbols;
    font-size: 2rem;
    vertical-align: middle;
  }
  @media screen and (max-width:650px) {
    .nowrap {
      display: block;
      margin: 25px 0;
    }
  }
</style>
```

### Javascript

```javascript
function createEl(element) {
  return document.createElement(element);
}

function elem(selector, parent = document){
  let elem = parent.querySelector(selector);
  return elem != false ? elem : false;
}

let navBar = elem(`.${bar}`);
let nav = elem('.nav-body');
let open = 'nav-open';
let exit = 'nav-exit';
let drop = 'nav-drop';
let pop = 'nav-pop';
let navDrop = elem(`.${drop}`);
let hidden = 'hidden';

```

### Swift

```swift
class Person {
  var residence: Residence?
}

class Residence {
  var rooms = [Room]()
  var numberOfRooms: Int {
    return rooms.count
  }

  
  subscript(i: Int) -> Room {
    get {
      return rooms[i]
    }
    set {
      rooms[i] = newValue
    }
  }
  
  func printNumberOfRooms() {
    print("The number of rooms is \(numberOfRooms)")
  }

  var address: Address?

}
```
