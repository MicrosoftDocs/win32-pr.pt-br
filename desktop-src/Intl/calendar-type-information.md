---
description: Este tópico descreve as informações de tipo de calendário (tipo de dados CALTYPE) usadas nas funções EnumCalendarInfo, EnumCalendarInfoEx, EnumCalendarInfoExEx, GetCalendarInfo e GetCalendarInfoEx.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Informações de tipo de calendário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a8e334a1b05f372f51c81ab8158294d46eebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836853"
---
# <a name="calendar-type-information"></a>Informações de tipo de calendário

Este tópico descreve as informações de tipo de calendário (tipo de dados CALTYPE) usadas nas funções [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)e [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) . Alguns desses valores também são usados pela função [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) .

As constantes CALTYPE a seguir podem ser usadas em combinação com quaisquer outras constantes CALTYPE.



| Constante                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_NOUSEROVERRIDE Cal          | **Windows me/98, windows 2000:** Use o padrão do sistema em vez da opção do usuário.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| CAL \_ retornar \_ nomes de GENITIVE \_ | **Windows 7 e posterior:** Recupere o resultado de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) na forma de nomes de genitive de meses, que são os nomes usados quando os nomes de mês são combinados com outros itens. Por exemplo, em ucraniano, o equivalente a janeiro é escrito "Січень" quando o mês é nomeado sozinho. No entanto, quando o nome do mês é usado em combinação, por exemplo, em uma data como 5 de janeiro de 2003, a forma genitive do nome é usada. Para o exemplo ucraniano, o nome do mês genitive é exibido como "5 січня 2003". Para obter mais informações, consulte [localidade \_ Return \_ GENITIVE \_ Names](locale-return-constants.md). |
| \_número de retorno da Cal \_          | **Windows me/98, windows 2000:** Recupere o resultado de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) como um número em vez de uma cadeia de caracteres. Isso só é válido para valores que começam com CAL \_ I.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CAL \_ usar \_ CP \_ ACP            | **Windows me/98, windows 2000:** Use a página de código ANSI (ACP) do sistema em vez da página de código de localidade para conversão de cadeia de caracteres. Isso só é relevante para versões ANSI de funções, por exemplo, **EnumCalendarInfoA**.                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

