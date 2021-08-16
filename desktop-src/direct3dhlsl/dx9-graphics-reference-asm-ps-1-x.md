---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: O assembler de sombreador de pixel é feito de um conjunto de instruções que operam em dados de pixel contidos em registros.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e10e4eee48490e7ae998e39d71265aef74339c1979112e2fcf0e47e5b07cda7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512937"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a>ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4

O assembler de sombreador de pixel é feito de um conjunto de instruções que operam em dados de pixel contidos em registros. As operações são expressas como instruções compostas por um operador e um ou mais operadores. As instruções usam registros para transferir dados dentro e fora do ALU do sombreador de pixel. Registros também podem ser usados por algumas instruções para manter resultados temporários.

> [!Note]  
> O suporte a HLSL para o sombreador de pixel 1.x foi preterido.

 

## <a name="instructions"></a>Instruções

Há duas categorias principais de instruções de sombreador de pixel: instruções aritméticas e instruções de endereçamento de textura. Instruções aritméticas modificam dados de cor. As operações de endereçamento de textura processam dados de coordenadas de textura e, na maioria dos casos, amostram uma textura. As instruções do sombreador de pixel são executados por pixel; ou seja, eles não têm conhecimento de outros pixels no pipeline.

As instruções de endereçamento de textura consomem um slot, mas as instruções aritméticas podem ser emparelhadas para habilitar os componentes de cor (RGB) e uma instrução de componente alfa em um único slot.

[ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ \_ 1 3, ps \_ 1 \_ 4 Instruções](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contém uma lista das instruções disponíveis.

Quando a multisampling está habilitada, os sombreadores de pixel são executados apenas uma vez por pixel, não uma vez para cada subpixel. A multisampling aumenta apenas a resolução de bordas de polígono, bem como testes de profundidade e estêncil. Por exemplo, se a multisampling 3x3 estiver habilitada e um triângulo que está sendo rasterizado for encontrado para abranger cinco dos nove subpixels para um pixel específico, o sombreador de pixel será executado uma vez e o mesmo resultado de cor será aplicado a todos os cinco subpixels.

## <a name="registers"></a>Registros

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ \_ 1 4 Registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) lista os diferentes registros usados pelo sombreador ALU.

## <a name="modifiers"></a>Modificadores

[Os modificadores para ps \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) podem ser usados para alterar a funcionalidade de uma instrução ou os dados lidos ou gravados em um registro.

O Direct3D 9 requer cálculos intermediários para manter pelo menos a precisão de 8 bits para todos os formatos de superfície. Recomendamos precisão mais alta (12 bits) para matemática em estágio e saturação para 8 bits entre estágios de textura. Não há suporte para modos de arredondamento modificáveis ou exceções. A multiplicação deve ter suporte com uma precisão de arredondamento para a mais próxima para manter a perda de precisão no mínimo.

## <a name="sampler-count"></a>Contagem de amostras

O número de amostras de textura disponíveis é:

-   Para ps \_ 1 \_ 0 – ps \_ 1 \_ 3, o máximo é 4.
-   Para ps \_ 1 \_ 4, o máximo é 6.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de pixel](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




