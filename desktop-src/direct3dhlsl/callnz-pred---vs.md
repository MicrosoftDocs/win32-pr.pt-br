---
title: callnz Pred – vs
description: Chame se não for zero, com um predicado. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo. Predicação usa um valor booliano para determinar se não deve executar a instrução.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1449ed9fb061ea2d5a83d37cb7c0d744a4c7e8b6517d49c0d2e32a10f7f5ed9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287020"
---
# <a name="callnz-pred---vs"></a>callnz Pred – vs

Chame se não for zero, com um predicado. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo. Predicação usa um valor booliano para determinar se não deve executar a instrução.

## <a name="syntax"></a>Sintaxe



| callnz l \# , \[ ! \] P0. w.x.y.|Iar|z|Mostrar |
|----------------------------------|



 

em que:

-   l \# é um [rótulo-vs](label---vs.md) marcando o início da sub-rotina a ser chamada.
-   \[!\] é um modificador opcional de negação.
-   P0 é o [registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} é o swizzle de replicação necessário em P0.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| callnz Pred            |      |      | x    | x     | x    | x     |



 

Essa instrução faz o seguinte:


```
if (specified register component is not zero)
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

 

 




