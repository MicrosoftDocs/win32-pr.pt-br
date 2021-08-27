---
title: Técnicas comuns para aprimorar os mapas de profundidade de sombra
description: Este artigo técnico fornece uma visão geral de alguns algoritmos comuns de mapa de profundidade de sombra e artefatos comuns, além de explicar várias técnicas, que vão desde o básico até o intermediário — que pode ser usado para aumentar a qualidade dos mapas de sombra padrão.
ms.assetid: bf994838-a261-0379-9301-eb9b250d216c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafff1b537830ae0ee681ed32932cca2b6274a4d9da3e0471ef498e0bef2d483
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102428"
---
# <a name="common-techniques-to-improve-shadow-depth-maps"></a>Técnicas comuns para aprimorar os mapas de profundidade de sombra

Os mapas de sombra, apresentados pela primeira vez em 1978, são uma técnica comum para adicionar sombras a jogos. Três décadas mais tarde, apesar de avanços em hardware e software, artefatos de sombreamento – ou seja, bordas shimmerings, alias de perspectiva e outros problemas de precisão — persistem.

Este artigo técnico fornece uma visão geral de alguns algoritmos comuns de mapa de profundidade de sombra e artefatos comuns, além de explicar várias técnicas, que vão desde o básico até o intermediário — que pode ser usado para aumentar a qualidade dos mapas de sombra padrão. A adição de mapas de sombra básicos a um título normalmente é simples, mas entender as nuances de artefatos de sombra pode ser desafiador. Este artigo técnico foi escrito para o desenvolvedor de gráficos intermediário que implementou sombras, mas não entende totalmente por que os artefatos específicos aparecem e não tem certeza de como contorná-los.

Selecionar as técnicas corretas para mitigar artefatos específicos não é trivial. Quando as deficiências do mapa de sombra são resolvidas, a diferença na qualidade pode ser impressionante (Figura 1). A implementação correta dessas técnicas melhora drasticamente as sombras padrão. As técnicas explicadas neste artigo são implementadas no exemplo CascadedShadowMaps11 no SDK do DirectX.

**Figura 1. Sombras com artefatos graves (à esquerda) e sombras após a implementação das técnicas descritas neste artigo (à direita)**

![sombras com artefatos graves (à esquerda) e sombras após a implementação das técnicas descritas neste artigo (à direita)](images/shadows-before-and-after.jpg)

## <a name="shadow-depth-maps-review"></a>profundidade da sombra Mapas revisão

O algoritmo de mapa de profundidade de sombra é um algoritmo de duas passagens. A primeira passagem gera um mapa de profundidade em espaço leve. Na segunda passagem, esse mapa é usado para comparar a profundidade de cada pixel em espaço leve em relação à sua profundidade correspondente no mapa de profundidade de espaço claro.

**Figura 2. Partes-chave de uma cena de sombra**

![partes-chave de uma cena de sombra](images/key-parts-of-shadow-scene.jpg)

### <a name="pass-1"></a>Pass 1

A cena é mostrada na Figura 2. Na primeira passagem (Figura 3), a geometria é renderizada em um buffer de profundidade do ponto de vista da luz. Mais especificamente, o sombreador de vértice transforma a geometria em um espaço de exibição clara.

O resultado final dessa primeira passagem é um buffer de profundidade que contém as informações de profundidade da cena do ponto de vista da luz. Isso agora pode ser usado em Pass 2 para determinar quais pixels são obstruídodos da luz.

**Figura 3. Primeira passagem de mapeamento de sombra básica**

![primeira passagem de mapeamento de sombra básica](images/first-pass-of-basic-hadow-mapping.png)

### <a name="pass-2"></a>Pass 2

Na segunda passagem (Figura 4), o sombreador de vértice transforma cada vértice duas vezes. Cada vértice é transformado no espaço de exibição da câmera e passado para o sombreador de pixel como a posição. Cada vértice também é transformado pela matriz da luz de exibição-projeção-Texture e passada para o sombreador de pixel como uma coordenada de textura. A matriz View-projetion-Texture é a mesma matriz usada para renderizar a cena na Pass 1 com uma transformação adicional. É uma transformação que dimensiona e traduz os pontos do espaço de exibição (– 1 a 1 em X e Y) para o espaço de textura (0 a 1 em X e 1 para 0 em Y).

