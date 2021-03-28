---
title: dcl_tessellator_domain (SM5-ASM)
description: Declare o domínio Tessellator em uma seção de declaração do sombreador envoltória e o sombreador de domínio.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8724ee9564239ffaca6f5c34a39fb1b4ef967e51
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365284"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a>\_domínio DCL Tessellator \_ (SM5-ASM)

Declare o domínio Tessellator em uma seção de declaração do sombreador envoltória e o sombreador de domínio.



| \_domínio DCL Tessellator \_ {Domain \_ Isoline \| domínio \_ Tri \| domínio \_ quádruplo} |
|---------------------------------------------------------------------------|



 



| Item                                                                                                                                                                                | Descrição                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*domínio \_ Isoline \| domínio \_ Tri \| domínio \_ quádruplo*<br/> | \[no \] domínio.<br/> |



 

## <a name="remarks"></a>Comentários

O comportamento será indefinido se o sombreador envoltória e o sombreador de domínio fornecerem incompatibilidade de domínios ou qualquer outro decalarations conflitante.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória                 | Domínio | Geometria | 16x16 | Computação |
|--------|----------------------|--------|----------|-------|---------|
|        | Seção de declarações | X      |          |       |         |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





