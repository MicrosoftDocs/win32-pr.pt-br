---
description: Associação de volume e LUN
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Associação de volume e LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f62e599f5b5e457a1ce6dbf6a52524d1b80d1
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104172396"
---
# <a name="volume-and-lun-binding"></a><span data-ttu-id="03fe0-103">Associação de volume e LUN</span><span class="sxs-lookup"><span data-stu-id="03fe0-103">Volume and LUN Binding</span></span>

<span data-ttu-id="03fe0-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="03fe0-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="03fe0-105">A associação é a criação de volumes ou LUNs.</span><span class="sxs-lookup"><span data-stu-id="03fe0-105">Binding is the creation of volumes or LUNs.</span></span> <span data-ttu-id="03fe0-106">Os volumes consistem em extensões de disco e LUNs que consistem em extensões de unidade.</span><span class="sxs-lookup"><span data-stu-id="03fe0-106">Volumes consist of disk extents and LUNs consist of drive extents.</span></span> <span data-ttu-id="03fe0-107">A associação seleciona um conjunto de mapeamentos para recursos físicos e ocorre dentro de um subsistema, em um pacote ou em ambos.</span><span class="sxs-lookup"><span data-stu-id="03fe0-107">Binding selects for a set of mappings to physical resources and occurs within a subsystem, within a pack, or both.</span></span> <span data-ttu-id="03fe0-108">Todos os programas de provedor dão suporte a associação parcialmente direcionada a um modelo no qual o chamador especifica apenas os atributos de associação de interesse específico e permite que o provedor escolha o restante.</span><span class="sxs-lookup"><span data-stu-id="03fe0-108">All provider programs support partially directed binding a model in which the caller specifies only those binding attributes of particular interest, and allows the provider to choose the rest.</span></span> <span data-ttu-id="03fe0-109">As operações no VDS para vincular volumes e LUNs são semelhantes, mas não idênticas.</span><span class="sxs-lookup"><span data-stu-id="03fe0-109">The operations in VDS for binding volumes and LUNs are similar but not identical.</span></span> <span data-ttu-id="03fe0-110">Por exemplo, os provedores de hardware podem oferecer opções de associação adicionais.</span><span class="sxs-lookup"><span data-stu-id="03fe0-110">For example, hardware providers can offer additional binding options.</span></span>

<span data-ttu-id="03fe0-111">O VDS dá suporte aos cinco tipos de associação de volume e LUN a seguir para configurações parcialmente direcionadas.</span><span class="sxs-lookup"><span data-stu-id="03fe0-111">VDS supports the following five volume and LUN binding types for partially directed configurations.</span></span> <span data-ttu-id="03fe0-112">(Os provedores de hardware podem e oferecem suporte a muitas outras associações.)</span><span class="sxs-lookup"><span data-stu-id="03fe0-112">(Hardware providers can and do support many other bindings.)</span></span>



| <span data-ttu-id="03fe0-113">Termo</span><span class="sxs-lookup"><span data-stu-id="03fe0-113">Term</span></span>                                                                                                                                             | <span data-ttu-id="03fe0-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="03fe0-114">Description</span></span>                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03fe0-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Único</span><span class="sxs-lookup"><span data-stu-id="03fe0-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Simple</span></span><br/>                                                     | <span data-ttu-id="03fe0-116">Mapeamento linear com apenas uma extensão contígua.</span><span class="sxs-lookup"><span data-stu-id="03fe0-116">Linear mapping with one and only one contiguous extent.</span></span><br/>                             |
| <span data-ttu-id="03fe0-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Estendidos</span><span class="sxs-lookup"><span data-stu-id="03fe0-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Spanned</span></span><br/>                                                 | <span data-ttu-id="03fe0-118">Mapeamento linear com várias extensões não contíguas em vários discos ou unidades.</span><span class="sxs-lookup"><span data-stu-id="03fe0-118">Linear mapping with multiple noncontiguous extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="03fe0-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Distribuídos</span><span class="sxs-lookup"><span data-stu-id="03fe0-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Striped</span></span><br/>                                                 | <span data-ttu-id="03fe0-120">Mapeamento que intercala extensões de volume contíguas em vários discos ou unidades.</span><span class="sxs-lookup"><span data-stu-id="03fe0-120">Mapping that interleaves contiguous volume extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="03fe0-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Espelhado</span><span class="sxs-lookup"><span data-stu-id="03fe0-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Mirrored</span></span><br/>                                             | <span data-ttu-id="03fe0-122">Mapeamento que mantém duas ou mais cópias de dados idênticas.</span><span class="sxs-lookup"><span data-stu-id="03fe0-122">Mapping that maintains two or more identical data copies.</span></span><br/>                           |
| <span data-ttu-id="03fe0-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Distribuído com paridade</span><span class="sxs-lookup"><span data-stu-id="03fe0-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Striped with parity</span></span><br/> | <span data-ttu-id="03fe0-124">Mapeamento que distribui informações de verificação de paridade em vários discos ou unidades.</span><span class="sxs-lookup"><span data-stu-id="03fe0-124">Mapping that distributes parity check information across multiple disks or drives.</span></span><br/>  |



 

