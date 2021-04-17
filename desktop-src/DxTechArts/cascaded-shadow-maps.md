---
title: Mapas de sombra em cascata
description: Os mapas de sombra em cascata (CSMs) são a melhor maneira de combater um dos erros mais predominantes com a aplicação de alias de perspectiva de sombreamento.
ms.assetid: d3570d0a-74e0-5b9c-6586-c933f630c4ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae70433f97f33c3cc28af8e282b14ea1f513cf4d
ms.sourcegitcommit: 54db9e6a00a5c8f68e7c1a16b8c6d4943374498c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "106165529"
---
# <a name="cascaded-shadow-maps"></a>Mapas de sombra em cascata

Os mapas de sombra em cascata (CSMs) são a melhor maneira de combater um dos erros mais predominantes com sombreamento: alias de perspectiva. Este artigo técnico, que pressupõe que o leitor está familiarizado com o mapeamento de sombra, resolve o tópico de CSMs. Especificamente, ele:

-   explica a complexidade do CSMs;
-   fornece detalhes sobre as possíveis variações dos algoritmos CSM;
-   Descreve as duas técnicas de filtragem mais comuns: PCF (filtragem mais próxima de percentual) e filtragem com mapas de sombra de variação (VSMs);
-   Identifica e aborda algumas das armadilhas comuns associadas à adição de filtragem ao CSMs; e
-   mostra como mapear CSMs para Direct3D 10 por meio de hardware do Direct3D 11.

O código usado neste artigo pode ser encontrado no SDK (Software Development Kit) do DirectX nos exemplos CascadedShadowMaps11 e VarianceShadows11. Este artigo se mostrará mais útil depois de implementar as técnicas abordadas no artigo técnico, [técnicas comuns para melhorar os mapas de profundidade de sombra](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps), são implementadas.

## <a name="cascaded-shadow-maps-and-perspective-aliasing"></a>Mapas de sombra em cascata e alias de perspectiva

O alias de perspectiva em um mapa de sombra é um dos problemas mais difíceis de superar. No artigo técnico, técnicas comuns para melhorar os mapas de profundidade de sombra, o alias de perspectiva é descrito e algumas abordagens para mitigar o problema são identificadas. Na prática, o CSMs tende a ser a melhor solução e é normalmente empregado em jogos modernos.

O conceito básico de CSMs é fácil de entender. Áreas diferentes da câmera frustum exigem mapas de sombra com resoluções diferentes. Os objetos mais próximos do olho exigem uma resolução maior do que fazer com mais objetos distantes. Na verdade, quando o olho se move muito próximo da geometria, os pixels mais próximos do olho podem exigir muita resolução que até mesmo um mapa de sombra de 4096 × 4096 é insuficiente.

A ideia básica do CSMs é particionar o frustum em vários Frusta. Um mapa de sombra é renderizado para cada subfrustum; em seguida, o sombreador de pixel faz amostras do mapa que mais se aproximará da resolução necessária (Figura 2).

**Figura 1. Cobertura do mapa de sombra**

![cobertura do mapa de sombra](images/shadow-map-coverage.png)

Na Figura 1, a qualidade é mostrada (da esquerda para a direita) da mais alta para a mais baixa. A série de grades que representa mapas de sombra com uma exibição frustum (cone invertido em vermelho) mostra como a cobertura de pixel é afetada com mapas de sombra de resolução diferentes. As sombras são da qualidade mais alta (pixels brancos) quando há um mapeamento de proporção de 1:1 pixels em espaço leve para texels no mapa de sombra. O alias de perspectiva ocorre na forma de mapas de textura grandes e bloqueados (imagem esquerda) quando muitos pixels são mapeados para o mesmo Texel de sombra. Quando o mapa de sombra é muito grande, ele está em amostra. Nesse caso, os texels são ignorados, os artefatos do shimmering são introduzidos e o desempenho é afetado.

**Figura 2. Qualidade de sombra CSM**

![qualidade de sombra CSM](images/csm-shadow-quality.png)

A Figura 2 mostra recortes da seção de qualidade mais alta em cada mapa de sombra na Figura 1. O mapa de sombra com os pixels mais bem colocados (no Apex) é mais próximo do olho. Tecnicamente, esses são mapas do mesmo tamanho, com branco e cinza usados para exemplificar o sucesso do mapa de sombra em cascata. O branco é ideal porque mostra uma boa cobertura – uma proporção de 1:1 para pixels de espaço de olho e texels de mapa de sombra.

CSMs exigem as etapas a seguir por quadro.