O sombreador de pixel recebe a posição interpolada e as coordenadas de textura interpoladas. Tudo o que é necessário para executar o teste de profundidade agora está nessa coordenada de textura. O teste de profundidade agora pode ser executado com a indexação do buffer de profundidade da primeira passagem com as coordenadas X e Y Texture e a comparação do valor de profundidade resultante em relação à coordenada de textura Z.

**Figura 4. Segunda passagem de mapeamento de sombra básica**

![segunda passagem de mapeamento de sombra básica](images/second-pass-of-basic-shadow-mapping.png)

## <a name="shadow-map-artifacts"></a>Artifacts de mapa de sombra

O algoritmo de mapa de profundidade de sombra é o algoritmo de sombreamento em tempo real mais amplamente usado, mas ainda produz vários artefatos que exigem mitigação. Os tipos de artefatos que podem ocorrer são resumidos a seguir.

### <a name="perspective-aliasing"></a>Alias de perspectiva

O alias de perspectiva, um artefato comum, é mostrado na Figura 5. Isso ocorre quando o mapeamento de pixels em espaço de exibição para texels no mapa de sombra não é uma taxa de um para um. Isso ocorre porque os pixels próximos ao plano próximo estão mais juntos e exigem uma resolução de mapa de sombra mais alta.

A Figura 6 mostra um mapa de sombra e um frustum de exibição. Perto do olho, os pixels estão mais próximos, e muitos pixels são mapeados para o mesmo texels de sombra. Os pixels pelo plano distante são distribuídos, reduzindo assim o alias de perspectiva.

**Figura 5. Alias de alta perspectiva (à esquerda) versus alias de perspectiva baixa (direita)**

![alias de alta perspectiva (à esquerda) versus alias de perspectiva baixa (direita)](images/high-perspective-aliasing-vs-low-perspective-aliasing.jpg)

Para a imagem à esquerda, o alias de perspectiva é maior; muitos pixels de espaço de olho são mapeados para o mesmo texels de mapa de sombra. Na imagem à direita, o alias de perspectiva é baixo porque há um mapeamento 1:1 entre os pixels de espaço de olho e texels de mapa de sombra.

**Figura 6. Exibir frustum com o mapa de sombra**

![Exibir frustum com o mapa de sombra](images/view-frustum-with-shadow-map.jpg)

Os pixels claros no plano distante representam o alias de baixa perspectiva e os pixels escuros no plano próximo representam o alias de alta perspectiva.

A resolução do mapa de sombra também pode ser muito alta. Embora uma resolução mais alta seja menos perceptível, isso pode resultar em objetos pequenos, como fios de telefone, sem a transmissão de sombras. Além disso, ter uma resolução muito alta pode causar sérios problemas de desempenho devido a padrões de acesso de textura.

Os mapas de sombra em perspectiva (PSMs) e os mapas de sombra de perspectiva (LSPSMs) tentam resolver o alias da perspectiva distorcendo a matriz de projeção da luz para posicionar mais texels perto do olho onde são necessárias. Infelizmente, nenhuma técnica é capaz de resolver o alias de perspectiva. A parametrização da transformação necessária para mapear pixels de espaço de olho para texels no mapa de sombra não pode ser associada por uma distorção linear. Uma parametrização logarítmica é necessária. PSMs Coloque muitos detalhes perto do olho, fazendo com que as sombras distantes sejam de baixa qualidade ou até mesmo desaparecerem. O LSPSMs realiza um trabalho melhor de encontrar um aterramento médio entre a resolução crescente perto do olho e deixar detalhes suficientes para objetos distantes. Ambas as técnicas são geradas para sombras ortográficas em algumas configurações de cena. Essa degeração pode ser feita com o processamento de um mapa de sombra separado para cada face da exibição frustum, embora isso seja caro. Os mapas de sombra de perspectiva logarítmica (LogPSMs) também renderizam um mapa separado por face da exibição frustum. Essa técnica usa a rasterização não linear para posicionar mais texels perto do olho. O D3D10 e o hardware de classe D3D11 não dão suporte à rasterização não linear. Para obter mais informações sobre essas técnicas e algoritmos, consulte a seção References.

