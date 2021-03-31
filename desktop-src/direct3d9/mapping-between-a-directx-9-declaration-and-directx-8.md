---
title: Mapear entre declarações D3D9 e D3D8
description: Esta tabela mapeia os membros de uma declaração D3DVERTEXELEMENT9 para uma declaração do Direct3D 8.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c52bd804907f201916386ef5fa5776a32a046b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645662"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a>Mapear entre declarações D3D9 e D3D8

Esta tabela mapeia os membros de uma declaração [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) para uma declaração do Direct3D 8.



| Uso do Direct3D 9           | Índice de uso do Direct3D 9 | Direct3D 8            |
|----------------------------|------------------------|-----------------------|
| \_Posição D3DDECLUSAGE     | 0                      | \_Posição D3DVSDE     |
| \_Posição D3DDECLUSAGE     | 1                      | D3DVSDE \_ POSITION2    |
| D3DDECLUSAGE \_ normal       | 0                      | D3DVSDE \_ normal       |
| D3DDECLUSAGE \_ normal       | 1                      | D3DVSDE \_ NORMAL2      |
| D3DDECLUSAGE \_ BLENDWEIGHT  | 0                      | D3DVSDE \_ BLENDWEIGHT  |
| D3DDECLUSAGE \_ BLENDINDICES | 0                      | D3DVSDE \_ BLENDINDICES |
| D3DDECLUSAGE \_ PSIZE        | 0                      | D3DVSDE \_ PSIZE        |
| \_Cor D3DDECLUSAGE        | 0                      | D3DVSDE \_ difuso      |
| \_Cor D3DDECLUSAGE        | 1                      | \_Especular D3DVSDE     |
| D3DDECLUSAGE \_ TEXCOORD     | n                      | D3DVSDE \_ TEXCOORDn    |



 

Quando uma declaração é usada com o processamento de vértice de hardware em um driver do Direct3D 7, o tempo de execução do Direct3D converte-o em um FVF com as seguintes regras:

-   Somente o fluxo 0 deve ser usado (evidente na MaxStreams Cap).
-   A ordem dos elementos de vértice deve ser a mesma que a ordem de bits FVF.
-   As lacunas nas coordenadas de textura não são permitidas.
-   Qualquer elemento Vertex não descrito na tabela não pode ser convertido em um FVF válido para todos os drivers anteriores ao DirectX 8 e, portanto, não pode ser usado nesses drivers.
-   Somente D3DDECLTYPE \_ FLOAT2 é permitido para elementos de vértice com D3DDECLUSAGE \_ TEXCOORD se o dispositivo não definir uma das D3DPTEXTURECAPS \_ PROJETADAs ou D3DPTEXTURECAPSs CUBEMAP \_ .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Declaração de vértice](vertex-declaration.md)
</dt> </dl>

 

 



