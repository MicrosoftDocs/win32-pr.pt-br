---
title: Auxiliares de HLSL
description: Para ajudar os autores de efeito na escrita de sombreadores de pixel vinculados, o d2d1effecthelpers. hlsli define um conjunto de extensões de linguagem HLSL na forma de métodos auxiliares e macros.
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8f43447c16d93ef9e1839ac319c761b975222a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916038"
---
# <a name="hlsl-helpers"></a>Auxiliares de HLSL

Para ajudar os autores de efeito na escrita de sombreadores de pixel vinculados, o d2d1effecthelpers. hlsli define um conjunto de extensões de linguagem HLSL na forma de métodos auxiliares e macros.

Para adicionar o d2d1effecthelpers. hlsli ao seu projeto, adicione uma \# instrução include no arquivo HLSL. d2d1effecthelpers. hlsli está localizado no mesmo local que outros cabeçalhos Direct2D, como d2d1. h; Ele pode ser referenciado na página de propriedades do arquivo HLSL adicionando a macro $ (WindowsSDK \_ IncludePath) à propriedade de diretórios de inclusão adicional. Observe que a \# instrução include deve vir após qualquer política de pré-processador, como a \_ contagem de entrada D2D \_ ter sido definida.

``` syntax
#include <d2d1effecthelpers.hlsli>
```

Direct2D não dá suporte à vinculação de sombreadores de computação ou de vértice. No entanto, se o efeito usar um sombreador de vértice e um sombreador de pixel, a saída do sombreador de pixel ainda poderá ser vinculada.

## <a name="preprocessor-directives"></a>Diretivas de pré-processador

As diretivas de pré-processador são necessárias para comunicar informações sobre o efeito. Isso inclui o número de entradas e o tipo de amostragem de cada entrada. Os valores a seguir devem ser definidos no código do sombreador de efeito acima do ponto de entrada do sombreador relevante quando aplicável.

-   `D2D_INPUT_COUNT <N>` : Declara o número de entradas de textura para o efeito. Se o efeito tiver um número variável de entradas, esse valor deverá ser definido adequadamente para cada ponto de entrada do sombreador. Definir esse valor é obrigatório.
-   `D2D_INPUT<N>_SIMPLE` : Declara a entrada enésima para usar a amostragem simples. Se não estiver definido, a entrada enésima será complexa. Definir esse valor é opcional.
-   `D2D_INPUT<N>_COMPLEX` : Declara a entrada enésima para usar amostragem complexa. Se não estiver definido, a entrada enésima será complexa. Definir esse valor é opcional.
-   `D2D_REQUIRES_SCENE_POSITION` : Indica que a função de sombreador chama métodos auxiliares que usam o valor de posição de cena (ou seja, a função auxiliar [D2DGetScenePosition](d2dgetsceneposition.md) ). Esse parâmetro só deve ser incluído quando necessário, já que apenas uma função por sombreador vinculado pode utilizar esse parâmetro. Definir esse valor é opcional.
-   `D2D_CUSTOM_ENTRY` : Indica que a função de sombreador de pixel consome a saída de um sombreador de vértice personalizado e, portanto, irá declarar seus parâmetros de entrada. Todas as entradas de sombreador de vértice personalizadas usam amostragem complexa e não podem consumir a saída de outra função de sombreador (ou seja, elas são somente pós-link). Definir esse valor é opcional.

Por exemplo:

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a>Funções auxiliares

As funções auxiliares são usadas como substituição para algumas funções intrínsecas HLSL nativas. No momento da compilação, essas funções auxiliares são redefinidas pelo Direct2D para a versão apropriada, dependendo do tipo de destino de compilação (sombreador completo ou função de exportação).

As funções auxiliares:

<dl>

[D2DGetInput](d2dgetinput.md)  
[D2DSampleInput](d2dsampleinput.md)  
[D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
[D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
[D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
[D2DGetScenePosition](d2dgetsceneposition.md)  
[\_Entrada do PS D2D \_](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vinculação de Sombreador de Efeito](effect-shader-linking.md)
</dt> </dl>

 

 




