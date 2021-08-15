---
title: callnz bool - ps
description: Chame se não for zero. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo. | callnz bool - ps
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
# <a name="callnz-bool---ps"></a>callnz bool - ps

Chame se não for zero. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] B\# |
|----------------------|



 

Em que:

-   l \# é um rótulo – [ps](label---ps.md) marcando o início da sub-rotina a ser chamada.
-   \[!\] é um modificador de negação opcional.
-   b \# identifica um Registro [Booliana Constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz bool           |      |      |      |      |      | x    | x     | x    | x     |



 

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

 

 




