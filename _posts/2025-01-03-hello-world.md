---
layout: post
title:  "Este é meu titulo!"
date:   2025-01-03 00:26:48 -0300
categories: welcome
---
## Meu título
# Meu sub-título
Texto texto texto texto texto texto texto

|Um  |Dois  |Tês  |
|---|---|---|
|ColunaA  |ColunaB  |ColunaC  |
|ColunaA  |ColunaB  |ColunaC  |

Texto texto texto texto texto texto texto

```
function test() {
  console.log("notice the blank line before this function?");
}
```

Texto texto texto texto texto texto texto

{% highlight javascript %}
function sayHello(name) {
  if (!name) {
    console.log('Hello World');
  } else {
    console.log(`Hello ${name}`);
  }  
}  
{% endhighlight %}


How to highlight code on a Jekyll site - Syntax HighlightingFebruary 11, 2019  1 minute read  
Menu
1 Jekyll Rouge Highlight Tag
Example:
2 GitHub Flavored Markdown Fenced Code Blocks
Example:
Example with language specified:
Result
References:
Support Jun
To have code snippets highlighted so that they are more reader-friendly, we have to wrap our code using the following syntax.

1 Jekyll Rouge Highlight TagPermalink
You can install kramdown markdown parser and rouge highlighter - Jekyll’s default highlighter using the following command:

gem install kramdown rouge
After installing kramdown and rouge, you can add the following to your _config.yml file.

markdown: kramdown
highlighter: rouge
    input: GFM
After that, you can now highlight your code by surrounding your code with {% highlight language %} and {% endhighlight %}. Replace languageCode with the code language. You can refer to this rouge doc for the list of supported languages.

Example:Permalink

{% highlight javascript %}
function sayHello(name) {
  if (!name) {
    console.log('Hello World');
  } else {
    console.log(`Hello ${name}`);
  }  
}  
{% endhighlight %}

You can read liquid tags doc for more detailed information.

2 GitHub Flavored Markdown Fenced Code BlocksPermalink
We can also use GitHub Fenced Code Blocks syntax. This syntax seems to be less verbose and cleaner.

Example:Permalink
```
function sayHello(name) {
  if (!name) {
    console.log('Hello World');
  } else {
    console.log(`Hello ${name}`);
  }
}

```
To syntax highlight for code of a specific language, you can add the language name next to the opening 3 backticks. You can refer to this rouge doc for the list of supported languages.

Example with language specified

```javascript
function sayHello(name) {
  if (!name) {
    console.log('Hello World');
  } else {
    console.log(`Hello ${name}`);
  }
}
```
