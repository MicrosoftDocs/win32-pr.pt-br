---
title: ne (sm4 – asm)
description: Comparação de ponto flutuante de vetor não igual a componente.
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 116f6197c33ef3c040d6c02b7aa561e03cdcc694a2878b6f16554c053a8862db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457336"
---
# <a name="ne-sm4---asm"></a>ne (sm4 – asm)

Comparação de ponto flutuante de vetor não igual a componente.



| ne dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|----------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                            |
|-----------------------------------------------------------------|--------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O resultado da operação.<br/>         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] Os componentes a comparar com *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[em \] Os componentes a comparar com *src0*.<br/> |



 

## <a name="remarks"></a>Comentários

Essa instrução executa a comparação float (*src0* != *src1*) para cada componente e grava o resultado *em dest*.

Se a comparação for verdadeira, 0xFFFFFFFF será retornado para esse componente. Caso contrário 0x0000000 será retornado.

Os desnorms são liberados antes da comparação com registros de origem originais inalterados.

+0 é igual a -0.

A comparação com NaN retorna true.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





