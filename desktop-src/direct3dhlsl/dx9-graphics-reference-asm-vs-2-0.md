---
title: vs_2_0
description: Saiba mais vs_2_0, um sombreador de vértice programável, que é feito de um conjunto de instruções que operam em dados de vértice.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe951d62b869a303a0c07839b46840dc8f9fda00
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010849"
---
# <a name="vs_2_0"></a>vs \_ 2 \_ 0

Um sombreador de vértice programável é feito de um conjunto de instruções que operam em dados de vértice. Registra dados de transferência dentro e fora do ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.

-   [Instruções – vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contém uma lista das instruções disponíveis.
-   [Registros – vs \_ 2 \_ 0 lista](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) os diferentes tipos de registros usados pelo ALU do sombreador de vértice.
-   [Modificadores de registro de sombreador de](dx9-graphics-reference-asm-vs-registers-modifiers.md) vértice são usados para modificar a maneira como uma instrução funciona.
-   [Modificadores de Registro de Origem do Sombreador de Vértice](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alteram os dados de registro de origem antes da instrução ser executado.
-   [O Swizzling do Registro de Origem](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.
-   [O Mascaramento do Registro de](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) Destino determina quais componentes do registro de destino são gravados.

## <a name="instruction-count"></a>Contagem de instruções

Cada sombreador de vértice pode ter até 256 instruções armazenadas. O número de instruções executados pode ser muito maior (devido ao suporte de loop/rep) e é limitado por D3DCAPS9. MaxVShaderInstructionsExecuted, que deve ser pelo menos 0xFFFF.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de vértice](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