1.  Particione o frustum em subfrusta.
2.  Compute uma projeção ortográfica para cada subfrustum.
3.  Renderizar um mapa de sombra para cada subfrustum.
4.  Renderizar a cena.

    1.  Associar os mapas de sombra e renderizar.
    2.  O sombreador de vértice faz o seguinte:

        -   Computa coordenadas de textura para cada subfrustum leve (a menos que a coordenada de textura necessária seja calculada no sombreador de pixels).
        -   Transforma e ilumina o vértice e assim por diante.

    3.  O sombreador de pixel faz o seguinte:

        -   Determina o mapa de sombra adequado.
        -   Transforma as coordenadas de textura, se necessário.
        -   A amostra da cascata.
        -   Acende o pixel.

## <a name="partitioning-the-frustum"></a>Particionando o frustum

O particionamento do frustum é o ato de criar subfrusta. Uma técnica para dividir o frustum é calcular intervalos de zero% a 100% na direção Z. Cada intervalo representa um plano próximo e um plano distante como uma porcentagem do eixo Z.

**Figura 3. Exibir frustums particionados arbitrariamente**

![Exibir frustums particionados arbitrariamente](images/view-frustums-partitioned-arbitrarily.png)

Na prática, recalcular as divisões de frustum por quadro causa bordas de sombra para shimmer. A prática geralmente aceita é usar um conjunto estático de intervalos em cascata por cenário. Nesse cenário, o intervalo ao longo do eixo Z é usado para descrever um subfrustum que ocorre ao particionar o frustum. Determinar os intervalos de tamanho corretos para uma determinada cena depende de vários fatores.

### <a name="orientation-of-the-scene-geometry"></a>Orientação da geometria da cena

Em relação à geometria da cena, a orientação da câmera afeta a seleção de intervalo em cascata. Por exemplo, uma câmera muito perto do solo, como uma câmera de aterramento em um jogo de futebol, tem um conjunto estático diferente de intervalos em cascata do que uma câmera no céu.

A Figura 4 mostra algumas câmeras diferentes e suas respectivas partições. Quando o intervalo Z da cena é muito grande, mais planos de divisão são necessários. Por exemplo, quando o olho é muito próximo do plano de chão, mas objetos distantes ainda são visíveis, várias cascatas podem ser necessárias. Dividindo o frustum de forma que mais divisões estejam perto do olho (em que o alias da perspectiva está mudando o mais rápido) também é valioso. Quando a maior parte da geometria é concentrados em uma pequena seção (como uma exibição de sobrecarga ou um simulador de voo) da exibição frustum, são necessárias menos cascatas.

**Figura 4. Configurações diferentes exigem divisões de frustum diferentes**

![configurações diferentes exigem divisões de frustum diferentes](images/different-configurations-require-different-frustum-splits.png)

Mantida Quando Geometry tem um intervalo dinâmico alto em Z, muitas cascatas são necessárias. Centraliza Quando a geometria tem um intervalo dinâmico baixo em Z, não há muito benefício de vários frustums. Adequada Somente três partições são necessárias quando o intervalo dinâmico é médio.

### <a name="orientation-of-the-light-and-the-camera"></a>Orientação da luz e da câmera

A matriz de projeção de cada cascata é ajustada rigidamente ao seu subfrustum correspondente. Em configurações nas quais a câmera de exibição e as direções claras são ortogonal, as cascatas podem se ajustar com pouca sobreposição. A sobreposição se torna maior à medida que a luz e a câmera de exibição se movem para o alinhamento paralelo (Figura 5). Quando a luz e a câmera de exibição são quase paralelas, ela é chamada de "Dueling Frusta" e é um cenário muito difícil para a maioria dos algoritmos de sombreamento. Não é incomum restringir a luz e a câmera para que esse cenário não ocorra. O CSMs, no entanto, executa muito melhor do que muitos outros algoritmos nesse cenário.

**Figura 5. Sobreposição em cascata aumenta conforme a direção da luz se torna paralela com a direção da câmera**

![sobreposição em cascata aumenta conforme a direção da luz se torna paralela com a direção da câmera](images/cascade-overlap-increases-as-light-direction-becomes.jpg)

Muitas implementações de CSM usam Frusta de tamanho fixo. O sombreador de pixel pode usar a profundidade Z para indexar na matriz de cascata quando o frustum é dividido em intervalos de tamanho fixo.

## <a name="calculating-a-view-frustum-bound"></a>Calculando um View-Frustum associado

Depois que os intervalos de frustum são selecionados, os subfrusta são criados usando um dos dois: ajustar à cena e ajustar à cascata.

