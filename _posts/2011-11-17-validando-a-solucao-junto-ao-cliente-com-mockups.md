---
lang: pt-br
layout: post
title: Validando a solução junto ao cliente com Mockups
tags:
- mockups
- prototipação
- User Experience
- user experience
status: publish
type: post
published: true
meta:
  _wpas_skip_linkedin: '1'
  _wpas_skip_twitter: '1'
  _wpas_skip_facebook: '1'
  _syntaxhighlighter_encoded: '1'
  _edit_last: '18856848'
  original_post_id: '543'
  _wp_old_slug: '543'
---
<p>Compartilho com vocês uma experiência na prática que tivemos recentemente em um cliente, sobre como nos ajudou, e muito, iniciar o desenvolvimento do software <strong>centrado na usabilidade do usuário</strong>.</p>

<h2>Primeira reunião</h2>
<p>Fizemos uma reunião presencial - na parte da manhã - de 2 horas no cliente para entender a necessidade de negócio. Parece simples, mas, tem uma questão muito importante nesta fase, que é <strong>separar o problema da solução</strong>. Pensando desta forma, conseguimos focar e entender os problemas atuais, suas causas e efeitos.</p>
<p>Após ter definido parte do conceito, achamos que, para validar o entendimento, seria legal rabiscar naquele momento alguns pré-protótipos frente ao cliente. Foi bem interessante pois conseguimos - além de verbalizar - mostrar no papel nosso entendimento, foi mais fácil para ambos, onde saímos mais confiantes.</p>

<h2>Lição de casa</h2>
<p>No mesmo dia, após o almoço - <strong>sem burocracia</strong> - voltamos e começamos um <em>brainstorm</em> com somente 2 pessoas, onde desenhamos na lousa e rabiscamos os primeiros <strong>protótipos</strong> no papel. O interessante neste processo, é que fizemos várias <strong>dramatizações</strong> - isso acontece direto, cada um encenando vários papeis relacionados ao negócio que estávamos resolvendo. Chega a ser engraçado, mas é muito <strong>produtivo</strong> e <strong>importante</strong>.</p>
<p>Ao final do dia, tínhamos em mãos toda uma visão da solução - centrada no usuário. Veja, fizemos tudo isso, em apenas um dia. Há, espera aí, você está me dizendo que desenho em lousa e papel é solução? E ainda tem mais, como já é solução se nem foi validada junto ao cliente. Direi como agimos para resolver esses fatos.</p>

<h2>Validando junto ao cliente</h2>
<p>No outro dia, logo cedo, estávamos conversando sobre a forma menos burocrática possível e <strong>ágil</strong> de validar a solução junto ao cliente. A forma que fazíamos em outros projetos era marcar outra reunião para levar todos os protótipos em papel e demonstrar ao cliente. Sempre foi muito ágil e produtivo. Neste caso, em praticamente 2 dias conseguiríamos validar toda uma visão de proposta de solução. Mas! Como sempre, queria <a title="Perigo na Zona de Conforto" href="https://leandroadacosta.com/2011/10/25/perigo-na-zona-de-conforto/" target="_blank">conquistar</a> algo diferente. Tinha na manga <strong>um jeito novo</strong> para testar.</p>
<p>Fui ao evento <a title="RubyConf 2011 " href="https://rubyconf2011.akitaonrails.com/" target="_blank">Ruby Conf 2011</a> nos dias 03 e 04 de novembro e assisti a palestra <strong><a title="Melhores Softwares através da Interface" href="https://www.eventials.com/rubyconfbr/recorded/M2UzZTJkMzY2MzdiNTg2NTUxNWM1MzI3NWY1YjRhMzYjIzQwMw_3D_3D" target="_blank">"Melhores Softwares através da Interface"</a></strong> do <strong><a href="https://twitter.com/danielvlopes" target="_blank">Daniel Lopes</a></strong>. Por sinal, <strong>excelente palestra</strong>. Ele enfatizou a importância do Designer de Interface saber programar, dos benefícios de começar o software pela interface, e uma forma diferente de validar propostas de solução - protótipos - junto ao cliente.</p>
<p>O que o Daniel passou de diferente do que já trabalhamos aqui na Cocento Tecnologia - e que achei muito legal - foi o <strong>jeito pragmático de validar junto ao cliente</strong>.</p>

<h2>Validando a proposta de solução com Mockups</h2>
<p>A idéia passada pelo <strong>Daniel Lopes</strong> é, em vez de validar os protótipos em papel ou photoshop/fireworks, é validar direto em <strong>protótipos funcionais</strong> - com fluxo entre as telas - já <strong>implementados em código</strong> - ruby/java/php/etc e html, css e js. E foi o que fizemos, logo na parte da manhã do segundo dia, criamos o projeto no GitHub implementamos as telas já em Ruby on Rails. Para isto, segue o conceito de <strong>Mockups</strong> apresentada pelo Daniel:</p>

Definimos a rota:

{% highlight ruby %}
Example::Application.routes.draw do

  scope '/mockups', :constraints => lambda { |e| not Rails.env.production? } do
    match '/:action', :controller => 'mockups', :actions => /[^/]+/
  end

end
{% endhighlight %}

Criamos o controller:

{% highlight ruby %}
class MockupsController < ApplicationController
  def books_list
  end

  def new_book
  end
end
{% endhighlight %}

Para cada método do controller implementamos a view em HTML, CSS e JS para simular alguns comportamentos, por fim, linkamos os fluxos entre elas:

{% highlight text %}
|~app/
| |+assets/
| |~controllers/
| | |-application_controller.rb
| | `-mockups_controller.rb
| |+helpers/
| |+mailers/
| |+models/
| `~views/
|   |~layouts/
|   | `-application.html.erb
|   `~mockups/
|     |-books_list.html.erb
|     `-new_book.html.erb
{% endhighlight %}

<h2>Resultado final</h2>
<p>Tínhamos no final do segundo dia um <strong>protótipo</strong> totalmente <strong>funcional</strong> e <strong>bonito</strong>. Pera aí, como em um dia conseguiram deixar o layout bonito? Vou abrir o segredo com vocês :). Para agilizar o processo, usamos todo um padrão para o front-end do <a title="Twitter Bootstrap" href="https://twitter.github.com/bootstrap/" target="_blank">Twitter Bootstrap</a>.</p>
<p>Fizemos a reunião no terceiro dia e o <strong>feedback</strong> foi <strong>excelente</strong>. <strong>Cliente</strong> muitíssimo <strong>satisfeito</strong> e a nossa equipe também. O importante é frisar que fizemos a primeira reunião de entendimento da necessidade até a codificação e validação em apenas 3 dias.</p>
<p>--</p>
<p>E você? Como faz para agilizar, diminuir os riscos e ser produtivo nas validações de proposta de solução junto ao cliente lá na sua empresa e/ou equipe?
Um abraço.</p>
