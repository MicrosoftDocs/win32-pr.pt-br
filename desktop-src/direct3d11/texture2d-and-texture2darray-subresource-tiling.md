---
title: Sub-recursos lado a lado de Texture2D e Texture2DArray
description: Estas tabelas mostram como sub-recursos Texture2D e Texture2DArray são agrupados lado a lado.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a7ded22fcb7e7e476a701c7db3063dfae33fda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366341"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a>Sub-recursos lado a lado de Texture2D e Texture2DArray

Essas tabelas mostram como os subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) são colocados ao lado. Os valores nestas tabelas não contam a compactação MIP final.

Esta tabela mostra como os sub-recursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) com contagens multisample de 1 são agrupados lado a lado.



| Bits/Pixel (1 amostra/pixel) | Dimensões do bloco (Pixels, LxA) |
|-----------------------------|-------------------------------|
| 8                           | 256x256                       |
| 16                          | 256x128                       |
| 32                          | 128x128                       |
| 64                          | 128x64                        |
| 128                         | 64x64                         |
| BC1,4                       | 512x256                       |
| BC2,3,5,6,7                 | 256x256                       |



 

As contagens de bits de formato não suportadas com os recursos do lado do suporte são formatos de 96 BPP, formatos de vídeo, \_ formato dxgi \_ \_ UNORM, \_ formato dxgi \_ R8G8 \_ B8G8 UNORM e \_ \_ formato dxgi \_ R8R8 \_ \_ G8B8 UNORM.

Esta tabela mostra como os sub-recursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) com várias contagens multisample são agrupados lado a lado.



| Contagem de multiamostras           | Dividir dimensões de bloco acima por (WxH) |
|-----------------------------|-------------------------------|
| 1                           | 1x1                           |
| 2                           | 2x1                           |
| 4                           | 2x2                           |
| 8                           | 4x2                           |
| 16                          | 4x4                           |



 

Somente as contagens de exemplo 1 e 4 são necessárias (e permitidas) para serem suportadas com recursos de lado. No momento, os recursos de lado não dão suporte a 2, 8 e 16, embora sejam mostrados.

As implementações podem optar por oferecer suporte ao modo de 2, 8 e/ou 16 amostras de anti-aliasing multiamostrador (MSAA) para recursos que não são de lado do ladrilho, mesmo que o recurso de lado não ofereça suporte a eles.

Os recursos com sublado com contagens de exemplo maiores que 1 não podem usar formatos de 128 BPP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como a área de um recurso do lado do ladrilho é colocada](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 