### <a name="fit-to-scene"></a>Ajustar à cena

Todos os Frusta podem ser criados com o mesmo plano próximo. Isso força a sobreposição das cascatas. O exemplo CascadedShadowMaps11 chama essa técnica ajustada à cena.

### <a name="fit-to-cascade"></a>Ajustar à cascata

Como alternativa, Frusta pode ser criado com o intervalo de partição real que está sendo usado como planos próximos e distantes. Isso causa um ajuste mais rígido, mas é degenerado para se ajustar à cena no caso de Dueling Frusta. Os exemplos de CascadedShadowMaps11 chamam essa técnica se ajustam à cascata.

Esses dois métodos são mostrados na Figura 6. Ajustar à cascata desperdiça menos resolução. O problema de ajustar à cascata é que a projeção ortográfica aumenta e diminui com base na orientação da exibição frustum. A técnica ajustar à cena ajusta a projeção ortográfica pelo tamanho máximo da exibição frustum removendo os artefatos que aparecem quando a câmera de exibição é movida. [Técnicas comuns para melhorar os mapas de profundidade de sombra](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) abordam os artefatos que aparecem quando a luz se move na seção "movendo a luz em incrementos de tamanho de Texel".

**Figura 6. Ajustar à cena versus ajustar à cascata**

![ajustar à cena em vez de ajustar à cascata](images/fit-to-scene-vs-fit-to-cascade.png)

## <a name="render-the-shadow-map"></a>Renderizar o mapa de sombra

O exemplo CascadedShadowMaps11 renderiza os mapas de sombra em um buffer grande. Isso ocorre porque o PCF em matrizes de textura é um recurso do Direct3D 10,1. Para cada cascata, um visor é criado para cobrir a seção do buffer de profundidade correspondente a essa cascata. Um sombreador de pixel nulo está associado porque apenas a profundidade é necessária. Por fim, o visor e a matriz de sombra corretos são definidos para cada cascata à medida que os mapas de profundidade são renderizados um de cada vez no buffer de sombra principal.

## <a name="render-the-scene"></a>Renderizar a cena

O buffer que contém as sombras agora está associado ao sombreador de pixel. Há dois métodos para selecionar a cascata implementada no exemplo CascadedShadowMaps11. Esses dois métodos são explicados com o código do sombreador.

### <a name="interval-based-cascade-selection"></a>Interval-Based seleção em cascata

**Figura 7. Seleção em cascata baseada em intervalo**

![seleção em cascata baseada em intervalo](images/interval-based-cascade-selection.jpg)

Na seleção baseada em intervalo (Figura 7), o sombreador de vértice computa a posição em espaço Mundial do vértice.


```C++
Output.vDepth = mul( Input.vPosition, m_mWorldView ).z;
```



O sombreador de pixel recebe a profundidade interpolada.


```C++
fCurrentPixelDepth = Input.vDepth;
```



A seleção em cascata baseada em intervalo usa uma comparação de vetor e um produto de ponto para determinar o cacade correto. O \_ sinalizador contagem em cascata \_ especifica o número de cascata. Os \_ dados m fCascadeFrustumsEyeSpaceDepths \_ restringem a exibição de partições frustum. Após a comparação, o fComparison contém um valor de 1 em que o pixel atual é maior que a barreira e um valor de 0 quando a cascata atual é menor. Um produto de ponto soma esses valores em um índice de matriz.


```C++
        float4 vCurrentPixelDepth = Input.vDepth;
        float4 fComparison = ( vCurrentPixelDepth > m_fCascadeFrustumsEyeSpaceDepths_data[0]);
        float fIndex = dot(
        float4( CASCADE_COUNT_FLAG > 0,
        CASCADE_COUNT_FLAG > 1,
        CASCADE_COUNT_FLAG > 2,
        CASCADE_COUNT_FLAG > 3)
        , fComparison );

        fIndex = min( fIndex, CASCADE_COUNT_FLAG );
        iCurrentCascadeIndex = (int)fIndex;
```



Depois que a cascata é selecionada, a coordenada de textura deve ser transformada na cascata correta.


```C++
vShadowTexCoord = mul( InterpolatedPosition, m_mShadow[iCascadeIndex] );
```



Essa coordenada de textura é usada para exemplificar a textura com a coordenada X e a coordenada Y. A coordenada Z é usada para fazer a comparação de profundidade final.

### <a name="map-based-cascade-selection"></a>Map-Based seleção em cascata