<span data-ttu-id="03fe0-125">As construções VDS são espelhadas, distribuídas e distribuídas com associações de paridade de mais de um membro.</span><span class="sxs-lookup"><span data-stu-id="03fe0-125">VDS constructs mirrored, striped, and striped with parity bindings from more than one member.</span></span> <span data-ttu-id="03fe0-126">Por exemplo, um espelho bidirecional tem dois membros.</span><span class="sxs-lookup"><span data-stu-id="03fe0-126">For example, a two-way mirror has two members.</span></span> <span data-ttu-id="03fe0-127">Cada membro pode ocupar extensões em mais de um disco ou unidade.</span><span class="sxs-lookup"><span data-stu-id="03fe0-127">Each member can occupy extents on more than one disk or drive.</span></span> <span data-ttu-id="03fe0-128">O VDS concatena as extensões para formar o membro e, em seguida, associa o volume ou LUN aos membros.</span><span class="sxs-lookup"><span data-stu-id="03fe0-128">VDS concatenates the extents to form the member and then binds the volume or LUN on the members.</span></span> <span data-ttu-id="03fe0-129">Um provedor pode dar suporte A todos os tipos de associação ou qualquer subconjunto.</span><span class="sxs-lookup"><span data-stu-id="03fe0-129">A provider can support all binding types, or any subset.</span></span> <span data-ttu-id="03fe0-130">No modelo de objeto do VDS, cada membro de um espelho é um objeto independente chamado de plex.</span><span class="sxs-lookup"><span data-stu-id="03fe0-130">In the VDS object model, each member of a mirror is an independent object called a plex.</span></span>

<span data-ttu-id="03fe0-131">Novamente, os tipos de volume e LUN são semelhantes, mas não são exatos.</span><span class="sxs-lookup"><span data-stu-id="03fe0-131">Again, volume and LUN types are similar, but not exact.</span></span> <span data-ttu-id="03fe0-132">Para obter uma descrição dos tipos de volume, consulte o [objeto volume](volume-object.md); para tipos de LUN, consulte o [objeto LUN](lun-object.md).</span><span class="sxs-lookup"><span data-stu-id="03fe0-132">For a description of volume types, see the [Volume Object](volume-object.md); for LUN types, see the [LUN Object](lun-object.md).</span></span> <span data-ttu-id="03fe0-133">Os tipos de associação são não tolerantes a falhas ou tolerantes a falhas.</span><span class="sxs-lookup"><span data-stu-id="03fe0-133">Binding types are either non-fault tolerant or fault tolerant.</span></span>

### <a name="non-fault-tolerant-binding"></a><span data-ttu-id="03fe0-134">Associação não tolerante a falhas</span><span class="sxs-lookup"><span data-stu-id="03fe0-134">Non-Fault Tolerant Binding</span></span>

