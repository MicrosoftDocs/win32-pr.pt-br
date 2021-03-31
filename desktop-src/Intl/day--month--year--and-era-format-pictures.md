---
description: O aplicativo usa os elementos descritos neste tópico para construir uma cadeia de caracteres de imagem de formato terminada em nulo.
ms.assetid: c18868a9-6912-46fd-93f5-d8021937b049
title: Imagens de formato de dia, mês, ano e era
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c83439cc33c1caf067b5c6f41234a6f1ddc4dcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829797"
---
# <a name="day-month-year-and-era-format-pictures"></a>Imagens de formato de dia, mês, ano e era

O aplicativo usa os elementos descritos neste tópico para construir uma cadeia de caracteres de imagem de formato terminada em nulo. Se os espaços forem usados para separar os elementos na cadeia de caracteres, esses espaços serão exibidos no mesmo local na cadeia de caracteres de saída.

> [!Note]  
> Os tipos de formato "d", "g" e "y" devem ser minúsculos e a letra "M" deve estar em letras maiúsculas.

 

Por exemplo, para obter a cadeia de caracteres de data "Qua, ago 31 94", o aplicativo usa a cadeia de caracteres de imagem "ddd", "MMM DD AA".

O aplicativo usa aspas simples para marcar caracteres para exibir exatamente como especificado. Se o aplicativo precisar exibir uma aspa simples, ele deverá posicionar duas aspas simples em uma linha. Por exemplo, ' abc ' ' bar ', é exibido como "abc'bar".

A tabela a seguir define os tipos de formato usados para representar dias.



| Tipo de formato | Significado                                                                                                                                                                                                                                                                                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d           | Dia do mês como dígitos sem zeros à esquerda para dias de dígito único.                                                                                                                                                                                                                                                                                                   |
| dd          | Dia do mês como dígitos com zeros à esquerda para dias de dígito único.                                                                                                                                                                                                                                                                                                      |
| ddd         | Dia abreviado da semana, conforme especificado por um valor de [ \_ \* SABBREVDAYNAME de localidade](locale-sabbrev-constants.md) , por exemplo, "Mon" em inglês (Estados Unidos).**Windows Vista e posterior:** se uma versão curta do dia da semana for necessária, seu aplicativo deverá usar as constantes [ \_ \* SSHORTESTDAYNAME de localidade](locale-sshortestdayname-constants.md) .<br/> |
| dddd        | Dia da semana, conforme especificado por um valor de [ \_ \* SDAYNAME de localidade](locale-sdayname-constants.md) .                                                                                                                                                                                                                                                                              |



 

A tabela a seguir define os tipos de formato usados para representar meses.



| Tipo de formato | Significado                                                                                                                                                                          |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M           | Mês como dígitos sem zeros à esquerda para meses de dígito único.                                                                                                                   |
| MM          | Mês como dígitos com zeros à esquerda para meses de dígito único.                                                                                                                      |
| MMM         | Mês abreviado como especificado por um valor de [ \_ \* SABBREVMONTHNAME de localidade](locale-sabbrev-constants.md) , por exemplo, "Nov" em inglês (Estados Unidos).                             |
| MMMM        | Mês conforme especificado por um valor de [ \_ \* SMONTHNAME de localidade](locale-smonthname-constants.md) , por exemplo, "novembro" para inglês (Estados Unidos) e "Noviembre" para espanhol (Espanha). |



 

A tabela a seguir define os tipos de formato usados para representar anos.



| Tipo de formato | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| a           | Ano representado apenas pelo último dígito.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| yy          | Ano representado apenas pelos dois últimos dígitos. Um zero à esquerda é adicionado a anos de um único dígito.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| yyyy        | Ano representado por um total de quatro ou cinco dígitos, dependendo do calendário usado. Os calendários budista tailandês e coreano têm anos de cinco dígitos. O padrão "aaaa" mostra cinco dígitos para esses dois calendários e quatro dígitos para todos os outros calendários com suporte. Os calendários que têm anos de um ou dois dígitos, como para a era do imperador japonês, são representados de forma diferente. Um ano de dígito único é representado com um zero à esquerda, por exemplo, "03". Um ano de dois dígitos é representado com dois dígitos, por exemplo, "13". Nenhum zero à esquerda adicional é exibido. |
| yyyyy       | Comporta-se de forma idêntica a "aaaa".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

A tabela a seguir define os tipos de formato usados para representar um período ou era.



| Tipo de formato | Significado                                                                                                                                                                              |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g, gg       | Cadeia de caracteres de período/era formatada conforme especificado pelo valor de SERASTRING de CAL \_ . As imagens de formato "g" e "GG" em uma cadeia de caracteres de data são ignoradas se não houver nenhuma cadeia de caracteres ou de período associada. |



 

 

 