A seleção baseada em mapa (Figura 8) testa os quatro lados da cascata para encontrar o mapa mais rígido que cobre o pixel específico. Em vez de calcular a posição no espaço de mundo, o sombreador de vértice calcula a posição do espaço de exibição para cada cascata. O sombreador de pixel itera em cascata a fim de dimensionar e deslocar as coordenadas de textura para que elas indexem a cascata atual. A coordenada de textura é então testada em relação aos limites de textura. Quando os valores X e Y da coordenada de textura se enquadram dentro de uma cascata, eles são usados para exemplificar a textura. A coordenada Z é usada para fazer a comparação de profundidade final.

**Figura 8. Seleção de cascata baseada em mapa**

![seleção de cascata baseada em mapa](images/map-based-cascade-selection.jpg)

### <a name="interval-based-selection-vs-map-based-selection"></a>Seleção de Interval-Based de seleção versus Map-Based

A seleção baseada em intervalo é ligeiramente mais rápida que a seleção baseada em mapa porque a seleção em cascata pode ser feita diretamente. A seleção baseada em mapa deve interceptar a coordenada de textura com os limites em cascata.

A seleção baseada em mapa usa a cascata com mais eficiência quando mapas de sombra não se alinham perfeitamente (veja a Figura 8).

## <a name="blend-between-cascades"></a>Misturar entre cascata

VSMs (discutido mais adiante neste artigo) e técnicas de filtragem, como PCF, podem ser usadas com CSMs de baixa resolução para produzir sombras suaves. Infelizmente, isso resulta em uma fenda visível (Figura 9) entre as camadas em cascata porque a resolução não corresponde. A solução é criar uma banda entre mapas de sombra em que o teste de sombra é executado para ambas as cascatas. Em seguida, o sombreador interpola linearmente entre os dois valores com base na localização do pixel na banda do Blend. Os exemplos CascadedShadowMaps11 e VarianceShadows11 fornecem um controle deslizante de GUI que pode ser usado para aumentar e diminuir essa faixa de desfoque. O sombreador executa uma ramificação dinâmica para que a grande maioria dos pixels só Leia da cascata atual.

**Figura 9. Fendas em cascata**

![fendas em cascata](images/cascade-seams.jpg)

Mantida Uma fenda visível pode ser vista onde as cascatas se sobrepõem. Adequada Quando as cascatas são mescladas entre, nenhuma fenda ocorre.

## <a name="filtering-shadow-maps"></a>Filtrando mapas de sombra

### <a name="pcf"></a>PCF

A filtragem de mapas de sombra comuns não produz sombras suaves e borradas. O hardware de filtragem desfoca os valores de profundidade e, em seguida, compara esses valores borrados com o Texel de espaço claro. A borda rígida resultante do teste de aprovação/reprovação ainda existe. O desfoque de mapas de sombra só serve para mover erroneamente a borda rígida. PCF habilita a filtragem em mapas de sombra. A ideia geral do PCF é calcular uma porcentagem do pixel em sombra com base no número de subamostras que passam o teste de profundidade sobre o número total de subamostras.

O hardware do Direct3D 10 e do Direct3D 11 pode executar o PCF. A entrada para uma amostra de PCF consiste na coordenada de textura e em um valor de profundidade de comparação. Para simplificar, o PCF é explicado com um filtro com quatro toques. O amostra de textura lê a textura quatro vezes, semelhante a um filtro padrão. No entanto, o resultado retornado é uma porcentagem dos pixels que passaram no teste de profundidade. A Figura 10 mostra como um pixel que passa um dos quatro testes de profundidade é 25% em sombra. O valor real retornado é uma interpolação linear baseada nas coordenadas de subtexel das leituras de textura para produzir um gradiente suave. Sem essa interpolação linear, o PCF de quatro toques só poderá retornar cinco valores: {0,0, 0,25, 0,5, 0,75, 1,0}.

**Figura 10. Imagem filtrada de PCF, com 25% do pixel selecionado coberto**

![imagem filtrada de PCF, com 25% do pixel selecionado coberto](images/pcf-filtered-image.png)

Também é possível fazer o PCF sem suporte a hardware ou estender o PCF para kernels maiores. Algumas técnicas até amostram com um kernel ponderado. Para fazer isso, crie um kernel (como um gaussiano) para uma grade N × N. Os pesos devem somar até 1. Em seguida, a textura é seguida por amostras de N2. Cada amostra é dimensionada pelos pesos correspondentes no kernel. O exemplo CascadedShadowMaps11 usa essa abordagem.

### <a name="depth-bias"></a>Tendência de profundidade

