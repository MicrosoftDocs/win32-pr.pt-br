---
title: Publicação de serviço
description: Os serviços se anunciam usando objetos armazenados no Active Directory Domain Services.
ms.assetid: 69e9256f-40ee-4aed-8213-1bbda0e508af
ms.tgt_platform: multiple
keywords:
- ANÚNCIO de publicação de serviço
- Active Directory, usando, publicação de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9437d9f4aa5184c53f2962d7b2640e933107501f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004896"
---
# <a name="service-publication"></a><span data-ttu-id="841e3-105">Publicação de serviço</span><span class="sxs-lookup"><span data-stu-id="841e3-105">Service Publication</span></span>

<span data-ttu-id="841e3-106">Os serviços se anunciam usando objetos armazenados no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="841e3-106">Services advertise themselves using objects stored in Active Directory Domain Services.</span></span> <span data-ttu-id="841e3-107">Isso é conhecido como *publicação de serviço*.</span><span class="sxs-lookup"><span data-stu-id="841e3-107">This is known as *service publication*.</span></span> <span data-ttu-id="841e3-108">Os clientes consultam o diretório para localizar serviços.</span><span class="sxs-lookup"><span data-stu-id="841e3-108">Clients query the directory to locate services.</span></span> <span data-ttu-id="841e3-109">Isso é chamado *de reunião do serviço cliente*.</span><span class="sxs-lookup"><span data-stu-id="841e3-109">This is called *client-service rendezvous*.</span></span> <span data-ttu-id="841e3-110">Esta seção aborda os tipos de objetos de diretório usados para publicação de serviço e explica como eles são usados para a reunião do serviço de cliente.</span><span class="sxs-lookup"><span data-stu-id="841e3-110">This section discusses the types of directory objects used for service publication and explains how they are used for client-service rendezvous.</span></span>

<span data-ttu-id="841e3-111">Esta seção aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="841e3-111">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="841e3-112">Uma visão geral da publicação de serviço</span><span class="sxs-lookup"><span data-stu-id="841e3-112">An overview of service publication</span></span>](about-service-publication.md)
-   [<span data-ttu-id="841e3-113">Problemas de segurança para publicação de serviço</span><span class="sxs-lookup"><span data-stu-id="841e3-113">Security issues for service publication</span></span>](security-issues-for-service-publication.md)
-   [<span data-ttu-id="841e3-114">Objetos de ponto de conexão</span><span class="sxs-lookup"><span data-stu-id="841e3-114">Connection point objects</span></span>](connection-points.md)
-   [<span data-ttu-id="841e3-115">Publicando com pontos de conexão de serviço (SCPs)</span><span class="sxs-lookup"><span data-stu-id="841e3-115">Publishing with service connection points (SCPs)</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="841e3-116">Quais informações armazenar em um ponto de conexão de serviço</span><span class="sxs-lookup"><span data-stu-id="841e3-116">What information to store in a service connection point</span></span>](service-connection-point-properties.md)
-   [<span data-ttu-id="841e3-117">Onde criar um ponto de conexão de serviço</span><span class="sxs-lookup"><span data-stu-id="841e3-117">Where to create a service connection point</span></span>](where-to-create-a-service-connection-point.md)
-   [<span data-ttu-id="841e3-118">Como publicar serviços replicáveis, baseados em host e de banco de dados usando pontos de conexão de serviço</span><span class="sxs-lookup"><span data-stu-id="841e3-118">How to publish replicable, host-based, and database services using service connection points</span></span>](service-connection-points-for-replicated-host-based-and-database-services.md)
-   [<span data-ttu-id="841e3-119">Criando e mantendo um ponto de conexão de serviço</span><span class="sxs-lookup"><span data-stu-id="841e3-119">Creating and maintaining a service connection point</span></span>](creating-and-maintaining-a-service-connection-point.md)
-   [<span data-ttu-id="841e3-120">Como um cliente consulta um SCP e o usa para associar a uma instância de serviço</span><span class="sxs-lookup"><span data-stu-id="841e3-120">How a client queries for an SCP and uses it to bind to a service instance</span></span>](how-clients-find-and-use-a-service-connection-point.md)
-   [<span data-ttu-id="841e3-121">Usando as APIs do serviço de nomes RPC (RpcNs) para publicar um serviço RPC</span><span class="sxs-lookup"><span data-stu-id="841e3-121">Using the RPC name service (RpcNs) APIs to publish an RPC service</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="841e3-122">RnR (registro e resolução do Windows Sockets) para publicar um serviço do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="841e3-122">Windows Sockets registration and resolution (RnR) to publish a Windows Sockets service</span></span>](publishing-with-windows-sockets-registration-and-resolution.md)
-   [<span data-ttu-id="841e3-123">Publicação de serviços baseados em COM no repositório de classe COM+</span><span class="sxs-lookup"><span data-stu-id="841e3-123">Publication of COM-based services in the COM+ class store</span></span>](publishing-com-services.md)

<span data-ttu-id="841e3-124">Para obter mais informações sobre como os serviços e clientes se autenticam, consulte [autenticação mútua usando o Kerberos](mutual-authentication-using-kerberos.md).</span><span class="sxs-lookup"><span data-stu-id="841e3-124">For more information about how services and clients authenticate each other, see [Mutual Authentication Using Kerberos](mutual-authentication-using-kerberos.md).</span></span> <span data-ttu-id="841e3-125">Para obter mais informações sobre contextos de segurança de serviço e contas de logon, consulte [contas de logon de serviço](service-logon-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="841e3-125">For more information about service security contexts and logon accounts, see [Service Logon Accounts](service-logon-accounts.md).</span></span>

 

 




