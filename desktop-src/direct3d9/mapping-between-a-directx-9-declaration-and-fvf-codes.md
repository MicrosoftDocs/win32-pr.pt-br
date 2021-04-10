---
description: Esta tabela mapeia os membros de uma declaração D3DVERTEXELEMENT9 para um código FVF.
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: Mapeamento entre uma declaração de Direct3D e códigos de FVF (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4831af7b8c03ae4abd5ac2847351d2a6c921fb97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087592"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a>Mapeamento entre uma declaração de Direct3D e códigos de FVF (Direct3D 9)

Esta tabela mapeia os membros de uma declaração [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) para um código FVF.



| Tipo de dados             | Uso                      | Índice de uso | FVF                       |
|-----------------------|----------------------------|-------------|---------------------------|
| D3DDECLTYPE \_ FLOAT3   | \_Posição D3DDECLUSAGE     | 0           | D3DFVF \_ XYZ               |
| D3DDECLTYPE \_ FLOAT4   | Posição de D3DDECLUSAGE \_    | 0           | D3DFVF \_ XYZRHW            |
| D3DDECLTYPE \_ floatn   | D3DDECLUSAGE \_ BLENDWEIGHT  | 0           | D3DFVF \_ XYZBn             |
| D3DDECLTYPE \_ UBYTE4   | D3DDECLUSAGE \_ BLENDINDICES | 0           | D3DFVF \_ XYZB (nWeights + 1) |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ normal       | 0           | D3DFVF \_ normal            |
| D3DDECLTYPE \_ FLOAT1   | D3DDECLUSAGE \_ PSIZE        | 0           | D3DFVF \_ PSIZE             |
| D3DDECLTYPE \_ D3DCOLOR | \_Cor D3DDECLUSAGE        | 0           | D3DFVF \_ difuso           |
| D3DDECLTYPE \_ D3DCOLOR | \_Cor D3DDECLUSAGE        | 1           | \_Especular D3DFVF          |
| D3DDECLTYPE \_ floatm   | D3DDECLUSAGE \_ TEXCOORD     | n           | D3DFVF \_ TEXCOORDSIZEm (n)  |
| D3DDECLTYPE \_ FLOAT3   | \_Posição D3DDECLUSAGE     | 1           | N/D                       |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ normal       | 1           | N/D                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Declaração de vértice](vertex-declaration.md)
</dt> </dl>

 

 



