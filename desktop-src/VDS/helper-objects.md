---
description: 'O VDS fornece dois objetos auxiliares: o objeto de enumeração e o objeto Async. Este tópico descreve cada um desses objetos e fornece links para exemplos de como os chamadores funcionam com cada um deles.'
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Objetos auxiliares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5193003abd10d9fa2c311b250272d9ad5847a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171989"
---
# <a name="helper-objects"></a><span data-ttu-id="8474f-104">Objetos auxiliares</span><span class="sxs-lookup"><span data-stu-id="8474f-104">Helper Objects</span></span>

<span data-ttu-id="8474f-105">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8474f-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="8474f-106">O VDS fornece dois objetos auxiliares: o objeto de enumeração e o objeto Async.</span><span class="sxs-lookup"><span data-stu-id="8474f-106">VDS provides two helper objects: the enumeration object and the async object.</span></span> <span data-ttu-id="8474f-107">Este tópico descreve cada um desses objetos e fornece links para exemplos de como os chamadores funcionam com cada um deles.</span><span class="sxs-lookup"><span data-stu-id="8474f-107">This topic describes each of these objects and provides links to examples of how callers work with each.</span></span>

## <a name="enumeration-object"></a><span data-ttu-id="8474f-108">Objeto de enumeração</span><span class="sxs-lookup"><span data-stu-id="8474f-108">Enumeration Object</span></span>

