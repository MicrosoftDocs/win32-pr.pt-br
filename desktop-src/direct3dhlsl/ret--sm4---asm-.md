---
title: RET (sm4-ASM)
description: Instrução de retorno.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d834cd9f32d6e38f40666ab235f705c0fc80513f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638862"
---
# <a name="ret-sm4---asm"></a>RET (sm4-ASM)

Instrução de retorno.



| RET |
|-----|



 

## <a name="remarks"></a>Comentários

Se estiver dentro de uma sub-rotina, retorne à instrução após a chamada. Se não estiver dentro de uma sub-rotina, encerre a execução do programa.

O exemplo a seguir mostra como usar essa instrução.

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                ret
```

### <a name="restrictions"></a>Restrições

-   **RET** pode aparecer em qualquer lugar em um programa, várias vezes.
-   Se uma instrução de [rótulo](label--sm4---asm-.md) aparecer em um sombreador, ela deverá ser precedida por um comando **RET** que não esteja aninhado em nenhuma instrução de controle de fluxo.
-   Se houver sub-rotinas em um sombreador, a última instrução no sombreador deverá ser uma **RET**.

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

 

 




