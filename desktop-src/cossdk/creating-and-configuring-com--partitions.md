---
description: Os administradores podem usar o COM+ para criar e configurar programaticamente partições COM+.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Criando e configurando partições COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf654c25c75cc2e12f55b7ee826184fdeb04a214
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500927"
---
# <a name="creating-and-configuring-com-partitions"></a><span data-ttu-id="906c8-103">Criando e configurando partições COM+</span><span class="sxs-lookup"><span data-stu-id="906c8-103">Creating and Configuring COM+ Partitions</span></span>

<span data-ttu-id="906c8-104">Os administradores podem usar o COM+ para criar e configurar programaticamente partições COM+.</span><span class="sxs-lookup"><span data-stu-id="906c8-104">Administrators can use COM+ to programmatically create and configure COM+ partitions.</span></span> <span data-ttu-id="906c8-105">Na verdade, todas as tarefas de criação e configuração que um administrador pode fazer nos serviços de componentes ou nas ferramentas administrativas de usuários e computadores Active Directory podem ser feitas usando coleções, objetos e interfaces COM+ ou por meio da interface do sistema de Active Directory (ADSI).</span><span class="sxs-lookup"><span data-stu-id="906c8-105">In fact, all creation and configuration tasks that an administrator can do from the Component Services or the Active Directory Users and Computers administrative tools can be done by using COM+ collections, objects, and interfaces or through the Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="906c8-106">**Windows XP:** A capacidade de criar, configurar ou delegar partições COM+ não está disponível.</span><span class="sxs-lookup"><span data-stu-id="906c8-106">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="906c8-107">A partição global é a única partição COM+ disponível.</span><span class="sxs-lookup"><span data-stu-id="906c8-107">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="906c8-108">\* \* Windows 2000: \* \* o serviço de partições COM+ não está disponível no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="906c8-108">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>

> [!Note]  
> <span data-ttu-id="906c8-109">O serviço de partições COM+ não está habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="906c8-109">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="906c8-110">Para usar o serviço de partições COM+, você deve habilitá-lo por meio da ferramenta de administração de serviços de componentes ou alterando a propriedade PartitionsEnabled na coleção [**LocalComputer**](localcomputer.md) para true.</span><span class="sxs-lookup"><span data-stu-id="906c8-110">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

<span data-ttu-id="906c8-111">Para realizar tarefas relacionadas à partição, o COM+ fornece os seguintes elementos de programação:</span><span class="sxs-lookup"><span data-stu-id="906c8-111">To accomplish partition-related tasks, COM+ provides the following programming elements:</span></span>