Os mapas de sombra em cascata (CSMs) são a técnica mais popular para lidar com o alias de perspectiva. Embora CSMs possa ser combinado com PSMs e LSPSMs, ele é desnecessário. O uso de CSMs para corrigir erros de alias de perspectiva é abordado no artigo complementar, [mapas de sombra em cascata](/windows/desktop/DxTechArts/cascaded-shadow-maps).

### <a name="projective-aliasing"></a>Alias projetado

O alias projetado é mais difícil de mostrar que o alias de perspectiva. As sombras disputadas destacadas na Figura 7 demonstram erros de alias projetados. O alias projetado ocorre quando o mapeamento entre texels no espaço da câmera para texels em espaço leve não é uma proporção de um para um; Isso ocorre devido à orientação da geometria em relação à câmera clara. O alias projetado ocorre conforme o plano tangente da geometria se torna paralelo aos raios claros.

**Figura 7. Alias de alta projeção versus alias de baixa projeção**

![alias de alta projeção versus alias de baixa projeção](images/high-projective-aliasing-vs-low%20projective-aliasing.jpg)

As técnicas usadas para aliviar erros de alias de perspectiva também atenuam o alias projetado. O alias projetado ocorre quando a superfície normal é ortogonal à luz; essas superfícies devem receber menos luz com base nas equações de iluminação difusa.

### <a name="shadow-acne-and-erroneous-self-shadowing"></a>Acne de sombra e incorreta Self-Shadowing

Sombra acne (Figura 8), um termo sinônimo de autosombreamento errôneo, ocorre quando o mapa de sombra quantizes a profundidade sobre um Texel inteiro. Quando o sombreador compara uma profundidade real com relação a esse valor, é provável que seja autosombreado, uma vez que ele deve ser sombreado.

Outro motivo para o Shadow acne é que o Texel em espaço leve está tão próximo da profundidade do Texel correspondente no mapa de profundidade que os erros de precisão fazem com que o teste de profundidade falhe erroneamente. Um motivo para essa diferença de precisão é que o mapa de profundidade foi calculado pelo hardware de rasterização de função fixa, enquanto a profundidade sendo comparada foi calculada pelo sombreador. O alias projetado também pode causar acne de sombra.

**Figura 8. Artefato acne sombra**

![artefato acne sombra](images/shadow-acne-artifact.jpg)

Conforme mostrado na imagem à esquerda, alguns de pixels falharam no teste de profundidade e criamos artefatos manchados e padrões moiré. Para reduzir a auto-sombreamento errado, os limites no plano próximo e o plano distante para a exibição de espaço frustum devem ser calculados da maneira mais rígida possível. A tendência de profundidade baseada em escala de inclinação e outros tipos de tendência são outras soluções usadas para mitigar o acne de sombra.

### <a name="peter-panning"></a>Peter panorâmica

O termo *Peter panorâmica* deriva seu nome do caractere de livro de um filho cuja sombra se tornou desanexada e que poderia voar. Esse artefato faz com que os objetos com sombras ausentes pareçam ser desanexados e flutuantes acima da superfície (Figura 9).

**Figura 9. Artefato do Peter panorâmica**

![artefato do Peter panorâmica](images/peter-panning-artifact.jpg)

Na imagem à esquerda, a sombra é desanexada do objeto, criando um efeito flutuante.

Uma técnica para remover a superfície acne é adicionar algum valor à posição de pixel em espaço leve; Isso é chamado de adição de um deslocamento de profundidade. Peter panorâmica resultados quando o deslocamento de profundidade usado é muito grande. Nesse caso, o deslocamento de profundidade faz com que o teste de profundidade passe erroneamente. Como o Shadow acne, Peter panorâmica é agravadas quando não há precisão suficiente no buffer de profundidade. Calcular os planos próximos e os planos distantes também ajuda a evitar Peter panorâmica.

