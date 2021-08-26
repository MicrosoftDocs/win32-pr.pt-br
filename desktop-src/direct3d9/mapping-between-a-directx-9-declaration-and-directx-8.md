---
title: Mapear entre declarações D3D9 e D3D8
description: Esta tabela mapeia os membros de uma declaração D3DVERTEXELEMENT9 para uma declaração direct3D 8.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38e6c94836499a6f2bf5dc4e88c76b822ef3143278581a4020e76dba16c9869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069026"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a>Mapear entre declarações D3D9 e D3D8

Esta tabela mapeia os membros [**de uma declaração D3DVERTEXELEMENT9**](d3dvertexelement9.md) para uma declaração direct3D 8.



| Uso do Direct3D 9           | Índice de uso do Direct3D 9 | Direct3D 8            |
|----------------------------|------------------------|-----------------------|
| D3DDECLUSAGE \_ POSITION     | 0                      | POSIÇÃO D3DVSDE \_     |
| D3DDECLUSAGE \_ POSITION     | 1                      | D3DVSDE \_ POSITION2    |
| D3DDECLUSAGE \_ NORMAL       | 0                      | D3DVSDE \_ NORMAL       |
| D3DDECLUSAGE \_ NORMAL       | 1                      | D3DVSDE \_ NORMAL2      |
| D3DDECLUSAGE \_ BLENDWEIGHT  | 0                      | D3DVSDE \_ BLENDWEIGHT  |
| D3DDECLUSAGE \_ BLENDINDICES | 0                      | D3DVSDE \_ BLENDINDICES |
| D3DDECLUSAGE \_ PSIZE        | 0                      | D3DVSDE \_ PSIZE        |
| COR D3DDECLUSAGE \_        | 0                      | D3DVSDE \_ DIFUSO      |
| COR D3DDECLUSAGE \_        | 1                      | D3DVSDE \_ SPECULAR     |
| D3DDECLUSAGE \_ TEXCOORD     | n                      | D3DVSDE \_ TEXCOORDn    |



 

Quando uma declaração é usada com o processamento de vértice de hardware em um driver Direct3D 7, o runtime do Direct3D a converte em uma FVF com as seguintes regras:

-   Somente o fluxo 0 deve ser usado (evidente no limite MaxStreams).
-   A ordem dos elementos de vértice deve ser a mesma que a ordem dos bits FVF.
-   Lacunas nas coordenadas de textura não são permitidas.
-   Qualquer elemento de vértice não descrito na tabela não pode ser convertido em um FVF válido para todos os drivers pré-DirectX 8 e, portanto, não pode ser usado nesses drivers.
-   Somente D3DDECLTYPE FLOAT2 é permitido para elementos de vértice com D3DDECLUSAGE TEXCOORD se o dispositivo não definir nenhuma das maiúsculas \_ \_ D3DPTEXTURECAPS PROJECTED ou \_ D3DPTEXTURECAPS \_ CUBEMAP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Declaração de vértice](vertex-declaration.md)
</dt> </dl>

 

 



