---
title: Sub-recursos lado a lado de Texture3D
description: Esta tabela mostra como os sub-recursos de Texture3D são colocados lado a lado.
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7a668f499a2f6d3911716d5d7bad60df4cd9e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988714"
---
# <a name="texture3d-subresource-tiling"></a>Sub-recursos lado a lado de Texture3D

Esta tabela mostra como os [**SubTexture3Ds**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) de subrecursos são enlados. Os valores nesta tabela não contam a compactação MIP final.

Esta tabela pega o agrupamento lado a lado do [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e divide cada uma das dimensões x/y por 4 e adiciona 16 camadas de profundidade. Todos os blocos do primeiro plano (plano 2D de blocos definindo as 16 primeiras camadas de profundidade) aparecem antes dos planos subsequentes.

> [!Note]  
> O suporte do [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) em recursos de blocos gráficos não é exposto na implementação inicial dos recursos do lado do quadrado, mas as formas de bloco desejadas são listadas aqui porque o suporte pode ser considerado em uma versão futura.

 



| Bits/Pixel (1 amostra/pixel) | Dimensões do bloco (Pixels, LxAxP) |
|-----------------------------|---------------------------------|
| 8                           | 64x32x32                        |
| 16                          | 32x32x32                        |
| 32                          | 32x32x16                        |
| 64                          | 32x16x16                        |
| 128                         | 16x16x16                        |
| BC1,4                       | 128x64x16                       |
| BC2,3,5,6,7                 | 64x64x16                        |



 

As contagens de bits de formato não suportadas com os recursos do lado do suporte são formatos de 96 BPP, formatos de vídeo, \_ formato dxgi \_ \_ UNORM, \_ formato dxgi \_ R8G8 \_ B8G8 UNORM e \_ \_ formato dxgi \_ R8R8 \_ \_ G8B8 UNORM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como a área de um recurso do lado do ladrilho é colocada](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 