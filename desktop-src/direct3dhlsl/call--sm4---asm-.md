---
title: chamada (sm4-ASM)
description: Chama uma sub-rotina marcada por onde o rótulo l \ aparece no programa.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dac86fa52140968443f01050cebc57718fea420
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638868"
---
# <a name="call-sm4---asm"></a>chamada (sm4-ASM)

Chama uma sub-rotina marcada por onde o rótulo **l \#** aparece no programa.



| chamar l\# |
|----------|



 



| Item                                                       | Descrição                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span id="l_"></span><span id="L_"></span>*debug\#*<br/> | \[no \] rótulo da sub-rotina.<br/> |



 

## <a name="remarks"></a>Comentários

Quando uma [RET](ret--sm4---asm-.md) é encontrada, retorna a execução para a instrução após essa chamada.

O formato do token contém o deslocamento do rótulo correspondente no sombreador como uma conveniência.

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

-   As sub-rotinas podem aninhar 32 de profundidade.
-   A pilha de endereços de retorno é gerenciada de forma transparente pela implementação.
-   Se já houver entradas 32 na pilha de endereços de retorno e uma **chamada** for emitida, a chamada será ignorada.
-   Não há nenhuma pilha de parâmetros automática. O aplicativo pode usar uma matriz de registro temporário indexável (x \# \[ \] ) para implementar manualmente uma pilha. No entanto, os endereços de retorno da chamada de sub-rotina não são visíveis e são ortogonal a qualquer gerenciamento de pilha manual feito pelo aplicativo.
-   A indexação do *parâmetro \# l* não é permitida.
-   Recursão não é permitida.

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

 

 





