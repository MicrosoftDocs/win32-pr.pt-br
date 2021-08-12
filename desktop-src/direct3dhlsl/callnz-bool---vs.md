---
title: callnz bool – vs
description: Chame se não for zero. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo. | callnz bool – vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a6d5a7646670d182b0b685ab742fb5b2094a89a717a31019165054bcbc4816b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287254"
---
# <a name="callnz-bool---vs"></a>callnz bool – vs

Chame se não for zero. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo.

## <a name="syntax"></a>Sintaxe



| callnz l \# , \[ ! \] B\# |
|----------------------|



 

em que:

-   em que l \# é um rótulo – [vs](label---vs.md) marcando o início da sub-rotina a ser chamada.
-   \[!\] é o modificador NOT booliana opcional.
-   b \# identifica um Registro [Booliana Constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| callnz bool            |      | x    | x    | x     | x    | x     |



 

Essa instrução faz o seguinte:


```
if (specified boolean register is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



Essa instrução consome um slot de instrução do sombreador de vértice.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




