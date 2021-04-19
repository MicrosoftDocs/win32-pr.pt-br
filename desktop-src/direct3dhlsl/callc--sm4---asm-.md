---
title: callc (sm4-ASM)
description: Chama condicionalmente uma sub-rotina marcada por onde o rótulo l \ aparece no programa.
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6bc8c9d1e4a99ce25f99253518482181cdb74d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988581"
---
# <a name="callc-sm4---asm"></a>callc (sm4-ASM)

Chama condicionalmente uma sub-rotina marcada por onde o rótulo **l \#** aparece no programa.



| callc { \_ z \|\_NZ} src0. Select \_ componente, l\# |
|----------------------------------------------|



 



| Item                                                            | Descrição                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] componente no qual testar a condição.<br/> |
| <span id="l_"></span><span id="L_"></span>*debug\#*<br/>      | \[no \] rótulo da sub-rotina.<br/>                  |



 

## <a name="remarks"></a>Comentários

Quando uma [RET](ret--sm4---asm-.md) é encontrada, retorna a execução para a instrução após essa chamada.

O formato do token contém o deslocamento do rótulo correspondente no sombreador como uma conveniência.

O exemplo a seguir mostra a instrução de chamada.


```
                ...
                callc_z  r1.y, l3 // if all bits in r0.x are 0, call l3
                callc_nz r2.z, l3 // if any bit in r0.x is nonzero, call l3
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
-   O registro de 32 bits fornecido pelo *src0* é testado em um nível de bit. Se algum bit for diferente de zero, **callc \_ NZ** executará a chamada. Se todos os bits forem zero, o **callc \_ z** executará a chamada.
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

 

 





