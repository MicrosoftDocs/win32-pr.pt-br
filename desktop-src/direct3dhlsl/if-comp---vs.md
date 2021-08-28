---
title: if_comp - vs
description: Iniciar um se bool - vs... else - vs... endif - vs bloco, com uma condição baseada em valores que podem ser computados em um sombreador. Essa instrução é usada para ignorar um bloco de código, com base em uma condição.
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 11c7abceb9b484c4cd104e136c47edeb55b93b5273f953cb6d98052e247513d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743576"
---
# <a name="if_comp---vs"></a>if \_ comp - vs

Iniciar um [se bool - vs](if-bool---vs.md)... [else - vs](else---vs.md)... [endif - vs](endif---vs.md) bloco, com uma condição baseada em valores que podem ser computados em um sombreador. Essa instrução é usada para ignorar um bloco de código, com base em uma condição.

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



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| se \_ comp               |      |      | x    | x     | x    | x     |



 

Essa instrução é usada para ignorar um bloco de código, com base em uma condição.


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



Tenha cuidado ao usar os modos de comparação iguais e não iguais em números de ponto flutuante. Como o arredondamento ocorre durante cálculos de ponto flutuante, a comparação pode ser feita em relação a um valor de epsilon (pequeno número não zero) para evitar erros.

As restrições incluem:

-   se \_ comp... [else - vs](else---vs.md)... [endif – blocos vs](endif---vs.md) (juntamente com os blocos if predicados) podem ser aninhados até 24 camadas de profundidade.
-   Os registros src0 e src1 exigem um swizzle de replicação.
-   se \_ blocos comp devem terminar com uma [instrução else - vs](else---vs.md) ou [endif - vs.](endif---vs.md)
-   se \_ comp... [else - vs](else---vs.md)... [endif – os blocos vs](endif---vs.md) não podem interferir em um bloco de loop. O bloco \_ se comp deve estar completamente dentro ou fora do loop - [vs](loop---vs.md) bloco.

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

 

 




