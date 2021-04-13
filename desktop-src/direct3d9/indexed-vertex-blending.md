---
description: A mesclagem de vértices indexados estende o suporte de mistura de vértice no Direct3D para permitir que as matrizes sejam usadas para mesclagem.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Mistura de vértices indexados (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cfe7b45831317fdf9e92525ed74bbd27323e99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456373"
---
# <a name="indexed-vertex-blending-direct3d-9"></a>Mistura de vértices indexados (Direct3D 9)

A mesclagem de vértices indexados estende o suporte de mistura de vértice no Direct3D para permitir que as matrizes sejam usadas para mesclagem. Essas matrizes são referenciadas usando um índice de matriz. Esses índices são fornecidos por vértice e se referem a uma paleta de até 256 matrizes. Cada índice é de 8 bits e cada vértice pode ter até quatro índices, o que permite que quatro matrizes sejam mescladas por vértice. Os índices são empacotados em um DWORD. Como os índices são especificados por vértice, até 12 matrizes podem afetar um único triângulo, e qualquer matriz na paleta pode afetar os vértices de uma chamada de desenho. Essa abordagem tem as seguintes vantagens.

-   Ele permite que mais matrizes afetem um único triângulo.
-   Ele permite que triângulos mais misturados sejam passados na mesma chamada de desenho.
-   Ele faz a mesclagem de vértice independente de índices de triângulo. Isso permite que malhas progressivas funcionem em conjunto com a mistura de vértice.

Uma desvantagem dessa abordagem é que ela não funciona com primitivas de superfície curvada quando o mosaico ocorre antes do processamento de vértice.

O diagrama a seguir demonstra como quatro matrizes podem afetar um vértice. Cada vértice tem até quatro índices, de modo que quatro matrizes podem ser mescladas por vértice. O diagrama usa as matrizes indexadas em 0, 2, 5 e 6.

![diagrama de mesclagem de vértice indexado usando 4 de 256 matrizes disponíveis](images/dword1.png)

O diagrama a seguir demonstra como até 12 matrizes podem afetar um triângulo. Usando índices especificados em uma base por vértice, até 12 matrizes podem afetar o triângulo.

![diagrama de mesclagem de vértice indexado para um triângulo usando 12 de 256 matrizes disponíveis](images/dword2.png)

A equação a seguir determina o caso geral de como as matrizes afetam um vértice.

![equação da mistura de vértices indexados](images/indexedvblend.png)

O <sub>modelo</sub> V é a posição de vértice do espaço do modelo de entrada. Index0.. Index3 são os índices de matriz por vértice empacotados em um DWORD. M \[ \] é a matriz de matrizes mundiais que são indexadas no. b ₀.. b ₂ são os pesos de mistura. O<sub>mundo</sub> V é a posição de vértice do espaço do mundo de saída.

Para obter mais informações sobre a mistura de vértices indexados, consulte [usando o Direct3D 9](using-indexed-vertex-blending.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem de geometria](geometry-blending.md)
</dt> </dl>

 

 



