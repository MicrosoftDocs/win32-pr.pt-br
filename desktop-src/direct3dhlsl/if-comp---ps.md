---
title: if_comp-PS
description: Inicie um If bool-PS... else-PS... endif-PS Block, com uma condição baseada em valores que poderiam ser computados em um sombreador. Essa instrução é usada para ignorar um bloco de código, com base em uma condição.
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638852"
---
# <a name="if_comp---ps"></a>Se \_ comp-PS

Inicie um [If bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... [endif-PS](endif---ps.md) Block, com uma condição baseada em valores que poderiam ser computados em um sombreador. Essa instrução é usada para ignorar um bloco de código, com base em uma condição.

## <a name="syntax"></a>Syntax



| Se \_ comp src0, src1 |
|---------------------|



 

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

    

     

-   src0 é um registro de origem. Replicate swizzle é necessário para selecionar um componente.
-   src1 é um registro de origem. Replicate swizzle é necessário para selecionar um componente.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Se \_ comp              |      |      |      |      |      | x    | x     | x    | x     |



 

Essa instrução é usada para ignorar um bloco de código, com base em uma condição.


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



Tenha cuidado ao usar os modos de comparação Equals e not Equals em números de ponto flutuante. Como o arredondamento ocorre durante cálculos de ponto flutuante, a comparação pode ser feita em relação a um valor de Épsilon (número pequeno de zeros) para evitar erros.

As restrições incluem:

-   Se \_ comp... [else-PS](else---ps.md)... [endif-](endif---ps.md) os blocos PS (juntamente com os blocos predicados [If](if-bool---ps.md) ) podem ser aninhados até 24 camadas de profundidade.
-   os registros src0 e src1 exigem uma swizzle replicate.
-   Se os \_ blocos de comp precisarem terminar com uma instrução [else-vs](else---vs.md) ou [endif-vs](endif---vs.md) .
-   Se \_ comp... [else-PS](else---ps.md)... [endif-os blocos de PS](endif---ps.md) não podem ampliar um bloco de loop. O \_ bloco If comp deve estar completamente dentro ou fora do bloco loop.

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

 

 




