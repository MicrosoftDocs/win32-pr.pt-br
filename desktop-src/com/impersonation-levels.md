---
title: Níveis de representação (COM)
description: Se a representação for realizada com sucesso, significa que o cliente concordou em permitir que o servidor seja o cliente para algum grau.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85286e5fa880ea7620d6f6ccb6107bf139ec2005
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103823996"
---
# <a name="impersonation-levels"></a><span data-ttu-id="848b2-103">Níveis de representação</span><span class="sxs-lookup"><span data-stu-id="848b2-103">Impersonation Levels</span></span>

<span data-ttu-id="848b2-104">Se a representação for realizada com sucesso, significa que o cliente concordou em permitir que o servidor seja o cliente para algum grau.</span><span class="sxs-lookup"><span data-stu-id="848b2-104">If impersonation succeeds, it means that the client has agreed to let the server be the client to some degree.</span></span> <span data-ttu-id="848b2-105">Os graus variados de representação são chamados de *níveis de representação* e indicam a quantidade de autoridade atribuída ao servidor quando ele está representando o cliente.</span><span class="sxs-lookup"><span data-stu-id="848b2-105">The varying degrees of impersonation are called *impersonation levels*, and they indicate how much authority is given to the server when it is impersonating the client.</span></span>

<span data-ttu-id="848b2-106">Atualmente, há quatro níveis de representação: *anônimo*, *identificar*, *representar* e *delegar*.</span><span class="sxs-lookup"><span data-stu-id="848b2-106">Currently, there are four impersonation levels: *anonymous*, *identify*, *impersonate*, and *delegate*.</span></span> <span data-ttu-id="848b2-107">A lista a seguir descreve brevemente cada nível de representação:</span><span class="sxs-lookup"><span data-stu-id="848b2-107">The following list briefly describes each impersonation level:</span></span>

<dl> <dt>

<span data-ttu-id="848b2-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anônimo (RPC \_ C \_ IMP \_ nível \_ anônimo)</span><span class="sxs-lookup"><span data-stu-id="848b2-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anonymous (RPC\_C\_IMP\_LEVEL\_ANONYMOUS)</span></span>
</dt> <dd>

<span data-ttu-id="848b2-109">O cliente é anônimo ao servidor.</span><span class="sxs-lookup"><span data-stu-id="848b2-109">The client is anonymous to the server.</span></span> <span data-ttu-id="848b2-110">O processo do servidor pode representar o cliente, mas o token de representação não contém nenhuma informação sobre o cliente.</span><span class="sxs-lookup"><span data-stu-id="848b2-110">The server process can impersonate the client, but the impersonation token does not contain any information about the client.</span></span> <span data-ttu-id="848b2-111">Esse nível só tem suporte no transporte de comunicação entre processos local.</span><span class="sxs-lookup"><span data-stu-id="848b2-111">This level is only supported over the local interprocess communication transport.</span></span> <span data-ttu-id="848b2-112">Todos os outros transportes promovem silenciosamente esse nível para identificar.</span><span class="sxs-lookup"><span data-stu-id="848b2-112">All other transports silently promote this level to identify.</span></span>

</dd> <dt>

<span data-ttu-id="848b2-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identificar (identificação de nível de imp do RPC \_ C \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="848b2-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identify (RPC\_C\_IMP\_LEVEL\_IDENTIFY)</span></span>
</dt> <dd>

<span data-ttu-id="848b2-114">O nível padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="848b2-114">The system default level.</span></span> <span data-ttu-id="848b2-115">O servidor pode obter a identidade do cliente e o servidor pode representar o cliente para executar verificações de ACL.</span><span class="sxs-lookup"><span data-stu-id="848b2-115">The server can obtain the client's identity, and the server can impersonate the client to do ACL checks.</span></span>

</dd> <dt>

<span data-ttu-id="848b2-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>Impersonate (representação de nível de imp do RPC \_ C \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="848b2-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>impersonate (RPC\_C\_IMP\_LEVEL\_IMPERSONATE)</span></span>
</dt> <dd>

<span data-ttu-id="848b2-117">O servidor pode representar o contexto de segurança do cliente ao atuar em nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="848b2-117">The server can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="848b2-118">O servidor pode acessar recursos locais como o cliente.</span><span class="sxs-lookup"><span data-stu-id="848b2-118">The server can access local resources as the client.</span></span> <span data-ttu-id="848b2-119">Se o servidor for local, ele poderá acessar os recursos de rede como o cliente.</span><span class="sxs-lookup"><span data-stu-id="848b2-119">If the server is local, it can access network resources as the client.</span></span> <span data-ttu-id="848b2-120">Se o servidor for remoto, ele poderá acessar apenas os recursos que estão no mesmo computador que o servidor.</span><span class="sxs-lookup"><span data-stu-id="848b2-120">If the server is remote, it can access only resources that are on the same computer as the server.</span></span>

</dd> <dt>

<span data-ttu-id="848b2-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>delegate (delegado de nível de imp do RPC \_ C \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="848b2-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>delegate (RPC\_C\_IMP\_LEVEL\_DELEGATE)</span></span>
</dt> <dd>

<span data-ttu-id="848b2-122">O nível de representação mais avançado.</span><span class="sxs-lookup"><span data-stu-id="848b2-122">The most powerful impersonation level.</span></span> <span data-ttu-id="848b2-123">Quando esse nível é selecionado, o servidor (local ou remoto) pode representar contexto de segurança do cliente ao atuar em nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="848b2-123">When this level is selected, the server (whether local or remote) can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="848b2-124">Durante a representação, as credenciais do cliente (local e de rede) podem ser passadas para qualquer número de computadores.</span><span class="sxs-lookup"><span data-stu-id="848b2-124">During impersonation, the client's credentials (both local and network) can be passed to any number of computers.</span></span>

