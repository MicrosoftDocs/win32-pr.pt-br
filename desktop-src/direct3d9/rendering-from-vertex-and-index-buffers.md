---
description: Os métodos de desenho indexados e não indexados têm suporte do Direct3D.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Renderização de vértices e buffers de índice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc42da3f25787d42b0bdccdd808013f51bfa3e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825602"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a>Renderização de vértices e buffers de índice (Direct3D 9)

Os métodos de desenho indexados e não indexados têm suporte do Direct3D. Os métodos indexados usam um único conjunto de índices para todos os componentes de vértice. Os dados de vértice são armazenados em buffers de vértice, e os dados de índice são armazenados em buffers de índice. Abaixo estão listados alguns cenários comuns para desenhar primitivos usando os buffers de vértice e de índice.

Esses exemplos comparam o uso de [**IDirect3DDevice9::D rawprimitive**](/windows/desktop/api) e [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a>Cenário 1: desenhar dois triângulos sem indexação

Digamos que você deseja desenhar o quad que é mostrado na ilustração a seguir.

![ilustração de um quadrado que consiste em dois triângulos](images/dip-fig1.png)

Se você usar o tipo primitivo da lista de triângulos para renderizar os dois triângulos, cada triângulo será armazenado como três vértices individuais, resultando em um buffer de vértice semelhante à ilustração a seguir.

![diagrama de um buffer de vértice que define três vértices para dois triângulos](images/dip-fig2.png)

A chamada de desenho é muito simples; começando no local 0 dentro do buffer de vértice, desenhe dois triângulos. Se a remoção estiver habilitada, a ordem dos vértices será importante. Este exemplo assume o estado de remoção no sentido anti-horário padrão, portanto, triângulos visíveis devem ser desenhados na ordem horária. O tipo primitivo da lista de triângulos simplesmente lê três vértices em ordem linear do buffer para cada triângulo, portanto, essa chamada vai desenhar triângulos (0, 1, 2) e (3, 4, 5):


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a>Cenário 2: desenhar dois triângulos com indexação

Como você observará, o buffer de vértice contém dados duplicados nos locais 0 e 4, 2 e 5. Isso faz sentido porque os dois triângulos compartilham dois vértices comuns. Esses dados duplicados são desperdícios e o buffer de vértice pode ser compactado usando um buffer de índice. Um buffer de vértice menor reduz a quantidade de dados de vértice que deve ser enviada ao adaptador gráfico. Ainda mais importante, usar um buffer de índice permite que o adaptador armazene vértices em um cache de vértice; Se o primitivo que está sendo desenhado contiver um vértice usado recentemente, esse vértice poderá ser buscado do cache em vez de lê-lo a partir do buffer de vértice, o que resultará em um grande aumento de desempenho.

Um buffer de índice ' Indexes ' no buffer de vértice para que cada vértice exclusivo precise ser armazenado apenas uma vez no buffer de vértice. O diagrama a seguir mostra uma abordagem indexada para o cenário de desenho anterior.

![diagrama de um buffer de índice para o buffer de vértice anterior](images/dip-fig3.png)

O buffer de índice armazena os valores de índice do VB, que fazem referência a um vértice específico dentro do buffer de vértice. Um buffer de vértice pode ser considerado como uma matriz de vértices, portanto, o índice do VB é simplesmente o índice no buffer de vértice para o vértice de destino. Da mesma forma, um índice de IB é um índice no buffer de índice. Isso pode ficar muito confuso muito rapidamente se você não tiver cuidado. portanto, verifique se está claro no vocabulário que está sendo usado: os valores de índice do VB são indexados no buffer de vértice, os valores de índice de IB são indexados no buffer de índice, e o próprio buffer de índice armazena os valores de índice do VB.

A chamada de desenho é mostrada abaixo. Os significados de todos os argumentos são discutidos em comprimento para o próximo cenário de desenho; por enquanto, apenas Observe que essa chamada está novamente instruindo o Direct3D a renderizar uma lista de triângulos que contém dois triangulares, começando no local 0 no buffer de índice. Essa chamada irá desenhar os mesmos dois triângulos na mesma ordem que antes, garantindo uma orientação horária adequada:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a>Cenário 3: desenhando um triângulo com indexação

Suponhamos agora que você deseja desenhar apenas o segundo triângulo, mas deseja usar o mesmo buffer de vértice e de índice que são usados ao desenhar todo o quad, conforme mostrado no diagrama a seguir.

![diagrama do buffer de índice e buffer de vértice do segundo triângulo](images/dip-fig4.png)

Para essa chamada de desenho, o primeiro índice IB usado é 3; Esse valor é chamado de StartIndex. O menor índice do VB usado é 0; Esse valor é chamado de MinIndex. Embora apenas três vértices sejam requeridos para desenhar o triângulo, esses três vértices são distribuídos em quatro locais adjacentes no buffer de vértice; o número de locais dentro do bloco contíguo de memória de buffer de vértice necessário para a chamada de desenho é chamado de NumVertices e será definido como 4 nesta chamada. Os valores MinIndex e NumVertices são, na verdade, apenas dicas para ajudar o Direct3D a otimizar o acesso à memória durante o processamento de vértices de software e pode simplesmente ser definido para incluir todo o buffer de vértice no preço do desempenho.

Aqui está a chamada de desenho para o caso de triângulo único; o significado do argumento BaseVertexIndex será explicado a seguir:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a>Cenário 4: desenhando um triângulo com indexação de deslocamento

BaseVertexIndex é um valor que é efetivamente adicionado a cada índice do VB armazenado no buffer de índice. Por exemplo, se tivéssemos passado um valor de 50 para BaseVertexIndex durante a chamada anterior, isso funcionaria como seria o mesmo que usar o buffer de índice no diagrama a seguir para a duração da chamada DrawIndexedPrimitive:

![diagrama de um buffer de índice com um valor de 50 para BaseVertexIndex](images/dip-fig5.png)

Esse valor raramente é definido como algo diferente de 0, mas pode ser útil se você quiser desacoplar o buffer de índice do buffer de vértice: se ao preencher o buffer de índice para uma malha específica, o local da malha dentro do buffer de vértice ainda não é conhecido. você pode simplesmente fingir que os vértices de malha estarão localizados no início do buffer de vértice; Quando chegar a hora de fazer a chamada de desenho, basta passar o local inicial real como o BaseVertexIndex.

Essa técnica também pode ser usada ao desenhar várias instâncias de uma malha usando um único buffer de índice; por exemplo, se o buffer de vértice contiver duas malhas com ordem de desenho idêntica, mas vértices ligeiramente diferentes (talvez diferentes cores difusas ou coordenadas de textura), ambas as malhas poderiam ser desenhadas usando valores diferentes para BaseVertexIndex. Dando um passo a esse conceito, você pode usar um buffer de índice para desenhar várias instâncias de uma malha, cada uma contida em um buffer de vértice diferente, simplesmente ligando qual buffer de vértice está ativo e ajustando o BaseVertexIndex conforme necessário. Observe que o valor BaseVertexIndex também é adicionado automaticamente ao argumento MinIndex, o que faz sentido quando você vê como ele é usado:

Vamos fingir que, novamente, desejamos desenhar apenas o segundo triângulo do Quad usando o mesmo buffer de índice que antes; no entanto, um buffer de vértice diferente está sendo usado no qual o quad está localizado no índice do VB 50. A ordem relativa dos vértices quádruplos permanece inalterada, apenas o local inicial dentro do buffer de vértice é diferente. O buffer de índice e o buffer de vértice se pareceriam com o diagrama a seguir.

![diagrama do buffer de índice e buffer de vértice com um índice vb de 50](images/dip-fig6.png)

Aqui está a chamada de desenho apropriada; Observe que BaseVertexIndex é o único valor que foi alterado do cenário anterior:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    50,                 // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Primitivos de renderização](rendering-primitives.md)
</dt> </dl>

 

 
