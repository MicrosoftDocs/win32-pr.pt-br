---
title: ps_1_1, ps_1_2, ps_1_3 ps_1_4
description: O Assembler do pixel shader é composto de um conjunto de instruções que operam em dados de pixel contidos em registros.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 761721a4de64e8a9168bcfea49ce7adf567ea7ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159280"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a>PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4

O Assembler do pixel shader é composto de um conjunto de instruções que operam em dados de pixel contidos em registros. As operações são expressas como instruções compostas de um operador e um ou mais operandos. As instruções usam registros para transferir dados para dentro e fora da ALU do sombreador de pixel. Os registros também podem ser usados por algumas instruções para manter resultados temporários.

> [!Note]  
> O suporte do HLSL para o pixel shader 1. x foi preterido.

 

## <a name="instructions"></a>Instruções

Há duas categorias principais de instruções de sombreador de pixel: instruções aritméticas e instruções de endereçamento de textura. As instruções aritméticas modificam os dados de cores. As operações de endereçamento de textura processam dados de coordenadas de textura e, na maioria dos casos, um exemplo de textura. As instruções do sombreador de pixel são executadas em uma base por pixel; ou seja, eles não têm nenhum conhecimento de outros pixels no pipeline.

As instruções de endereçamento de textura consomem um slot, mas as instruções aritméticas podem ser emparelhadas para habilitar os componentes de cor (RGB) e uma instrução de componente alfa em um único slot.

[as \_ instruções PS 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contêm uma lista das instruções disponíveis.

Quando a multiamostragem está habilitada, os sombreadores de pixel só são executados uma vez por pixel, não uma vez para cada subpixel. A multiamostração aumenta apenas a resolução das bordas do polígono, bem como os testes de profundidade e de estêncil. Por exemplo, se a multiamostragem 3x3 estiver habilitada e um triângulo sendo rasterizado for encontrado para cobrir cinco dos nove subpixels para um pixel específico, o sombreador de pixel será executado uma vez e o mesmo resultado de cor é aplicado a todos os cinco subpixels.

## <a name="registers"></a>Registros

[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) lista os diferentes registros usados pela alu do sombreador.

## <a name="modifiers"></a>Modificadores

Os [modificadores para PS \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) podem ser usados para alterar a funcionalidade de uma instrução ou os dados lidos ou gravados em um registro.

O Direct3D 9 requer cálculos intermediários para manter pelo menos a precisão de 8 bits para todos os formatos de superfície. É recomendável uma precisão mais alta (12 bits) para matemática em etapas e saturação para 8 bits entre estágios de textura. Não há suporte para modos ou exceções de arredondamento modificáveis. A multiplicação deve ser suportada com uma precisão de Round-to-mais próximo para manter o mínimo de perda de precisão.

## <a name="sampler-count"></a>Contagem de amostras

O número de amostragens de textura disponíveis é:

-   Para \_ o PS 1 \_ 0-PS \_ 1 \_ 3, o máximo é 4.
-   Para \_ o PS 1 \_ 4, o máximo é 6.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de pixel](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




