---
description: Muitas vezes, os pontos especificados para vértices não correspondem exatamente aos pixels na tela. Quando isso acontece, o Direct3D aplica as regras de rasterização de triângulo para decidir quais pixels se aplicam a um determinado triângulo.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Regras de rasterização (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b2f12e0064202fcbca58f52cb163166d0a82
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104172398"
---
# <a name="rasterization-rules-direct3d-9"></a>Regras de rasterização (Direct3D 9)

Muitas vezes, os pontos especificados para vértices não correspondem exatamente aos pixels na tela. Quando isso acontece, o Direct3D aplica as regras de rasterização de triângulo para decidir quais pixels se aplicam a um determinado triângulo.

-   [Regras de rasterização de triângulo](#triangle-rasterization-rules)
-   [Regras de ponto e linha](#point-and-line-rules)
-   [Regras de Sprite de ponto](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a>Regras de rasterização de triângulo

O Direct3D usa uma convenção de preenchimento superior esquerdo para preencher a geometria. Essa é a mesma convenção utilizada para retângulos em GDI e OpenGL. No Direct3D, o centro do pixel é o ponto determinante. Se o centro está dentro de um triângulo, o pixel é parte do triângulo. Os centros de pixel estão localizados em coordenadas de números inteiros.

Essa descrição das regras de rasterização de triângulos utilizada pelo Direct3D não se aplica necessariamente a todo o hardware disponível. O teste pode revelar pequenas variações na implementação dessas regras.

A ilustração a seguir mostra um retângulo cujo canto superior esquerdo está em (0, 0) e o canto inferior direito em (5, 5). Esse retângulo preenche 25 pixels, como esperado. A largura do retângulo é definida como direita menos esquerda. A altura é definida como parte inferior menos superior.

![ilustração de um quadrado numerado dividido em seis linhas e colunas](images/pixmap.png)

Na convenção de preenchimento superior esquerdo, *superior* refere-se à localização vertical dos trechos horizontais e *esquerdo* refere-se à localização horizontal dos pixels em uma extensão. Uma borda não pode ser superior, a menos que seja horizontal. Em geral, a maioria dos triângulos tem somente as margens esquerda e direita. A ilustração a seguir mostra uma borda superior e uma borda direita.

![ilustração de um quadrado numerado que contém dois triângulos](images/triedge.png)

A convenção de preenchimento superior esquerdo determina a ação executada pelo Direct3D quando um triângulo passa pelo centro de um pixel. A ilustração a seguir mostra dois triângulos, um em (0, 0), (5, 0) e (5, 5) e o outro em (0, 5), (0, 0) e (5, 5). O primeiro triângulo nesse caso tem 15 pixels (mostrado em preto), enquanto o segundo tem apenas 10 pixels (mostrado em cinza), pois a borda compartilhada é a esquerda do primeiro triângulo.

![ilustração de um quadrado numerado que mostra dois triângulos](images/twotris.png)

Se você definir um retângulo com o canto superior esquerdo em (0,5; 0,5) e o canto inferior direito em (2,5; 4,5), o ponto central desse retângulo é em (2,5; 1,5). Quando o rasterizador Direct3D criar mosaicos com esse retângulo, o centro de cada pixel está especificamente dentro de cada um dos quatro triângulos e não requer a convenção de preenchimento superior esquerdo. A ilustração a seguir mostra isso. Os pixels do retângulo são identificados de acordo com o triângulo no qual o Direct3D os inclui.

![Mostra um quadrado numerado que contém um retângulo dividido em quatro triângulos.](images/noambig.png)

Se você mover o retângulo na ilustração anterior para que o canto superior esquerdo fique em (1,0; 1,0), o canto inferior direito em (3,0; 5,0) e o centro aponte para (2,0; 3,0), o Direct3D aplica a convenção de preenchimento superior esquerdo. A maioria dos pixels desse retângulo amplia a fronteira entre dois ou mais triângulos, como demonstrado na ilustração a seguir.

![ilustração de um quadrado numerado que contém um retângulo dividido em quatro triângulos](images/fillrule.png)

Para os dois retângulos, os mesmos pixels são afetados, conforme mostrado na ilustração a seguir.

![ilustração de pixels que são afetados pelos dois quadrados numerados anteriores](images/samepix.png)

## <a name="point-and-line-rules"></a>Regras de ponto e linha

Os pontos são renderizados igual aos sprites de ponto, que são renderizado como quadrilaterais alinhado à tela e, portanto, seguem as mesmas regras de renderização do polígono.

As regras de renderização de linha não as mesmas para [linhas de GDI](../gdi/lines.md).

Para obter informações sobre a renderização de linha AntiAlias, consulte [**ID3DXLine**](id3dxline.md).

## <a name="point-sprite-rules"></a>Regras de sprite de ponto

Os sprites de ponto e os primitivos de patch são rasterizados como se os primitivos fossem transformados em triângulos antes e os triângulos resultante fossem rasterizados. Para obter mais informações, consulte [Point sprites (Direct3D 9)](point-sprites.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coordenar sistemas e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
