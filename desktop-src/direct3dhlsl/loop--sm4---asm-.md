---
title: loop (sm4-ASM)
description: Especifica um loop que itera até que uma instrução break seja encontrada.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dfc3090e71c1101e2c2748924de24f5443363ede76b86130cf63c3a319c76ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043764"
---
# <a name="loop-sm4---asm"></a>loop (sm4-ASM)

Especifica um loop que itera até que uma instrução break seja encontrada.



| loop |
|------|



 

## <a name="remarks"></a>Comentários

o **loop** pode iterar indefinidamente, embora a execução geral do sombreador possa ser forçada a terminar depois que um número de instruções for executado.

Flow blocos de controle podem ser aninhados até 64 de profundidade por sub-rotina e principal. O compilador HLSL não gerará sub-rotinas que excedam esse limite. O comportamento das instruções de fluxo de controle além de 64 níveis de profundidade por sub-rotina é indefinido.

O formato do token contém o deslocamento da instrução [ENDLOOP](endloop--sm4---asm-.md) correspondente no sombreador como uma conveniência.

O exemplo a seguir mostra como usar a instrução loop.

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

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

 

 




