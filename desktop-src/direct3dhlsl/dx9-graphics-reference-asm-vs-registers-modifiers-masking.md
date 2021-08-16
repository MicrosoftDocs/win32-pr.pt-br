---
title: Mascaramento do Registro de Destino
description: Mascaramento especifica quais componentes do registro de destino serão atualizados com o resultado de uma instrução. Os registros de textura têm um conjunto de regras e registros sem texto têm outro conjunto de regras.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1a8d45e847f7da785bd09b83e778d140cee68007add882066b508b38043550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119680"
---
# <a name="destination-register-masking"></a>Mascaramento do Registro de Destino

Mascaramento especifica quais componentes do registro de destino serão atualizados com o resultado de uma instrução. Os registros de textura têm um conjunto de regras e registros sem texto têm outro conjunto de regras.

-   Dx9 \_ graphics \_ reference \_ asm vs \_ \_ registers modifiers masking \_ - Esta seção contém regras para aplicar \_ máscaras a registros de destino.
-   Máscaras \_ de Registro de Textura – os registros de textura têm algumas regras \_ exclusivas.

## <a name="destination-register-masking"></a>Mascaramento do Registro de Destino

Conforme mostrado na tabela a seguir, o mascaramento (em que é um dos registros válidos do sombreador de vértice) pode ser aplicado aos [componentes individuais](dx9-graphics-reference-asm-vs-registers.md)dos dados vetoriais.



| Modificador de componente | Descrição      |
|--------------------|------------------|
| r.{x}{y}{z}{w}     | Máscara de destino |



 

-   Em geral, especificar máscaras de gravação de registro de destino é um bom estilo de codificação. Ele facilita a leitura e a manutenção do código.
-   Qualquer combinação de componentes pode ser especificada (incluindo nenhum), desde que x precede y, y precede z e z precede w.
-   Os registros de saída oPts e oFog devem usar apenas uma máscara.
-   Determinadas instruções exigem que o registro de destino use uma única máscara de gravação: exp, expp, log, logp, pow, rcp e rsq.
-   Na versão 1.0, a instrução frc exigia uma das seguintes combinações de máscara: .x ou .y ou .xy. A versão 2.0 não tem restrição de máscara.
-   Sincos requer uma das seguintes combinações de máscara: .x ou .y ou .xyz.
-   m3x2 requer a máscara de gravação .xy.
-   M3x3 e m4x3 exigem a máscara de gravação .xyz.
-   m3x4 e m4x4 exigem a máscara de gravação .xyz ou a máscara de gravação padrão (xyzw).

## <a name="texture-register-masks"></a>Máscaras de registro de textura

As regras de validação para usar modificadores em registros de coordenadas de textura são mais rígidas do que as regras de validação para outros registros.

-   Se oTn for gravado, todos os registros anteriores (oTn-1 ~ oT0) também deverão ser gravados.
-   A máscara de gravação "combinada" para qualquer registro oT \# deve ser exatamente uma das seguintes:
    -   .x
    -   .xy
    -   .xyz
    -   .xyzw (que é equivalente a não usar nenhum modificador de componente)

Por exemplo, um sombreador de vértice pode ser produzido para registros de textura em instruções separadas.


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



Ou então, as instruções podem ser combinadas.


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

 

 




