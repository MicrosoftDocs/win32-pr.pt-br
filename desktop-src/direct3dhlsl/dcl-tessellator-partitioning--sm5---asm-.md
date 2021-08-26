---
title: dcl_tessellator_partitioning (SM5-ASM)
description: Declare o particionamento Tessellator em uma seção de declaração do sombreador envoltória.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae40873db4042e568ae637634e75db6f4746985a316bf9c1e092e6b0925b51b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068496"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a>particionamento de Tessellator de DCL \_ \_ (SM5-ASM)

Declare o particionamento Tessellator em uma seção de declaração do sombreador envoltória.



| particionamento de Tessellator de DCL \_ \_ {particionamento \_ inteiro \| particionamento de \_ pow2 \|\_fração fracionária \_ ímpar \| particionamento de \_ frações \_ até mesmo} |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Descrição                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*Particionando o pow2 de particionamento de inteiros Particionando o particionamento \_ \| \_ \| \_ \_ estranho fracionário \| \_ \_ uniforme*<br/> | \[no \] particionamento Tessellator.<br/> |



 

## <a name="remarks"></a>Comentários

Do ponto de vista do hardware, o \_ pow2 se comporta exatamente como o \_ inteiro. Cabe ao autor do sombreador HLSL e/ou compilercode arredondar TessFactors para potências de 2.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória                 | Domínio | Geometry | 16x16 | Computação |
|--------|----------------------|--------|----------|-------|---------|
|        | Seção de declarações |        |          |       |         |



 

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

 

 





