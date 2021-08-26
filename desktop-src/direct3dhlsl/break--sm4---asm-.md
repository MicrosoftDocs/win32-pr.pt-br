---
title: break (sm4 – asm)
description: Move o ponto de execução para a instrução após o próximo endloop ou endswitch.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17ca99b0e16da016145f7f23fe6e4ce6bd410325ff98d4c6dd1387943fbc718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983336"
---
# <a name="break-sm4---asm"></a>break (sm4 – asm)

Move o ponto de execução para a instrução após o próximo [endloop](endloop--sm4---asm-.md) ou [endswitch](endswitch--sm4---asm-.md).



| break |
|-------|



 

## <a name="remarks"></a>Comentários

O formato do token contém o deslocamento da instrução **endloop** ou **endswitch** correspondente no Sombreador como uma conveniência.

O exemplo a seguir mostra a **instrução break.**


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



Essa instrução deve aparecer dentro de **um endloop** de loop ou, em um /  **caso,** em uma **opção** / **terminawitch**.

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

 

 




