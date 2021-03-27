---
title: movc (sm4-ASM)
description: Movimentação condicional de componente. | movc (sm4-ASM)
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91aa3116b7bc13102386c57c9b8c63d3534147a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989182"
---
# <a name="movc-sm4---asm"></a>movc (sm4-ASM)

Movimentação condicional de componente.



| movc \[ \_ SAT \] dest \[ . Mask \] , src0 \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . swizzle \] , |
|----------------------------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço do resultado da operação. <br/> Se *src0*, então *dest*  =  *src1* else   =  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes nos quais testar a condição.<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nos \] componentes a serem movidos. <br/>                                                                                     |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[nos \] componentes a serem movidos.<br/>                                                                                      |



 

## <a name="remarks"></a>Comentários

O exemplo a seguir mostra como usar essa instrução.

``` syntax
                for each component in dest[.mask]
                    if the corresponding component in src0 (POS-swizzle)
                       has any bit set
                    {
                        copy this component (POS-swizzle) from src1 into dest
                    }
                    else
                    {
                        copy this component (POS-swizzle) from src2 into dest
                    }
                endfor
```

Os modificadores em *src1* e *src2*, diferente de swizzle, assumem que os dados são de ponto flutuante. A ausência de modificadores apenas move dados sem alterar bits.

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

 

 





