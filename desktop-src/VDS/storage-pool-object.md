---
description: Um objeto de pool de armazenamento modela um pool de armazenamento em um subsistema de armazenamento.
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: Objeto do pool de armazenamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44719b825193faa75546ba1a0f7b42155a3e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810280"
---
# <a name="storage-pool-object"></a><span data-ttu-id="1f3d5-103">Objeto do pool de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1f3d5-103">Storage Pool Object</span></span>

<span data-ttu-id="1f3d5-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1f3d5-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="1f3d5-105">Um objeto de pool de armazenamento modela um pool de armazenamento em um subsistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-105">A storage pool object models a storage pool in a storage subsystem.</span></span>

<span data-ttu-id="1f3d5-106">Um pool de armazenamento contém extensões de unidade de uma ou mais unidades que são gerenciadas pelo mesmo provedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-106">A storage pool contains drive extents from one or more drives that are managed by the same hardware provider.</span></span>

<span data-ttu-id="1f3d5-107">A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1f3d5-107">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="1f3d5-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f3d5-108">Type</span></span>                                              | <span data-ttu-id="1f3d5-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="1f3d5-109">Element</span></span>                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f3d5-110">Interfaces que são sempre expostas por este objeto</span><span class="sxs-lookup"><span data-stu-id="1f3d5-110">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="1f3d5-111">**IVdsStoragePool**</span><span class="sxs-lookup"><span data-stu-id="1f3d5-111">**IVdsStoragePool**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| <span data-ttu-id="1f3d5-112">Enumerações associadas</span><span class="sxs-lookup"><span data-stu-id="1f3d5-112">Associated enumerations</span></span>                           | <span data-ttu-id="1f3d5-113">[**VDS \_ \_Tipo de RAID**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**\_ \_ \_ status do pool de armazenamento VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)e [**\_ \_ \_ tipo de pool de armazenamento VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).</span><span class="sxs-lookup"><span data-stu-id="1f3d5-113">[**VDS\_RAID\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**VDS\_STORAGE\_POOL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status), and [**VDS\_STORAGE\_POOL\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).</span></span>                                                                                                                                  |
| <span data-ttu-id="1f3d5-114">Estruturas associadas</span><span class="sxs-lookup"><span data-stu-id="1f3d5-114">Associated structures</span></span>                             | <span data-ttu-id="1f3d5-115">[**VDS \_ HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**\_ \_ atributos do pool VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**\_ \_ \_ atributos personalizados do pool do VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**\_ \_ \_ \_ extensão de unidade do pool de armazenamento VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)e [**\_ \_ \_ prop pool de armazenamento do VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop).</span><span class="sxs-lookup"><span data-stu-id="1f3d5-115">[**VDS\_HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**VDS\_POOL\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**VDS\_POOL\_CUSTOM\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**VDS\_STORAGE\_POOL\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent), and [**VDS\_STORAGE\_POOL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop).</span></span> |



 

 

 