## <a name="techniques-to-improve-shadow-maps"></a>Técnicas para melhorar o Mapas de sombra

Adicionar sombras a um título é um processo. A primeira etapa é obter mapas de sombra básicos funcionando. A segunda é garantir que todos os cálculos básicos sejam concluídos de maneira ideal: Frusta se ajustam o mais rigidamente possível, os planos próximos/distantes se encaixam rigidamente, a tendência de escala de inclinação é usada e assim por diante. Depois que as sombras básicas estiverem habilitadas e a melhor aparência possível, o desenvolvedor terá uma ideia mais adequada de quais algoritmos são necessários para obter as sombras a uma fidelidade suficiente. Dicas básicas que podem ser necessárias para obter mapas de sombra básicos que examinam seus melhores são fornecidos nesta seção.

### <a name="slope-scale-depth-bias"></a>Slope-Scale a tendência de profundidade

Como mencionado anteriormente, o sombreamento automático pode levar ao acne de sombra. Adicionar muita diferença pode resultar em Peter Panorâmicaing. Além disso, polígonos com inclinação acentuada (em relação à luz) sofrem mais de alias projetado do que polígonos com inclinação superficial (em relação à luz). Por isso, cada valor de mapa de profundidade pode precisar de um deslocamento diferente, dependendo da inclinação do polígono em relação à luz.

O hardware do Direct3D 10 tem a capacidade de inclinar um polígono com base em sua inclinação em relação à direção da exibição. Isso tem o efeito de aplicar uma grande diferença a um polígono que é exibido de ponta para a direção da luz, mas não aplica qualquer tendência a um polígono voltado diretamente para a luz. A Figura 10 ilustra como dois pixels vizinhos podem alternar entre sombreados e não sombreados ao testar a mesma inclinação não tendenciosa.

**Figura 10. Inclinação de profundidade dimensionada em comparação com profundidade não polarizada**

![inclinação de profundidade dimensionada em comparação com profundidade não polarizada](images/slope-scaled-depth-bias-compared-to-unbiased-depth.png)

### <a name="calculating-a-tight-projection"></a>Calculando uma projeção justa

Ajustar rigidamente a projeção da luz à exibição frustum aumenta a cobertura do mapa de sombra. A Figura 11 ilustra que usar uma projeção arbitrária ou ajustar a projeção aos limites da cena resulta em um alias de perspectiva mais alto.

**Figura 11. Frustum de sombra arbitrária e sombra frustum ajuste à cena**

![frustum de sombra arbitrária e sombra frustum ajuste à cena](images/arbitrary-shadow-frustum-and-shadow-frustum-fit-to-scene.jpg)

A exibição é do ponto de vista da luz. O trapézio representa o frustum da câmera de exibição. A grade desenhada sobre a imagem representa o mapa de sombra. A imagem à direita mostra que o mesmo mapa de sombra de resolução cria mais cobertura de Texel quando se ajusta mais rigidamente à cena.

A Figura 12 ilustra os frustums que se ajustam corretamente. Para calcular a projeção, os oito pontos que compõem a exibição frustum são transformados em espaço leve. Em seguida, os valores mínimo e máximo em X e Y são encontrados. Esses valores compõem os limites de uma projeção ortográfica.

**Figura 12. Ajuste de projeção de sombra para exibir frustum**

![ajuste de projeção de sombra para exibir frustum](images/shadow-projection-fit-to-view-frustum.jpg)

Também é possível recortar o frustum para a cena AABB para obter um limite mais rígido. Isso não é recomendável em todos os casos porque isso pode alterar o tamanho da projeção da câmera clara do quadro para o quadro. Muitas técnicas, como as descritas na seção movendo a luz Texel-Sized incrementos, apresentam melhores resultados quando o tamanho da projeção da luz permanece constante em todos os quadros.

### <a name="calculating-the-near-plane-and-far-plane"></a>Calculando o plano próximo e o plano distante

Os planos próximos e distantes são as partes finais necessárias para calcular a matriz de projeção. Quanto mais detalhadamente os planos, mais preciso os valores no buffer de profundidade.

