---
description: A mesclagem de vértice indexada estende o suporte à mesclagem de vértices no Direct3D para permitir que matrizes sejam usadas para mesclagem.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Mesclagem de vértice indexada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3d45e3ff72a33cd21265d1e4aa25e237e2a73e473914898d5c1057316d4ca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728685"
---
# <a name="indexed-vertex-blending-direct3d-9"></a>Mesclagem de vértice indexada (Direct3D 9)

A mesclagem de vértice indexada estende o suporte à mesclagem de vértices no Direct3D para permitir que matrizes sejam usadas para mesclagem. Essas matrizes são referenciadas usando um índice de matriz. Esses índices são fornecidos por vértice e se referem a uma paleta de até 256 matrizes. Cada índice é de 8 bits e cada vértice pode ter até quatro índices, o que permite que quatro matrizes sejam mescladas por vértice. Os índices são empacotados em um DWORD. Como os índices são especificados por vértice, até 12 matrizes podem afetar um único triângulo e qualquer matriz na paleta pode afetar os vértices de uma chamada de desenho. Essa abordagem tem as seguintes vantagens.

-   Ele permite que mais matrizes afetem um único triângulo.
-   Ele permite que mais triângulos mistos sejam passados na mesma chamada de desenho.
-   Ele torna a mesclagem de vértice independente de índices de triângulo. Isso permite que malhas progressivas funcionem em conjunto com a combinação de vértices.

Uma desvantagem dessa abordagem é que ela não funciona com primitivos de superfície curva quando o mosaico ocorre antes do processamento de vértice.

O diagrama a seguir demonstra como quatro matrizes podem afetar um vértice. Cada vértice tem até quatro índices, portanto, quatro matrizes podem ser mescladas por vértice. O diagrama usa as matrizes indexadas em 0, 2, 5 e 6.

![diagrama de mesclagem de vértice indexado usando 4 de 256 matrizes disponíveis](images/dword1.png)

O diagrama a seguir demonstra como até 12 matrizes podem afetar um triângulo. Usando índices especificados por vértice, até 12 matrizes podem afetar o triângulo.

![diagrama de mesclagem de vértice indexado para um triângulo usando 12 de 256 matrizes disponíveis](images/dword2.png)

A equação a seguir determina o caso geral de como as matrizes ativas um vértice.

![equação de mesclagem de vértice indexada](images/indexedvblend.png)

O <sub>modelo V</sub> é a posição do vértice de espaço do modelo de entrada. Index0.. Index3 são os índices de matriz por vértice empacotados em uma DWORD. M \[ \] é a matriz de matrizes de mundo que são indexadas. b.. b são os pesos da mistura. V<sub>world é</sub> a posição de vértice de espaço do mundo de saída.

Para obter mais informações sobre a combinação de vértices indexados, consulte [Using Indexed Vertex Blending (Direct3D 9)](using-indexed-vertex-blending.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem de geometria](geometry-blending.md)
</dt> </dl>

 

 



