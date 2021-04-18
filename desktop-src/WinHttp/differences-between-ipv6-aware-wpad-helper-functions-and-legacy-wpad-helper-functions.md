---
title: Funções auxiliares de WPAD IPv6-Aware e Legacy
description: Diferenças entre IPv6-Aware funções auxiliares WPAD e funções auxiliares WPAD herdadas
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511b7f04aa0a2abe04b99562c15aeb3a53bdaadf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771648"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a>Funções auxiliares de WPAD IPv6-Aware e Legacy

As tabelas a seguir explicam as diferenças entre as novas funções auxiliares WPAD e as funções auxiliares WPAD herdadas. As novas funções são marcadas com um asterisco.



<table>
<thead>
<tr class="header">
<th>Funções</th>
<th>Entrada</th>
<th>Saída</th>
<th>Motivo da alteração</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>dnsResolve</td>
<td>Host</td>
<td>Endereço IPv4</td>
<td rowspan="2">A função ex retornará uma lista de IPv6/IPv4. Necessário, uma vez que os endereços IPv6 ou IPv4 podem ter vários endereços unicast para uma única interface. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>dnsResolveEx*</td>
<td>Host</td>
<td>Lista de endereços IPv6/IPv4</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Funções</th>
<th>Entrada</th>
<th>Saída</th>
<th>Motivo da alteração</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>isresolveble</td>
<td>Host IPv4</td>
<td>VERDADEIRO/FALSO</td>
<td rowspan="2">A função ex retornará TRUE se um host puder resolver para um endereço IPv6 ou IPv4. A função Legacy retornará TRUE se o host for resolvido para um endereço IPv4. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>isResolveableEx*</td>
<td>Host IPv6/IPv4</td>
<td>VERDADEIRO/FALSO</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Funções</th>
<th>Entrada</th>
<th>Saída</th>
<th>Motivo da alteração</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>myIPAddress</td>
<td>nenhum</td>
<td>Endereço IPv4</td>
<td rowspan="2">A função ex retornará uma lista de IPv6/IPv4. Necessário, uma vez que os endereços IPv6 ou IPv4 podem ter vários endereços unicast para uma única interface $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>myIPAddressEx*</td>
<td>nenhum</td>
<td>Lista de endereços IPv6/IPv4</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Funções</th>
<th>Entrada</th>
<th>Saída</th>
<th>Motivo da alteração</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>isInNet</td>
<td>Host, padrão de endereço IP separado por pontos, máscara de endereço IP</td>
<td>VERDADEIRO/FALSO</td>
<td rowspan="2">Forneça uma forma independente da versão do IP para descobrir se um endereço IP está em uma determinada sub-rede. Além disso, a notação de máscara no IPv4 é preterida. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>isInNetEx*</td>
<td>Prefixo IP do endereço IP</td>
<td>VERDADEIRO/FALSO</td>

</tr>
</tbody>
</table>



 



| Funções           | Entrada                       | Saída                             | Motivo da alteração                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| sortIPAddressList\* | Lista de endereços IPv6/IPv4 | Lista classificada de endereços IPv6/IPv4 | Não há nenhuma função herdada equivalente porque as funções herdadas retornaram apenas um único endereço IPv4, portanto, não havia necessidade de classificar. |



 



| Funções          | Entrada | Saída                     | Motivo da alteração                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| getClientVersion\* | nenhum  | Número de versão do mecanismo WPAD | Atualmente, essa função retorna a versão 1,0. Adicionamos essa função para permitir que os administradores de ti atualizem seu WPAD para funcionar com versões diferentes do mecanismo WPAD sem causar interrupções em sua implantação existente. |



 

> [!Note]  
> Essa funcionalidade requer o Windows Internet Explorer 7 ou superior.

 

 

 



