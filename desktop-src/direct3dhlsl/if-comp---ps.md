---
title: if_comp - ps
description: Inicie um se bool - ps... else - ps... endif – bloco ps, com uma condição com base em valores que podem ser computados em um sombreador. Essa instrução é usada para ignorar um bloco de código, com base em uma condição.
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5d0a2271dbd67902a039ddadf585611ed98fdb115f468c3962baa8cb46f48508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788966"
---
# <a name="if_comp---ps"></a>if \_ comp - ps

Inicie um [se bool - ps](if-bool---ps.md)... [else - ps](else---ps.md)... [endif – bloco ps,](endif---ps.md) com uma condição com base em valores que podem ser computados em um sombreador. Essa instrução é usada para ignorar um bloco de código, com base em uma condição.

## <a name="syntax"></a>Syntax



| se \_ comp src0, src1 |
|---------------------|



 

Em que:

-   \_comp é uma comparação entre os dois registros de origem. Pode ser um dos seguintes: 

    | Syntax | Comparação            |
    |--------|-----------------------|
    | \_Gt   | Maior que          |
    | \_Tenente   | Menor que             |
    | \_Ge   | Maior ou igual |
    | \_Le   | Inferior ou igual    |
    | \_Eq   | Igual a              |
    | \_Ne   | É diferente de          |

    

     

-   src0 é um registro de origem. Replicar swizzle é necessário para selecionar um componente.
-   src1 é um registro de origem. Replicar swizzle é necessário para selecionar um componente.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| se \_ comp              |      |      |      |      |      | x    | x     | x    | x     |



 

Essa instrução é usada para ignorar um bloco de código, com base em uma condição.


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



Tenha cuidado ao usar os modos de comparação iguais e não iguais em números de ponto flutuante. Como o arredondamento ocorre durante cálculos de ponto flutuante, a comparação pode ser feita em relação a um valor de epsilon (pequeno número não zero) para evitar erros.

As restrições incluem:

-   se \_ comp... [else - ps](else---ps.md)... [endif – blocos ps](endif---ps.md) (juntamente com os blocos [if](if-bool---ps.md) predicados) podem ser aninhados até 24 camadas de profundidade.
-   Os registros src0 e src1 exigem um swizzle de replicação.
-   se \_ blocos comp devem terminar com uma [instrução else - vs](else---vs.md) ou [endif - vs.](endif---vs.md)
-   se \_ comp... [else - ps](else---ps.md)... [endif – blocos ps](endif---ps.md) não podem montar um bloco de loop. O bloco \_ se comp deve estar completamente dentro ou fora do bloco de loop.

## <a name="example"></a>Exemplo

Essa instrução fornece controle de fluxo dinâmico condicional.


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




