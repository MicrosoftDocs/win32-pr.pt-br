---
description: Um mapa de valor é uma matriz vinculada a uma propriedade com os qualificadores Value e ValueMap.
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: Qualificadores valueMap e value
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 34b95b540a99dfaecefcbe0b87e817fd0c44c58606921046476b3411cdd256e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107375"
---
# <a name="valuemap-and-value-qualifiers"></a>Qualificadores valueMap e value

Um mapa de valor é uma matriz vinculada a uma propriedade com os **qualificadores Value** e **ValueMap.**

A propriedade atua como um índice na matriz, mantendo um valor que representa um dos valores na matriz. Usando o código MOF, você pode ter os seguintes tipos de mapas de valor:

-   Mapeamento de matriz para um inteiro.

    Você pode definir uma matriz com o **qualificador Value** e vincular a matriz diretamente a uma propriedade integer, conforme mostrado no exemplo a seguir:

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    Neste exemplo, o valor da **propriedade Status** é um índice na matriz de cadeia de caracteres definida pelo **Valor**. A propriedade só pode assumir valores que correspondem às posições ordinais na matriz **Value** menos 1. Por exemplo, definir **Status** como "1" é mapeando para o valor "Erro". A propriedade index pode usar apenas valores que correspondem a posições na **matriz Value.** Por exemplo, se a matriz tiver 10 entradas, a propriedade de índice poderá contar de 0 a 9, não 30 ou 177.

-   Mapeamento de matriz para outro mapeamento de matriz para um inteiro.

    Se você quiser criar um índice que não use um sistema ordinal de contagem, use o qualificador **ValueMap.** O **qualificador ValueMap** configura outra matriz que contém um sistema de numeração de índice arbitrário, conforme mostrado no exemplo a seguir:

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    Embora você deve colocar os valores de **ValueMap** entre aspas, o WMI considera os valores inteiros. Portanto, neste exemplo, você pode definir a propriedade **Status** como um inteiro no conjunto **ValueMap:** 1, 3, 99 ou 0. O WMI mapeia cada inteiro de uma posição ordinal na matriz de cadeia de caracteres **ValueMap** para uma posição correspondente na **matriz Value.** Por exemplo, definir **Status** como 0 mapeia para "Desconhecido".

-   Mapeamento de matriz para outro mapeamento de matriz para uma cadeia de caracteres.

    Se você não quiser usar um inteiro para indexar sua matriz, poderá usar uma cadeia de caracteres para manter um dos valores possíveis em sua matriz. Para fazer isso, você deve definir uma matriz **Value** e **ValueMap** que contêm cadeias de caracteres, conforme mostrado no exemplo a seguir:

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    Com uma propriedade de cadeia de caracteres, os valores reais aceitável da propriedade são as entradas na **matriz ValueMap.** Por exemplo, você pode definir **Status** como "OK" ou "Desconhecido".

O aplicativo pode aproveitar os mapeamentos de uma maneira útil. É decisão do provedor impor um intervalo legal de valores.

## <a name="remarks"></a>Comentários

Ao decidir se os qualificadores **ValueMap** Value ou /   / **BitMap BitValues** devem ser usado, determine se qualquer um dos valores que está sendo indicado pode ocorrer simultaneamente. Se vários valores simultâneos puderem existir, você deverá usar **BitMap** / **BitValues**. Se todos os valores são mutuamente exclusivos, você deve usar os qualificadores **ValueMap** / **Value.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[BitMap e BitValues](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



