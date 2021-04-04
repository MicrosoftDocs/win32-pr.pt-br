---
description: Objetos de provedor de software
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Objetos de provedor de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16f81cd975c892760d1851720e65584453e7745
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "103837547"
---
# <a name="software-provider-objects"></a><span data-ttu-id="490dd-103">Objetos de provedor de software</span><span class="sxs-lookup"><span data-stu-id="490dd-103">Software Provider Objects</span></span>

<span data-ttu-id="490dd-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="490dd-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="490dd-105">Objetos de provedor de software modelam dispositivos físicos, como discos IDE e CD-ROMs, e elementos virtuais como pacotes, volumes e plexes de volume.</span><span class="sxs-lookup"><span data-stu-id="490dd-105">Software provider objects model physical devices, such as IDE disks and CD-ROMs, and virtual elements like packs, volumes, and volume plexes.</span></span> <span data-ttu-id="490dd-106">A ilustração a seguir mostra a relação entre o objeto de provedor e o conjunto de objetos de provedor de software, bem como a relação entre os vários objetos de provedor de software.</span><span class="sxs-lookup"><span data-stu-id="490dd-106">The following illustration shows the relationship between the provider object and the set of software provider objects, as well as the relationship between the various software provider objects themselves.</span></span>

![Diagrama que mostra a relação entre um ' provedor ' e objetos de provedor de software, como ' Pack ' e ' volume '.](images/vdsswobjects.png)

<span data-ttu-id="490dd-108">Um objeto de provedor pode conter zero ou mais pacotes.</span><span class="sxs-lookup"><span data-stu-id="490dd-108">A provider object can contain zero or more packs.</span></span> <span data-ttu-id="490dd-109">Um objeto de pacote pode conter zero ou mais discos e volumes.</span><span class="sxs-lookup"><span data-stu-id="490dd-109">A pack object can contain zero or more disks and volumes.</span></span> <span data-ttu-id="490dd-110">Um volume que consiste em pelo menos um plex de volume e cada Plex de volume pode ser mapeado para um ou mais discos, dependendo do tipo de plex.</span><span class="sxs-lookup"><span data-stu-id="490dd-110">A volume comprises of at least one volume plex and each volume plex can map to one or more disks, depending on the plex type.</span></span> <span data-ttu-id="490dd-111">O VDS gerencia discos não alocados diretamente, sem um contêiner de pacote.</span><span class="sxs-lookup"><span data-stu-id="490dd-111">VDS manages unallocated disks directly, without a pack container.</span></span> <span data-ttu-id="490dd-112">Os tópicos restantes desta seção descrevem os objetos de pacote, disco, volume e Plex de volume.</span><span class="sxs-lookup"><span data-stu-id="490dd-112">The remaining topics of this section describe the pack, disk, volume, and volume plex objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="490dd-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="490dd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="490dd-114">Modelo de objeto VDS</span><span class="sxs-lookup"><span data-stu-id="490dd-114">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
