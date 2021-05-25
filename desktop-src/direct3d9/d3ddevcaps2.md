---
description: Sinalizadores de funcionalidade do driver D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6296db9b338d5f9a8c8ede702a784baf1fdfd462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343201"
---
# <a name="d3ddevcaps2"></a>D3DDEVCAPS2

Sinalizadores de funcionalidade do driver D3DDEVCAPS2.



| \#Definir                                        | Descrição                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH                | O dispositivo dá suporte ao mosaico adaptável de patches RT                                                                                                                                                                       |
| D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH                 | O dispositivo dá suporte ao mosaico adaptável de N patches.                                                                                                                                                                       |
| D3DDEVCAPS2 \_ PODE \_ STRETCHRECT \_ DE \_ TEXTURAS   | O dispositivo dá [**suporte ao StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) usando uma textura como a origem.                                                                                                                       |
| D3DDEVCAPS2 \_ DMAPNPATCH                         | O dispositivo dá suporte a mapas de deslocamento para N patches.                                                                                                                                                                          |
| D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH               | O dispositivo dá suporte a mapas de deslocamento pré-mpados para N patches. Para obter mais informações sobre mapeamento de deslocamento, consulte [Mapeamento de deslocamento (Direct3D 9)](displacement-mapping.md).                                           |
| D3DDEVCAPS2 \_ STREAMOFFSET                       | O dispositivo dá suporte a deslocamentos de fluxo.                                                                                                                                                                                           |
| D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET | Vários elementos de vértice poderão compartilhar o mesmo deslocamento em um fluxo se D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET for definido pelo dispositivo e a declaração de vértice não tiver um elemento \_ com D3DDECLUSAGE \_ POSITIONT0. |



 

## <a name="constant-information"></a>Informações constantes



| Requisito                         | Valor           |
|--------------------------|------------|
| parâmetro                   | d3d9caps. h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
