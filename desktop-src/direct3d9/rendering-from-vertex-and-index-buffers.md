---
description: Os métodos de desenho indexados e não indexados são suportados pelo Direct3D.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Renderização de vértice e buffers de índice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4290dc2ff40e1ec0448e3948342aa3b02ac62bf9866a44958ea53bee9658d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092582"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a>Renderização de vértice e buffers de índice (Direct3D 9)

Os métodos de desenho indexados e não indexados são suportados pelo Direct3D. Os métodos indexados usam um único conjunto de índices para todos os componentes de vértice. Os dados de vértice são armazenados em buffers de vértice e os dados de índice são armazenados em buffers de índice. Veja abaixo alguns cenários comuns para desenhar primitivos usando buffers de vértice e índice.

Esses exemplos comparam o uso [**de IDirect3DDevice9::D rawPrimitive**](/windows/desktop/api) [**e IDirect3DDevice9::D rawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a>Cenário 1: desenhando dois triângulos sem indexação

Digamos que você queira desenhar o quádruplo mostrado na ilustração a seguir.

![ilustração de um quadrado que consiste em dois triângulos](images/dip-fig1.png)

Se você usar o tipo primitivo Lista de Triângulos para renderizar os dois triângulos, cada triângulo será armazenado como três vértices individuais, resultando em um buffer de vértice semelhante à ilustração a seguir.

![diagrama de um buffer de vértice que define três vértices para dois triângulos](images/dip-fig2.png)

A chamada de desenho é muito simples; começando no local 0 dentro do buffer de vértice, desenhe dois triângulos. Se o descarte estiver habilitado, a ordem dos vértices será importante. Este exemplo assume o estado de respeção padrão no sentido horário, portanto, triângulos visíveis devem ser desenhados em ordem horário. O tipo primitivo Lista de Triângulos simplesmente lê três vértices na ordem linear do buffer para cada triângulo, portanto, essa chamada desenhará triângulos (0, 1, 2) e (3, 4, 5):


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a>Cenário 2: Desenhando dois triângulos com indexação

Como você observará, o buffer de vértice contém dados duplicados nos locais 0 e 4, 2 e 5. Isso faz sentido porque os dois triângulos compartilham dois vértices comuns. Esses dados duplicados são desperdícios e o buffer de vértice pode ser compactado usando um buffer de índice. Um buffer de vértice menor reduz a quantidade de dados de vértice que devem ser enviados para o adaptador gráfico. Ainda mais importante, o uso de um buffer de índice permite que o adaptador armazene vértices em um cache de vértice; se o primitivo que está sendo desenhado contiver um vértice usado recentemente, esse vértice poderá ser buscado do cache em vez de lê-lo do buffer de vértice, o que resulta em um grande aumento de desempenho.

Um buffer de índice 'indexes' no buffer de vértice, portanto, cada vértice exclusivo precisa ser armazenado apenas uma vez no buffer de vértice. O diagrama a seguir mostra uma abordagem indexada para o cenário de desenho anterior.

![diagrama de um buffer de índice para o buffer de vértice anterior](images/dip-fig3.png)

O buffer de índice armazena valores de Índice VB, que referenciam um vértice específico dentro do buffer de vértice. Um buffer de vértice pode ser pensado como uma matriz de vértices, portanto, o Índice VB é simplesmente o índice no buffer de vértice para o vértice de destino. Da mesma forma, um Índice IB é um índice no buffer de índice. Isso poderá ficar muito confuso muito rapidamente se você não tiver cuidado, portanto, certifique-se de que você esteja claro sobre o vocabulário que está sendo usado: índice de valores de índice de VB no buffer de vértice, índice de valores de índice IB no buffer de índice e o buffer de índice em si armazena valores de Índice VB.

A chamada de desenho é mostrada abaixo. Os significados de todos os argumentos são discutidos por fim para o próximo cenário de desenho; por enquanto, basta observar que essa chamada está instruindo o Direct3D a renderizar uma lista de triângulos contendo dois triângulos, começando no local 0 dentro do buffer de índice. Essa chamada desenhará os mesmos dois triângulos exatamente na mesma ordem de antes, garantindo uma orientação adequada no sentido horário:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a>Cenário 3: Desenhando um triângulo com indexação

Pretenda agora que você deseja desenhar apenas o segundo triângulo, mas deseja usar o mesmo buffer de vértice e buffer de índice que são usados ao desenhar todo o quad, conforme mostrado no diagrama a seguir.

![diagrama do buffer de índice e do buffer de vértice para o segundo triângulo](images/dip-fig4.png)

Para essa chamada de desenho, o primeiro índice IB usado é 3; esse valor é chamado de StartIndex. O índice de VB mais baixo usado é 0; esse valor é chamado de MinIndex. Embora apenas três vértices sejam necessários para desenhar o triângulo, esses três vértices são distribuídos em quatro locais adjacentes no buffer de vértice; O número de locais dentro do bloco contíguo de memória do buffer de vértice necessário para a chamada de desenho é chamado NumVertices e será definido como 4 nesta chamada. Os valores MinIndex e NumVertices são apenas dicas para ajudar o Direct3D a otimizar o acesso à memória durante o processamento do vértice de software e podem ser simplesmente definidos para incluir todo o buffer de vértice pelo preço do desempenho.

Aqui está a chamada de desenho para o único caso de triângulo; o significado do argumento BaseVertexIndex será explicado em seguida:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a>Cenário 4: Desenhando um triângulo com indexação de deslocamento

BaseVertexIndex é um valor que é efetivamente adicionado a cada Índice VB armazenado no buffer de índice. Por exemplo, se tivessemos passado um valor de 50 para BaseVertexIndex durante a chamada anterior, isso funcionalmente seria o mesmo que usar o buffer de índice no diagrama a seguir durante a chamada DrawIndexedPrimitive:

![diagrama de um buffer de índice com um valor de 50 para basevertexindex](images/dip-fig5.png)

Esse valor raramente é definido como algo diferente de 0, mas pode ser útil se você quiser desa dissociar o buffer de índice do buffer de vértice: se ao preencher o buffer de índice para uma malha específica, o local da malha dentro do buffer de vértice ainda não for conhecido, você poderá simplesmente simular que os vértices de malha estarão localizados no início do buffer de vértice; Quando chegar a hora de fazer a chamada de desenho, basta passar o local inicial real como BaseVertexIndex.

Essa técnica também pode ser usada ao desenhar várias instâncias de uma malha usando um único buffer de índice; por exemplo, se o buffer de vértice contiver duas malhas com ordem de desenho idêntica, mas vértices ligeiramente diferentes (talvez cores difusas ou coordenadas de textura diferentes), ambas as malhas poderão ser desenhadas usando valores diferentes para BaseVertexIndex. Levando esse conceito um passo além, você pode usar um buffer de índice para desenhar várias instâncias de uma malha, cada uma contida em um buffer de vértice diferente, simplesmente por meio do ciclo de qual buffer de vértice está ativo e ajustando o BaseVertexIndex conforme necessário. Observe que o valor BaseVertexIndex também é adicionado automaticamente ao argumento MinIndex, o que faz sentido quando você vê como ele é usado:

Pretenda agora que queremos desenhar novamente apenas o segundo triângulo do quad usando o mesmo buffer de índice que antes; no entanto, um buffer de vértice diferente está sendo usado no qual o quad está localizado no Índice VB 50. A ordem relativa dos vértices quad permanece inalterada, somente o local inicial dentro do buffer de vértice é diferente. O buffer de índice e o buffer de vértice seriam parecidos com o diagrama a seguir.

![diagrama do buffer de índice e do buffer de vtex com um índice vb de 50](images/dip-fig6.png)

Aqui está a chamada de desenho apropriada; observe que BaseVertexIndex é o único valor que foi alterado do cenário anterior:


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

[Renderização de primitivos](rendering-primitives.md)
</dt> </dl>

 

 
