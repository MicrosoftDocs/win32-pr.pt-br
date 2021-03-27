---
title: vs_2_0
description: Um sombreador de vértice programável é composto de um conjunto de instruções que operam em dados de vértice. Registra dados de transferência dentro e fora da ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce4e986e610ff95716cd6899d6167e4f69efe042
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104967049"
---
# <a name="vs_2_0"></a>vs \_ 2 \_ 0

Um sombreador de vértice programável é composto de um conjunto de instruções que operam em dados de vértice. Registra dados de transferência dentro e fora da ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.

-   [Instruções-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contém uma lista das instruções disponíveis.
-   [Registros-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lista os diferentes tipos de registros usados pela alu do sombreador de vértice.
-   Os [modificadores de registro do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers.md) são usados para modificar a maneira como uma instrução funciona.
-   [Modificadores de registro de origem do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alteram os dados de registro de origem antes da execução da instrução.
-   [O Swizzling de registro de origem](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.
-   O [mascaramento do registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quais componentes do registro de destino são gravados.

## <a name="instruction-count"></a>Contagem de instruções

Cada sombreador de vértice pode ter até 256 instruções armazenadas. O número de instruções executadas pode ser muito maior (devido ao suporte de loop/Rep) e é limitado por D3DCAPS9. MaxVShaderInstructionsExecuted, que deve ser pelo menos 0xFFFF.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de vértice](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




