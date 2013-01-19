---
layout: post
title: TDC 2012 São Paulo Highlights
tags:
- Comunidade
- comunidade
- ruby
- ruby-on-rails
- the developers conference
status: publish
type: post
published: true
meta:
  _edit_last: '18856848'
  jabber_published: '1342659792'
  _wpas_done_facebook: '1'
  _wpas_done_twitter: '1'
  _wpas_skip_linkedin: '1'
---
<a href="{{ site.url }}/img/posts/tdc-2012/tdc-2012-sao-paulo-1.jpg"><img src="{{ site.url }}/img/posts/tdc-2012/tdc-2012-sao-paulo-1.jpg?w=300" alt="TDC 2012 São Paulo" style="max-width:640px"></a>

Sábado 07/07/2012 participei da conferência de desenvolvedores de software (<a href="http://www.thedevelopersconference.com.br/tdc/2012/index.html" target="_blank">TDC 2012 São Paulo</a>) na Universidade Anhembi Morumbi. Antes de falar sobre as palestras deixo um recado: ir a eventos é sempre muito bom, além do networking ser importante, vejo a troca de experiências como o maior benefício. O profissional de TI que não tem o senso de comunidade, está deixando de lado algo muito valioso.

<a href="{{ site.url }}/img/posts/tdc-2012/tdc-2012-sao-paulo-4.jpg"><img src="{{ site.url }}/img/posts/tdc-2012/tdc-2012-sao-paulo-4.jpg?w=300" alt="TDC 2012 São Paulo" style="max-width:640px"></a>

O evento aconteceu de 4 a 8 de Julho. Consegui ir somente no Sábado (dia 07) na <a href="http://www.thedevelopersconference.com.br/tdc/2012/saopaulo/trilha-ruby#programacao" target="_blank">trilha de Ruby</a> - sim, somente a linguagem Ruby, sem falar do framework <a href="http://rubyonrails.com.br/" target="_blank">Rails</a>. Das palestras, que por sinal foram muito boas, consegui tirar alguns pontos importantes que gostaria de compartilhá-los.

<a href="{{ site.url }}/img/posts/tdc-2012/tdc-2012-sao-paulo-3.jpg"><img src="{{ site.url }}/img/posts/tdc-2012/tdc-2012-sao-paulo-3.jpg?w=300" alt="Ricardo Valeriano - TDC 2012 São Paulo" style="max-width:640px"></a>

O dia começou com a palestra do grande <a href="http://blog.ricardovaleriano.com/" target="_blank">Ricardo Valeriano</a> sobre "<strong>A ferramenta ideal: uma questão de perspectiva.</strong>" e, como sempre, deu um show de dinamismo, descontraindo bastante a galera com seus slides cheios de <em>memes</em>, gostei bastante. Seguem os <em>highlights</em>:
<ul>
	<li>Desenvolver software é muito complexo, em sua maioria criasse um legado a longo prazo que não é sustentável. No começo e durante o desenvolvimento os profissionais tomam decisões sobre quais ferramentas vão usar - seja lá qual for, seja uma api específica, um framework, a linguagem a utilizar, ou etc. - sem entender completamente o porque, sem saber criticar as suas escolhas. Se preocupar sempre com o legado é essencial, no futuro pode ser outra pessoa ou equipe que vai encontrar um monstro ou um projeto bem estruturado, pense nisso. O projeto tem que se manter sustentável ao longo do tempo. Tenha em mente e entenda sempre as desvantagens da decisão tomada, assim você conseguirá evoluir o software com qualidade.</li>
	<li>Domine a linguagem ao ponto de criticar os pontos negativos. Não existe tecnologia ruim, a decisão depende do contexto, depende da pessoa e do momento.</li>
</ul>
<a href="http://cassiomarques.wordpress.com/" target="_blank">Cassio Marques</a> foi o único que falou de Rails além de Ruby. Cassio palestrou sobre "<strong>Porque você não deve usar os callbacks do ActiveRecord</strong>" (<a title="Porque você não deve usar os callbacks do ActiveRecord" href="https://speakerdeck.com/u/cassiomarques/p/porque-voce-nao-deve-usar-os-callbacks-do-activerecord" target="_blank">slides da palestra</a>), achei muito interessante os pontos abordados. Seguem os <em>highlights</em>:
<ul>
	<li>O teste está lento? Não sabe porque? Cuidado! Lembre-se que os callbacks do ActiveRecord nos seus modelos são executados quando você persiste objetos durante a execução dos testes.</li>
	<li>Não coloque regras de negócio nos callbacks pois será difícil de manter. Sendo assim, não tenha medo de isolar essa lógica criando outras classes se você está desenvolvendo orientado a objetos. Lembre-se que cada objeto deve fazer o mínimo possível e tem que fazer isso bem. Cuidado com convenções, elas são boas para criar um framework, mas não necessariamente para o contexto necessário para seu código.</li>
	<li>Ao codificar tenha em mente a clareza ao invés de não concisão. Como assim? É quando você acha que é o expert por escrever seu código de um jeito bonitinho, por exemplo, deixando o código com tudo inline só porque no Ruby é legal. Na verdade isso pode ser ruim, pois bonito é muitas vezes diferente de um código com <a href="http://blog.caelum.com.br/codigo-conciso-claro-e-breve/" target="_blank">clareza e concisão</a>, cuidado.</li>
</ul>
<a href="http://blog.qmx.me" target="_blank">Douglas 'qmx' Campos</a> palestrou sobre "<strong>Ruby é lento?</strong>", ele abordou alguns pontos fortes e fracos da linguagem e a comparou com outras linguagens também, foi bem interessante. Seguem os <em>highlights</em>:
<ul>
	<li>Ruby não é lento, mas pode ser lento, tudo depende de como foi usado. Ruby foi feito para deixar o programador feliz, quero dizer que tem muitas formas legais de programar as coisas e justamente por causa disso pode ser que fique lento. O desenvolvedor tem que saber que quanto mais poder e flexibilidade ele tem em mãos com a linguagem, maior é a responsabilidade dele em não fazer cagada com a performance.</li>
</ul>
E por fim uma dica, essa foi dada por <a href="http://nandovieira.com.br" target="_blank">Nando Vieira</a>:
<ul>
	<li>Você perde muito tempo configurando ambientes desde o zero para o desenvolvedor novo na equipe ou empresa? Dê uma olhada nisso: <a href="http://vagrantup.com/" target="_blank">http://vagrantup.com</a>.</li>
</ul>
Bom, foi o que consegui resumir das palestras. Espero ter ajudado.
Um abraço.