O buffer de profundidade pode ser de 16 bits, de 24 bits ou de 32 bits, com valores entre 0 e 1. Em geral, os buffers de profundidade são um ponto fixo, com os valores próximos ao plano próximo agrupados mais de perto do que os valores próximos ao plano distante. O grau de precisão disponível para o buffer de profundidade é determinado pela proporção do plano próximo ao plano distante. Usar o mais rígido possível plano próximo/longe pode permitir o uso de um buffer de profundidade de 16 bits. Um buffer de profundidade de 16 bits pode reduzir o uso da memória enquanto aumenta a velocidade de processamento.

### <a name="aabb-based-near-plane-and-far-plane"></a>AABB-Based próximo plano e plano distante

Uma maneira fácil e simples de calcular o plano próximo e o avião é transformar o volume delimitador da cena em espaço leve. O menor valor de coordenada Z é o plano próximo e o maior valor de coordenada Z é o plano distante. Para muitas configurações da cena e da luz, essa abordagem é suficiente. No entanto, o pior cenário pode resultar em uma perda significativa de precisão no buffer de profundidade; A Figura 13 mostra esse cenário. Aqui, a faixa do plano próximo ao plano distante é quatro vezes maior do que o necessário.

A exibição frustum na Figura 13 foi intencionalmente escolhida para ser pequena. Uma pequena exibição frustum é mostrada em uma cena muito grande que consiste em pilares que se estendem da câmera de exibição. Usar o AABB de cena para os planos próximos e distantes não é o ideal. o algoritmo CSM descrito na [sombra em cascata Mapas](/windows/desktop/DxTechArts/cascaded-shadow-maps) artigo técnico deve calcular planos próximos e distantes para frustums muito pequenos.

**Figura 13. Planos próximos e distantes com base em AABB de cena**

![planos próximos e distantes com base em AABB de cena](images/near-far-%20planes-based-on-scene-aabb.jpg)

### <a name="frustum-based-near-plane-and-far-plane"></a>Frustum-Based próximo plano e plano distante

Outra técnica para calcular os planos próximos e distantes é transformar o frustum em espaço leve e usar os valores mínimo e máximo em Z como os planos próximos e distantes, respectivamente. A Figura 14 ilustra os dois problemas com essa abordagem. Primeiro, o cálculo é muito conservador, como mostrado quando o frustum se estende além da geometria da cena. Em segundo lugar, o plano próximo poderia ser muito apertado, fazendo com que os transmissões de sombra sejam cortados.

**Figura 14. Planos próximos e distantes com base apenas na exibição frustum**

![planos próximos e distantes com base apenas na exibição frustum](images/near-far-planes-based-solely-on-view-frustum.jpg)

### <a name="light-frustum-intersected-with-scene-to-calculate-near-and-far-planes"></a>Frustum claro interseccionado com a cena para calcular planos próximos e distantes

A maneira correta de calcular os planos próximos e distantes é mostrada na Figura 15. Quatro dos planos do frustum de luz ortográfica foram calculados usando o mínimo e o máximo das coordenadas X e Y da exibição frustum em espaço leve. Os dois últimos planos da exibição ortogonal frustum são os planos próximos e distantes. Para encontrar esses planos, os limites da cena são recortados em relação aos quatro planos de frustum claros conhecidos. Os valores Z menores e maiores do limite recentemente recortado representam o plano próximo e o plano distante, respectivamente.

O código que executa essa operação está localizado no exemplo CascadedShadowMaps11. Os oito pontos que compõem o AABB do mundo são transformados em espaço leve. Transformar os pontos em espaço leve simplifica os testes de recorte. Os quatro planos conhecidos do frustum Light agora podem ser representados como linhas. O volume delimitador de cenas em espaço leve pode ser representado como seis quadrilaterals. Esses 6 quadrilaterals podem então ser transformados em 12 triângulos para recortes baseados em triângulo. Os triângulos são recortados em relação aos planos conhecidos da exibição frustum (são linhas horizontais e verticais em X e Y em espaço leve). Quando um ponto de interseção é encontrado em X e Y, o triângulo 3D é recortado nesse ponto. Os valores Z mínimo e máximo de todos os triângulos recortados são os planos próximos e distantes. O exemplo CascadedShadowMaps11 mostra como executar esse recorte na função **ComputeNearAndFar** .

