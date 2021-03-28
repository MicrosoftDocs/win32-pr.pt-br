---
title: ne (sm4-ASM)
description: Comparação de ponto flutuante de vetor por componente sem igual.
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e53ff726047bd1870e6c836f4508bdf87001b3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365233"
---
# <a name="ne-sm4---asm"></a>ne (sm4-ASM)

Comparação de ponto flutuante de vetor por componente sem igual.



| ne dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\] |
|----------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                            |
|-----------------------------------------------------------------|--------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] resultado da operação.<br/>         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes para comparar com o *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nos \] componentes para comparar com o *src0*.<br/> |



 

## <a name="remarks"></a>Comentários

Essa instrução executa a comparação de float (*src0* ! = *src1*) para cada componente e grava o resultado em *dest*.

Se a comparação for verdadeira, 0xFFFFFFFF será retornado para esse componente. Caso contrário, 0x0000000 será retornado.

As normas são liberadas antes da comparação com os registros de origem originais intocados.

+ 0 é igual a-0.

A comparação com NaN retorna true.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





