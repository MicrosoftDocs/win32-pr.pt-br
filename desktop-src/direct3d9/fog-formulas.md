---
description: Os aplicativos C++ podem controlar como a neblina afeta a cor dos objetos em uma cena alterando como o Microsoft Direct3D computa efeitos de neblina à distância.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Fórmulas de neblina (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150a00d491f1e3fc1ea1444209449c1c2a825d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825709"
---
# <a name="fog-formulas-direct3d-9"></a>Fórmulas de neblina (Direct3D 9)

Os aplicativos C++ podem controlar como a neblina afeta a cor dos objetos em uma cena alterando como o Microsoft Direct3D computa efeitos de neblina à distância. O tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) contém membros que identificam as três fórmulas de neblina. Todas as fórmulas calculam um fator de neblina como uma função de distância, determinados parâmetros que seu aplicativo define.

## <a name="linear-fog"></a>Neblina linear

Isso é definido com a equação linear D3DFOG a seguir \_ .

![equação da neblina linear do Direct3D](images/fogliner.png)

onde

-   Start é a distância na qual os efeitos de neblina começam.
-   End é a distância na qual os efeitos de neblina não aumentam mais.
-   d representa profundidade ou distância do ponto de vista. Para a neblina baseada em intervalo, o valor de d é a distância entre a posição da câmera e um vértice. Para a neblina não baseada em intervalo, o valor de d é o valor absoluto da coordenada Z no espaço da câmera.

## <a name="exponential-fog"></a>Neblina exponencial

As fórmulas linear e exponencial têm suporte para sombra de pixel e sombra de vértice.

Isso é definido com a equação D3DFOG de exp a seguir \_ .

![equação da neblina exponencial do Direct3D](images/fogexp.png)

onde

-   e é a base de logaritmos naturais (aproximadamente 2,71828).
-   densidade é uma densidade de neblina arbitrária que pode variar de 0,0 a 1,0.
-   d representa profundidade, ou a distância do ponto de vista, conforme mencionado anteriormente.

Isso é definido com a seguinte \_ equação D3DFOG EXP2.

![equação da neblina exponencial de Direct3D 2](images/fogexp2.png)

onde

-   e é a base dos logaritmos naturais, conforme mencionado acima.
-   densidade é uma densidade de neblina arbitrária que pode variar de 0,0 a 1,0, conforme mencionado acima.
-   d representa profundidade, ou a distância do ponto de vista, conforme mencionado acima.

> [!Note]  
> O sistema armazena o fator de neblina no componente alfa da cor especular para um vértice. Se seu aplicativo executar sua própria transformação e iluminação, você poderá inserir valores de fator de neblina manualmente, a serem aplicados pelo sistema durante a renderização.

 

O grafo a seguir mostra essas fórmulas, usando valores comuns como nos parâmetros da fórmula.

![grafo das fórmulas de neblina ao longo da distância e da quantidade de cores](images/foggraph.png)

D3DFOG \_ linear é 1,0 no início e 0,0 no final. Ele não é medido em relação aos planos próximos ou distantes.

Quando o Direct3D calcula os efeitos de neblina, ele usa o fator de neblina de uma das equações anteriores na equação de mesclagem a seguir.

![equação de efeitos de neblina para Direct3D](images/fogcalc.png)

Essa fórmula dimensiona efetivamente a cor do polígono C atual pelo fator de neblina f e adiciona o produto à cor de neblina C, dimensionada pelo inverso de bit-a-dia do fator de neblina. O valor de cor resultante é uma mistura da cor da neblina e da cor original, como um fator de distância. A fórmula se aplica a todos os dispositivos com suporte no Microsoft DirectX 7,0 e posterior. Para o dispositivo de rampa herdado, o fator de neblina dimensiona os componentes de cores difusas e especulares, clamped para o intervalo de 0,0 e 1,0, inclusive. O fator de neblina normalmente começa em 1,0 para o plano próximo e diminui para 0,0 no plano distante.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de neblina](fog-types.md)
</dt> </dl>

 

 
