---
title: ps_2_0
description: Um sombreador de pixel programável é composto de um conjunto de instruções que operam em dados de pixel. Registra dados de transferência dentro e fora da ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98b0f252d87a1f7e08c3531415d7ebcb93d4f6f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104966989"
---
# <a name="ps_2_0"></a>PS \_ 2 \_ 0

Um sombreador de pixel programável é composto de um conjunto de instruções que operam em dados de pixel. Registra dados de transferência dentro e fora da ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.

-   [as \_ instruções do PS 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contêm uma lista das instruções disponíveis.
-   [os \_ registros PS 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lista os diferentes tipos de registros usados pela alu do sombreador de vértice.
-   [Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) São usados para modificar a maneira como uma instrução funciona.
-   A [máscara de gravação do registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quais componentes do registro de destino são gravados.
-   [Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alteram os dados de registro de origem antes da execução da instrução.
-   [O Swizzling de registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.

## <a name="instruction-count"></a>Contagem de instruções

Os sombreadores têm restrições para contagens de instrução máximas. Slots de instrução total: 96 (64 aritmética e 32 Texture).

## <a name="sampler-count"></a>Contagem de amostras

O número de amostragens de textura disponíveis é 16.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de pixel](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




