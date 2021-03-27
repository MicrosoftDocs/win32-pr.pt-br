---
title: Otimizando sombreadores HLSL
description: Esta seção descreve estratégias de finalidade geral que você pode usar para otimizar seus sombreadores. Você pode aplicar essas estratégias a sombreadores que são escritos em qualquer linguagem, em qualquer plataforma.
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- linguagem de sombreamento de alto nível
- HLSL, desempenho
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06d3bb806e98e489020aa1755ef2a6c952459d86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005906"
---
# <a name="optimizing-hlsl-shaders"></a>Otimizando sombreadores HLSL

Esta seção descreve estratégias de finalidade geral que você pode usar para otimizar seus sombreadores. Você pode aplicar essas estratégias a sombreadores que são escritos em qualquer linguagem, em qualquer plataforma.

-   [Saiba onde executar cálculos de sombreador](#know-where-to-perform-shader-calculations)
-   [Ignorar instruções desnecessárias](#skip-unnecessary-instructions)
-   [Variáveis de pacote e Interpolants](#pack-variables-and-interpolants)
-   [Reduzir a complexidade do sombreador](#reduce-shader-complexity)
-   [Tópicos relacionados](#related-topics)
-   [Tópicos relacionados](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a>Saiba onde executar cálculos de sombreador

Os sombreadores de vértice executam operações que incluem a busca de vértices e a execução de transformação de matriz de dados de vértice. Normalmente, os sombreadores de vértice são executados uma vez por vértice.

Sombreadores de pixel executam operações que incluem a busca de dados de textura e a execução de cálculos de iluminação. Normalmente, os sombreadores de pixel são executados uma vez por pixel para uma determinada parte da geometria.

Normalmente, pixels ultrapassam vértices em uma cena, portanto, sombreadores de pixel são executados com mais frequência do que os sombreadores de vértice.

Ao criar algoritmos de sombreador, tenha em mente o seguinte:

-   Faça cálculos no sombreador de vértice, se possível. Um cálculo que é executado em um sombreador de pixel é muito mais caro do que um cálculo que é executado em um sombreador de vértice.
-   Considere o uso de cálculos por vértice para melhorar o desempenho em situações como malhas densas. Para malhas densas, os cálculos por vértice podem produzir resultados que são visualmente indistinguíveis dos resultados produzidos com cálculos por pixel.

## <a name="skip-unnecessary-instructions"></a>Ignorar instruções desnecessárias

No HLSL, a ramificação dinâmica fornece a capacidade de limitar o número de instruções executadas. Portanto, a ramificação dinâmica pode ajudar a acelerar o tempo de execução do sombreador. Se a geometria ou os pixels não forem exibidos, use a ramificação dinâmica para sair do sombreador ou para limitar as instruções. Por exemplo, se um pixel não estiver aceso, não haverá nenhum ponto na execução do algoritmo de iluminação.

A tabela a seguir lista alguns casos em que você pode testar condições em seu sombreador e usar a ramificação dinâmica para ignorar instruções desnecessárias. A tabela não é abrangente. Em vez disso, ele é destinado a fornecer ideias para otimizar seu código.



| Condição a ser verificada                                    | Resposta no sombreador       |
|-------------------------------------------------------|------------------------------|
| A seleção alfa determina que um pixel não será visto. | Ignore o restante do sombreador. |
| O pixel ou a geometria é totalmente fogged.                | Ignore o restante do sombreador. |
| Os pesos da capa são zero.                                | Ignorar Bones.                  |
| A atenuação de luz é zero.                            | Ignorar iluminação.               |
| Termo Lambertian não positivo.                         | Ignorar iluminação.               |



 

## <a name="pack-variables-and-interpolants"></a>Variáveis de pacote e Interpolants

Lembre-se do espaço necessário para dados do sombreador. Empacotar a quantidade de informações em uma variável ou interpolação o mais possível. Às vezes, as informações de duas variáveis podem ser incluídas no espaço de memória de uma única variável.

## <a name="reduce-shader-complexity"></a>Reduzir a complexidade do sombreador

Mantenha seus sombreadores pequenos e simples. Em geral, os sombreadores com menos instruções são executados mais rapidamente do que os sombreadores com mais instruções. Também é mais fácil depurar e otimizar sombreadores menores e menos complexos.

## <a name="related-topics"></a>Tópicos relacionados

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




