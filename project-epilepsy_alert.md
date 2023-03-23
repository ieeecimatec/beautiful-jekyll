---
layout: page
title: Epilepsy Alert
subtitle: Detecção de gatilhos à epilepsia fotossensível
# cover-img: /assets/img/babyiot/babyiot-cover.jpg
---

<img src="../assets/img/epilepsy_alert/cover.png" width="100%"/>

### Apresentação
<p style="text-align:justify">
<b>Epilepsy Alert</b> é um projeto desenvolvido para detectar partes de vídeos que possam causar gatilhos à pessoas com epilepsia fotossensível. O aplicativo consegue analisar vídeos localizados no computador e vídeos do youtube por meio de link, além disso, também é capaz de marcar os pontos de gatilho ao longo dele.
</p>

### Introdução
<p style="text-align:justify;">
A epilepsia é uma doença que afeta cerca de 1 em cada 100 pessoas ao redor do mundo, das quais 3-5% podem sofrer gatilhos por luzes pulsantes ou por padrões contrastantes de luz, sendo essa uma condição conhecida como Epilepsia Fotossensível. Alguns vídeos com variações de iluminação rápida ou com padrões de alto contraste podem causar problemas às pessoas com essa condição e até mesmo desconforto às pessoas que não são afetadas por essa doença. Dessa forma, faz-se necessário identificar conteúdos prejudiciais detectando-os antes mesmo de ser distribuído ou visualizado.
<br><br>
Por conta dessa falta de fiscalização na internet, muitos ataques cibernéticos com o intuito de prejudicar as pessoas com fotossensibilidade já foram executados, até mesmo episódios televisivos afetaram crianças pelo mundo com o famoso episódio do	Porygon de Pokémon.
</p>

### Desenvolvimento
<p style="text-align:justify;">
O desenvolvimento do programa se deu inicialmente em detectar os padrões nos quais identificam possíveis flashes nocivos:
<ul>
  <li>Um flash potencialmente prejudicial ocorre quando há um par de mudanças opostas na luminância de 20 cd/m2 ou mais.</li>
  <li>A frequência do flash é superior a 3 Hz</li>
  <li>Uma sequência de imagens piscando com duração superior a 5s pode constituir um risco mesmo que esteja de acordo com as orientações acima.</li>
</ul>
</p>
<p style="text-align:justify;">
O aplicativo foi programado em Python por conta da sua facilidade no trabalho com imagens através da biblioteca openCV de visão computacional, que foi utlizada para computar a luminância de cada frame e utilizar os resultados na verificação das outras condições. Além disso, com o uso do tkinter foi possível desenvolver uma interface funcional e objetiva, ao fim o uso e multiprocessamento ajuda na velocidade de processamento.
<br><br>
Para detecção de um flash prejudicial foi necessário converter os valores RGB (vermelho, verde e azul) de cada pixel em seu valor correspondente à luminância através da fórmula:
<br><br>
Com esse valor para cada pixel fez-se uma média de todo o frame, seguinte a isto foi verificado a quantidade de frames por segundo do vídeo e com essas informações atestar se o ocorreram no mínimo 3 mudanças de contraste com diferença de luminância de 20 cd/m2 ou mais na quantidade de frames equivalente a 1 segundo, para satisfazer a condição de 3 Hz.
</p>

### Conclusão
<p style="text-align:justify;">
A análise do vídeo e a sinalização das partes que podem causar gatilhos à epilepsia fotossensível foi um sucesso, a aplicação consegue identificar esses momentos, mostrar em quaus pontos do vídeo eles acontecem e ainda gerar um gráfico de luminância do vídeo para análise em tempo real.
</p>

<img style="display:block; margin: 0 auto;" src="../assets/img/epilepsy_alert/video-timestamps.png" width="75%">
<p style="text-align:center"><small>Imagem 1. Vídeo com indentificação dos tempos danosos</small></p>

<img style="display:block; margin: 0 auto;" src="../assets/img/epilepsy_alert/video-graphics.png" width="75%">
<p style="text-align:center"><small>Imagem 2. Gráfico com mudanças da luminão ao longo do vídeo</small></p>

<p style="text-align:justify;">
Entretanto, sua precisão ainda não é perfeita, havendo possibilidade de otimizações no código Além disso, outra oportunidade de melhoria observada, foi a possibilidade de desenvolver um plugin, capaz de fazer essa análise em tempo real durante a reprodução de vídeos no YouTube, ou em outros sites pela Internet.
</p>
<br>

### Equipe de Desenvolvimento
<div class="row">
  <div class=" col-xl-auto offset-xl-0 col-lg-3 offset-lg-0">
    <div class="mobile-side-scroller">
      <table class="table-borderless highlight">
        <thead>
          <tr>
            <th style="text-align:center"><img src="{{ 'assets/img/voluntarios/icaro_yan.png' | relative_url }}" width="100" alt="ícaro yan" class="img-fluid rounded-circle"/></th>
            <th></th>
            <th style="text-align:center"><img src="{{ 'assets/img/voluntarios/joao_vitor_mendes.png' | relative_url }}" width="100" alt="joao vitor" class="img-fluid rounded-circle"/></th>
            <th></th>
            <th style="text-align:center"><img src="{{ 'assets/img/voluntarios/yasmin_bonfim.jpg' | relative_url }}" width="100" alt="yasmin bonfim" class="img-fluid rounded-circle"/></th>
          </tr>
        </thead>
        <tbody>
          <tr class="font-weight-bolder" style="text-align:center">
            <td style="text-align:center; padding:10px 0px" width="33%">Ícaro Yan</td>
            <td></td>
            <td style="text-align:center; padding:10px 0px" width="33%">João Vitor</td>
            <td></td>
            <td style="text-align:center; padding:10px 0px" width="33%">Yasmin Bonfim</td>
          </tr>
          <tr style="vertical-align:center">
            <td style="text-align:center">
            <small>Voluntário desde 2022<p>Líder do projeto</p></small></td>
            <td></td>
            <td style="text-align:center">
            <small>Voluntário desde 2022</small></td>
            <td></td>
            <td style="text-align:center">
            <small>Voluntária desde 2022</small></td>
            <td></td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</div>