Há mais duas técnicas que podem ser usadas para calcular os mais rígidos planos próximos e distantes. Essas técnicas não são mostradas no exemplo CascadedShadowMaps.

-   Os planos mais rígidos próximos e distantes poderiam ser calculados interseccionando uma hierarquia de uma cena ou objetos individuais em uma cena em relação ao frustum claro. Isso seria computacionalmente mais complexo. Embora não esteja ilustrado no exemplo CascadedShadowMaps11, isso pode ser uma técnica válida para alguns blocos.
-   O plano distante pode ser calculado com o mínimo de:

    -   A maior profundidade da exibição frustum em espaço leve.
    -   A maior profundidade da interseção da exibição frustum e da cena AABB.

Essa abordagem pode ser problemática quando usada com mapas de sombra em cascata, onde é possível indexar fora de um frustum de exibição. Nesse caso, o mapa de sombra pode estar faltando Geometry.

**Figura 15. Planos próximos e distantes com base na interseção dos quatro planos calculados do frustum claro e da geometria delimitadora da cena**

![planos próximos e distantes com base na interseção dos quatro planos calculados do frustum claro e da geometria delimitadora da cena](images/near-far-plane-based-on-intersection-of-four.jpg)

### <a name="moving-the-light-in-texel-sized-increments"></a>Movendo a luz em incrementos de Texel-Sized

Um artefato comum em mapas de sombra é o efeito de borda shimmering. À medida que a câmera se move, os pixels ao longo das bordas são clareados e escurecedos. Isso não pode ser visto em imagens ainda, mas é muito perceptível e atrapalhando em tempo real. A Figura 16 realça esse problema e a figura 17 mostra como as bordas de sombra devem ser exibidas.

O erro de borda shimmering ocorre porque a matriz de projeção Light está sendo recalculada sempre que a câmera se move. Isso cria diferenças sutis nos mapas de sombra gerados. Todos os fatores a seguir podem influenciar a matriz criada para associar a cena.

-   Tamanho da exibição frustum
-   Orientação da exibição frustum
-   Local da luz
-   Local da câmera

Toda vez que essa matriz é alterada, as bordas de sombras podem ser alteradas.

**Figura 16. Bordas de sombra shimmering**

![bordas de sombra shimmering](images/shimmering-shadow-edges.jpg)

Os pixels ao longo da borda da sombra entram e saem da sombra à medida que a câmera se move da esquerda para a direita.

**Figura 17. Sombras sem bordas shimmerings**

![sombras sem bordas shimmerings](images/shadows-without-shimmering-edges.jpg)

As bordas de sombra permanecem constantes à medida que a câmera se move da esquerda para a direita.

Para luzes direcionais, a solução para esse problema é arredondar o valor mínimo/máximo em X e Y (que compõem os limites de projeção ortográficas) para incrementos de tamanho de pixel. Isso pode ser feito com uma operação de divisão, uma operação de andar e uma multiplicação.


```C++
        vLightCameraOrthographicMin /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMin = XMVectorFloor( vLightCameraOrthographicMin );
        vLightCameraOrthographicMin *= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax = XMVectorFloor( vLightCameraOrthographicMax );
        vLightCameraOrthographicMax *= vWorldUnitsPerTexel;
```



O valor de vWorldUnitsPerTexel é calculado por meio de um limite da exibição frustum e dividindo pelo tamanho do buffer.


```C++
        FLOAT fWorldUnitsPerTexel = fCascadeBound /
        (float)m_CopyOfCascadeConfig.m_iBufferSize;
        vWorldUnitsPerTexel = XMVectorSet( fWorldUnitsPerTexel, fWorldUnitsPerTexel,                            0.0f, 0.0f );
```



O limite do tamanho máximo da exibição frustum resulta em uma ajuste mais flexível para a projeção ortográfica.

É importante observar que a textura tem um pixel maior em largura e altura ao usar essa técnica. Isso mantém as coordenadas de sombra da indexação fora do mapa de sombra.

### <a name="back-face-and-front-face"></a>Face traseira e face frontal

