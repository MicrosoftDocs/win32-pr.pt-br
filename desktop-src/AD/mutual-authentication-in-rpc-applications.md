---
title: Autenticação mútua em aplicativos RPC
description: Os serviços RPC podem usar pontos de conexão de serviço para publicar por conta própria ou podem usar as APIs do serviço de nomes RPC (RpcNs).
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- Autenticação mútua no AD de aplicativos RPC
- Active Directory, usando, autenticação mútua, RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a8591056293c916205b5b600c1b1a061d169f0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823647"
---
# <a name="mutual-authentication-in-rpc-applications"></a><span data-ttu-id="a86fd-105">Autenticação mútua em aplicativos RPC</span><span class="sxs-lookup"><span data-stu-id="a86fd-105">Mutual Authentication in RPC Applications</span></span>

<span data-ttu-id="a86fd-106">Os serviços RPC podem usar pontos de conexão de serviço para publicar por conta própria ou podem usar as APIs do serviço de nomes RPC (RpcNs).</span><span class="sxs-lookup"><span data-stu-id="a86fd-106">RPC services can use service connection points to publish themselves, or they can use the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="a86fd-107">Este tópico discute como executar a autenticação mútua com um serviço RPC que se publica usando as APIs do serviço de nomes RPC (RpcNs).</span><span class="sxs-lookup"><span data-stu-id="a86fd-107">This topic discusses how to perform mutual authentication with an RPC service that publishes itself using the RPC name service (RpcNs) APIs.</span></span>

<span data-ttu-id="a86fd-108">**Para registrar um SPN no diretório**</span><span class="sxs-lookup"><span data-stu-id="a86fd-108">**To register an SPN in the directory**</span></span>

