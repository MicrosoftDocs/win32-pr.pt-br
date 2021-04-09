---
description: Esta página descreve o comportamento das opções de soquete multicast com base em vários Estados de configurações de opção de soquete.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Comportamento da opção de soquete multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd10094750bea59b844ad1fcdac70be0c7f9646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010486"
---
# <a name="multicast-socket-option-behavior"></a>Comportamento da opção de soquete multicast

Esta página descreve o comportamento das opções de soquete multicast com base em vários Estados de configurações de opção de soquete.

Por exemplo, esta página descreve o comportamento quando a opção de soquete de associação de origem de adição de IP \_ \_ \_ é definida em um soquete para o qual a \_ opção de associação de origem Adicionar IP \_ \_ já foi definida com o par de grupo/origem especificado na mesma interface de rede. É permitido chamar IP \_ Adicionar Associação de \_ origem \_ no mesmo grupo em uma interface de rede diferente.

Esta página ajuda a projetar e solucionar corretamente os aplicativos de multicast do Windows Sockets. 

<table>
<thead>
<tr class="header">
<th>Opção de soquete inicial</th>
<th>Opção de soquete subsequente em conflito</th>
<th>Erro retornado</th>
<th>Comentários</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">IP_ADD_MEMBERSHIP $ {REMOVER} $<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Não chame IP_ADD_MEMBERSHIP com o mesmo grupo mais de uma vez na mesma interface de rede.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Não chame IP_ADD_SOURCE_MEMBERSHIP com o mesmo grupo chamado anteriormente com IP_ADD_MEMBERSHIP na mesma interface de rede.</td>

</tr>
<tr class="odd">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Em vez disso, use IP_BLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Retorna um erro ao tentar desbloquear um par de grupo/fonte que não foi bloqueado anteriormente na mesma interface de rede.</td>

</tr>
<tr class="odd">
<td>IP_DROP_MEMBERSHIP</td>
<td>Qualquer chamada subsequente no mesmo grupo ou par de origem/grupo</td>
<td>WSAEINVAL</td>
<td>Fazer chamadas de opção de soquete em um grupo ou par de origem que não está atualmente na lista de inclusão (devido à remoção de associação, ou de outra forma) resulta em um erro.</td>
</tr>
<tr class="even">
<td rowspan="3">IP_ADD_SOURCE_MEMBERSHIP $ {REMOVER} $<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Não chame IP_ADD_MEMBERSHIP com o mesmo grupo chamado anteriormente com IP_ADD_SOURCE_MEMBERSHIP na mesma interface de rede.</td>
</tr>
<tr class="odd">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Não chame IP_ADD_SOURCE_MEMBERSHIP com o mesmo par de grupo/fonte chamado anteriormente com IP_ADD_SOURCE_MEMBERSHIP na mesma interface de rede.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Retorna um erro ao tentar desbloquear um par de grupo/fonte que não foi bloqueado anteriormente na mesma interface de rede.</td>

</tr>
<tr class="odd">
<td rowspan="2">IP_DROP_SOURCE_MEMBERSHIP $ {REMOVER} $<br />
</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Retorna um erro ao tentar desbloquear um par de grupo/fonte que não foi bloqueado anteriormente na mesma interface de rede.</td>
</tr>
<tr class="even">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Retorna um erro ao tentar descartar um par de grupo/fonte que não está na lista de inclusão na mesma interface de rede.</td>

</tr>
<tr class="odd">
<td rowspan="3">IP_BLOCK_SOURCE $ {REMOVER} $<br />
</td>
<td>IP_BLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Retorna um erro ao tentar bloquear um par de grupo/fonte que já está bloqueado na mesma interface de rede.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Em vez disso, use IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="odd">
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Em vez disso, use IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Retorna um erro ao tentar desbloquear um par de grupo/fonte que não está na lista bloqueada na mesma interface de rede.</td>
</tr>
</tbody>
</table>



 

 

 