Mapas de sombra devem ser renderizados com a remoção de face de fundo padrão, um processo que ignora a rasterização de objetos que o visualizador não pode ver e acelera a renderização da cena. Outra opção comum é renderizar mapas de sombra com a remoção de face frontal habilitada, o que significa que os objetos voltados para o visualizador são eliminados. O argumento para isso é que ele ajuda com o sombreamento automático, pois a geometria que compõe a parte posterior dos objetos é um deslocamento ligeiramente. Há dois problemas com essa ideia.

-   Qualquer objeto com geometria de frente ou verso inadequada causa artefatos no mapa de sombra. No entanto, ter uma geometria incorreta ou de face traseira causará outros problemas, por isso pode ser seguro pressupor que a geometria de frente e de verso seja feita corretamente. Pode ser impraticável criar faces traseiras para geometria baseada em Sprite, como folhagem.
-   Peter panorâmica e lacunas de sombra perto da base de objetos, como paredes, têm mais probabilidade de ocorrer porque a diparidade de profundidade de sombra é muito pequena.

### <a name="shadow-mapfriendly-geometry"></a>Mapa de sombra – geometria amigável

Criar geometria que funciona bem em mapas de sombra permite mais flexibilidade ao combater artefatos como Peter Panorâmicaing e Shadow acne.

As bordas rígidas são problemáticas para sombreamento automático. A diparidade de profundidade próxima à ponta da borda é muito pequena. Mesmo um pequeno deslocamento pode fazer com que os objetos percam suas sombras (Figura 18).

**Figura 18. Bordas nítidas causam artefatos que derivam de uma diparidade de profundidade com deslocamentos**

![bordas nítidas causam artefatos que derivam de uma diparidade de profundidade com deslocamentos](images/sharp-edges-cause%20artifacts.jpg)

Objetos estreitos, como paredes, devem ter backups mesmo se nunca estiverem visíveis. Isso aumentará a diparidade de profundidade.

Também é importante certificar-se de que a direção que a geometria está enfrentando está correta; ou seja, o fora de um objeto deve ser voltado e o dentro de um objeto deve ser frente. Isso é importante para o processamento com a remoção de face para frente habilitada, bem como para combater os efeitos de tendência de profundidade.

## <a name="summary"></a>Resumo

As técnicas descritas neste artigo podem ser usadas para aumentar a qualidade dos mapas de sombra padrão. A próxima etapa é examinar as técnicas que podem funcionar bem com mapas de sombra padrão. CSMs são recomendadas como uma técnica superior para combater o alias de perspectiva. A filtragem mais próxima ou os mapas de sombra de variação podem ser usados para suavizar as bordas de sombra. consulte o artigo técnico [Mapas de sombra em cascata](/windows/desktop/DxTechArts/cascaded-shadow-maps) para obter mais informações.

Donnelly, W. e Lauritzen, A [mapas sombra de variação](https://portal.acm.org/citation.cfm?doid=1111411.1111440). Symposium em gráficos 3D interativos, procedimentos de Symposium de 2006 em jogos e gráficos 3D interativos. 2006, pp. 161 – 165.

Engel, Woflgang F. section 4. Mapas de sombra em cascata. ShaderX5, *técnicas de renderização avançadas*, Wolfgang F. Engel, Ed. Charles River Media, Boston, Massachusetts. 2066h PP. 197 – 206.

Stamminger, Marc e Drettakis, George. [Mapas de sombra em perspectiva](https://portal.acm.org/citation.cfm?id=566616). Conferência Internacional em gráficos de computador e técnicas interativas, *procedimentos da conferência anual de 29 em gráficos de computador e técnicas interativas*. 2002, PP 557 – 562.

Wimmer, M., Scherzer, D. e Purgathofer, W. [mapas sombra da perspectiva do espaço](https://www.cg.tuwien.ac.at/research/vr/lispsm/shadows_egsr2004_revised.pdf). Eurographics Symposium na renderização. 2064h Revisado em 10 de junho de 2005. [Technische Universität Wien](https://www.cg.tuwien.ac.at/research/vr/lispsm/).

 

 
