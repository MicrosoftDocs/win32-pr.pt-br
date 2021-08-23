---
title: Auxiliares HLSL
description: Para ajudar os autores de efeito a escrever sombreadores de pixel vinculáveis, d2d1effecthelpers.hlsli define um conjunto de extensões de linguagem HLSL na forma de macros e métodos auxiliares.
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608ae4b47b96616f8818cd45b466c02a7b09b2171383fbe82ecbe055ed0915b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569556"
---
# <a name="hlsl-helpers"></a>Auxiliares HLSL

Para ajudar os autores de efeito a escrever sombreadores de pixel vinculáveis, d2d1effecthelpers.hlsli define um conjunto de extensões de linguagem HLSL na forma de macros e métodos auxiliares.

Para adicionar d2d1effecthelpers.hlsli ao seu projeto, adicione uma \# instrução include no arquivo HLSL. d2d1effecthelpers.hlsli está localizado no mesmo local que outros Direct2D como d2d1.h; ele pode ser referenciado na página de propriedades do arquivo HLSL adicionando a macro $(WindowsSDK IncludePath) à propriedade Diretórios de Inclusão \_ Adicionais. Observe que a \# instrução include deve vir após qualquer diretiva de pré-processador, como D2D \_ INPUT \_ COUNT, ter sido definida.

``` syntax
#include <d2d1effecthelpers.hlsli>
```

Direct2D dá suporte à vinculação de computação ou sombreadores de vértice. No entanto, se o efeito usar um sombreador de vértice e um sombreador de pixel, a saída do sombreador de pixel ainda poderá ser vinculada.

## <a name="preprocessor-directives"></a>Diretivas de pré-processador

As diretivas de pré-processador são necessárias para comunicar informações sobre o efeito. Isso inclui o número de entradas e o tipo de amostragem de cada entrada. Os valores a seguir devem ser definidos no código do sombreador de efeito acima do ponto de entrada do sombreador relevante quando aplicável.

-   `D2D_INPUT_COUNT <N>` : declara o número de entradas de textura para o efeito. Se o efeito tiver um número variável de entradas, esse valor deverá ter o escopo apropriado para cada ponto de entrada do sombreador. Definir esse valor é obrigatório.
-   `D2D_INPUT<N>_SIMPLE` : declara a Nª entrada para usar amostragem simples. Se não estiver definida, a entrada Nº padrão será complexa. Definir esse valor é opcional.
-   `D2D_INPUT<N>_COMPLEX` : declara a Nª entrada para usar amostragem complexa. Se não estiver definida, a entrada Nº padrão será complexa. Definir esse valor é opcional.
-   `D2D_REQUIRES_SCENE_POSITION`: indica que a função de sombreador chama métodos auxiliares que usam o valor da posição da cena (ou seja, a função auxiliar [D2DGetScenePosition).](d2dgetsceneposition.md) Esse parâmetro só deve ser incluído quando necessário, pois apenas uma função por sombreador vinculado pode utilizar esse parâmetro. Definir esse valor é opcional.
-   `D2D_CUSTOM_ENTRY` : indica que a função de sombreador de pixel consome a saída de um sombreador de vértice personalizado e, portanto, declarará seus parâmetros de entrada. Todas as entradas de sombreador de vértice personalizadas usam amostragem complexa e não podem consumir a saída de outra função de sombreador (ou seja, são apenas pós-vinculáveis). Definir esse valor é opcional.

Por exemplo:

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a>Funções auxiliares

As funções auxiliares são usadas como uma substituição para algumas funções nativas intrínsecas HLSL. No tempo de compilação, essas funções auxiliares são redefinidas por Direct2D na versão apropriada, dependendo do tipo de destino de compilação (sombreador completo ou função de exportação).

As funções auxiliares:

<dl>

[D2DGetInput](d2dgetinput.md)  
[D2DSampleInput](d2dsampleinput.md)  
[D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
[D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
[D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
[D2DGetScenePosition](d2dgetsceneposition.md)  
[ENTRADA D2D \_ PS \_](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vinculação de Sombreador de Efeito](effect-shader-linking.md)
</dt> </dl>

 

 




