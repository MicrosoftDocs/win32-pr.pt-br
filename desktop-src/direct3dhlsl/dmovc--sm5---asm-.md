---
title: dmovc (sm5 – asm)
description: Movimentação condicional por componente. | dmovc (sm5 – asm)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc0ed15d81a91d8a93ce99eda3fa17b91900e0045301f1c5b5d1f56e4448954a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792377"
---
# <a name="dmovc-sm5---asm"></a>dmovc (sm5 – asm)

Movimentação condicional por componente.



| dmovc \[ \_ sat \] dest \[ \] .mask, src0 \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle, \] \[ - \] src2 \[ \_ abs \] \[ .swizzle, \] |
|-----------------------------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O destino de movimentação.<br/> Se *src0*, *dest*  =  *src1* else *dest*  =  *src2*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] Os componentes para testar a condição.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[em \] Os componentes a mover se a condição for verdadeira.<br/>                                       |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[em \] Os componentes a mover se a condição for false.<br/>                                      |



 

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

As máscaras válidas para dest são .xy, .zw, .xyzw.

Os swizzles válidos para *src0* são qualquer coisa. Os dois primeiros componentes pós-swizzle são usados para identificar dois valores de condição de 32 bits.

Os swizzles válidos para *src1* e *src2* que contêm doubles são .xyzw, .xyxy, .zwxy, .zwzw. são .xy, .zw e .xyzw.

Os seguintes *mapeamentos de src* abaixo são pós-swizzle:

-   *dest* é um vec2 duplo em (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src0* é um vec2 de 32bits/componente em x e y (zw ignorado).
-   *src1* é um vec2 duplo em (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src2* é um vec2 duplo em (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

Os modificadores em *src1* e *src2*, além do swizzle, supõem que os dados são duplos. A ausência de modificadores move dados sem alterar bits.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





