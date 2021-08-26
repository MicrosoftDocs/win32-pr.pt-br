---
title: callnz Pred-PS
description: Chame com um predicado, se não for zero. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo. Predicação usa um valor booliano para determinar se não deve executar a instrução.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f56699a4853b7012401529ecfad6fbfb0006e21990a99a2fe5631faebd57674d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983286"
---
# <a name="callnz-pred---ps"></a>callnz Pred-PS

Chame com um predicado, se não for zero. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo. Predicação usa um valor booliano para determinar se não deve executar a instrução.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] P0. w.x.y.|Iar|z|Mostrar |
|----------------------------------|



 

Em que:

-   em que l \# é um [rótulo-PS](label---ps.md) marcando o início da sub-rotina a ser chamada.
-   \[!\] é um modificador opcional de negação.
-   P0 é o registro de predicado. Consulte [registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} é o swizzle de replicação necessário em P0.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz Pred           |      |      |      |      |      | x    | x     | x    | x     |



 

Essa instrução faz o seguinte:


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




