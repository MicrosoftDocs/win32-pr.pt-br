---
title: callnz bool-PS
description: Chamar se não for zero. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo. | callnz bool-PS
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 793feb1934b86b46f26050a67b5f26d94b9f277e31735c4d1912805374bab903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516619"
---
# <a name="callnz-bool---ps"></a>callnz bool-PS

Chamar se não for zero. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] b\# |
|----------------------|



 

Em que:

-   l \# é um [rótulo-PS](label---ps.md) marcando o início da sub-rotina a ser chamada.
-   \[!\] é um modificador opcional de negação.
-   b \# identifica um [registro booliano constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| bool callnz           |      |      |      |      |      | x    | x     | x    | x     |



 

Essa instrução faz o seguinte:


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




