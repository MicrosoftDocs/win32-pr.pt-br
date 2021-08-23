---
title: Tendência de profundidade
description: Polígonos que são coplanar no espaço 3D podem ser feitos para aparecer como se não fossem coplanar adicionando um Bias z (ou uma tendência de profundidade) a cada um.
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f707a038a2da8ebe9c1adc21f6081c85f5a63fbbc1c360a4dfbbf5765d845d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990156"
---
# <a name="depth-bias"></a>Tendência de profundidade

Polígonos que são coplanar no espaço 3D podem ser feitos para aparecer como se não fossem coplanar adicionando um Bias z (ou uma tendência de profundidade) a cada um.

Essa é uma técnica comumente usada para garantir que as sombras em uma cena sejam exibidas corretamente. Por exemplo, uma sombra em uma parede provavelmente terá o mesmo valor de profundidade que a parede. Se um aplicativo renderizar uma parede primeiro e, em seguida, uma sombra, a sombra pode não estar visível ou os artefatos de profundidade podem estar visíveis.


Um aplicativo pode ajudar a garantir que polígonos coplanar sejam renderizados corretamente adicionando a tendência (do membro **DepthBias** do [**D3D11 \_ rasterizador \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) aos valores z que o sistema usa ao renderizar os conjuntos de polígonos de coplanar. Polígonos com um valor z maior serão desenhados na frente de polígonos com um valor z menor.

Há duas opções para calcular a tendência de profundidade.

1.  Se o buffer de profundidade atualmente associado ao estágio output-merger tiver um formato **UNORM** ou nenhum buffer de profundidade estiver associado, o valor de tendência será calculado da seguinte maneira:
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    em que *r* é o valor mínimo representável > 0 no formato de buffer de profundidade convertido em **float32**. Os valores **DepthBias** e **SlopeScaledDepthBias** são membros da estrutura [**\_ \_ DESC1 do rasterizador D3D11**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) . O valor de **MaxDepthSlope** é o máximo dos declives horizontal e vertical do valor de profundidade no pixel.
2.  Se um buffer de profundidade de ponto flutuante estiver associado ao estágio de mesclagem de saída, o valor de tendência será calculado da seguinte maneira:
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    em que *r* é o número de bits mantissa na representação de ponto flutuante (excluindo o bit oculto); por exemplo, 23 para **float32**.

O valor de tendência é então clamped assim:


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



Em seguida, o valor de tendência é usado para calcular a profundidade de pixels.


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



As operações de tendência de profundidade ocorrem em vértices após o recorte, portanto, a diferença de profundidade não tem efeito no recorte geométrico. O valor de tendência é constante para um determinado primitivo e é adicionado ao valor z para cada vértice antes da configuração do interpolador. Quando você usa [os níveis de recurso](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 e superior, todos os cálculos de tendência são executados usando aritmética de ponto flutuante de 32 bits. A tendência não é aplicada a primitivas de ponto ou de linha, exceto para linhas desenhadas no modo de wireframe.

Um dos artefatos com sombras com base no buffer de sombra é o acne de sombra ou um sombreamento de superfície em si devido a pequenas diferenças entre a computação de profundidade em um sombreador e a profundidade da mesma superfície no buffer de sombra. Uma maneira de aliviar isso é usar **DepthBias** e **SlopeScaledDepthBias** ao renderizar um buffer de sombra. A ideia é distribuir as superfícies o suficiente ao renderizar um buffer de sombra para que o resultado da comparação (entre o buffer de sombra z e o sombreador z) seja consistente em toda a superfície e evite a autosombra local.

No entanto, usar **DepthBias** e **SlopeScaledDepthBias** pode introduzir novos problemas de renderização quando um polígono exibido em um ângulo extremamente nítido faz com que a equação de tendência gere um valor z muito grande. Isso, em vigor, envia o polígono extremamente longe da superfície original no mapa de sombra. Uma maneira de ajudar a aliviar esse problema específico é usar o **DepthBiasClamp**, que fornece um limite superior (positivo ou negativo) na magnitude da diferença de z calculada.

> [!Note]  
> Para [os níveis de recurso](overviews-direct3d-11-devices-downlevel-intro.md) 9,1, 9,2, 9,3, **DepthBiasClamp** não tem suporte.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estágio de fusão de saída](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




