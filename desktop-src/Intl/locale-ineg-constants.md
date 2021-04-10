---
description: Este tópico define as constantes de INEG de localidade \_ \* usadas pelo NLS.
ms.assetid: 3a1e4a63-31bd-4ff9-a3ca-af357389e179
title: Constantes LOCALE_INEG *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17c61f0ca769206f30b84aa73cc3548ad9b915
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296447"
---
# <a name="locale_ineg-constants"></a>\_Constantes INEG de localidade \*

Este tópico define as constantes de INEG de localidade \_ \* usadas pelo NLS.



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
<td>LOCALE_INEGCURR</td>
<td>Modo de moeda negativa. 
<table>
<thead>
<tr class="header">
<th>Mode</th>
<th>Formato para moeda negativa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Parêntese esquerdo, símbolo monetário, número, parêntese direito; por exemplo, ($1.01)</td>
</tr>
<tr class="even">
<td>1</td>
<td>Sinal negativo, símbolo monetário, número; por exemplo,-$1.01</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Símbolo monetário, sinal negativo, número; por exemplo, US $-1,1</td>
</tr>
<tr class="even">
<td>3</td>
<td>Símbolo monetário, número, sinal negativo; por exemplo, $1.01-</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Parêntese esquerdo, número, símbolo monetário, parêntese direito; por exemplo, ($1.01)</td>
</tr>
<tr class="even">
<td>5</td>
<td>Sinal negativo, número, símbolo monetário; por exemplo,-$1.01</td>
</tr>
<tr class="odd">
<td>6</td>
<td>Número, sinal negativo, símbolo monetário; por exemplo, 1,1-$</td>
</tr>
<tr class="even">
<td>7</td>
<td>Número, símbolo monetário, sinal negativo; por exemplo, $1.01-</td>
</tr>
<tr class="odd">
<td>8</td>
<td>Sinal negativo, número, espaço, símbolo monetário (como #5, mas com um espaço antes do símbolo monetário); por exemplo,-$1.01</td>
</tr>
<tr class="even">
<td>9</td>
<td>Sinal negativo, símbolo monetário, espaço, número (como #1, mas com um espaço após o símbolo monetário); por exemplo,-$1.01</td>
</tr>
<tr class="odd">
<td>10</td>
<td>Número, espaço, símbolo monetário, sinal negativo (como #7, mas com um espaço antes do símbolo monetário); por exemplo, $1.01-</td>
</tr>
<tr class="even">
<td>11</td>
<td>Símbolo monetário, espaço, número, sinal negativo (como #3, mas com um espaço após o símbolo monetário); por exemplo, $1.01-</td>
</tr>
<tr class="odd">
<td>12</td>
<td>Símbolo monetário, espaço, sinal negativo, número (como #2, mas com um espaço após o símbolo monetário); por exemplo, US $-1,1</td>
</tr>
<tr class="even">
<td>13</td>
<td>Número, sinal negativo, espaço, símbolo monetário (como #6, mas com um espaço antes do símbolo monetário); por exemplo, 1,1-$</td>
</tr>
<tr class="odd">
<td>14</td>
<td>Parêntese esquerdo, símbolo monetário, espaço, número, parêntese direito (como #0, mas com um espaço após o símbolo monetário); por exemplo, ($1.01)</td>
</tr>
<tr class="even">
<td>15</td>
<td>Parêntese esquerdo, número, espaço, símbolo monetário, parêntese direito (como #4, mas com um espaço antes do símbolo monetário); por exemplo, ($1.01)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>LOCALE_INEGNUMBER</td>
<td>Modo de número negativo, ou seja, o formato de um número negativo. 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Formatar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Parêntese esquerdo, número, parêntese direito; por exemplo, (1,1)</td>
</tr>
<tr class="even">
<td>1</td>
<td>Sinal negativo, número; por exemplo,-1,1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Sinal negativo, espaço, número; por exemplo,-1,1</td>
</tr>
<tr class="even">
<td>3</td>
<td>Número, sinal negativo; por exemplo, 1,1-</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Número, espaço, sinal negativo; por exemplo, 1,1-</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>LOCALE_INEGSEPBYSPACE</td>
<td>Separação do sinal negativo em um valor monetário. Esse valor será 1 se o símbolo monetário for separado por um espaço do valor negativo ou 0 se não for.</td>
</tr>
<tr class="even">
<td>LOCALE_INEGSIGNPOSN</td>
<td>Índice de formatação para os valores de moeda de entrada negativos. 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Parênteses ao redor da quantidade e do símbolo monetário.</td>
</tr>
<tr class="even">
<td>1</td>
<td>O sinal precede o número.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>O sinal segue o número.</td>
</tr>
<tr class="even">
<td>3</td>
<td>O sinal precede o símbolo monetário.</td>
</tr>
<tr class="odd">
<td>4</td>
<td>O sinal segue o símbolo monetário.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>LOCALE_INEGSYMPRECEDES</td>
<td>Posição do símbolo monetário em um valor monetário negativo. Esse valor será 1 se o símbolo monetário precede o valor negativo, ou 0 se o símbolo segue o valor.</td>
</tr>
</tbody>
</table>



 

 

 



