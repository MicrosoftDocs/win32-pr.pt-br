---
title: Orda (SM5-ASM)
description: Comparação de precisão dupla maior que ou igual a um componente.
ms.assetid: 2E769077-E861-4EFA-817F-7D1AE998746C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508354affbabe1ebab70be31ab45f0e7f80d0765
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006872"
---
# <a name="dge-sm5---asm"></a>Orda (SM5-ASM)

Comparação de precisão dupla maior que ou igual a um componente.



| Orda \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos resultados da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | Os componentes para comparar com *src1*.<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | Os componentes para comparar com *src0*.<br/>                |



 

## <a name="remarks"></a>Comentários

Essa instrução executa a comparação de ponto flutuante de precisão dupla (*src0*  >=  *src1*) para cada componente e grava o resultado em *dest*.

Se a comparação for verdadeira, 32-bit 0xFFFFFFFF será retornado para esse componente. Caso contrário, 32 bits 0x00000000 será retornado.

A comparação com NaN retorna false.

As máscaras de *destino* válidas são um ou dois componentes. Isto é:. x,. y,. z,. w,. XY,. XZ,. XW,. yz,. YW,. zw o primeiro componente de *destino* na máscara recebe o resultado de 32 bits para a primeira comparação dupla. O segundo componente na máscara, se presente, recebe o resultado de 32 bits para a segunda comparação dupla.

O swizzles válido para os parâmetros de origem são. xyzw,. xyxy,. zwxy,. zwzw. Os seguintes mapeamentos *src* são swizzle:

-   *src0* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





