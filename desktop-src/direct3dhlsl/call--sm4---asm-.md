---
title: call (sm4 – asm)
description: Chama uma sub-rotina marcada pelo local em que o rótulo l\ aparece no programa.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c55ce1c0005014928c006e29c9d7d08c3cadc3d11fee870ea1c9fa39df514fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516649"
---
# <a name="call-sm4---asm"></a>call (sm4 – asm)

Chama uma sub-rotina marcada por onde o **rótulo l \#** aparece no programa.



| call l\# |
|----------|



 



| Item                                                       | Descrição                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span id="l_"></span><span id="L_"></span>*L\#*<br/> | \[em \] O rótulo da sub-rotina.<br/> |



 

## <a name="remarks"></a>Comentários

Quando um [ret](ret--sm4---asm-.md) for encontrado, retorne a execução para a instrução após essa chamada.

O formato do token contém o deslocamento do rótulo correspondente no Sombreador como uma conveniência.

O exemplo a seguir mostra a instrução de chamada.


```
                ...
                call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret
```



### <a name="restrictions"></a>Restrições

-   Sub-rotinas podem aninhar 32 profundidades.
-   A pilha de endereços de retorno é gerenciada de forma transparente pela implementação.
-   Se já houver 32 entradas na pilha de endereços de retorno e uma chamada for emitida, **a** chamada será ignorada.
-   Não há nenhuma pilha de parâmetros automática. O aplicativo pode usar uma matriz de registro temporário indexável (x \# \[ \] ) para implementar manualmente uma pilha. No entanto, os endereços de retorno de chamada de sub-rotina não são visíveis e são ortogonais para qualquer gerenciamento de pilha manual feito pelo aplicativo.
-   A indexação do *parâmetro l \#* não é permitida.
-   A recursão não é permitida.

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

 

 





