---
description: IDIGITSUBSTITUTION de localidade \_
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c063ed5b937c3e4c4ae06e40631b9795f6a73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089855"
---
# <a name="locale_idigitsubstitution"></a>IDIGITSUBSTITUTION de localidade \_

**Windows 2000:** A forma de dígitos. Por exemplo, os dígitos arábico, tailandês e Índico têm formas clássicas diferentes dos dígitos europeus. Para localidades com [ \_ SNATIVEDIGITS de localidade](locale-snative-constants.md) especificadas como valores diferentes de ASCII 0-9, esse valor especifica se a preferência deve ser dada a esses outros dígitos para fins de exibição. Por exemplo, se um valor de 2 for escolhido, os dígitos especificados pela localidade \_ SNATIVEDIGITS sempre serão usados. Se um 1 for escolhido, os dígitos ASCII 0-9 serão sempre usados. Se um 0 for escolhido, o ASCII será usado em algumas circunstâncias e os dígitos especificados por \_ SNATIVEDIGITS de localidade serão usados em outros, dependendo do contexto.



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
<td>0</td>
<td>Substituição baseada em contexto. Os dígitos são exibidos com base no texto anterior na mesma saída. Os dígitos europeus seguem scripts latinos, Arabic-Indic dígitos seguem texto em árabe e outros dígitos nacionais seguem texto escrito em vários outros scripts. Quando não há texto anterior, a localidade e a ordem de leitura exibida determinam a substituição de dígitos, conforme mostrado na tabela a seguir.
<table>
<thead>
<tr class="header">
<th>Locale</th>
<th>Sentido de leitura</th>
<th>Dígitos usados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Árabe</td>
<td>Da direita para a esquerda</td>
<td>Indo-arábico</td>
</tr>
<tr class="even">
<td>Tailandês</td>
<td>Da esquerda para a direita</td>
<td>Dígitos tailandeses</td>
</tr>
<tr class="odd">
<td>Todos os outros</td>
<td>Qualquer</td>
<td>Nenhuma substituição usada</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>1</td>
<td>Nenhuma substituição foi usada. Compatibilidade total com Unicode.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Substituição de dígito nativo. As formas nacionais são exibidas de acordo com LOCALE_SNATIVEDIGITS.</td>
</tr>
</tbody>
</table>



 

 

 



