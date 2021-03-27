---
title: break_comp-vs
description: Interromper condicionalmente o loop atual no ENDLOOP-vs ou endrep-vs mais próximo.
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823450"
---
# <a name="break_comp---vs"></a>interromper \_ comp-vs

Interromper condicionalmente o loop atual no [ENDLOOP-vs](endloop---vs.md) ou [endrep-vs](endrep---vs.md)mais próximo.

## <a name="syntax"></a>Syntax



| \_src0 de quebra de comp, src1 |
|------------------------|



 

Em que:

-   \_comp é uma comparação entre os dois registros de origem. Pode ser um dos seguintes: 

    | Syntax | Comparação            |
    |--------|-----------------------|
    | \_gt   | Maior que          |
    | \_lt   | Menor que             |
    | \_GE   | Maior ou igual |
    | \_quivo   | Inferior ou igual    |
    | \_EQ   | Igual a              |
    | \_m   | Não igual a          |

    

     

-   src0 é um registro de origem. Replicate swizzle é necessário para selecionar um único componente.
-   src1 é um registro de origem. Replicate swizzle é necessário para selecionar um único componente.

## <a name="remarks"></a>Comentários

Essa instrução tem suporte nas versões a seguir.



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| interromper \_ comp            |      |      | x    | x     | x    | x     |



 

Quando a comparação for verdadeira, ela será interrompida no loop atual, conforme mostrado.


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




