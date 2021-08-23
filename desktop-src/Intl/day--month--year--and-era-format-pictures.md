---
description: O aplicativo usa os elementos descritos neste tópico para construir uma cadeia de caracteres de imagem de formato terminada em nulo.
ms.assetid: c18868a9-6912-46fd-93f5-d8021937b049
title: Imagens de formato de dia, mês, ano e era
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ae1adf82a202ebb08f199bb252e59c0f35aab8ad35b60ac57a8ebbe102711c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068266"
---
# <a name="day-month-year-and-era-format-pictures"></a>Imagens de formato de dia, mês, ano e era

O aplicativo usa os elementos descritos neste tópico para construir uma cadeia de caracteres de imagem de formato terminada em nulo. Se espaços são usados para separar os elementos na cadeia de caracteres, esses espaços aparecerão no mesmo local na cadeia de caracteres de saída.

> [!Note]  
> Os tipos de formato "d", "g" e "y" devem estar em letras minúsculas e a letra "M" deve estar em letras maiúsculas.

 

Por exemplo, para obter a cadeia de caracteres de data "Wed, Aug 31 94", o aplicativo usa a cadeia de caracteres de imagem "ddd',' MMM dd yy".

O aplicativo usa aspas simples para marcar caracteres para exibir exatamente conforme especificado. Se o aplicativo deve exibir uma aspas simples, ele deve colocar duas aspas simples em uma linha. Por exemplo, 'abc''bar', é exibido como "abc'bar".

A tabela a seguir define os tipos de formato usados para representar dias.



| Tipo de formato | Significado                                                                                                                                                                                                                                                                                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d           | Dia do mês como dígitos sem zeros à esquerda para dias de dígito único.                                                                                                                                                                                                                                                                                                   |
| dd          | Dia do mês como dígitos com zeros à esquerda para dias de dígito único.                                                                                                                                                                                                                                                                                                      |
| ddd         | Abreviado dia da semana, conforme especificado por um valor [ \_ LOCALE SABBREVDAYNAME, \*](locale-sabbrev-constants.md) por exemplo, "Mon" em inglês (Estados Unidos).**Windows Vista e posterior:** se uma versão curta do dia da semana for necessária, seu aplicativo deverá usar as constantes [ \_ LOCALE SSHORTESTDAYNAME. \*](locale-sshortestdayname-constants.md)<br/> |
| dddd        | Dia da semana, conforme especificado por um [valor LOCALE \_ SDAYNAME. \* ](locale-sdayname-constants.md)                                                                                                                                                                                                                                                                              |



 

A tabela a seguir define os tipos de formato usados para representar meses.



| Tipo de formato | Significado                                                                                                                                                                          |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M           | Mês como dígitos sem zeros à esquerda para meses de dígito único.                                                                                                                   |
| MM          | Mês como dígitos com zeros à esquerda para meses de dígito único.                                                                                                                      |
| MMM         | Mês abreviado conforme especificado por um valor [ \_ LOCALE \* SABBREVMONTHNAME,](locale-sabbrev-constants.md) por exemplo, "Nov" em inglês (Estados Unidos).                             |
| MMMM        | Mês conforme especificado por um valor [ \_ LOCALE SMONTHNAME, \* ](locale-smonthname-constants.md) por exemplo, "Novembro" para inglês (Estados Unidos) e "Noviembre" para espanhol (Espanha). |



 

A tabela a seguir define os tipos de formato usados para representar anos.



| Tipo de formato | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| a           | Ano representado apenas pelo último dígito.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| yy          | Ano representado apenas pelos dois últimos dígitos. Um zero à esquerda é adicionado para anos de dígito único.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| yyyy        | Ano representado por um total de quatro ou cinco dígitos, dependendo do calendário usado. Calendários tailandeses e coreanos têm anos de cinco dígitos. O padrão "aaaa" mostra cinco dígitos para esses dois calendários e quatro dígitos para todos os outros calendários com suporte. Calendários que têm anos de dígito único ou de dois dígitos, como para a era japonês, são representados de maneira diferente. Um ano de dígito único é representado com um zero à esquerda, por exemplo, "03". Um ano de dois dígitos é representado com dois dígitos, por exemplo, "13". Nenhum zero à esquerda adicional é exibido. |
| yyyyy       | Comporta-se de forma idêntica a "aaaa".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

A tabela a seguir define os tipos de formato usados para representar um período ou era.



| Tipo de formato | Significado                                                                                                                                                                              |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g, gg       | Cadeia de caracteres de período/era formatada conforme especificado pelo valor \_ CAL SERASTRING. As imagens de formato "g" e "gg" em uma cadeia de caracteres de data serão ignoradas se não houver nenhuma cadeia de caracteres de era ou período associada. |



 

 

 




