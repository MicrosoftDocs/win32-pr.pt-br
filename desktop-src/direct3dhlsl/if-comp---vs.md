---
title: if_comp-vs
description: Inicie um If bool-vs... else-vs... endif-vs Block, com uma condição baseada em valores que poderiam ser computados em um sombreador. Essa instrução é usada para ignorar um bloco de código, com base em uma condição.
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadbe9620367efc75f821a711de89eb3498d247f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988553"
---
# <a name="if_comp---vs"></a>Se \_ comp-vs

Inicie um [If bool-vs](if-bool---vs.md)... [else-vs](else---vs.md)... [endif-vs](endif---vs.md) Block, com uma condição baseada em valores que poderiam ser computados em um sombreador. Essa instrução é usada para ignorar um bloco de código, com base em uma condição.

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



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Se \_ comp               |      |      | x    | x     | x    | x     |



 

Essa instrução é usada para ignorar um bloco de código, com base em uma condição.


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



Tenha cuidado ao usar os modos de comparação Equals e not Equals em números de ponto flutuante. Como o arredondamento ocorre durante cálculos de ponto flutuante, a comparação pode ser feita em relação a um valor de Épsilon (número pequeno de zeros) para evitar erros.

As restrições incluem:

-   Se \_ comp... [else-vs](else---vs.md)... [endif – blocos vs](endif---vs.md) (juntamente com os blocos predicados If) podem ser aninhados até 24 camadas de profundidade.
-   os registros src0 e src1 exigem uma swizzle replicate.
-   Se os \_ blocos de comp precisarem terminar com uma instrução [else-vs](else---vs.md) ou [endif-vs](endif---vs.md) .
-   Se \_ comp... [else-vs](else---vs.md)... [endif – blocos vs](endif---vs.md) não podem ampliar um bloco de loop. O \_ bloco If comp deve estar completamente dentro ou fora do bloco [loop vs](loop---vs.md) .

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

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