-   <span data-ttu-id="906c8-112">Métodos e propriedades da interface [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) na classe [**COMAdminCatalog**](comadmincatalog.md) :</span><span class="sxs-lookup"><span data-stu-id="906c8-112">Methods and properties of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface on the [**COMAdminCatalog**](comadmincatalog.md) class:</span></span>
    -   <span data-ttu-id="906c8-113">Propriedade [**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) .</span><span class="sxs-lookup"><span data-stu-id="906c8-113">[**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) property.</span></span>
    -   <span data-ttu-id="906c8-114">Propriedade [**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="906c8-114">[**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) property.</span></span>
    -   <span data-ttu-id="906c8-115">Propriedade [**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) .</span><span class="sxs-lookup"><span data-stu-id="906c8-115">[**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) property.</span></span>
    -   <span data-ttu-id="906c8-116">Método [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .</span><span class="sxs-lookup"><span data-stu-id="906c8-116">[**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>
    -   <span data-ttu-id="906c8-117">Método [**Getparticionaid**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="906c8-117">[**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) method.</span></span>
    -   <span data-ttu-id="906c8-118">Método [**Getparticionaname**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) .</span><span class="sxs-lookup"><span data-stu-id="906c8-118">[**GetPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) method.</span></span>
    -   <span data-ttu-id="906c8-119">Propriedade [**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="906c8-119">[**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) property.</span></span>
-   <span data-ttu-id="906c8-120">Um conjunto de objetos COM+ para criar e gerenciar partições no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="906c8-120">A set of COM+ objects for creating and managing partitions in Active Directory.</span></span>
-   <span data-ttu-id="906c8-121">Uma chave do registro do COM+, **PartitionCache**, para alterar o tamanho do cache da partição.</span><span class="sxs-lookup"><span data-stu-id="906c8-121">A COM+ registry key, **PartitionCache**, for changing the partition cache size.</span></span>
-   <span data-ttu-id="906c8-122">Um conjunto de [coleções de administração com+](com--administration-collections.md)relacionadas a partições:</span><span class="sxs-lookup"><span data-stu-id="906c8-122">A set of partitions-related [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="906c8-123">Coleção de [**partições**](partitions.md) .</span><span class="sxs-lookup"><span data-stu-id="906c8-123">[**Partitions**](partitions.md) collection.</span></span>
    -   <span data-ttu-id="906c8-124">Coleção [**PartitionUsers**](partitionusers.md) .</span><span class="sxs-lookup"><span data-stu-id="906c8-124">[**PartitionUsers**](partitionusers.md) collection.</span></span>
    -   <span data-ttu-id="906c8-125">Coleção [**RolesForPartition**](rolesforpartition.md) .</span><span class="sxs-lookup"><span data-stu-id="906c8-125">[**RolesForPartition**](rolesforpartition.md) collection.</span></span>
    -   <span data-ttu-id="906c8-126">Coleção [**UsersInPartitionRole**](usersinpartitionrole.md) .</span><span class="sxs-lookup"><span data-stu-id="906c8-126">[**UsersInPartitionRole**](usersinpartitionrole.md) collection.</span></span>
-   <span data-ttu-id="906c8-127">Propriedades de outras [coleções de administração do com+](com--administration-collections.md):</span><span class="sxs-lookup"><span data-stu-id="906c8-127">Properties of other [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="906c8-128">Propriedade PartitionID na coleção [**ApplicationInstances**](applicationinstances.md) .</span><span class="sxs-lookup"><span data-stu-id="906c8-128">PartitionID property on the [**ApplicationInstances**](applicationinstances.md) collection.</span></span>
    -   <span data-ttu-id="906c8-129">Propriedade AppPartitionID na coleção de [**aplicativos**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="906c8-129">AppPartitionID property on the [**Applications**](applications.md) collection.</span></span>
    -   <span data-ttu-id="906c8-130">Propriedades PartitionDescription, PartitionID e PartitionName na coleção [**FilesForImport**](filesforimport.md) .</span><span class="sxs-lookup"><span data-stu-id="906c8-130">PartitionDescription, PartitionID, and PartitionName properties on the [**FilesForImport**](filesforimport.md) collection.</span></span>
    -   <span data-ttu-id="906c8-131">Propriedades DSPartitionLookupEnabled, LocalPartitionLookupEnabled e PartitionsEnabled na coleção [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="906c8-131">DSPartitionLookupEnabled, LocalPartitionLookupEnabled, and PartitionsEnabled properties on the [**LocalComputer**](localcomputer.md) collection.</span></span>
    -   <span data-ttu-id="906c8-132">Propriedades EventClassPartitionID e SubscriberPartitionID na coleção [**SubscriptionsForComponent**](subscriptionsforcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="906c8-132">EventClassPartitionID and SubscriberPartitionID properties on the [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>
    -   <span data-ttu-id="906c8-133">Propriedades EventClassPartitionID e SubscriberPartitionID na coleção [**TransientSubscriptions**](transientsubscriptions.md) .</span><span class="sxs-lookup"><span data-stu-id="906c8-133">EventClassPartitionID and SubscriberPartitionID properties on the [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="906c8-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="906c8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="906c8-135">Coletando métricas de partição</span><span class="sxs-lookup"><span data-stu-id="906c8-135">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="906c8-136">Configurando o cache de partição</span><span class="sxs-lookup"><span data-stu-id="906c8-136">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="906c8-137">Agrupando aplicativos em partições</span><span class="sxs-lookup"><span data-stu-id="906c8-137">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="906c8-138">Gerenciando partições locais</span><span class="sxs-lookup"><span data-stu-id="906c8-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="906c8-139">Gerenciando partições no Active Directory</span><span class="sxs-lookup"><span data-stu-id="906c8-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="906c8-140">Configurando direitos administrativos para uma partição</span><span class="sxs-lookup"><span data-stu-id="906c8-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



