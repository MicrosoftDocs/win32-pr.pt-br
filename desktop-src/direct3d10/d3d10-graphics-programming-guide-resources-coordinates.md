---
description: Os sistemas de coordenadas para Direct3D 10 são definidos para pixels e texels.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Sistemas de coordenadas (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba84cd7d807474a1ff41f873d16cbd7eee07224
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646517"
---
# <a name="coordinate-systems-direct3d-10"></a>Sistemas de coordenadas (Direct3D 10)

Os sistemas de coordenadas para Direct3D 10 são definidos para pixels e texels.



|                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D 9 e o Direct3D 10:<br/> O Direct3D 10 define o canto superior esquerdo do pixel superior esquerdo como a origem de um destino de renderização.<br/> O Direct3D 9 define o centro do pixel superior esquerdo como a origem de um destino de renderização.<br/> |



 

-   [Sistema de coordenadas de pixel](#pixel-coordinate-system)
    -   [Sistema de coordenadas de pixel para Direct3D 9](#pixel-coordinate-system-for-direct3d-9)
-   [Sistema de coordenadas Texel](#texel-coordinate-system)
    -   [Sistema de coordenadas Texel](#texel-coordinate-system)
-   [Tópicos relacionados](#related-topics)

## <a name="pixel-coordinate-system"></a>Sistema de coordenadas de pixels

O sistema de coordenadas de pixels no Direct3D 10 define a origem de um destino de renderização no canto superior esquerdo. conforme mostrado no diagrama a seguir. Os centros de pixels são separados por (0,5f;0,5f) de locais de números inteiros.

![diagrama do sistema de coordenadas de pixels no direct3d 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a>Sistema de coordenadas de pixel para Direct3D 9

Para referência, aqui está o sistema de coordenadas de pixel para o Direct3D 9, que definiu a origem ou um destino de renderização como o centro do pixel superior esquerdo, (0,5, 0.5) fora do canto superior esquerdo, conforme mostrado no diagrama a seguir. No Direct3D 9, os centros de pixel estão em locais inteiros.

![diagrama do sistema de coordenadas de pixel no Direct3D 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a>Sistema de coordenadas de texel

O sistema de coordenadas de texel é originado no canto superior esquerdo da textura, conforme mostrado no diagrama a seguir. Isso torna a renderização de texturas alinhadas na tela trivial (no Direct3D 10), pois o sistema de coordenadas de pixel é alinhado com o sistema de coordenadas Texel.

![diagrama do sistema de coordenadas de texel](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a>Sistema de coordenadas de texel

As coordenadas de textura são representadas por um número normalizado ou dimensionado; cada coordenada de textura é mapeada de acordo com um texel específico da seguinte maneira:

Para uma coordenada normalizada:

-   Amostragem de ponto: Texel \# = Floor ( \* largura U)
-   Amostragem linear: esquerda Texel \# = Floor ( \* largura U), direita Texel \# = Left Texel \# + 1

Para uma coordenada dimensionada:

-   Amostragem de ponto: Texel \# = Floor (U)
-   Amostragem linear: esquerda Texel \# = Floor (U-0,5), direita Texel \# = Left Texel \# + 1

Onde a largura é a largura da textura (em texels).

O encapsulamento do endereço da textura ocorre após o cálculo da localização de texel.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




