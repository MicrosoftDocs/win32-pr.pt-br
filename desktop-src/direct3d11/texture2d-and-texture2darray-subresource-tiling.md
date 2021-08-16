---
title: Sub-recursos lado a lado de Texture2D e Texture2DArray
description: Estas tabelas mostram como sub-recursos Texture2D e Texture2DArray são agrupados lado a lado.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ee7cc181845785ab978dc5d58b1e131a7f32c34a6d04006af1ac8034f089ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530431"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a>Sub-recursos lado a lado de Texture2D e Texture2DArray

Essas tabelas mostram como as sub-recursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) são lado a lado. Os valores nestas tabelas não contam a compactação MIP final.

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



 

As contagens de bits de formato sem suporte com recursos lado a lado são formatos de 96 bpp, formatos de vídeo, FORMATO DXGI \_ \_ R1 \_ UNORM, FORMATO DXGI \_ \_ R8G8 \_ B8G8 \_ UNORM e FORMATO DXGI \_ \_ R8R8 \_ G8B8 \_ UNORM.

Esta tabela mostra como os sub-recursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) com várias contagens multisample são agrupados lado a lado.



| Contagem de vários exemplos           | Dividir dimensões de lado acima por (WxH) |
|-----------------------------|-------------------------------|
| 1                           | 1x1                           |
| 2                           | 2x1                           |
| 4                           | 2x2                           |
| 8                           | 4x2                           |
| 16                          | 4x4                           |



 

Somente as contagens de exemplo 1 e 4 são necessárias (e permitidas) para serem suportadas com recursos lado a lado. Atualmente, os recursos lado a lado não são suportados 2, 8 e 16, embora sejam mostrados.

As implementações podem optar por dar suporte ao modo de MSAA (antialiasing multisample multisample) de 2, 8 e/ou 16 para recursos não lado a lado, embora o recurso lado a lado não os suporte.

Recursos lado a lado com contagens de exemplo maiores que 1 não podem usar 128 formatos bpp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como a área de um recurso lado a lado é lado a lado](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 