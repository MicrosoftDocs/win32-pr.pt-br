---
title: callnz bool-vs
description: Chamar se não for zero. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo. | callnz bool-vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3932f4c5d50445b3220a0460a5c434a1ff8aae4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989258"
---
# <a name="callnz-bool---vs"></a>callnz bool-vs

Chamar se não for zero. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] b\# |
|----------------------|



 

em que:

-   Onde l \# é um [rótulo-vs](label---vs.md) marcando o início da sub-rotina a ser chamada.
-   \[!\] é o modificador booliano NOT opcional.
-   b \# identifica um [registro booliano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| bool callnz            |      | x    | x    | x     | x    | x     |



 

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

 

 




