---
description: As expressões são instruções matemáticas ou lógicas que são usadas no lado direito de um sinal de igual. Há muitos tipos de expressões.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Expressões (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daeffeb09a2c2f496f73d492581cb2b51ac2e518e176bbbc848889bef5716b25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985696"
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

    Os tokens não são sensíveis a minúsculas.

7.  NULO

    ```
    NULL
    ```

    

    NULL só pode ser atribuído a um sombreador, amostrador ou um objeto de textura.

8.  Bloco assembly

    ```
    asm { code }
    ```

    

    Blocos de assembly PS devem ser atribuídos ao estado PIXELSHADER.

    Os blocos de assembly do VS devem ser atribuídos ao estado VERTEXSHADER.

9.  Bloco de estado do sampler

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    Blocos de estado de amostra são sequências de atribuições de textura ou estado de estágio não indexado do sampler.

    Os blocos de estado de amostra devem ser atribuídos ao estado de efeito SAMPLER.

10. Bloco de estado de efeito

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    Blocos de estado são sequências de estado geral. Os blocos de estado podem ser aninhados, mas não podem conter referências circulares.

    Os blocos de estado devem ser atribuídos ao estado de efeito STATEBLOCK.

11. Compilação HLSL

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    O sombreador de vértice vs. n target indica a versão do sombreador de \_ \_ vértice D3DVS \_ VERSION(m, n). O sombreador de pixel ps m n target indica a versão do \_ \_ \_ sombreador de pixel D3DPS VERSION(m, n).

    Expressões de compilação de linguagem de alto nível do sombreador de vértice só podem ser atribuídas ao estado de efeito VERTEXSHADER. Expressões de compilação de linguagem de alto nível do sombreador de pixel só podem ser atribuídas ao estado de efeito PIXELSHADER.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



