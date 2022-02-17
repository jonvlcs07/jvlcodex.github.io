---

title: "Go Templates"
date: 2022-01-11T19:26:25-03:00
lastmod: 
tags: ['hugo', 'blogging']
draft: true

---


A linguagem Go utiliza um biblioteca templates que faz exatamente o que está escrito no nome, ela cria templates programados com uma sintaxe específica para serem usados em HTML.<!--more-->

Para aprender como ela funciona nada melhor que brincar um pouco com os elementos básicos e para isso eu construi um shortcode em html chamado `learning_go_templates.html`. Nele é possível ver os exemplos que eu utilizei para aprendizado.

Primeiramente templates lidam com duas coisas:

1. texto
2. ações

Texto é qualquer coisa que for escrita no html e que será printada sem mudaça nenhuma:


```html
This is a text and will be rendered unchanged
```

```html
This is a text and will be rendered unchanged
```

Actions are how we can program templates to do things, they are set of beggining with `{{` and ending with `}}`

```html
{{"Everything between here is an action"}}
```
```html
Everything between here is an action
```



Comments in go are written using:

{{< learning_go_templates >}}