A tendência de profundidade se torna ainda mais importante quando kernels PCF grandes são usados. Ele só é válido para comparar a profundidade de espaço leve de um pixel em relação ao pixel que mapeia para o mapa de profundidade. Os vizinhos do mapa de profundidade do Texel se referem a uma posição diferente. Essa profundidade provavelmente será semelhante, mas pode ser muito diferente dependendo da cena. A Figura 11 realça os artefatos que ocorrem. Uma única profundidade é comparada a três texels vizinhas no mapa de sombra. Um dos testes de profundidade falha erroneamente porque sua profundidade não se correlaciona com a profundidade de espaço claro computada da geometria atual. A solução recomendada para esse problema é usar um deslocamento maior. No entanto, muito grande parte de um deslocamento pode resultar em Peter panorâmica. Calcular um grande plano próximo e plano distante ajuda a reduzir os efeitos do uso de um deslocamento.

**Figura 11. Auto-sombreamento errôneo**

![auto-sombreamento errôneo](images/erroneous-self-shadowing.png)

Os resultados de sombreamento automático errôneos da comparação de pixels na profundidade de espaço leve para o texels no mapa de sombra que não se correlacionam. A profundidade em espaço leve se correlaciona com a sombra Texel 2 no mapa de profundidade. Texel 1 é maior que a intensidade de espaço leve, enquanto 2 é igual e 3 é menor. Texels 2 e 3 passam o teste de profundidade, enquanto o Texel 1 falha.

### <a name="calculating-a-per-texel-depth-bias-with-ddx-and-ddy-for-large-pcfs"></a>Calculando uma tendência de profundidade de Per-Texel com campo DDX e DDY para grandes PCFs

Calcular uma tendência de profundidade por Texel com **campo DDX** e **ddy** para grandes PCFs é uma técnica que calcula a tendência de profundidade correta — pressupondo que a superfície seja planar — para o mapa de sombra adjacente Texel.

Essa técnica se adapta à profundidade de comparação a um plano usando as informações derivadas. Como essa técnica é computacionalmente complexa, ela deve ser usada somente quando uma GPU tiver ciclos de computação para spare. Quando kernels muito grandes são usados, essa pode ser a única técnica que funciona para remover artefatos de sombreamento automático sem causar o Peter panorâmica.

A Figura 12 realça o problema. A profundidade no espaço leve é conhecida por um Texel que está sendo comparado. As profundidades de espaço leve que correspondem ao texels vizinho no mapa de profundidade são desconhecidas.

**Figura 12. Mapa de cena e profundidade**

![mapa de cena e profundidade](images/scene-and-depth-map.png)

A cena renderizada é mostrada à esquerda e o mapa de profundidade com um bloco Texel de exemplo é mostrado à direita. O Texel de espaço de olho é mapeado para o pixel rotulado como D no centro do bloco. Essa comparação é precisa. A profundidade correta no espaço de olho que se correlaciona com os pixels que o vizinho D é desconhecido. O mapeamento do texels vizinho de volta para o espaço de olho só será possível se considerarmos que o pixel pertence ao mesmo triângulo que D.

A profundidade é conhecida pelo Texel que se correlaciona com a posição de espaço leve. A profundidade é desconhecida para o texels vizinho no mapa de profundidade.

Em um alto nível, essa técnica usa as operações HLSL **campo DDX** e **ddy** para encontrar a derivação da posição de espaço leve. Isso não é trivial porque as operações derivadas retornam o gradiente da profundidade de espaço leve em relação ao espaço da tela. Para converter isso em um gradiente da profundidade de espaço leve em relação ao espaço leve, uma matriz de conversão deve ser calculada.

### <a name="explanation-with-shader-code"></a>Explicação com código de sombreador

Os detalhes do restante do algoritmo são fornecidos como uma explicação do código do sombreador que executa essa operação. Esse código pode ser encontrado no exemplo CascadedShadowMaps11. A Figura 13 mostra como as coordenadas de textura de espaço leve são mapeadas para o mapa de profundidade e como as derivações em X e Y podem ser usadas para criar uma matriz de transformação.

**Figura 13. Espaço de tela para matriz de espaço leve**

![espaço de tela para matriz de espaço leve](images/screen-space-to-light-space-matrix.png)

Os derivativos da posição de espaço leve em X e Y são usados para criar essa matriz.

A primeira etapa é calcular o derivativo da posição de exibição clara.


```C++
          float3 vShadowTexDDX = ddx (vShadowMapTextureCoordViewSpace);
          float3 vShadowTexDDY = ddy (vShadowMapTextureCoordViewSpace);
```



