---
description: O modelo de luz do Direct3D abrange a iluminação ambiente, difusa, especular e de emissão.
ms.assetid: cf870c89-4be0-4b95-92aa-ec7bcdc6d9dd
title: Matemática de iluminação (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1c6ffa8a1142c1be40993dcd8130b4708f2b509c8a5a1f05e234d0231c3bdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728331"
---
# <a name="mathematics-of-lighting-direct3d-9"></a>Matemática de iluminação (Direct3D 9)

O modelo de luz do Direct3D abrange a iluminação ambiente, difusa, especular e de emissão. Isso é flexibilidade suficiente para solucionar problemas de uma diversas situações de iluminação. Você se refere à quantidade total de luz em uma cena como a iluminação global e a computa usando a equação a seguir.


```
Global Illumination = Ambient Light + Diffuse Light + Specular Light + Emissive Light 
```



A [iluminação de ambiente (Direct3D 9)](ambient-lighting.md) é a iluminação constante. É constante em todas as direções e cores de ti todos os pixels de um objeto são iguais. Ela é rápida de calcular, mas deixa os objetos com uma aparência simples e irreal. Para ver como a iluminação de ambiente é calculada pelo Direct3D, consulte iluminação de ambiente (Direct3D 9).

A [iluminação difusa (Direct3D 9)](diffuse-lighting.md) depende da direção da luz e da superfície do objeto normal. Varia na superfície de um objeto como resultado da direção da luz de alteração e do vetor de numeração de superfície em alteração. É necessário mais tempo para calcular a iluminação difusa porque ela é alterada para cada vértice de objeto, mas a vantagem de usá-la é que ela sombreia objetos e dá a eles profundidade tridimensional (3D). Para ver como a iluminação difusa é calculada no Direct3D, consulte iluminação difusa (Direct3D 9).

A [Iluminação especular (Direct3D 9)](specular-lighting.md) identifica os destaques brilhantes especulares que ocorrem quando a luz atinge uma superfície de objeto e reflete de volta para a câmera. É mais intensa do que a luz difusa e fica mais rapidamente na superfície do objeto. O cálculo da iluminação especular demora mais do que o da iluminação difusa, no entanto, a vantagem de usá-lo é que ele adiciona detalhes significativas à superfície. Para ver como a iluminação especular é calculada no Direct3D, consulte Iluminação especular (Direct3D 9).

A [iluminação emissiva (Direct3D 9)](emissive-lighting.md) é a luz emitida por um objeto; por exemplo, um brilho. Para ver como a iluminação emissiva é calculada no Direct3D, consulte iluminação emissiva (Direct3D 9).

A iluminação realista pode ser realizada ao aplicar cada um desses tipos de iluminação a uma cena 3D. Os valores calculados para componentes de ambiente, emissão e difusa são reproduzidos como a cor do vértice difusa; o valor do componente de iluminação especular é reproduzido como a cor do vértice especular. Os valores de luz ambiente, difusa e especular podem ser afetados pelo fator de atenuação e destaque da luz específica. Para obter mais informações sobre como a atenuação funciona, consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md).

Para obter um efeito de iluminação mais realista, é possível adicionar mais luzes; no entanto, a cena leva mais tempo para renderizar. Para obter todos os efeitos desejados por um designer, alguns jogos usam mais processamento da CPU do que está normalmente disponível. Nesse caso, é comum reduzir o número de cálculos de iluminação ao mínimo usando mapas de luz e ambiente para adicionar a iluminação à cena com mapas de textura.

A iluminação é calculada no espaço da câmera. Para ver como as transformações de iluminação são calculadas, consulte [transformações de espaço da câmera (Direct3D 9)](camera-space-transformations.md). A iluminação otimizada pode ser computada no espaço do modelo, quando existem condições especiais: vetores normais já estão normalizados (D3DRS \_ NORMALIZENORMALS é true), a mesclagem de vértice não é necessária, as matrizes de transformação são ortogonal e assim por diante.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Luzes e materiais](lights-and-materials.md)
</dt> </dl>

 

 



