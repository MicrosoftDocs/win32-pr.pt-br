---
description: O filtro de correspondência de padrões notifica o driver para aceitar quadros que têm um padrão específico em um deslocamento específico.
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: Gravando o filtro PATTERNMATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759186"
---
# <a name="writing-the-patternmatch-filter"></a>Gravando o filtro PATTERNMATCH

O filtro de correspondência de padrões notifica o driver para aceitar quadros que têm um padrão específico em um deslocamento específico. Você pode especificar um máximo de quatro correspondências de padrão detalhadas, que podem ser combinadas em instruções lógicas or ou OR para a avaliação de Monitor de Rede driver.

Para implementar correspondências de padrão, use as seguintes estruturas de Monitor de Rede:

-   [**EXPRESSÃO**](expression.md)
-   [**ANDEXP**](andexp.md)
-   [**PATTERNMATCH**](patternmatch.md)

Para avaliar uma instrução **ou** , Combine dois a quatro padrões corresponde a uma estrutura [**ANDEXP**](andexp.md) (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3). Para avaliar uma instrução AND, combine uma a quatro estruturas **ANDEXP** e uma estrutura de [**expressão**](expression.md) (AndExp1 && AndExp2).

## <a name="pattern-match-definitions"></a>Definições de correspondência de padrões

Uma correspondência de padrão único é definida pela estrutura [**PATTERNMATCH**](patternmatch.md) . Uma correspondência individual pode operar de uma de duas maneiras.

Normalmente, o driver assumirá a base de deslocamento (que pode ser a \_ base de deslocamento em \_ relação \_ ao \_ quadro, a base de deslocamento \_ \_ em relação \_ ao \_ \_ protocolo efetivo, a base de deslocamento \_ \_ em relação \_ ao \_ IPX ou a \_ base de deslocamento \_ em relação \_ ao \_ IP) e a contagem inicial. O driver contará os bytes de deslocamento a partir daí e corresponderá aos dados encontrados com os primeiros bytes de comprimento em **PatternToMatch**. Se forem iguais, e os sinalizadores de correspondência de padrão \_ \_ \_ não forem definidos, esse padrão passará. Se forem diferentes e os sinalizadores de \_ correspondência de padrão \_ \_ não tiverem sido definidos, o padrão passará. Caso contrário, esse padrão falhará.

Ou:

Se o sinalizador de correspondência de padrões de \_ \_ \_ porta sinalizadores \_ especificado estiver definido e a base estiver definida como deslocamento em \_ \_ relação \_ ao \_ IPX ou deslocamento em \_ \_ relação \_ ao \_ IP, a comparação será mais complexa. Primeiro, o driver garante que o protocolo de base offset esteja lá, então o driver verifica se a porta especificada corresponde à porta no quadro. Por fim, o driver garante que o membro **PatternToMatch** corresponda como antes, com a exceção de que o deslocamento é do final do IP ou IPX. Observe que, se a base não for uma dessas duas, o sinalizador de \_ correspondência de padrões \_ porta de sinalizadores \_ \_ especificado será ignorado e o padrão será avaliado como acima.

Para avaliar uma correspondência de padrão único, uma estrutura de [**expressão**](expression.md) deve ter um membro **AndExp** contendo uma correspondência de padrão única.

A criação do filtro de correspondência de padrões envolve a criação de estruturas [**PATTERNMATCH**](patternmatch.md) e a combinação lógica com as estruturas [**expression**](expression.md) e [**ANDEXP**](andexp.md) .

**Para gravar um filtro de PATTERNMATCH**

1.  Na estrutura [**ANDEXP**](andexp.md) , preencha a matriz com correspondências de padrão.
2.  Preencha a estrutura de [**expressão**](expression.md) com uma matriz de membros **AndExp** .
3.  Não exceda um total de quatro correspondências de padrão para o filtro de captura.
4.  Na estrutura [**PATTERNMATCH**](patternmatch.md) , selecione um tipo de sinalizador.
5.  Selecione uma base de deslocamento.
6.  Enumere um valor de porta.
7.  Defina o valor de deslocamento.
8.  Defina o comprimento do padrão.
9.  Enumere o valor padrão.

## <a name="patternmatch-examples"></a>Exemplos de PATTERNMATCH

Esse quadro representa um deslocamento padrão.

![quadro de deslocamento padrão](images/offs-pat.png)

O fragmento de código é implementado como:

``` syntax
Basis  ->   IP
Offset ->   4 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

Este quadro descreve um deslocamento especificado pela porta (em relação a IPX).

![quadro de deslocamento especificado pela porta](images/stan-pat.png)

O código de exemplo é implementado como:

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



