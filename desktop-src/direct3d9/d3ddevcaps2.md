---
description: Sinalizadores de capacidade do driver D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e774076f5ad93abf5ab1ffc343f573497592728f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164009"
---
# <a name="d3ddevcaps2"></a>D3DDEVCAPS2

Sinalizadores de capacidade do driver D3DDEVCAPS2.



|                                                 |                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definir                                        | Descrição                                                                                                                                                                                                               |
| D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH                | O dispositivo dá suporte a mosaico adaptável de RT-patches                                                                                                                                                                       |
| D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH                 | O dispositivo dá suporte a mosaico adaptável de N-patches.                                                                                                                                                                       |
| D3DDEVCAPS2 \_ pode \_ STRETCHRECT \_ de \_ texturas   | O dispositivo dá suporte a [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) usando uma textura como a origem.                                                                                                                       |
| D3DDEVCAPS2 \_ DMAPNPATCH                         | O dispositivo dá suporte a mapas de substituição para N-patches.                                                                                                                                                                          |
| D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH               | O dispositivo dá suporte a mapas de deslocamento de amostra para N-patches. Para obter mais informações sobre mapeamento de deslocamento, consulte [mapeamento de deslocamento (Direct3D 9)](displacement-mapping.md).                                           |
| D3DDEVCAPS2 \_ STREAMOFFSET                       | O dispositivo dá suporte a deslocamentos de fluxo.                                                                                                                                                                                           |
| D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET | Vários elementos de vértice podem compartilhar o mesmo deslocamento em um fluxo se D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET for definido pelo dispositivo e a declaração de vértice não tiver um elemento com D3DDECLUSAGE \_ POSITIONT0. |



 

## <a name="constant-information"></a>Informações constantes



|                          |            |
|--------------------------|------------|
| parâmetro                   | d3d9caps. h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
