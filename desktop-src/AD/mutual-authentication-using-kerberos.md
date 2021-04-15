---
title: Autenticação mútua usando Kerberos
description: A autenticação mútua é um recurso de segurança no qual um processo de cliente deve provar sua identidade para um serviço, e o serviço deve provar sua identidade para o cliente, antes que qualquer tráfego de aplicativo seja transmitido pela conexão de cliente/serviço.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, usando a autenticação mútua
- Active Directory, usando, segurança, autenticação mútua
- ANÚNCIO de segurança
- segurança do AD, autenticação mútua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cf2e68c1983dde9221cc3fa89866b5358ee6eb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105753621"
---
# <a name="mutual-authentication-using-kerberos"></a><span data-ttu-id="68d09-107">Autenticação mútua usando Kerberos</span><span class="sxs-lookup"><span data-stu-id="68d09-107">Mutual Authentication Using Kerberos</span></span>

<span data-ttu-id="68d09-108">A autenticação mútua é um recurso de segurança no qual um processo de cliente deve provar sua identidade para um serviço, e o serviço deve provar sua identidade para o cliente, antes que qualquer tráfego de aplicativo seja transmitido pela conexão de cliente/serviço.</span><span class="sxs-lookup"><span data-stu-id="68d09-108">Mutual authentication is a security feature in which a client process must prove its identity to a service, and the service must prove its identity to the client, before any application traffic is transmitted over the client/service connection.</span></span>

<span data-ttu-id="68d09-109">Active Directory Domain Services e Windows oferecem suporte para SPN (nomes de entidade de serviço), que são um componente-chave no mecanismo Kerberos pelo qual um cliente autentica um serviço.</span><span class="sxs-lookup"><span data-stu-id="68d09-109">Active Directory Domain Services and Windows provide support for service principal names (SPN), which are a key component in the Kerberos mechanism by which a client authenticates a service.</span></span> <span data-ttu-id="68d09-110">Um SPN é um nome exclusivo que identifica uma instância de um serviço e está associado à conta de logon na qual a instância de serviço é executada.</span><span class="sxs-lookup"><span data-stu-id="68d09-110">An SPN is a unique name that identifies an instance of a service and is associated with the logon account under which the service instance runs.</span></span> <span data-ttu-id="68d09-111">Os componentes de um SPN são de tal forma que um cliente pode compor um SPN para um serviço sem a conta de logon do serviço.</span><span class="sxs-lookup"><span data-stu-id="68d09-111">The components of an SPN are such that a client can compose an SPN for a service without the service logon account.</span></span> <span data-ttu-id="68d09-112">Isso permite que o cliente solicite ao serviço que autentique sua conta, mesmo que o cliente não tenha o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="68d09-112">This enables the client to request the service to authenticate its account even though the client does not have the account name.</span></span>

<span data-ttu-id="68d09-113">Esta seção inclui uma visão geral do:</span><span class="sxs-lookup"><span data-stu-id="68d09-113">This section includes an overview of:</span></span>

-   <span data-ttu-id="68d09-114">Autenticação mútua usando Kerberos.</span><span class="sxs-lookup"><span data-stu-id="68d09-114">Mutual authentication using Kerberos.</span></span>
-   <span data-ttu-id="68d09-115">Compor um SPN exclusivo.</span><span class="sxs-lookup"><span data-stu-id="68d09-115">Composing a unique SPN.</span></span>
-   <span data-ttu-id="68d09-116">Como um instalador de serviço registra SPNs no objeto de conta associado a uma instância de serviço.</span><span class="sxs-lookup"><span data-stu-id="68d09-116">How a service installer registers SPNs on the account object associated with a service instance.</span></span>
-   <span data-ttu-id="68d09-117">Como um aplicativo cliente usa um objeto SCP (ponto de conexão de serviço) da instância de serviço no Active Directory Domain Services para recuperar dados dos quais compor um SPN para o serviço.</span><span class="sxs-lookup"><span data-stu-id="68d09-117">How a client application uses a service instance's service connection point (SCP) object in Active Directory Domain Services to retrieve data from which to compose an SPN for the service.</span></span>
-   <span data-ttu-id="68d09-118">Como um aplicativo cliente usa um SPN de serviço em conjunto com a interface de provedor de suporte de segurança (SSPI) para autenticar o serviço.</span><span class="sxs-lookup"><span data-stu-id="68d09-118">How a client application uses a service SPN in conjunction with the Security Support Provider Interface (SSPI) to authenticate the service.</span></span>
-   <span data-ttu-id="68d09-119">Um exemplo de código para um aplicativo de serviço/cliente do Windows Sockets que usa um SCP e SSPI para executar a autenticação mútua.</span><span class="sxs-lookup"><span data-stu-id="68d09-119">A code example for a Windows Sockets client/service application that uses an SCP and SSPI to perform mutual authentication.</span></span>
-   <span data-ttu-id="68d09-120">Um exemplo de código para um cliente/serviço RPC que executa autenticação mútua usando o serviço de nome RPC e a autenticação RPC.</span><span class="sxs-lookup"><span data-stu-id="68d09-120">A code example for an RPC client/service that performs mutual authentication using the RPC name service and RPC authentication.</span></span>
-   <span data-ttu-id="68d09-121">Como um serviço de RnR (registro e resolução do Windows Sockets) usa SPNs para executar a autenticação mútua.</span><span class="sxs-lookup"><span data-stu-id="68d09-121">How a Windows Sockets Registration and Resolution (RnR) service uses SPNs to perform mutual authentication.</span></span>

<span data-ttu-id="68d09-122">Esta seção aborda o uso do serviço Domínio do Active Directory para autenticação mútua, em particular, a finalidade dos pontos de conexão de serviço e nomes de entidade de serviço na autenticação mútua.</span><span class="sxs-lookup"><span data-stu-id="68d09-122">This section discusses using Active Directory Domain Service for mutual authentication, in particular, the purpose of service connection points and service principal names in mutual authentication.</span></span> <span data-ttu-id="68d09-123">Não é uma discussão completa de como usar SSPI para autenticação mútua ou autenticação e suporte de segurança disponíveis para aplicativos RPC e Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="68d09-123">It is not a complete discussion of how to use SSPI for mutual authentication or the authentication and security support available for RPC and Windows Sockets applications.</span></span>

<span data-ttu-id="68d09-124">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="68d09-124">For more information, see:</span></span>

-   [<span data-ttu-id="68d09-125">Publicando com pontos de conexão de serviço</span><span class="sxs-lookup"><span data-stu-id="68d09-125">Publishing with service connection points</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="68d09-126">SSPI</span><span class="sxs-lookup"><span data-stu-id="68d09-126">SSPI</span></span>](/windows/desktop/SecAuthN/sspi)
-   [<span data-ttu-id="68d09-127">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="68d09-127">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [<span data-ttu-id="68d09-128">RPC</span><span class="sxs-lookup"><span data-stu-id="68d09-128">RPC</span></span>](/windows/desktop/Rpc/rpc-start-page)

 

 