As GPUs de classe do Direct3D 11 calculam esses derivativos executando 2 × 2 quatro pixels em paralelo e subtraindo as coordenadas de textura do vizinho em X para **campo DDX** e do vizinho em Y para **ddy**. Esses dois derivativos compõem as linhas de uma matriz 2 × 2. Em sua forma atual, essa matriz poderia ser usada para converter pixels vizinhos de espaço na tela em interrupções de espaço leve. No entanto, o inverso dessa matriz é necessário. Uma matriz que transforma os pixels vizinhos de espaço leve em inclinação de espaço na tela é necessária.


```C++
          float2x2 matScreentoShadow = float2x2( vShadowTexDDX.xy, vShadowTexDDY.xy );
          float fInvDeterminant = 1.0f / fDeterminant;

          float2x2 matShadowToScreen = float2x2 (
          matScreentoShadow._22 * fInvDeterminant,
          matScreentoShadow._12 * -fInvDeterminant,
          matScreentoShadow._21 * -fInvDeterminant,
          matScreentoShadow._11 * fInvDeterminant );
```



**Figura 14. Espaço leve para a tela-espaço**

![espaço leve para a tela-espaço](images/light-space-to-screen-space.png)

Essa matriz é usada para transformar as duas texels acima e à direita da Texel atual. Esses vizinhos são representados como um deslocamento do Texel atual.


```C++
          float2 vRightShadowTexelLocation = float2( m_fTexelSize, 0.0f );
          float2 vUpShadowTexelLocation = float2( 0.0f, m_fTexelSize );
          float2 vRightTexelDepthRatio = mul( vRightShadowTexelLocation,
          matShadowToScreen );
          float2 vUpTexelDepthRatio = mul( vUpShadowTexelLocation,
          matShadowToScreen );
```



A proporção que a matriz cria é, por fim, multiplicada pelas derivações de profundidade para calcular os deslocamentos de profundidade para os pixels vizinhos.


```C++
            float fUpTexelDepthDelta =
            vUpTexelDepthRatio.x * vShadowTexDDX.z
            + vUpTexelDepthRatio.y * vShadowTexDDY.z;
            float fRightTexelDepthDelta =
            vRightTexelDepthRatio.x * vShadowTexDDX.z
            + vRightTexelDepthRatio.y * vShadowTexDDY.z;
```



Esses pesos agora podem ser usados em um loop PCF para adicionar um deslocamento à posição.


```C++
    for( int x = m_iPCFBlurForLoopStart; x < m_iPCFBlurForLoopEnd; ++x ) 
    {
        for( int y = m_iPCFBlurForLoopStart; y < m_iPCFBlurForLoopEnd; ++y )
            {
            if ( USE_DERIVATIVES_FOR_DEPTH_OFFSET_FLAG )
            {
            depthcompare += fRightTexelDepthDelta * ( (float) x ) +
            fUpTexelDepthDelta * ( (float) y );
            }
            // Compare the transformed pixel depth to the depth read
            // from the map.
            fPercentLit += g_txShadow.SampleCmpLevelZero( g_samShadow,
            float2(
            vShadowTexCoord.x + ( ( (float) x ) * m_fNativeTexelSizeInX ) ,
            vShadowTexCoord.y + ( ( (float) y ) * m_fTexelSize )
            ),
            depthcompare
            );
            }
     }
```



## <a name="pcf-and-csms"></a>PCF e CSMs

O PCF não funciona em matrizes de textura no Direct3D 10. Para usar o PCF, todas as cascata são armazenadas em um Atlas de textura grande.

### <a name="derivative-based-offset"></a>Deslocamento de Derivative-Based

A adição dos deslocamentos baseados em derivações para CSMs apresenta alguns desafios. Isso ocorre devido a um cálculo derivado dentro do controle de fluxo divergente. O problema ocorre devido a uma maneira fundamental de operar as GPUs. As GPUs Direct3D11 operam em 2 × 2 quatro processadores de pixels. Para executar um derivativo, as GPUs geralmente subtraim a cópia do pixel atual de uma variável da cópia do pixel vizinho da mesma variável. Como isso acontece varia de GPU para GPU. As coordenadas de textura são determinadas por seleção baseada em mapa ou em cascata baseada em intervalo. Alguns pixels em um pixel Quad escolhem uma cascata diferente do restante dos pixels. Isso resulta em emendas visíveis entre mapas de sombra porque os deslocamentos com base em derivação agora estão completamente errados. A solução é executar o derivativo em coordenadas de textura de espaço de exibição clara. Essas coordenadas são as mesmas para cada cascata.

### <a name="padding-for-pcf-kernels"></a>Preenchimento de kernels PCF

