---
description: As expressões são instruções matemáticas ou lógicas que são usadas no lado direito de um sinal de igual. Há muitos tipos de expressões.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Expressões (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa574069094853eb506f7a1b38cdb6cd4379d3b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757342"
---
# <a name="expressions-direct3d-9"></a>Expressões (Direct3D 9)

As expressões são instruções matemáticas ou lógicas que são usadas no lado direito de um sinal de igual. Há muitos tipos de expressões.

## <a name="expressions"></a>Expressões

1.  Referência de variável
    ```
    ( variable ) or<variable >
    ```

    

2.  Escalar numérico
    ```
    scalar 
    ```

    

3.  Expressão numérica

    ```
    ( numeric expression )
    ```

    

    Todas as expressões HLL numéricas padrão têm suporte aqui.

4.  Construtor
    ```
    type ( constructor arguments )
    ```

    

5.  Lista de inicializadores

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    Os escalares devem ser valores escalares literais.

    O número de inicializadores deve ser compatível com a variável (estado) no lado esquerdo do sinal de igual.

6.  Expressão OR

    ```
    token [ | token ... ]
    ```

    

    Os tokens devem ser compatíveis com a variável (estado) no lado esquerdo do sinal de igual.

    Os tokens não diferenciam maiúsculas de minúsculas.

7.  NULO

    ```
    NULL
    ```

    

    NULL só pode ser atribuído a um sombreador, amostra ou objeto de textura.

8.  Bloco de assembly

    ```
    asm { code }
    ```

    

    Os blocos de assembly do PS devem ser atribuídos ao estado PIXELSHADER.

    Os blocos de assembly do VS devem ser atribuídos ao estado VERTEXSHADER.

9.  Bloco de estado de amostra

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    Os blocos de estado de amostra são sequências de estado de estágio de amostra não indexado ou atribuições de textura.

    Os blocos de estado de amostra devem ser atribuídos ao estado de efeito de amostra.

10. Bloco de estado do estado de efeito

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    Os blocos de estado são sequências de estado geral. Os blocos de estado podem ser aninhados, mas não podem conter referências circulares.

    Os blocos de estado devem ser atribuídos ao estado de efeito STATEBLOCK.

11. HLSL compilar

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    O destino do sombreador de vértice vs \_ m \_ n indica a \_ versão do sombreador de vértice da versão D3DVS (m, n). O destino do pixel shader PS \_ m \_ n Target indica a \_ versão do sombreador de pixel da versão D3DPS (m, n).

    As expressões de compilação de linguagem de alto nível do sombreador de vértice só podem ser atribuídas ao estado de efeito VERTEXSHADER. As expressões de compilação de linguagem de alto nível do sombreador de pixel só podem ser atribuídas ao estado de efeito PIXELSHADER.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato do efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



