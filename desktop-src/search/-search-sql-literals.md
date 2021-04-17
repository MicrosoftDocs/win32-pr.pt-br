---
description: Um literal é uma cadeia de caracteres que representa um valor em uma instrução de consulta. Você usa literais para comparar valores de coluna ou para especificar termos de pesquisa. O Windows Search dá suporte aos seguintes tipos de literais.
ms.assetid: cc526174-3c91-402d-b7d0-69fc9a61c3f9
title: Literais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e066f62a39bc46ec2ff7bf44c187d33f3832ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790401"
---
# <a name="literals"></a>Literais

Um literal é uma cadeia de caracteres que representa um valor em uma instrução de consulta. Você usa literais para comparar valores de coluna ou para especificar termos de pesquisa. O Windows Search dá suporte aos seguintes tipos de literais.


-   **Literais de cadeia de caracteres** podem ter qualquer comprimento e podem conter caracteres ANSI ou Unicode. Você deve colocar literais de cadeia de caracteres entre aspas simples ('). Para incluir uma aspa simples dentro de uma literal de cadeia de caracteres, use duas aspas simples (' '). Representa uma cadeia de caracteres vazia como duas aspas simples consecutivas (' ').
-   Os **literais numéricos** podem conter os dígitos 0-9, um ponto e a letra e (ou e). Os literais numéricos representam números, incluindo inteiros positivos e negativos, números decimais e valores de moeda. Os literais numéricos podem ser definidos usando a notação científica (por exemplo, 2.3 E-05). Não coloque um literal numérico entre aspas simples ou ele será interpretado como um literal de cadeia de caracteres e comparado usando técnicas de comparação de cadeia de caracteres. Os valores de moeda não podem conter símbolos de moeda.
-   Os **literais hexadecimais** podem conter os dígitos 0-9 e as letras a-f e a-f. Um literal hexadecimal representa um inteiro não assinado especificado na notação hexadecimal. Os literais hexadecimais devem começar com 0x.
    > [!Note]  
    > O padrão SQL-92 requer que os literais hexadecimais sejam colocados entre aspas simples; no entanto, o Windows Search não oferece suporte a essa notação.

     

-   **Literais boolianos** representam valores lógicos e podem ser **true** ou **false**. Não coloque um literal booliano entre aspas simples ou ele é interpretado como um literal de cadeia de caracteres.
-   Os **literais de data** representam datas específicas, carimbos de hora ou horas relativas e estão entre aspas simples. Você deve colocar datas no formato ano/mês/dia horas: minutos: segundos ou ano-mês-dia, horas: minutos: segundos, em que o mês, o dia e o ano são números. Especifique o ano com um valor de quatro dígitos, por exemplo, 2004. Os valores de hora devem estar no formato horas: minutos: segundos. A sintaxe de tempo relativa se baseia na [função DateAdd](-search-sql-dateadd.md).

 

 