Índice de kernels PCF fora de uma partição em cascata se o buffer de sombra não for preenchido. A solução é preencher a borda externa da cascata por uma metade do tamanho do kernel PCF. Isso deve ser implementado no sombreador que seleciona a cascata e na matriz de projeção que deve renderizar a cascata grande o suficiente para que a borda seja preservada.

## <a name="variance-shadow-maps"></a>Mapas de sombra de variação

VSMs (consulte [variação de mapas de sombra](https://portal.acm.org/citation.cfm?doid=1111411.1111440) por Donnelly e Lauritzen para obter mais informações) habilitar Filtragem de mapa de sombra direta. Ao usar o VSMs, toda a potência do hardware de filtragem de textura pode ser usada. Triline e anisotropic (Figura 15) a filtragem pode ser usada. Além disso, VSMs pode ser borrado diretamente por meio de convolução. VSMs têm algumas desvantagens; dois canais de dados de profundidade devem ser armazenados (profundidade e profundidade ao quadrado). Quando as sombras se sobrepõem, o sangramento claro é comum. No entanto, eles funcionam bem com resoluções mais baixas e podem ser combinados com CSMs.

**Figura 15. Filtragem de anisotropic**

![filtragem de anisotropic](images/anisotropic-filtering.png)

### <a name="algorithm-details"></a>Detalhes do algoritmo

O VSMs funciona renderizando a profundidade e a profundidade quadrada em um mapa de sombra de dois canais. Esse mapa de sombra de dois canais pode ser desfocado e filtrado da mesma forma que uma textura normal. Em seguida, o algoritmo usa a desigualdade do Chebychev no sombreador de pixel para estimar a fração da área de pixel que passaria no teste de profundidade.

O sombreador de pixel busca os valores de profundidade e de profundidade quadrada.


```C++
        float  fAvgZ  = mapDepth.x; // Filtered z
        float  fAvgZ2 = mapDepth.y; // Filtered z-squared
```



A comparação de profundidade é executada.


```C++
        if ( fDepth <= fAvgZ )
        {
        fPercentLit = 1;
        }
```



Se a comparação de profundidade falhar, a porcentagem do pixel que está acesa será estimada. A variação é calculada como média de quadrados menos o quadrado-de-média.


```C++
        float variance = ( fAvgZ2 ) − ( fAvgZ * fAvgZ );
        variance = min( 1.0f, max( 0.0f, variance + 0.00001f ) );
```



O valor fPercentLit é estimado com a desigualdade de Chebychev.


```C++
        float mean           = fAvgZ;
        float d              = fDepth - mean;
        float fPercentLit    = variance / ( variance + d*d );
```



## <a name="light-bleeding"></a>Sangramento claro

A maior desvantagem do VSMs é o sangramento claro (Figura 16). A perda de luz ocorre quando vários contornos de sombra se occludem entre bordas. VSMs sombrear as bordas de sombras com base em diparidades de profundidade. Quando as sombras se sobrepõem, há uma diparidade de profundidade no centro de uma região que deve ser sombreada. Isso é um problema com o uso do algoritmo VSM.

**Figura 16. Sangramento de VSM**

![sangramento de VSM](images/vsm-light-bleeding.png)

Uma solução parcial para o problema é elevar o fPercentLit a uma potência. Isso tem o efeito de retardar o desfoque, o que pode causar artefatos em que a diparidade de profundidade é pequena. Às vezes, existe um valor mágico que alivia o problema.


```C++
fPercentLit = pow( p_max, MAGIC_NUMBER );
```



Uma alternativa para elevar o percentual de aceso a uma potência é evitar configurações em que as sombras se sobrepõem. Até mesmo as configurações de sombra altamente ajustadas têm várias restrições em luz, câmera e geometria. O sangramento claro também é reduzido com o uso de texturas de resolução mais alta.

Os mapas de sombra de variação em camadas (LVSMs) resolvem o problema às custas de dividir o frustum em camadas perpendiculares à luz. O número de mapas necessários seria muito grande quando CSMs também estão sendo usados.

Além disso, Andrew Lauritzen, coautor do artigo sobre VSMs e autor de um papel em LVSMs, abordou a combinação de mapas de sombra exponencial (ESMs) com VSMs para neutralizar a mistura de luz em um [Fórum de Beyond3D](https://forum.beyond3d.com/showthread.php?t=47427).

## <a name="vsms-with-csms"></a>VSMs com CSMs

O exemplo VarianceShadow11 combina VSMs e CSMs. A combinação é razoavelmente simples. O exemplo segue as mesmas etapas do exemplo CascadedShadowMaps11. Como o PCF não é usado, as sombras são desfocadas em uma convolução separáveis de duas passagens. Não usar o PCF também permite que o exemplo use matrizes de textura em vez de um Atlas de textura. O PCF em matrizes de textura é um recurso do Direct3D 10,1.

### <a name="gradients-with-csms"></a>Gradientes com CSMs

O uso de gradientes com CSMs pode produzir uma fenda ao longo da borda entre duas cascatas, como mostrado na figura 17. A instrução de exemplo usa derivações entre pixels para calcular informações, como o nível de mipmap, necessário para o filtro. Isso causa um problema em particular para a seleção de mipmap ou a filtragem de anisotropic. Quando os pixels em um quad usam ramificações diferentes no sombreador, os derivativos calculados pelo hardware da GPU são inválidos. Isso resulta em uma fenda denteada ao longo do mapa de sombra.

**Figura 17. Fendas em bordas em cascata devido à filtragem de anisotropic com controle de fluxo divergente**

![fendas em bordas em cascata devido à filtragem de anisotropic com controle de fluxo divergente](images/seams-on-cascade-borders-due-to-anisotropic.jpg)

Esse problema é resolvido com a computação dos derivativos na posição no espaço de exibição clara; a coordenada de espaço de exibição clara não é específica para a cascata selecionada. As derivações computadas podem ser dimensionadas pela parte de escala da matriz de textura de projeção para o nível de mipmap correto.


```C++
        float3 vShadowTexCoordDDX = ddx( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDX *= m_vCascadeScale[iCascade].xyz;
        float3 vShadowTexCoordDDY = ddy( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDY *= m_vCascadeScale[iCascade].xyz;

        mapDepth += g_txShadow.SampleGrad( g_samShadow, vShadowTexCoord.xyz,
        vShadowTexCoordDDX, vShadowTexCoordDDY );
```



## <a name="vsms-compared-to-standard-shadows-with-pcf"></a>VSMs em comparação com as sombras padrão com PCF

VSMs e PCF tentam aproximar a fração da área de pixel que passaria no teste de profundidade. O VSMs trabalha com filtragem de hardware e pode ser desfocado com kernels do separáveis. Os kernels de convolução separáveis são consideravelmente mais baratos de implementar do que um kernel completo. Além disso, VSMs comparar uma profundidade de espaço leve em relação a um valor no mapa de profundidade de espaço claro. Isso significa que o VSMs não tem os mesmos problemas de deslocamento que o PCF. Tecnicamente, VSMs são profundidade de amostragem em uma área maior, bem como a execução de uma análise estatística. Isso é menos preciso do que PCF. Na prática, o VSMs faz um trabalho muito bom de mesclagem, o que resulta em menos deslocamento necessário. Conforme descrito acima, a desvantagem do número um para VSMs é o sangramento claro.

VSMs e PCF representam uma compensação entre a potência de computação da GPU e a largura de banda da textura da GPU. VSMs exigem que mais matemática seja executada para calcular a variância. PCF requer mais largura de banda de memória de textura. Os kernels PCF grandes podem rapidamente se tornar afunilados pela largura de banda da textura. Com o aumento de energia da GPU aumentando mais rapidamente do que a largura de banda da GPU, os VSMs estão se tornando mais práticos dos dois algoritmos. O VSMs também parece melhor com mapas de sombra de resolução mais baixa devido à mesclagem e filtragem.

## <a name="summary"></a>Resumo

O CSMs oferece uma solução para o problema de alias de perspectiva. Há várias configurações possíveis para obter a fidelidade visual necessária para um título. O PCF e o VSMs são amplamente usados e devem ser combinados com CSMs para reduzir o alias.

## <a name="references"></a>Referências

Donnelly, W. e Lauritzen, os [mapas de sombra. variância](https://portal.acm.org/citation.cfm?doid=1111411.1111440). No SI3D ' 06: procedimentos do Symposium 2006 em jogos e gráficos 3D interativos. 2006. PP. 161 – 165. Nova York, NY, EUA: ACM Press.

Lauritzen, Andrew e McCool, Michael. [Mapas de sombra de variância em camadas](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992). Procedimentos de interface gráfica 2008, 28 de maio, 2008, Windsor, Ontário, Canadá.

Engel, Woflgang F. section 4. Mapas de sombra em cascata. ShaderX5, técnicas de renderização avançadas, Wolfgang F. Engel, Ed. Charles River Media, Boston, Massachusetts. 2006. PP. 197 – 206.

 

 