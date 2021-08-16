---
title: Otimizando sombreadores HLSL
description: Esta seção descreve estratégias de uso geral que você pode usar para otimizar seus sombreadores. Você pode aplicar essas estratégias a sombreadores escritos em qualquer idioma, em qualquer plataforma.
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- linguagem de sombreador de alto nível
- HLSL, desempenho
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bc707f88fcc731146fcd3a5bbca641e6f0515a728b07af0863894d249c16a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726136"
---
# <a name="optimizing-hlsl-shaders"></a>Otimizando sombreadores HLSL

Esta seção descreve estratégias de uso geral que você pode usar para otimizar seus sombreadores. Você pode aplicar essas estratégias a sombreadores escritos em qualquer idioma, em qualquer plataforma.

-   [Saber onde executar cálculos de sombreador](#know-where-to-perform-shader-calculations)
-   [Ignorar instruções desnecessárias](#skip-unnecessary-instructions)
-   [Variáveis de pacote e interpolantes](#pack-variables-and-interpolants)
-   [Reduzir a complexidade do sombreador](#reduce-shader-complexity)
-   [Tópicos relacionados](#related-topics)
-   [Tópicos relacionados](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a>Saber onde executar cálculos de sombreador

Sombreadores de vértice executam operações que incluem buscar vértices e executar a transformação de matriz de dados de vértice. Normalmente, os sombreadores de vértice são executados uma vez por vértice.

Sombreadores de pixel executam operações que incluem buscar dados de textura e executar cálculos de iluminação. Normalmente, os sombreadores de pixel são executados uma vez por pixel para uma determinada parte da geometria.

Normalmente, pixels ultrapassam vértices em uma cena, de modo que os sombreadores de pixel são executados com mais frequência do que sombreadores de vértice.

Ao criar algoritmos de sombreador, lembre-se do seguinte:

-   Execute cálculos no sombreador de vértice, se possível. Um cálculo executado em um sombreador de pixel é muito mais caro do que um cálculo executado em um sombreador de vértice.
-   Considere o uso de cálculos por vértice para melhorar o desempenho em situações como malhas densas. Para malhas densas, cálculos por vértice podem produzir resultados visualmente indistinguíveis de resultados produzidos com cálculos por pixel.

## <a name="skip-unnecessary-instructions"></a>Ignorar instruções desnecessárias

No HLSL, a ramificação dinâmica fornece a capacidade de limitar o número de instruções executadas. Portanto, a ramificação dinâmica pode ajudar a acelerar o tempo de execução do sombreador. Se geometria ou pixels não são exibidos, use a ramificação dinâmica para sair do sombreador ou para limitar as instruções. Por exemplo, se um pixel não estiver aceso, não há nenhum ponto na execução do algoritmo de iluminação.

A tabela a seguir lista alguns casos em que você pode testar condições em seu sombreador e usar a ramificação dinâmica para ignorar instruções desnecessárias. A tabela não é abrangente. Em vez disso, ele se destina a dar ideias para otimizar seu código.



| Condição a ser verificada                                    | Resposta no sombreador       |
|-------------------------------------------------------|------------------------------|
| A verificação alfa determina que um pixel não será visto. | Ignore o restante do sombreador. |
| O pixel ou a geometria é totalmente cortado.                | Ignore o restante do sombreador. |
| Os pesos da capa são zero.                                | Ignorar o esqueleto.                  |
| A atenuação de luz é zero.                            | Ignore a iluminação.               |
| Termo lambertiano não positivo.                         | Ignore a iluminação.               |



 

## <a name="pack-variables-and-interpolants"></a>Variáveis de pacote e interpolantes

Cuidado com o espaço necessário para os dados do sombreador. Empacote o máximo de informações em uma variável ou interpolante possível. Às vezes, as informações de duas variáveis podem ser empacotadas no espaço de memória de uma única variável.

## <a name="reduce-shader-complexity"></a>Reduzir a complexidade do sombreador

Mantenha seus sombreadores pequenos e simples. Em geral, sombreadores com menos instruções são executados mais rapidamente do que sombreadores com mais instruções. Também é mais fácil de depurar e otimizar sombreadores menores e menos complexos.

## <a name="related-topics"></a>Tópicos relacionados

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