<span data-ttu-id="848b2-125">Para que a representação funcione no nível de representante, os seguintes requisitos devem ser atendidos:</span><span class="sxs-lookup"><span data-stu-id="848b2-125">For impersonation to work at the delegate level, the following requirements must be met:</span></span>

-   <span data-ttu-id="848b2-126">O cliente deve definir o nível de representação para o delegado de nível de imp do RPC \_ C \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="848b2-126">The client must set the impersonation level to RPC\_C\_IMP\_LEVEL\_DELEGATE.</span></span>
-   <span data-ttu-id="848b2-127">A conta do cliente não deve ser marcada como "a conta é confidencial e não pode ser delegada" no serviço de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="848b2-127">The client account must not be marked "Account is sensitive and cannot be delegated" in the Active Directory Service.</span></span>
-   <span data-ttu-id="848b2-128">A conta do servidor deve ser marcada com o atributo "confiável para delegação" no serviço de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="848b2-128">The server account must be marked with the "Trusted for delegation" attribute in the Active Directory Service.</span></span>
-   <span data-ttu-id="848b2-129">Os computadores que hospedam o cliente, o servidor e todos os servidores "downstream" devem estar em execução em um domínio.</span><span class="sxs-lookup"><span data-stu-id="848b2-129">The computers hosting the client, the server, and any "downstream" servers must all be running in a domain.</span></span>

</dd> </dl>

<span data-ttu-id="848b2-130">Ao escolher o nível de representação, o cliente informa ao servidor como ele pode ir para representar o cliente.</span><span class="sxs-lookup"><span data-stu-id="848b2-130">By choosing the impersonation level, the client tells the server how far it can go in impersonating the client.</span></span> <span data-ttu-id="848b2-131">O cliente define o nível de representação no proxy que ele usa para se comunicar com o servidor.</span><span class="sxs-lookup"><span data-stu-id="848b2-131">The client sets the impersonation level on the proxy it uses to communicate with the server.</span></span>

## <a name="setting-the-impersonation-level"></a><span data-ttu-id="848b2-132">Definindo o nível de representação</span><span class="sxs-lookup"><span data-stu-id="848b2-132">Setting the Impersonation Level</span></span>

<span data-ttu-id="848b2-133">Há duas maneiras de definir o nível de representação:</span><span class="sxs-lookup"><span data-stu-id="848b2-133">There are two ways to set the impersonation level:</span></span>

-   <span data-ttu-id="848b2-134">O cliente pode defini-lo processwide, por meio de uma chamada para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="848b2-134">The client can set it processwide, through a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="848b2-135">Um cliente pode definir a segurança em nível de proxy em uma interface de um objeto remoto por meio de uma chamada para [**IClientSecurity:: setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (ou a função auxiliar [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).</span><span class="sxs-lookup"><span data-stu-id="848b2-135">A client can set proxy-level security on an interface of a remote object through a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (or the helper function [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).</span></span>

<span data-ttu-id="848b2-136">Você define o nível de representação passando um valor xxx apropriado de nível de imp do RPC \_ C \_ \_ \_ para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) por meio do parâmetro *dwImpLevel* .</span><span class="sxs-lookup"><span data-stu-id="848b2-136">You set the impersonation level by passing an appropriate RPC\_C\_IMP\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwImpLevel* parameter.</span></span>

<span data-ttu-id="848b2-137">Serviços de autenticação diferentes dão suporte à representação em nível de delegado para diferentes extensões.</span><span class="sxs-lookup"><span data-stu-id="848b2-137">Different authentication services support delegate-level impersonation to different extents.</span></span> <span data-ttu-id="848b2-138">Por exemplo, o NTLMSSP dá suporte à representação de nível delegado entre threads e entre processos, mas não entre computadores.</span><span class="sxs-lookup"><span data-stu-id="848b2-138">For instance, NTLMSSP supports cross-thread and cross-process delegate-level impersonation, but not cross-computer.</span></span> <span data-ttu-id="848b2-139">Por outro lado, o protocolo Kerberos dá suporte à representação em nível de delegado entre limites de computador, enquanto Schannel não oferece suporte a qualquer representação no nível de delegado.</span><span class="sxs-lookup"><span data-stu-id="848b2-139">On the other hand, the Kerberos protocol supports delegate-level impersonation across computer boundaries, while Schannel does not support any impersonation at the delegate level.</span></span> <span data-ttu-id="848b2-140">Se você tiver um proxy no nível de Impersonate e desejar definir o nível de representação como delegado, [**deverá chamar**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) SetConstant usando as constantes padrão para cada parâmetro, exceto o nível de representação.</span><span class="sxs-lookup"><span data-stu-id="848b2-140">If you have a proxy at impersonate level and you want to set the impersonation level to delegate, you should call [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) using the default constants for every parameter except the impersonation level.</span></span> <span data-ttu-id="848b2-141">O COM escolherá o NTLM localmente e o protocolo Kerberos remotamente (quando o protocolo Kerberos funcionará).</span><span class="sxs-lookup"><span data-stu-id="848b2-141">COM will choose NTLM locally and the Kerberos protocol remotely (when the Kerberos protocol will work).</span></span>

## <a name="related-topics"></a><span data-ttu-id="848b2-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="848b2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="848b2-143">Delegação e representação</span><span class="sxs-lookup"><span data-stu-id="848b2-143">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> </dl>

 

 