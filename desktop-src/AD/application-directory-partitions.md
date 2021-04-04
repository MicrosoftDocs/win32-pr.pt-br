---
title: Partições de diretório de aplicativos
description: No Windows Server 2003, Active Directory Domain Services dá suporte a partições de diretório de aplicativos.
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- AD de partições do diretório de aplicativos
- AD de partições de diretório de aplicativo, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a8e035231aa24569b6fad6d5a7e0e62eaa5a30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007363"
---
# <a name="application-directory-partitions"></a><span data-ttu-id="c8880-105">Partições de diretório de aplicativos</span><span class="sxs-lookup"><span data-stu-id="c8880-105">Application Directory Partitions</span></span>

<span data-ttu-id="c8880-106">No Windows Server 2003, Active Directory Domain Services dá suporte a partições de diretório de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c8880-106">In Windows Server 2003, Active Directory Domain Services support application directory partitions.</span></span> <span data-ttu-id="c8880-107">Uma partição de diretório de aplicativo pode conter uma hierarquia de qualquer tipo de objeto, exceto entidades de segurança, e pode ser configurada para replicar para qualquer conjunto de controladores de domínio na floresta.</span><span class="sxs-lookup"><span data-stu-id="c8880-107">An application directory partition can contain a hierarchy of any type of objects, except security principals, and can be configured to replicate to any set of domain controllers in the forest.</span></span> <span data-ttu-id="c8880-108">Ao contrário de uma partição de domínio, uma partição de diretório de aplicativo não precisa ser replicada para todos os controladores de domínio em um domínio e a partição pode ser replicada para controladores de domínio em domínios diferentes da floresta.</span><span class="sxs-lookup"><span data-stu-id="c8880-108">Unlike a domain partition, an application directory partition is not required to replicate to all domain controllers in a domain and the partition can replicate to domain controllers in different domains of the forest.</span></span> <span data-ttu-id="c8880-109">Para obter mais informações sobre partições de diretório de aplicativos, consulte [sobre partições de diretório de aplicativo](about-application-directory-partitions.md).</span><span class="sxs-lookup"><span data-stu-id="c8880-109">For more information about application directory partitions, see [About Application Directory Partitions](about-application-directory-partitions.md).</span></span>

<span data-ttu-id="c8880-110">Uma partição de diretório de aplicativo pode ser criada.</span><span class="sxs-lookup"><span data-stu-id="c8880-110">An application directory partition can be created.</span></span> <span data-ttu-id="c8880-111">modificado e excluído usando as operações padrão ADSI, LDAP e [System. DirectoryServices](/dotnet/api/system.directoryservices) .</span><span class="sxs-lookup"><span data-stu-id="c8880-111">modified and deleted using standard ADSI, LDAP and [System.DirectoryServices](/dotnet/api/system.directoryservices) operations.</span></span> <span data-ttu-id="c8880-112">O contexto de segurança necessário para criar e modificar uma partição de diretório de aplicativo é o mesmo que para criar uma partição de domínio.</span><span class="sxs-lookup"><span data-stu-id="c8880-112">The security context required to create and modify an application directory partition is the same as that for creating a domain partition.</span></span>

<span data-ttu-id="c8880-113">Os tópicos a seguir descrevem como trabalhar com partições de diretório de aplicativo:</span><span class="sxs-lookup"><span data-stu-id="c8880-113">The following topics describe how to work with application directory partitions:</span></span>

-   [<span data-ttu-id="c8880-114">Replicação de partição de diretório de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c8880-114">Application Directory Partition Replication</span></span>](application-directory-partition-replication.md)
-   [<span data-ttu-id="c8880-115">Segurança de partição de diretório de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c8880-115">Application Directory Partition Security</span></span>](application-directory-partition-security.md)
-   [<span data-ttu-id="c8880-116">Criando uma partição de diretório de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c8880-116">Creating an Application Directory Partition</span></span>](creating-an-application-directory-partition.md)
-   [<span data-ttu-id="c8880-117">Excluindo uma partição de diretório de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c8880-117">Deleting an Application Directory Partition</span></span>](deleting-an-application-directory-partition.md)
-   [<span data-ttu-id="c8880-118">Enumerando partições de diretório de aplicativo em uma floresta</span><span class="sxs-lookup"><span data-stu-id="c8880-118">Enumerating Application Directory Partitions in a Forest</span></span>](enumerating-application-directory-partitions-in-a-forest.md)
-   [<span data-ttu-id="c8880-119">Localizando um servidor de host de partição de diretório de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c8880-119">Locating an Application Directory Partition Host Server</span></span>](locating-an-application-directory-partition-host-server.md)
-   [<span data-ttu-id="c8880-120">Adicionando ou excluindo uma réplica de partição de diretório de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c8880-120">Adding or Deleting an Application Directory Partition Replica</span></span>](adding-or-deleting-an-application-directory-partition-replica.md)
-   [<span data-ttu-id="c8880-121">Enumerando réplicas de uma partição de diretório de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c8880-121">Enumerating Replicas of an Application Directory Partition</span></span>](enumerating-replicas-of-an-application-directory-partition.md)
-   [<span data-ttu-id="c8880-122">Modificando configuração de partição de diretório de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c8880-122">Modifying Application Directory Partition Configuration</span></span>](modifying-application-directory-partition-configuration.md)

 

 