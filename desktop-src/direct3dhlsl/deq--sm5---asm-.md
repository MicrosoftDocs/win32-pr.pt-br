---
title: DEQ (SM5-ASM)
description: Comparação de igualdade de precisão dupla de componente.
ms.assetid: 99806989-D3A0-43F4-832A-5F1BD9C59A11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5781c0b7d757e8bf72b81da54a4d6a8fe7467a40fa2509abdf093e27eb119ddc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950546"
---
# <a name="deq-sm5---asm"></a>DEQ (SM5-ASM)

Comparação de igualdade de precisão dupla de componente.



| DEQ \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos resultados da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes para comparar com o *src1*.<br/>         |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nos \] componentes para comparar com o *src0*.<br/>         |



 

## <a name="remarks"></a>Comentários

Essa instrução executa a comparação de ponto flutuante de precisão dupla (*src0*  ==  *src1*) para cada componente e grava o resultado em *dest*.

Se a comparação for verdadeira, 32-bit 0xFFFFFFFF será retornado para esse componente. Caso contrário, 32 bits 0x00000000 será retornado.

A comparação com NaN retorna false.

As máscaras de *destino* válidas são de um ou dois componentes. Isto é:. x,. y,. z,. w,. XY,. XZ,. XW,. yz,. YW,. zw o primeiro componente de *destino* na máscara recebe o resultado de 32 bits para a primeira comparação dupla. O segundo componente na máscara, se presente, recebe o resultado de 32 bits para a segunda comparação dupla.

O swizzles válido para os parâmetros de origem são. xyzw,. xyxy,. zwxy,. zwzw. Os seguintes mapeamentos *src* são swizzle:

-   *src0* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
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

 

 





