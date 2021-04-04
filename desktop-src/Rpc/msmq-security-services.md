---
title: Serviços de segurança MSMQ
description: As mensagens RPC síncronas podem usar qualquer um dos recursos de segurança disponíveis no tempo de execução RPC. Consulte segurança para obter mais detalhes.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084716"
---
# <a name="msmq-security-services"></a><span data-ttu-id="82625-104">Serviços de segurança MSMQ</span><span class="sxs-lookup"><span data-stu-id="82625-104">MSMQ Security Services</span></span>

<span data-ttu-id="82625-105">As mensagens RPC síncronas podem usar qualquer um dos recursos de segurança disponíveis no tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="82625-105">Synchronous RPC messages can use any of the security features available from the RPC run time.</span></span> <span data-ttu-id="82625-106">Consulte [segurança](security.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="82625-106">See [Security](security.md) for more details.</span></span>

<span data-ttu-id="82625-107">Chamadas de mensagens assíncronas \[ [](/windows/desktop/Midl/message) \] não podem usar a segurança RPC porque não há handshake entre cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="82625-107">Asynchronous \[ [message](/windows/desktop/Midl/message)\] calls cannot use RPC security because there is no handshake between client and server.</span></span> <span data-ttu-id="82625-108">Na verdade, o servidor pode nem mesmo estar em execução no momento da chamada.</span><span class="sxs-lookup"><span data-stu-id="82625-108">In fact, the server may not even be running at the time of the call.</span></span> <span data-ttu-id="82625-109">Para acessar os serviços de segurança fornecidos pelo MSMQ (serviços de enfileiramento de mensagens), o aplicativo cliente deve chamar [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) para controlar o nível de autenticação e privacidade de suas chamadas para o servidor.</span><span class="sxs-lookup"><span data-stu-id="82625-109">To access the security services provided by Message Queuing Services (MSMQ), the client application should call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) to control the level of authentication and privacy for its calls to the server.</span></span>

<span data-ttu-id="82625-110">O aplicativo de servidor pode chamar [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) de dentro de uma chamada de procedimento remoto para determinar o nível de segurança para essa chamada.</span><span class="sxs-lookup"><span data-stu-id="82625-110">The server application can call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) from within a remote procedure call to determine the security level for that call.</span></span> <span data-ttu-id="82625-111">O mapeamento entre as constantes de segurança RPC e a segurança do MSMQ é mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="82625-111">The mapping between RPC security constants and MSMQ security is shown in the following table.</span></span>



| <span data-ttu-id="82625-112">Nível de segurança RPC</span><span class="sxs-lookup"><span data-stu-id="82625-112">RPC security level</span></span>                | <span data-ttu-id="82625-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="82625-113">Description</span></span>                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="82625-114">\_ \_ nenhum nível de autenticação \_ RPC</span><span class="sxs-lookup"><span data-stu-id="82625-114">RPC\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="82625-115">A chamada não é autenticada ou criptografada.</span><span class="sxs-lookup"><span data-stu-id="82625-115">The call is not authenticated or encrypted.</span></span>                                                |
| <span data-ttu-id="82625-116">\_integridade de pkt do nível de autenticação RPC \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="82625-116">RPC\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="82625-117">A chamada é autenticada usando a segurança do MSMQ.</span><span class="sxs-lookup"><span data-stu-id="82625-117">The call is authenticated using MSMQ security.</span></span>                                             |
| <span data-ttu-id="82625-118">\_privacidade do PCT no nível de autenticação RPC \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="82625-118">RPC\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="82625-119">A chamada é autenticada e criptografada à medida que ela viaja entre a fila do cliente e do servidor.</span><span class="sxs-lookup"><span data-stu-id="82625-119">The call is authenticated and encrypted as it travels between the client and server queue.</span></span> |



 

<span data-ttu-id="82625-120">O servidor também pode forçar a chamada de autenticação e criptografia chamando [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) e Configurando o RPC \_ c \_ MQ \_ authtemplate \_ nível \_ None, RPC \_ c \_ MQ \_ Authn \_ nível de autenticação do \_ PCT \_ e \_ sinalizadores de privacidade de \_ \_ \_ \_ pkt do MQ \_ de [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) RPC c.</span><span class="sxs-lookup"><span data-stu-id="82625-120">The server can also force call authentication and encryption by calling [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) and setting the RPC\_C\_MQ\_AUTHN\_LEVEL\_NONE, RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_INTEGRITY and RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_PRIVACY flags in the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure.</span></span>

 

 