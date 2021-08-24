---
title: ret (sm4 – asm)
description: Instrução return.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7482c2c7351944824e2590f5c87dac63bde8f639a5ad42dffdfc71e4134603b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853746"
---
# <a name="ret-sm4---asm"></a>ret (sm4 – asm)

Instrução return.



| Ret |
|-----|



 

## <a name="remarks"></a>Comentários

Se estiver dentro de uma sub-rotina, retorne à instrução após a chamada. Se não estiver dentro de uma sub-rotina, encente a execução do programa.

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

-   **ret** pode aparecer em qualquer lugar em um programa, qualquer número de vezes.
-   Se uma [instrução](label--sm4---asm-.md) de rótulo aparecer em um Sombreador, ela deverá ser precedida por um comando **ret** que não esteja aninhado em nenhuma instrução de controle de fluxo.
-   Se houver sub-rotinas em um Sombreador, a última instrução no sombreador deverá ser **um ret**.

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

 

 




