---
description: No Direct3D, todas as imagens bidimensionais (2D) são representadas por um intervalo linear de memória chamado superfície.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Formatos de superfície (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78aad64940510a080ba05d0513e7f66d33912a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087703"
---
# <a name="surface-formats-direct3d-9"></a>Formatos de superfície (Direct3D 9)

No Direct3D, todas as imagens bidimensionais (2D) são representadas por um intervalo linear de memória chamado superfície. Uma superfície pode ser considerada como uma matriz 2D, em que cada elemento contém um valor de cor representando uma pequena seção da imagem, chamada pixel. O nível de detalhe de uma imagem é definido pelo número de pixels necessários para representar a imagem e o número de bits necessários para o espectro de cores da imagem. Por exemplo, uma imagem com 800 pixels de largura por 600 pixels de altura com 32 bits de cor para cada pixel (escrito como 800x600x32) será mais detalhada do que uma imagem com 640 pixels de largura por 480 pixels de altura com 16 bits de cor para cada pixel (escrito como 640x480x16). Da mesma forma, a imagem mais detalhada exigirá uma superfície maior para armazenar os dados. Para uma imagem 800x600x32, as dimensões da matriz da superfície serão 800x600 e cada elemento conterá um valor de 32 bits para representar sua cor.

Todas as superfícies têm um tamanho e armazenam um número específico de bits que representam cores. Os bits que representam a cor são separados em elementos de cor individuais: vermelho, verde e azul. No Direct3D, todos os elementos de cor são definidos pelo tipo enumerado [D3DFORMAT](d3dformat.md) . Um formato de cor do Direct3D é dividido no número de bytes reservados para cada cor. Por exemplo, um formato de cor de 16 bits no Direct3D é definido como D3DFMT \_ R5G6B5, em que 5 bits são reservados para vermelho (R), 6 bits para verde (G) e 5 bits para azul (B).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Superfícies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 