<span data-ttu-id="03fe0-135">Os volumes não tolerantes a falhas e os LUNs não oferecem recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="03fe0-135">Non-fault tolerant volumes and LUNs do not offer disaster recovery.</span></span> <span data-ttu-id="03fe0-136">Se um dos eixos que contribui para um volume ou LUN tolerante a falhas não falhar, todo o volume ou LUN falhará.</span><span class="sxs-lookup"><span data-stu-id="03fe0-136">If one of the spindles that contributes to a non-fault tolerant volume or LUN fails, the entire volume or LUN fails.</span></span> <span data-ttu-id="03fe0-137">No Exchange para o risco de dados, os volumes tolerantes a falhas e LUNs oferecem desempenho de entrada/saída que geralmente é superior ao dos volumes tolerantes a falhas e LUNs.</span><span class="sxs-lookup"><span data-stu-id="03fe0-137">In exchange for the risk to data, non-fault tolerant volumes and LUNs offer input/output performance that is generally superior to that of fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="03fe0-138">O VDS dá suporte aos três tipos de não-tolerância a falhas a seguir: simples, estendido e distribuído.</span><span class="sxs-lookup"><span data-stu-id="03fe0-138">VDS supports the following three non-fault tolerant types: simple, spanned, and striped.</span></span>

<span data-ttu-id="03fe0-139">Simples</span><span class="sxs-lookup"><span data-stu-id="03fe0-139">Simple</span></span>

![Diagrama que mostra um tipo simples tolerante a falhas com 2 pacotes e 2 subsistemas.](images/vdssimplelunvol.png)

<span data-ttu-id="03fe0-141">Estendido</span><span class="sxs-lookup"><span data-stu-id="03fe0-141">Spanned</span></span>

![Diagrama que mostra um tipo de tolerância a falhas não com falha estendida com 1 pacote e 1 subsistema.](images/vdsspanlunvol.png)

<span data-ttu-id="03fe0-143">Distribuídos</span><span class="sxs-lookup"><span data-stu-id="03fe0-143">Striped</span></span>

![Diagrama que mostra um tipo não tolerante a falhas distribuído com 1 pacote e 1 subsistema.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a><span data-ttu-id="03fe0-145">Associação tolerante a falhas</span><span class="sxs-lookup"><span data-stu-id="03fe0-145">Fault Tolerant Binding</span></span>

<span data-ttu-id="03fe0-146">Os seguintes volumes tolerantes a falhas e LUNs oferecem recuperação de desastre.</span><span class="sxs-lookup"><span data-stu-id="03fe0-146">The following fault tolerant volumes and LUNs offer disaster recovery.</span></span> <span data-ttu-id="03fe0-147">Se um dos eixos que contribuem para um volume tolerante a falhas ou LUN falhar, os dados poderão ser recuperados.</span><span class="sxs-lookup"><span data-stu-id="03fe0-147">If one of the spindles that contributes to a fault tolerant volume or LUN fails, the data can be recovered.</span></span> <span data-ttu-id="03fe0-148">No Exchange para segurança de dados, o desempenho de entrada/saída de volumes tolerantes a falhas e LUNs é geralmente inferior ao de volumes tolerantes a falhas e LUNs.</span><span class="sxs-lookup"><span data-stu-id="03fe0-148">In exchange for data security, the input/output performance of fault tolerant volumes and LUNs is generally inferior to that of non-fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="03fe0-149">O VDS dá suporte a dois tipos de tolerância a falhas: espelhado e distribuído com paridade.</span><span class="sxs-lookup"><span data-stu-id="03fe0-149">VDS supports two fault tolerant types: mirrored and striped with parity.</span></span>

<span data-ttu-id="03fe0-150">Espelhado (espelho de três vias)</span><span class="sxs-lookup"><span data-stu-id="03fe0-150">Mirrored (three-way mirror)</span></span>

![Diagrama que mostra um tipo de tolerância a falhas de falha (espelho de 3 vias) espelhado.](images/vdsmirrorlunvol.png)

<span data-ttu-id="03fe0-152">Distribuído com paridade</span><span class="sxs-lookup"><span data-stu-id="03fe0-152">Striped with parity</span></span>

![Diagrama que mostra uma faixa com tipo tolerante a falhas de paridade.](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a><span data-ttu-id="03fe0-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03fe0-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03fe0-155">Visão geral da configuração</span><span class="sxs-lookup"><span data-stu-id="03fe0-155">Configuration Overview</span></span>](configuration.md)
</dt> <dt>

[<span data-ttu-id="03fe0-156">Objeto de volume</span><span class="sxs-lookup"><span data-stu-id="03fe0-156">Volume Object</span></span>](volume-object.md)
</dt> <dt>

[<span data-ttu-id="03fe0-157">Objeto LUN</span><span class="sxs-lookup"><span data-stu-id="03fe0-157">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