As constantes CALTYPE a seguir são mutuamente exclusivas e não podem ser usadas em combinação umas com as outras em uma chamada de função.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAL_ICALINTVALUE</td>
<td>Um valor inteiro que indica o tipo de calendário do calendário alternativo.</td>
</tr>
<tr class="even">
<td>CAL_ITWODIGITYEARMAX</td>
<td><strong>Windows me/98, windows 2000:</strong> Um valor inteiro que indica o limite superior do intervalo de anos de dois dígitos.</td>
</tr>
<tr class="odd">
<td>CAL_IYEAROFFSETRANGE</td>
<td>Uma ou mais cadeias de caracteres terminadas em nulo que especificam os deslocamentos de ano para cada um dos intervalos de era. A última cadeia de caracteres tem um caractere nulo de terminação extra. Esse valor varia em formato, dependendo do tipo de calendário opcional.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME1</td>
<td>Nome nativo abreviado do primeiro dia da semana.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME2</td>
<td>Nome nativo abreviado do segundo dia da semana.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME3</td>
<td>Nome nativo abreviado do terceiro dia da semana.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME4</td>
<td>Nome nativo abreviado do quarto dia da semana.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME5</td>
<td>Nome nativo abreviado do quinto dia da semana.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME6</td>
<td>Nome nativo abreviado do sexto dia da semana.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME7</td>
<td>Nome nativo abreviado do sétimo dia da semana.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVERASTRING</td>
<td><strong>Windows 7 e posterior:</strong> Nome nativo abreviado de uma era. A era completa é representada pela constante de CAL_SERASTRING.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME1</td>
<td>Nome nativo abreviado do primeiro mês do ano.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME2</td>
<td>Nome nativo abreviado do segundo mês do ano.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME3</td>
<td>Nome nativo abreviado do terceiro mês do ano.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME4</td>
<td>Nome nativo abreviado do quarto mês do ano.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME5</td>
<td>Nome nativo abreviado do quinto mês do ano.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME6</td>
<td>Nome nativo abreviado do sexto mês do ano.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME7</td>
<td>Nome nativo abreviado do sétimo mês do ano.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME8</td>
<td>Nome nativo abreviado do oitavo mês do ano.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME9</td>
<td>Nome nativo abreviado do nono mês do ano.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME10</td>
<td>Nome nativo abreviado do décimo mês do ano.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME11</td>
<td>Nome nativo abreviado do décimo primeiro mês do ano.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME12</td>
<td>Nome nativo abreviado do décimo-mês do ano.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME13</td>
<td>Nome nativo abreviado do décimo terceiro mês do ano, se existir.</td>
</tr>
<tr class="odd">
<td>CAL_SCALNAME</td>
<td>Nome nativo do calendário alternativo.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME1</td>
<td>Nome nativo do primeiro dia da semana.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME2</td>
<td>Nome nativo do segundo dia da semana.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME3</td>
<td>Nome nativo do terceiro dia da semana.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME4</td>
<td>Nome nativo do quarto dia da semana.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME5</td>
<td>Nome nativo do quinto dia da semana.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME6</td>
<td>Nome nativo do sexto dia da semana.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME7</td>
<td>Nome nativo do sétimo dia da semana.</td>
</tr>
<tr class="odd">
<td>CAL_SERASTRING</td>
<td>Uma ou mais cadeias de caracteres terminadas em nulo que especificam cada um dos pontos de código Unicode especificando a era associada a CAL_IYEAROFFSETRANGE. A última cadeia de caracteres tem um caractere nulo de terminação extra. Esse valor varia em formato, dependendo do tipo de calendário opcional.</td>
</tr>
<tr class="even">
<td>CAL_SLONGDATE</td>
<td>Formatos de data por extenso para o tipo de calendário.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHDAY</td>
<td><strong>Windows 7 e posterior:</strong> Formato do mês e dia para o tipo de calendário. A formatação é semelhante à CAL_SLONGDATE. Por exemplo, se o padrão mês/dia for o nome completo do mês seguido do número do dia com zeros à esquerda, por exemplo, de &quot; setembro de 03 &quot; , o formato será &quot; MMMM dd &quot; . Aspas simples podem ser usadas para inserir caracteres que não são de formato, por exemplo, ' de ' em espanhol.
<blockquote>
[!Note]<br />
Este tipo de calendário dá suporte a apenas um formato.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME1</td>
<td>Nome nativo do primeiro mês do ano.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME2</td>
<td>Nome nativo do segundo mês do ano.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME3</td>
<td>Nome nativo do terceiro mês do ano.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME4</td>
<td>Nome nativo do quarto mês do ano.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME5</td>
<td>Nome nativo do quinto mês do ano.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME6</td>
<td>Nome nativo do sexto mês do ano.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME7</td>
<td>Nome nativo do sétimo mês do ano.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME8</td>
<td>Nome nativo do oitavo mês do ano.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME9</td>
<td>Nome nativo do nono mês do ano.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME10</td>
<td>Nome nativo do décimo mês do ano.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME11</td>
<td>Nome nativo do décimo primeiro mês do ano.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME12</td>
<td>Nome nativo do décimo mês do ano.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME13</td>
<td>Nome nativo do décimo terceiro mês do ano, se existir.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTDATE</td>
<td>Formatos de data abreviada para o tipo de calendário.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME1</td>
<td><strong>Windows Vista e posterior:</strong> Nome nativo curto do primeiro dia da semana.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME2</td>
<td><strong>Windows Vista e posterior:</strong> Nome nativo curto do segundo dia da semana.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME3</td>
<td><strong>Windows Vista e posterior:</strong> Nome nativo curto do terceiro dia da semana.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME4</td>
<td><strong>Windows Vista e posterior:</strong> Nome nativo curto do quarto dia da semana.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME5</td>
<td><strong>Windows Vista e posterior:</strong> Nome nativo curto do quinto dia da semana.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME6</td>
<td><strong>Windows Vista e posterior:</strong> Nome nativo curto do sexto dia da semana.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME7</td>
<td><strong>Windows Vista e posterior:</strong> Nome nativo curto do sétimo dia da semana.</td>
</tr>
<tr class="odd">
<td>CAL_SYEARMONTH</td>
<td><strong>Windows me/98, windows 2000:</strong> Os formatos de ano/mês para os calendários especificados.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Se o nome nativo do dia da semana ou de um mês for uma cadeia de caracteres vazia, esse nome será idêntico ao nome especificado nas informações de localidade correspondentes e, portanto, não será duplicado aqui.

 

 

 




