---
description: '\_Constantes de retorno de localidade \*'
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: Constantes LOCALE_RETURN *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d3e5017a6463457b7bc36358e9956365430c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171292"
---
# <a name="locale_return-constants"></a>\_Constantes de retorno de localidade \*

Este tópico define as constantes de retorno de localidade \_ \* usadas pelo NLS.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LOCALE_RETURN_GENITIVE_NAMES</td>
<td><strong>Windows 7 e posterior:</strong> Recupere os nomes de genitive de meses, que são os nomes usados quando os nomes de mês são combinados com outros itens. Por exemplo, em ucraniano, o equivalente a janeiro é escrito &quot; Січень &quot; quando o mês é nomeado sozinho. No entanto, quando o nome do mês é usado em combinação, por exemplo, em uma data como 5 de janeiro de 2003, a forma genitive do nome é usada. Para o exemplo ucraniano, o nome do mês genitive é exibido como &quot; 5 січня 2003 &quot; . A lista de nomes de meses genitive começa com janeiro e é delimitada por ponto-e-vírgula. Se não houver nenhum mês 13, use um ponto e vírgula em seu lugar no final da lista.
<blockquote>
[!Note]<br />
Os nomes de meses genitive não existem em todos os idiomas.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>LOCALE_RETURN_NUMBER</td>
<td><strong>Windows me/98, Windows NT 4,0 e posterior:</strong> Recupere um número. Essa constante faz com que <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> ou <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> recupere um valor como um número em vez de uma cadeia de caracteres. O buffer que recebe o valor deve ser pelo menos o comprimento de um valor DWORD. Essa constante pode ser combinada com qualquer outra constante com um nome que comece com &quot; LOCALE_I &quot; .</td>
</tr>
</tbody>
</table>



 

 

 




