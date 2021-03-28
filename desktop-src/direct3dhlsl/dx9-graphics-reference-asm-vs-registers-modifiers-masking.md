---
title: Máscara de registro de destino
description: O mascaramento especifica quais componentes do registro de destino serão atualizados com o resultado de uma instrução. Os registros de textura têm um conjunto de regras e os registros de não-textura têm outro conjunto de regras.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364211"
---
# <a name="destination-register-masking"></a>Máscara de registro de destino

O mascaramento especifica quais componentes do registro de destino serão atualizados com o resultado de uma instrução. Os registros de textura têm um conjunto de regras e os registros de não-textura têm outro conjunto de regras.

-   referência de gráficos do DX9 \_ \_ \_ ASM \_ vs \_ registra \_ \_ mascaramento de modificadores – esta seção contém regras para aplicar máscaras aos registros de destino.
-   \_ \_ Máscaras de registro de textura – os registros de textura têm algumas regras exclusivas.

## <a name="destination-register-masking"></a>Máscara de registro de destino

Conforme mostrado na tabela a seguir, o mascaramento (em que é um dos registros válidos do [sombreador](dx9-graphics-reference-asm-vs-registers.md)de vértices do sombreador de vértice) pode ser aplicado aos componentes individuais dos dados de vetor.



| Modificador de componente | Description      |
|--------------------|------------------|
| r. {x} {y} {z} {w}     | Máscara de destino |



 

-   Em geral, especificar máscaras de gravação de registro de destino é um bom estilo de codificação. Torna o código mais fácil de ler e manter.
-   Qualquer combinação de componentes pode ser especificada (incluindo nenhum), desde que x preceda y, y preceda z e z preceda w.
-   Os registros de saída de oFog e de entrada devem usar apenas uma máscara.
-   Algumas instruções exigem que o registro de destino use uma única máscara de gravação: exp, expp, log, LogP, pow, RCP e RSQ.
-   Na versão 1,0, a instrução FRC exigia uma das seguintes combinações de máscara:. x ou. y ou. XY. A versão 2,0 não tem restrição de máscara.
-   Sincos requer uma das seguintes combinações de máscara:. x ou. y ou. xyz.
-   M3X2 requer a máscara de gravação. XY.
-   m3x3 e m4x3 exigem a máscara de gravação. xyz.
-   M3x4 e m4x4 exigem a máscara de gravação. xyz ou a xyzw (máscara de gravação padrão).

## <a name="texture-register-masks"></a>Máscaras de registro de textura

As regras de validação para usar modificadores em registros de coordenadas de textura são mais rígidas do que as regras de validação para outros registros.

-   Se oTn for gravado, todos os registros anteriores (oTn-1 ~ oT0) também precisarão ser escritos.
-   A máscara de gravação "combinada" para qualquer \# registro de OT deve ser exatamente uma das seguintes:
    -   . x
    -   . XY
    -   . xyz
    -   . xyzw (que é equivalente a não usar nenhum modificador de componente)

Por exemplo, um sombreador de vértice pode gerar uma saída para os registros de textura em instruções separadas.


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



Ou, as instruções podem ser combinadas.


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



Essas restrições se aplicam somente aos registros de coordenadas de textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




