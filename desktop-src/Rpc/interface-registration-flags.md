---
title: Sinalizadores de registro de interface (rpcdce. h)
description: As constantes a seguir são usadas no parâmetro flags das funções RpcServerRegisterIf2 e RpcServerRegisterIfEx.
ms.assetid: 387311c0-13df-4497-a0ac-ce6aec0e726c
topic_type:
- apiref
api_name:
- RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH
- RPC_IF_ALLOW_LOCAL_ONLY
- RPC_IF_AUTOLISTEN
- RPC_IF_OLE
- RPC_IF_ALLOW_UNKNOWN_AUTHORITY
- RPC_IF_ALLOW_SECURE_ONLY
- RPC_IF_SEC_NO_CACHE
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af938038d2bc7000d80268fb4cb00941f6b282b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086229"
---
# <a name="interface-registration-flags"></a>Sinalizadores de registro de interface

As constantes a seguir são usadas no parâmetro *flags* das funções [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) e [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <dt><strong>0</strong></dt> </dl></td>
<td style="text-align: left;">Semântica de interface padrão.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </dl></td>
<td style="text-align: left;">Quando esse sinalizador de interface é registrado, o tempo de execução RPC invoca o retorno de chamada de segurança registrado para todas as chamadas, independentemente da identidade, da sequência de protocolos ou do nível de autenticação do cliente.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador está disponível a partir do Windows XP com SP2 e do Windows Server 2003 com SP1. Quando esse sinalizador não é definido, o RPC filtra automaticamente todas as chamadas não autenticadas antes que elas atinjam o retorno de chamada de segurança.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">Quando esse sinalizador de interface é registrado, o tempo de execução RPC rejeita as chamadas feitas por clientes remotos. Todas as chamadas locais usando as sequências de protocolo ncadg_ * e ncacn_ * também são rejeitadas, com exceção de ncacn_np. O RPC permite chamadas de ncacn_NP somente se a chamada não vier de SRV. Chamadas de Ncalrpc são sempre processadas.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador está disponível a partir do Windows XP com SP2 e do Windows Server 2003 com SP1.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </dl></td>
<td style="text-align: left;">Esta é uma interface de <strong>escuta automática</strong> . O tempo de execução começa a escutar chamadas assim que a primeira interface de autolistagem é registrada e para de ouvir quando a última interface Autolistar é cancelada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <dt><strong>RPC_IF_OLE</strong></dt> </dl></td>
<td style="text-align: left;">Reservado para OLE. Não use esse sinalizador.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </dl></td>
<td style="text-align: left;">Atualmente não implementado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">Limita as conexões com os clientes que usam um nível de autorização superior a RPC_C_AUTHN_LEVEL_NONE. A especificação desse sinalizador permite que os clientes cheguem na sessão <strong>nula</strong> . No Windows XP e no Windows Server 2003, esses clientes não são permitidos. Os clientes que falham no teste de RPC_IF_ALLOW_SECURE_ONLY recebem um erro de RPC_S_ACCESS_DENIED. O uso do sinalizador RPC_IF_ALLOW_SECURE_ONLY não implica nem garante um alto nível de privilégio na parte do usuário que está chamando. O RPC apenas verifica se o usuário tem credenciais válidas; o usuário que está chamando pode estar usando a conta de convidado ou outras contas com poucos privilégios. Não assuma o alto privilégio quando RPC_IF_ALLOW_SECURE_ONLY é usado.<br/> <strong>Windows NT 4,0 e Windows me/98/95:  </strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </dl></td>
<td style="text-align: left;">Desabilita o cache de retorno de chamada de segurança, forçando um retorno de chamada de segurança para cada chamada RPC em uma determinada interface.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador está disponível a partir do Windows XP com SP2 e do Windows Server 2003 com SP1.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