<span data-ttu-id="8474f-109">Um objeto de enumeração é enumerado por meio de um conjunto de objetos VDS de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="8474f-109">An enumeration object enumerates through a set of VDS objects of a given type.</span></span> <span data-ttu-id="8474f-110">Os objetos podem ser provedores, subsistemas, controladores, LUNs, plexes de LUN, unidades, pacotes de disco, discos, volumes ou plexes de volume.</span><span class="sxs-lookup"><span data-stu-id="8474f-110">Objects can be providers, subsystems, controllers, LUNs, LUN plexes, drives, disk packs, disks, volumes, or volume plexes.</span></span> <span data-ttu-id="8474f-111">Os chamadores podem obter um ponteiro para um objeto específico selecionando o objeto desejado da enumeração que é retornada pelo método apropriado.</span><span class="sxs-lookup"><span data-stu-id="8474f-111">Callers can get a pointer to a specific object by selecting the desired object from the enumeration that is returned by the appropriate method.</span></span> <span data-ttu-id="8474f-112">Para obter um exemplo de código, consulte [trabalhando com objetos de enumeração](working-with-enumeration-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8474f-112">For a code example, see [Working with Enumeration Objects](working-with-enumeration-objects.md).</span></span>

<span data-ttu-id="8474f-113">A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8474f-113">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="8474f-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="8474f-114">Type</span></span>                                              | <span data-ttu-id="8474f-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="8474f-115">Element</span></span>                                  |
|---------------------------------------------------|------------------------------------------|
| <span data-ttu-id="8474f-116">Interfaces que são sempre expostas por este objeto</span><span class="sxs-lookup"><span data-stu-id="8474f-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="8474f-117">**IEnumVdsObject**</span><span class="sxs-lookup"><span data-stu-id="8474f-117">**IEnumVdsObject**</span></span>](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| <span data-ttu-id="8474f-118">Enumerações associadas</span><span class="sxs-lookup"><span data-stu-id="8474f-118">Associated enumerations</span></span>                           | <span data-ttu-id="8474f-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8474f-119">None.</span></span>                                    |
| <span data-ttu-id="8474f-120">Estruturas associadas</span><span class="sxs-lookup"><span data-stu-id="8474f-120">Associated structures</span></span>                             | <span data-ttu-id="8474f-121">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8474f-121">None.</span></span>                                    |



 

## <a name="async-object"></a><span data-ttu-id="8474f-122">Objeto Async</span><span class="sxs-lookup"><span data-stu-id="8474f-122">Async Object</span></span>

<span data-ttu-id="8474f-123">Um objeto assíncrono gerencia operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="8474f-123">An async object manages asynchronous operations.</span></span> <span data-ttu-id="8474f-124">Os métodos que iniciam operações assíncronas retornam um ponteiro para uma interface [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) , que permite que o chamador cancele, aguarde e consulte o status da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8474f-124">Methods that initiate asynchronous operations return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface, which allows the caller to cancel, wait for, and query the status of the asynchronous operation.</span></span>

<span data-ttu-id="8474f-125">As operações de longa execução do VDS tendem a ser implementadas de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8474f-125">Long-running VDS operations tend to be implemented asynchronously.</span></span> <span data-ttu-id="8474f-126">Os programas básicos e dinâmicos do provedor de software implementam métodos assíncronos de forma consistente para operações de volume, partição e disco.</span><span class="sxs-lookup"><span data-stu-id="8474f-126">The basic and dynamic software provider programs implement asynchronous methods consistently for volume, partition, and disk operations.</span></span> <span data-ttu-id="8474f-127">Os provedores de hardware também implementam métodos assíncronos de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8474f-127">Hardware providers optionally implement async-related methods asynchronously.</span></span> <span data-ttu-id="8474f-128">Independentemente de como o provedor implementa o método, a operação deve retornar um ponteiro para uma interface [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) para o chamador.</span><span class="sxs-lookup"><span data-stu-id="8474f-128">Regardless of how the provider implements the method, the operation must return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface to the caller.</span></span> <span data-ttu-id="8474f-129">Para obter um exemplo de código, consulte [gerenciando operações assíncronas](managing-asynchronous-operations.md).</span><span class="sxs-lookup"><span data-stu-id="8474f-129">For a code example, see [Managing Asynchronous Operations](managing-asynchronous-operations.md).</span></span>

<span data-ttu-id="8474f-130">As operações assíncronas incluem:</span><span class="sxs-lookup"><span data-stu-id="8474f-130">Asynchronous operations include:</span></span>

-   <span data-ttu-id="8474f-131">Criação de um LUN, volume ou partição.</span><span class="sxs-lookup"><span data-stu-id="8474f-131">Creating a LUN, volume, or partition.</span></span>
-   <span data-ttu-id="8474f-132">Formatando um volume ou uma partição.</span><span class="sxs-lookup"><span data-stu-id="8474f-132">Formatting a volume or partition.</span></span>
-   <span data-ttu-id="8474f-133">Adicionar ou remover um plex de LUN ou volume.</span><span class="sxs-lookup"><span data-stu-id="8474f-133">Adding or removing a LUN or volume plex.</span></span>
-   <span data-ttu-id="8474f-134">Quebrando um plex de volume.</span><span class="sxs-lookup"><span data-stu-id="8474f-134">Breaking a volume plex.</span></span>
-   <span data-ttu-id="8474f-135">Estendendo ou reduzindo um LUN ou volume.</span><span class="sxs-lookup"><span data-stu-id="8474f-135">Extending or shrinking a LUN or volume.</span></span>
-   <span data-ttu-id="8474f-136">Recuperando um LUN ou volume.</span><span class="sxs-lookup"><span data-stu-id="8474f-136">Recovering a LUN or volume.</span></span>
-   <span data-ttu-id="8474f-137">Limpando um disco.</span><span class="sxs-lookup"><span data-stu-id="8474f-137">Cleaning a disk.</span></span>
-   <span data-ttu-id="8474f-138">Substituindo um disco.</span><span class="sxs-lookup"><span data-stu-id="8474f-138">Replacing a disk.</span></span>

<span data-ttu-id="8474f-139">A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8474f-139">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="8474f-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="8474f-140">Type</span></span>                                              | <span data-ttu-id="8474f-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="8474f-141">Element</span></span>                        |
|---------------------------------------------------|--------------------------------|
| <span data-ttu-id="8474f-142">Interfaces que são sempre expostas por este objeto</span><span class="sxs-lookup"><span data-stu-id="8474f-142">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="8474f-143">**IVdsAsync**</span><span class="sxs-lookup"><span data-stu-id="8474f-143">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| <span data-ttu-id="8474f-144">Enumerações associadas</span><span class="sxs-lookup"><span data-stu-id="8474f-144">Associated enumerations</span></span>                           | <span data-ttu-id="8474f-145">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8474f-145">None.</span></span>                          |
| <span data-ttu-id="8474f-146">Estruturas associadas</span><span class="sxs-lookup"><span data-stu-id="8474f-146">Associated structures</span></span>                             | <span data-ttu-id="8474f-147">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8474f-147">None.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="8474f-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8474f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8474f-149">Modelo de objeto VDS</span><span class="sxs-lookup"><span data-stu-id="8474f-149">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="8474f-150">**IVdsAsync**</span><span class="sxs-lookup"><span data-stu-id="8474f-150">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[<span data-ttu-id="8474f-151">Trabalhando com objetos de enumeração</span><span class="sxs-lookup"><span data-stu-id="8474f-151">Working with Enumeration Objects</span></span>](working-with-enumeration-objects.md)
</dt> <dt>

[<span data-ttu-id="8474f-152">Gerenciando operações assíncronas</span><span class="sxs-lookup"><span data-stu-id="8474f-152">Managing Asynchronous Operations</span></span>](managing-asynchronous-operations.md)
</dt> </dl>

 

 
