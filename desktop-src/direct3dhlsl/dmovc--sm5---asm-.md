---
title: dmovc (SM5-ASM)
description: Movimentação condicional de componente. | dmovc (SM5-ASM)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e364e6340733c42ae69412db726851329eb2809d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104370856"
---
# <a name="dmovc-sm5---asm"></a>dmovc (SM5-ASM)

Movimentação condicional de componente.



| dmovc \[ \_ SAT \] dest \[ . Mask \] , src0 \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . swizzle \] , |
|-----------------------------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] destino da movimentação.<br/> Se *src0*, então *dest*  =  *src1* else   =  *src2*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes para os quais testar a condição.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nos \] componentes a serem movidos, se a condição for verdadeira.<br/>                                       |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[nos \] componentes a serem movidos, se a condição for falsa.<br/>                                      |



 

## <a name="remarks"></a>Comentários

O exemplo a seguir mostra como usar essa instrução.

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

As máscaras válidas para dest são. XY,. zw,. xyzw.

O swizzles válido para *src0* é qualquer coisa. Os dois primeiros componentes swizzle são usados para facilitar valores de condição de 2 32 bits.

O swizzles válido para *src1* e *src2* contendo duplos são. xyzw,. xyxy,. zwxy,. zwzw. são. XY,. zw e. xyzw.

Os seguintes mapeamentos *src* abaixo são swizzle:

-   *dest* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src0* é um vec2 de 32 bits/componente entre x e y (ZW ignorado).
-   *src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src2* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

Os modificadores em *src1* e *src2*, diferente de swizzle, assumem que os dados são duplos. A ausência de modificadores move dados sem alterar bits.

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

 

 





