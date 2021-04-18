---
description: Um mapa de valor é uma matriz vinculada a uma propriedade com os qualificadores Value e ValueMap.
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: Qualificadores de valor e ValueMap
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df85342df9543e4d62b04482785ec31bb5bd3982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760629"
---
# <a name="valuemap-and-value-qualifiers"></a>Qualificadores de valor e ValueMap

Um mapa de valor é uma matriz vinculada a uma propriedade com os qualificadores **Value** e **ValueMap** .

A propriedade atua como um índice na matriz, mantendo um valor que representa um dos valores na matriz. Usando o código MOF, você pode ter os seguintes tipos de mapas de valor:

-   Mapeamento de matriz para um inteiro.

    Você pode definir uma matriz com o qualificador de **valor** e vincular a matriz diretamente a uma propriedade de número inteiro, conforme mostrado no exemplo a seguir:

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    Neste exemplo, o valor da propriedade **status** é um índice na matriz de cadeia de caracteres definida pelo **valor**. A propriedade só pode assumir valores que correspondam às posições ordinais na matriz de **valor** menos 1. Por exemplo, a configuração de **status** como "1" é mapeada para o valor "erro". A propriedade index só pode ter valores que correspondam a posições na matriz **Value** . Por exemplo, se a matriz tiver 10 entradas, a propriedade index poderá obter a história de 0 a 9, não 30 ou 177.

-   Mapeamento de matriz para outro mapeamento de matriz para um inteiro.

    Se você quiser criar um índice que não usa um sistema ordinal de contagem, use o qualificador **ValueMap** . O qualificador **ValueMap** configura outra matriz que contém um sistema de numeração de índice arbitrário, conforme mostrado no exemplo a seguir:

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    Embora seja necessário posicionar os valores de **ValueMap** entre aspas, o WMI considera os valores inteiros. Portanto, neste exemplo, você pode definir a propriedade **status** como um número inteiro no conjunto **ValueMap** : 1, 3, 99 ou 0. O WMI mapeia cada inteiro de uma posição ordinal na matriz de cadeia de caracteres **ValueMap** para uma posição correspondente na matriz **Value** . Por exemplo, definir **status** como 0 é mapeado para "desconhecido".

-   Mapeamento de matriz para outro mapeamento de matriz para uma cadeia de caracteres.

    Se você não quiser usar um inteiro para indexar sua matriz, você pode usar uma cadeia de caracteres para armazenar um dos valores possíveis em sua matriz. Para fazer isso, você deve definir um **valor** e uma matriz **ValueMap** que contenham cadeias de caracteres, conforme mostrado no exemplo a seguir:

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    Com uma propriedade de cadeia de caracteres, os valores reais permitidos da propriedade são as entradas na matriz **ValueMap** . Por exemplo, você pode definir **status** como "OK" ou "desconhecido".

Cabe ao aplicativo aproveitar os mapeamentos de uma maneira útil. Cabe ao provedor impor um intervalo legal de valores.

## <a name="remarks"></a>Comentários

Ao decidir se deve usar o  / **valor** de ValueMap ou os / qualificadores **bitvalues** de bitmap, determine se algum dos valores indicados pode ocorrer simultaneamente. Se vários valores simultâneos puderem existir, você deverá usar o **bitmap** / **bitvalues**. Se todos os valores forem mutuamente exclusivos, você deverá usar os  / qualificadores de **valor** ValueMap.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[BitMap e bitvalues](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



