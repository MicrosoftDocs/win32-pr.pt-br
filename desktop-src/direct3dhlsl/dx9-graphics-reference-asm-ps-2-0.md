---
title: ps_2_0
description: Saiba mais ps_2_0, um sombreador de pixel programável, que é feito de um conjunto de instruções que operam em dados de pixel.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a2433c8490af06d23d8dccef676ec206fdbb88c0
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010979"
---
# <a name="ps_2_0"></a>ps \_ 2 \_ 0

Um sombreador de pixel programável é feito de um conjunto de instruções que operam em dados de pixel. Registra dados de transferência dentro e fora do ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.

-   [ps \_ 2 \_ 0 Instruções](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contém uma lista das instruções disponíveis.
-   [ps \_ 2 \_ 0 Registra lista](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) os diferentes tipos de registros usados pelo ALU do sombreador de vértice.
-   [Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) São usados para modificar a maneira como uma instrução funciona.
-   [A Máscara de Gravação do Registro de](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) Destino determina quais componentes do registro de destino são gravados.
-   [Modificadores de Registro de Origem do Sombreador de Pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alteram os dados do registro de origem antes da instrução ser executado.
-   [O Swizzling do Registro de Origem](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.

## <a name="instruction-count"></a>Contagem de instruções

Os sombreadores têm restrições para contagens máximas de instruções. Total de slots de instrução: 96 (aritmética de 64 e 32 textura).

## <a name="sampler-count"></a>Contagem de amostras

O número de amostras de textura disponíveis é 16.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de pixel](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




