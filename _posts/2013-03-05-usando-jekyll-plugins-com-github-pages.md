---
layout: post
title: Usando Jekyll + Plugins com GitHub Pages
description: Depois de pesquisar um pouco, achei uma abordagem simples e fácil de solucionar isso.
---
Usar **Jekyll** com **GitHub Pages**, funciona muito bem, mas se for adicionar algum **plugin do Jekyll**, não funciona, o **GitHub Pages** não dá suporte. Depois de pesquisar um pouco, achei uma **abordagem simples** e fácil de solucionar isso. Como eu quis usar plugins - no seu caso isso pode ser opcional - aqui neste meu [novo blog]({{ site.url }}/novo-blog-no-ar) eu desenvolvi usando **Jekyll + Plugins** e hospedadei no **GitHub Pages**.

## Breve introdução
Leia caso não saiba do que se trata.

### O que é GitHub Pages

É um caminho fácil, simples e de graça para **hospedar o site** do seu projeto ou por exemplo seu blog pessoal. No site do [GitHub Pages](http://pages.github.com) explica tudo como funciona.

### O que é Jekyll

É uma forma simples de **gerar sites estáticos** em **Ruby**. Tem várias vantagens. O mais legal é que o **GitHub Pages** oferece **suporte** para usar **Jekyll**. As coisas funcionam como mágica :). Só acessar o repositório do [Jekyll](https://github.com/mojombo/jekyll) no **GitHub** e ler a documentação para colocar seu primeiro site no ar.

### O que é Jekyll plugin
O **Jekyll plugin** permite criar **conteúdos específicos** e **customizados** no site. Por exemplo, neste blog eu usei um plugin que dei o nome de [code_tag.rb](https://github.com/leandroadacosta/leandroadacosta.github.com/blob/source/_plugins/code_tag.rb) para facilitar a leitura de trechos de código que escrevo nos posts ao usuário. Basicamente o plugin faz o *highlight* automático do texto - gerando HTML e CSS - de acordo com o tipo de linguagem que desejar, seja Ruby, HTML, CSS, etc.

## Solução
Para usar **plugins customizados + GitHub Pages** é preciso de começo separar em duas branchs:

* `branch source` onde está o **código fonte**.
* `branch master` onde está o **código final gerado pelo   Jekyll**.

Adicionar no `.gitignore` a pasta `/_site` que é gerada pelo **Jekyll**. Este simples detalhe permite trocar da **branch source** para **master** e ainda manter os arquivos gerados na pasta `/_site`.

Para acontecer a mágica, é preciso mover os arquivos finais de dentro da pasta `/_site` para a pasta raiz da **branch master** e comitar na master esses arquivos gerados antes de dar push pro **GitHub**. Para entender melhor, veja abaixo:

{% highlight bash %}

git checkout source
// seja lá qualquer alteração feita
git status & git add & git commit
jekyll
git checkout master
cp -r _site/* . && rm -rf _site/ && touch .nojekyll
git status & git add & git commit
git push -all origin

{% endhighlight %}

Pronto. A parte chata é que você move e comita na **branch master** os códigos gerados pelo **Jekyll**. A parte boa é que você tem a **branch source** pra trabalhar tranquilamente no seu site e, o melhor de tudo, funciona com **Jekyll plugins**.

Pra facilitar a tarefa de copiar, criei um alias no meu bash:

{% highlight bash %}

alias jekyll-copy="cp -r _site/* . && rm -rf _site/ && touch .nojekyll"

{% endhighlight %}

Veja todo o código dessa abordagem de duas branchs no [repositório deste blog](https://github.com/leandroadacosta/leandroadacosta.github.com).

Espero ter ajudado.
