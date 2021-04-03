---
description: Descreve os formatos de data com suporte para uso na cláusula WHERE do WQL.
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: Formatos de data WQL-Supported
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01e5741de24943defc4df0e59e7255bc1a37effd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828656"
---
# <a name="wql-supported-date-formats"></a>Formatos de data WQL-Supported

Além do formato de data e **hora** do WMI, os seguintes formatos de datas têm suporte para uso na cláusula **Where** do WQL.

O formato de hora exibido é diferente para localidades diferentes. Os scripts que se conectam a computadores remotos devem especificar a hora no formato apropriado para a localidade do computador de destino.

Por exemplo, o Estados Unidos formato de data e hora é MM-DD-AAAA. Se um script em um computador dos EUA se conecta a um computador de destino em uma localidade onde o formato é DD-MM-AAAA, as consultas são processadas no computador de destino como DD-MM-AAAA. Para evitar resultados diferentes entre as localidades, use o formato [**DateTime**](datetime.md) . Para obter mais informações, consulte [formato de data e hora](date-and-time-format.md).



<table>
<thead>
<tr class="header">
<th>Formatar</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Mon [th] dd [,] [AA] AA</td>
<td>Mês (escrito ou abreviado em três letras), dia, vírgula opcional e dois ou ano de quatro dígitos.<br/> <dl> 21 de janeiro de 1932<br />
21 de janeiro de 32<br />
Jan 21 1932<br />
Jan 21 32<br />
</dl></td>
</tr>
<tr class="even">
<td>Mon [th] [,] aaaa</td>
<td>Mês (escrito ou abreviado em três letras), vírgula opcional e ano de quatro dígitos.<br/> <dl> Janeiro de 1932<br />
Jan 1932<br />
</dl></td>
</tr>
<tr class="odd">
<td>Mon [th] [AA] aa dd</td>
<td>Mês (escrito ou abreviado em três letras), dois ou quatro dígitos de ano e dia.<br/> <dl> Janeiro de 1932 21<br />
Jan 32 21<br />
</dl></td>
</tr>
<tr class="even">
<td>DD MON [th] [,] [] [AA] AA</td>
<td>Dia do mês, mês (escrito ou abreviado em três letras), vírgula opcional, espaço opcional e dois ou ano de quatro dígitos.<br/> <dl> 21 de janeiro de 1932<br />
21 Jan32<br />
</dl></td>
</tr>
<tr class="odd">
<td>DD [AA] AA Mon [th]</td>
<td>Dia do mês, dois ou quatro dígitos de ano e mês (a grafia ou abreviada em três letras).<br/> <dl> 21 1932 de janeiro<br />
</dl></td>
</tr>
<tr class="even">
<td>[AA] AA Mon [th] dd</td>
<td>Ano de dois ou quatro dígitos, mês (escrito ou abreviado em três letras) e dia.<br/> <dl> 21 a 1932 de janeiro<br />
</dl></td>
</tr>
<tr class="odd">
<td>aaaa Mon [th]</td>
<td>Ano e mês de dois ou quatro dígitos (ou seja, escrito ou abreviado em três letras).<br/> <dl> 1932 de janeiro<br />
</dl></td>
</tr>
<tr class="even">
<td>aaaa DD MON [th]</td>
<td>Ano, dia e mês de dois ou quatro dígitos (por escrito ou abreviado em três letras).<br/> <dl> 1932 21 de janeiro<br />
</dl></td>
</tr>
<tr class="odd">
<td>D M {/-.} DD {/-.} [AA] AA</td>
<td>Mês, dia e dois ou um ano de quatro dígitos. Observe que os separadores devem ser iguais.<br/></td>
</tr>
<tr class="even">
<td>DD {/-.} D M {/-.} [AA] AA</td>
<td>Dia do mês, mês e dois ou ano de quatro dígitos. Observe que os separadores devem ser iguais.<br/></td>
</tr>
<tr class="odd">
<td>D M {/-.} [AA] AA {/-.} yyyy</td>
<td>Mês, dois ou quatro dígitos de ano e dia. Observe que os separadores devem ser iguais.<br/></td>
</tr>
<tr class="even">
<td>DD {/-.} [AA] AA {/-.} D D</td>
<td>Dia do mês, dois ou quatro dígitos de ano e mês. Observe que os separadores devem ser iguais.<br/></td>
</tr>
<tr class="odd">
<td>[AA] AA {/-.} DD {/-.} D D</td>
<td>Ano, dia e mês de dois ou quatro dígitos. Observe que os separadores devem ser iguais.<br/></td>
</tr>
<tr class="even">
<td>[AA] AA {/-.} D M {/-.} yyyy</td>
<td>Ano, mês e dia de dois ou quatro dígitos. Observe que os separadores devem ser iguais.<br/></td>
</tr>
<tr class="odd">
<td>[AA] yyMMdd</td>
<td>Ano, mês e dia de dois ou quatro dígitos, sem espaços.<br/></td>
</tr>
<tr class="even">
<td>aaaa [MM [DD]]</td>
<td>Ano de dois ou quatro dígitos, mês opcional e dia opcional, sem espaços.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cláusula WHERE](where-clause.md)
</dt> </dl>

 

 




