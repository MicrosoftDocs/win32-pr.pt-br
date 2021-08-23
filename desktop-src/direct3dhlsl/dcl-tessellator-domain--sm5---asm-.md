---
title: dcl_tessellator_domain (sm5 – asm)
description: Declare o domínio do mosaico em uma seção de declaração de sombreador de chassi e o sombreador de domínio.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52a027e9fab091cf31e8577266015e974ec78033fe19a9542f0aa3c6ca4651db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986706"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a>domínio do \_ mosaico dcl \_ (sm5 – asm)

Declare o domínio do mosaico em uma seção de declaração de sombreador de chassi e o sombreador de domínio.



| dcl \_ tessellator \_ domain {domain \_ isoline \| domain \_ tri \| domínio \_ quad} |
|---------------------------------------------------------------------------|



 



| Item                                                                                                                                                                                | Descrição                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*domínio \_ isoline \| domain tri domain \_ \| \_ quad*<br/> | \[em \] O domínio.<br/> |



 

## <a name="remarks"></a>Comentários

O comportamento será indefinido se o sombreador de chassi e o sombreador de domínio fornecerem domínios incompatibilidades ou qualquer outro decalatório conflitante.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco                 | Domínio | Geometry | Pixel | Computação |
|--------|----------------------|--------|----------|-------|---------|
|        | Seção Declarações | X      |          |       |         |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





