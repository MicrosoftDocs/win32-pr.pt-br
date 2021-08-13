---
title: break_comp-PS
description: Interromper o loop atual no ENDLOOP-PS ou endrep-PS mais próximo, com base em uma comparação por componente.
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fa79b7aa50bc734ddc1f9fb1fd54e4130c48518dd47ed429b4177b8fb867d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794449"
---
# <a name="break_comp---ps"></a>interromper \_ comp-PS

Interromper o loop atual no [ENDLOOP-PS](endloop---ps.md) ou [endrep-PS](endrep---ps.md)mais próximo, com base em uma comparação por componente.

## <a name="syntax"></a>Sintaxe



| \_src0 de quebra de comp, src1 |
|------------------------|



 

Em que:

-   \_comp é uma comparação escalar (ou única) entre os dois registros de origem. Pode ser um dos seguintes: 

    | Sintaxe | Comparação            |
    |--------|-----------------------|
    | \_gt   | Maior que          |
    | \_lt   | Menor que             |
    | \_GE   | Maior ou igual |
    | \_quivo   | Inferior ou igual    |
    | \_EQ   | Igual a              |
    | \_m   | É diferente de          |

    

     

-   src0 é um registro de origem. Replicate swizzle será necessário se você selecionar um único componente.
-   src1 é um registro de origem. Replicate swizzle será necessário se você selecionar um único componente.

## <a name="remarks"></a>Comentários

Essa instrução tem suporte nas versões a seguir.



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| interromper \_ comp           |      |      |      |      |      | x    | x     | x    | x     |



 

Quando a comparação for verdadeira, ela será interrompida no loop atual, conforme mostrado.


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




