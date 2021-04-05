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
# <a name="interface-registration-flags"></a><span data-ttu-id="3f0b0-103">Sinalizadores de registro de interface</span><span class="sxs-lookup"><span data-stu-id="3f0b0-103">Interface Registration Flags</span></span>

<span data-ttu-id="3f0b0-104">As constantes a seguir são usadas no parâmetro *flags* das funções [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) e [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) .</span><span class="sxs-lookup"><span data-stu-id="3f0b0-104">The following constants are used in the *Flags* parameter of the [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) and [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) functions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3f0b0-105">Constante</span><span class="sxs-lookup"><span data-stu-id="3f0b0-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3f0b0-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f0b0-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <span data-ttu-id="3f0b0-107"><dt><strong>0</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3f0b0-107"><dt><strong>0</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3f0b0-108">Semântica de interface padrão.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-108">Standard interface semantics.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <span data-ttu-id="3f0b0-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3f0b0-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3f0b0-110">Quando esse sinalizador de interface é registrado, o tempo de execução RPC invoca o retorno de chamada de segurança registrado para todas as chamadas, independentemente da identidade, da sequência de protocolos ou do nível de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-110">When this interface flag is registered, the RPC runtime invokes the registered security callback for all calls, regardless of identity, protocol sequence, or authentication level of the client.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3f0b0-111">Esse sinalizador está disponível a partir do Windows XP com SP2 e do Windows Server 2003 com SP1.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-111">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span> <span data-ttu-id="3f0b0-112">Quando esse sinalizador não é definido, o RPC filtra automaticamente todas as chamadas não autenticadas antes que elas atinjam o retorno de chamada de segurança.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-112">When this flag is not set, RPC automatically filters all unauthenticated calls before they reach the security callback.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <span data-ttu-id="3f0b0-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3f0b0-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3f0b0-114">Quando esse sinalizador de interface é registrado, o tempo de execução RPC rejeita as chamadas feitas por clientes remotos.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-114">When this interface flag is registered, the RPC runtime rejects calls made by remote clients.</span></span> <span data-ttu-id="3f0b0-115">Todas as chamadas locais usando as sequências de protocolo ncadg_ \* e ncacn_ \* também são rejeitadas, com exceção de ncacn_np.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-115">All local calls using ncadg_\* and ncacn_\* protocol sequences are also rejected, with the exception of ncacn_np.</span></span> <span data-ttu-id="3f0b0-116">O RPC permite chamadas de ncacn_NP somente se a chamada não vier de SRV.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-116">RPC allows ncacn_NP calls only if the call does not come from SRV.</span></span> <span data-ttu-id="3f0b0-117">Chamadas de Ncalrpc são sempre processadas.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-117">Calls from ncalrpc are always processed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3f0b0-118">Esse sinalizador está disponível a partir do Windows XP com SP2 e do Windows Server 2003 com SP1.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-118">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <span data-ttu-id="3f0b0-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3f0b0-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3f0b0-120">Esta é uma interface de <strong>escuta automática</strong> .</span><span class="sxs-lookup"><span data-stu-id="3f0b0-120">This is an <strong>auto-listen</strong> interface.</span></span> <span data-ttu-id="3f0b0-121">O tempo de execução começa a escutar chamadas assim que a primeira interface de autolistagem é registrada e para de ouvir quando a última interface Autolistar é cancelada.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-121">The run time begins listening for calls as soon as the first autolisten interface is registered, and stops listening when the last autolisten interface is unregistered.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <span data-ttu-id="3f0b0-122"><dt><strong>RPC_IF_OLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3f0b0-122"><dt><strong>RPC_IF_OLE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3f0b0-123">Reservado para OLE.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-123">Reserved for OLE.</span></span> <span data-ttu-id="3f0b0-124">Não use esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-124">Do not use this flag.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <span data-ttu-id="3f0b0-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3f0b0-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3f0b0-126">Atualmente não implementado.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-126">Currently not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <span data-ttu-id="3f0b0-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3f0b0-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3f0b0-128">Limita as conexões com os clientes que usam um nível de autorização superior a RPC_C_AUTHN_LEVEL_NONE.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-128">Limits connections to clients that use an authorization level higher than RPC_C_AUTHN_LEVEL_NONE.</span></span> <span data-ttu-id="3f0b0-129">A especificação desse sinalizador permite que os clientes cheguem na sessão <strong>nula</strong> .</span><span class="sxs-lookup"><span data-stu-id="3f0b0-129">Specifying this flag allows clients to come through on the <strong>NULL</strong> session.</span></span> <span data-ttu-id="3f0b0-130">No Windows XP e no Windows Server 2003, esses clientes não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-130">On Windows XP and Windows Server 2003, such clients are not allowed.</span></span> <span data-ttu-id="3f0b0-131">Os clientes que falham no teste de RPC_IF_ALLOW_SECURE_ONLY recebem um erro de RPC_S_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-131">Clients that fail the RPC_IF_ALLOW_SECURE_ONLY test receive an RPC_S_ACCESS_DENIED error.</span></span> <span data-ttu-id="3f0b0-132">O uso do sinalizador RPC_IF_ALLOW_SECURE_ONLY não implica nem garante um alto nível de privilégio na parte do usuário que está chamando.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-132">Using the RPC_IF_ALLOW_SECURE_ONLY flag does not imply or guarantee a high level of privilege on the part of the calling user.</span></span> <span data-ttu-id="3f0b0-133">O RPC apenas verifica se o usuário tem credenciais válidas; o usuário que está chamando pode estar usando a conta de convidado ou outras contas com poucos privilégios.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-133">RPC only checks that the user has valid credentials; the calling user may be using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="3f0b0-134">Não assuma o alto privilégio quando RPC_IF_ALLOW_SECURE_ONLY é usado.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-134">Do not assume high privilege when RPC_IF_ALLOW_SECURE_ONLY is used.</span></span><br/> <span data-ttu-id="3f0b0-135"><strong>Windows NT 4,0 e Windows me/98/95:  </strong></span><span class="sxs-lookup"><span data-stu-id="3f0b0-135"><strong>Windows NT 4.0 and Windows Me/98/95:  </strong></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <span data-ttu-id="3f0b0-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3f0b0-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3f0b0-137">Desabilita o cache de retorno de chamada de segurança, forçando um retorno de chamada de segurança para cada chamada RPC em uma determinada interface.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-137">Disables security callback caching, forcing a security callback for each RPC call on a given interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3f0b0-138">Esse sinalizador está disponível a partir do Windows XP com SP2 e do Windows Server 2003 com SP1.</span><span class="sxs-lookup"><span data-stu-id="3f0b0-138">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="3f0b0-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f0b0-139">Requirements</span></span>



| <span data-ttu-id="3f0b0-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f0b0-140">Requirement</span></span> | <span data-ttu-id="3f0b0-141">Valor</span><span class="sxs-lookup"><span data-stu-id="3f0b0-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3f0b0-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f0b0-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3f0b0-143">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3f0b0-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3f0b0-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f0b0-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3f0b0-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3f0b0-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3f0b0-146">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3f0b0-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f0b0-147"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f0b0-147"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





