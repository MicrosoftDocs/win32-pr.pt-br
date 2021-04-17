---
title: continuar (sm4-ASM)
description: Continua a execução no início do loop atual.
ms.assetid: 3F0021B2-50D1-407C-9EE4-1CB679E184BF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53b023e998fcf131a387fc009cfc8cb133ff6a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988579"
---
# <a name="continue-sm4---asm"></a>continuar (sm4-ASM)

Continua a execução no início do loop atual.



| continue |
|----------|



 

## <a name="remarks"></a>Comentários

**continue** pode ser usado somente dentro de um [loop](loop--sm4---asm-.md) ou [ENDLOOP](endloop--sm4---asm-.md).

O exemplo a seguir mostra como usar a instrução **continue** .


```
                loop
                    if_na r0.x
                        break
                    endif
                    if_z r1.x
                        ...
                        continue
                    endif
                    ...
                endloop
```



O formato do token contém o deslocamento da instrução de loop correspondente no sombreador como uma conveniência.

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

 

 