1.  <span data-ttu-id="a86fd-109">Chame a função [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para compor um SPN (nome da entidade de serviço) para o serviço.</span><span class="sxs-lookup"><span data-stu-id="a86fd-109">Call the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose a service principal name (SPN) for the service.</span></span>
2.  <span data-ttu-id="a86fd-110">Chame a função [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) para registrar o SPN na conta de serviço ou conta de computador em cujo contexto o serviço será executado.</span><span class="sxs-lookup"><span data-stu-id="a86fd-110">Call the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function to register the SPN on the service account or computer account in whose context the service will run.</span></span>

<span data-ttu-id="a86fd-111">**Para registrar um serviço com o serviço de cadastramento de RPC**</span><span class="sxs-lookup"><span data-stu-id="a86fd-111">**To register a service with the RPC naming service**</span></span>

1.  <span data-ttu-id="a86fd-112">Verifique se os SPNs apropriados estão registrados na conta sob a qual o serviço está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="a86fd-112">Verify that the appropriate SPNs are registered on the account under which the service is running.</span></span> <span data-ttu-id="a86fd-113">Para obter mais informações, consulte [tarefas de manutenção de conta de logon](logon-account-maintenance-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="a86fd-113">For more information, see [Logon Account Maintenance Tasks](logon-account-maintenance-tasks.md).</span></span>
2.  <span data-ttu-id="a86fd-114">Chame a função [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) para registrar o SPN de serviço com o serviço de autenticação RPC e especifique o **RPC \_ C \_ Authn \_ GSS \_ Negotiate** como o serviço de autenticação a ser usado.</span><span class="sxs-lookup"><span data-stu-id="a86fd-114">Call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function to register the service SPN with the RPC authentication service, and specify **RPC\_C\_AUTHN\_GSS\_NEGOTIATE** as the authentication service to use.</span></span>

<span data-ttu-id="a86fd-115">Para obter mais informações sobre como executar a autenticação mútua em um serviço RPC, consulte [escrevendo um servidor SSPI autenticado](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).</span><span class="sxs-lookup"><span data-stu-id="a86fd-115">For more information about performing mutual authentication in an RPC service, see [Writing an Authenticated SSPI Server](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).</span></span>

<span data-ttu-id="a86fd-116">**Para autenticar o serviço do cliente**</span><span class="sxs-lookup"><span data-stu-id="a86fd-116">**To authenticate the service from the client**</span></span>

1.  <span data-ttu-id="a86fd-117">Extraia o nome do host da Associação RPC.</span><span class="sxs-lookup"><span data-stu-id="a86fd-117">Extract the host name from the RPC Binding.</span></span>
2.  <span data-ttu-id="a86fd-118">Redija o SPN para o serviço chamando a função [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) com a classe de serviço, o nome do host DNS e o nome do serviço; Esse é o nome distinto do ponto de conexão no caso de RpcNs.</span><span class="sxs-lookup"><span data-stu-id="a86fd-118">Compose the SPN for the service by calling the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function with the service class, the DNS host name, and the service name; that is the distinguished name of the connection point in the case of RpcNs.</span></span>

    <span data-ttu-id="a86fd-119">Para obter mais informações sobre como compor um SPN para um serviço de RpcNs, consulte [composição de SPNs para um serviço de RpcNs](composing-spns-for-an-rpcns-service.md).</span><span class="sxs-lookup"><span data-stu-id="a86fd-119">For more information about composing an SPN for an RpcNs service, see [Composing SPNs for an RpcNs Service](composing-spns-for-an-rpcns-service.md).</span></span>

3.  <span data-ttu-id="a86fd-120">Configure uma estrutura [**de \_ \_ QoS de segurança RPC**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) para solicitar autenticação mútua.</span><span class="sxs-lookup"><span data-stu-id="a86fd-120">Set up an [**RPC\_SECURITY\_QOS**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) structure to request mutual authentication.</span></span>
4.  <span data-ttu-id="a86fd-121">Chame a função [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) para definir os dados de autenticação para a associação RPC.</span><span class="sxs-lookup"><span data-stu-id="a86fd-121">Call the [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function to set the authentication data for the RPC binding.</span></span> <span data-ttu-id="a86fd-122">O cliente deve solicitar pelo menos **a \_ \_ integridade de \_ pkt do \_ nível \_ de autenticação RPC C** para garantir que as comunicações não tenham sido adulteradas.</span><span class="sxs-lookup"><span data-stu-id="a86fd-122">The client must request at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY** to ensure that communications have not been tampered.</span></span> <span data-ttu-id="a86fd-123">Para aumentar a segurança, o cliente deve especificar a **privacidade do PCT do \_ nível de \_ autenticação \_ \_ \_ RPC C** para solicitar a criptografia.</span><span class="sxs-lookup"><span data-stu-id="a86fd-123">For increased security, the client should specify **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** to request encryption.</span></span>
5.  <span data-ttu-id="a86fd-124">Execute a chamada RPC.</span><span class="sxs-lookup"><span data-stu-id="a86fd-124">Perform the RPC call.</span></span>

<span data-ttu-id="a86fd-125">Para obter mais informações sobre como executar a autenticação mútua em um cliente RPC, consulte [escrevendo um cliente SSPI autenticado](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).</span><span class="sxs-lookup"><span data-stu-id="a86fd-125">For more information about performing mutual authentication in an RPC client, see [Writing an Authenticated SSPI Client](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).</span></span>

<span data-ttu-id="a86fd-126">**Para autenticar o cliente do serviço**</span><span class="sxs-lookup"><span data-stu-id="a86fd-126">**To authenticate the client from the service**</span></span>

1.  <span data-ttu-id="a86fd-127">Chame a função [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) para verificar os parâmetros de autenticação especificados pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="a86fd-127">Call the [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) function to verify the authentication parameters specified by the client.</span></span> <span data-ttu-id="a86fd-128">Se o cliente não tiver solicitado o nível de autenticação desejado, rejeite a chamada.</span><span class="sxs-lookup"><span data-stu-id="a86fd-128">If the client has not requested the desired level of authentication, reject the call.</span></span> <span data-ttu-id="a86fd-129">Lembre-se de que um serviço RPC deve verificar o nível de autenticação, o serviço de autenticação e a identidade do cliente em cada chamada para garantir que o cliente tenha sido autenticado corretamente.</span><span class="sxs-lookup"><span data-stu-id="a86fd-129">Be aware that an RPC service must verify the authentication level, authentication service, and client identity on every call to ensure that the client has been properly authenticated.</span></span>
2.  <span data-ttu-id="a86fd-130">Chame a função [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) para representar o cliente.</span><span class="sxs-lookup"><span data-stu-id="a86fd-130">Call the [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) function to impersonate the client.</span></span>
3.  <span data-ttu-id="a86fd-131">Execute a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="a86fd-131">Perform the requested operation.</span></span>
4.  <span data-ttu-id="a86fd-132">Chame a função [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) para reverter para o contexto de segurança do serviço.</span><span class="sxs-lookup"><span data-stu-id="a86fd-132">Call the [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) function to revert to the service security context.</span></span>

<span data-ttu-id="a86fd-133">Para obter mais informações sobre a representação do cliente RPC, consulte [representação do cliente](/windows/desktop/Rpc/client-impersonation).</span><span class="sxs-lookup"><span data-stu-id="a86fd-133">For more information about RPC client impersonation, see [Client Impersonation](/windows/desktop/Rpc/client-impersonation).</span></span>

<span data-ttu-id="a86fd-134">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="a86fd-134">For more information, see:</span></span>

-   [<span data-ttu-id="a86fd-135">Publicando com o serviço de nomes RPC (RpcNs)</span><span class="sxs-lookup"><span data-stu-id="a86fd-135">Publishing with the RPC Name Service (RpcNs)</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="a86fd-136">Noções básicas de segurança RPC</span><span class="sxs-lookup"><span data-stu-id="a86fd-136">RPC Security Essentials</span></span>](/windows/desktop/Rpc/rpc-security-essentials)

 

 