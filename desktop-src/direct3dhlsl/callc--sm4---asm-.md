---
title: callc (sm4 – asm)
description: Chama condicionalmente uma sub-rotina marcada pelo local em que o rótulo l\ aparece no programa.
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcb751b57a09704a2fec7a9c3afb69362873e3a1d2b43091efd984f67623188a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727156"
---
# <a name="callc-sm4---asm"></a>callc (sm4 – asm)

Chama condicionalmente uma sub-rotina marcada por onde o **rótulo l \#** aparece no programa.



| callc{ \_ z\|\_Componente nz} src0.select, \_ l\# |
|----------------------------------------------|



 



| Item                                                            | Descrição                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] componente no qual testar a condição.<br/> |
| <span id="l_"></span><span id="L_"></span>*L\#*<br/>      | \[em \] O rótulo da sub-rotina.<br/>                  |



 

## <a name="remarks"></a>Comentários

Quando um [ret](ret--sm4---asm-.md) for encontrado, retorne a execução para a instrução após essa chamada.

O formato do token contém o deslocamento do rótulo correspondente no Sombreador como uma conveniência.

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

-   Sub-rotinas podem aninhar 32 profundidades.
-   A pilha de endereços de retorno é gerenciada de forma transparente pela implementação.
-   Se já houver 32 entradas na pilha de endereços de retorno e uma chamada for emitida, **a** chamada será ignorada.
-   Não há nenhuma pilha de parâmetros automática. O aplicativo pode usar uma matriz de registro temporário indexável (x \# \[ \] ) para implementar manualmente uma pilha. No entanto, os endereços de retorno de chamada de sub-rotina não são visíveis e são ortogonais para qualquer gerenciamento de pilha manual feito pelo aplicativo.
-   A indexação do *parâmetro l \#* não é permitida.
-   O registro de 32 bits fornecido pelo *src0* é testado em um nível de bit. Se qualquer bit for diferente de zero, **callc \_ nz** executará a chamada. Se todos os bits são zero, **callc \_ z** executará a chamada.
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

 

 





