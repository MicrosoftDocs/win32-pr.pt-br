---
description: Objeto da unidade
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Objeto da unidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df8501c79f9381dba80a1fe0276014dccdf7a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169665"
---
# <a name="drive-object"></a><span data-ttu-id="d9e91-103">Objeto da unidade</span><span class="sxs-lookup"><span data-stu-id="d9e91-103">Drive Object</span></span>

<span data-ttu-id="d9e91-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d9e91-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="d9e91-105">Um objeto de unidade modela uma unidade de disco físico que está contida em um subsistema.</span><span class="sxs-lookup"><span data-stu-id="d9e91-105">A drive object models a physical disk drive that is contained within a subsystem.</span></span> <span data-ttu-id="d9e91-106">Cada unidade conecta-se a um barramento, ocupa um slot e contém um conjunto de extensões de unidade.</span><span class="sxs-lookup"><span data-stu-id="d9e91-106">Each drive connects to a bus, occupies a slot, and contains a set of drive extents.</span></span> <span data-ttu-id="d9e91-107">Cada unidade pode contribuir com extensões para qualquer número de LUNs.</span><span class="sxs-lookup"><span data-stu-id="d9e91-107">Each drive can contribute extents to any number of LUNs.</span></span> <span data-ttu-id="d9e91-108">Uma unidade também pode ser designada como um hot spare.</span><span class="sxs-lookup"><span data-stu-id="d9e91-108">A drive can also be designated as a hot spare.</span></span>

<span data-ttu-id="d9e91-109">Use o método [**IVdsSubSystem:: QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) para determinar as unidades contidas em um subsistema específico.</span><span class="sxs-lookup"><span data-stu-id="d9e91-109">Use the [**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) method to determine the drives that are contained by a specific subsystem.</span></span> <span data-ttu-id="d9e91-110">Os chamadores podem obter um ponteiro para uma unidade específica selecionando o objeto de unidade desejado da enumeração que é retornada pelo método **QueryDrives** ou invocando o método [**IVdsSubSystem:: GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) e passando o número de barramento e slot desejado.</span><span class="sxs-lookup"><span data-stu-id="d9e91-110">Callers can get a pointer to a specific drive by selecting the desired drive object from the enumeration that is returned by the **QueryDrives** method, or by invoking the [**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) method and passing in the desired bus and slot number.</span></span> <span data-ttu-id="d9e91-111">Com um objeto Drive, você pode definir o status da unidade e a consulta para propriedades da unidade, extensões de unidade associadas e o subsistema que contém a unidade.</span><span class="sxs-lookup"><span data-stu-id="d9e91-111">With a drive object, you can set the drive status and query for drive properties, associated drive extents, and the subsystem containing the drive.</span></span>

<span data-ttu-id="d9e91-112">Além de um identificador de objeto, um nome e um número de série, as propriedades do objeto da unidade incluem o status, a integridade e os sinalizadores da unidade; o tamanho em bytes; e um número de barramento e slot.</span><span class="sxs-lookup"><span data-stu-id="d9e91-112">In addition to an object identifier, a name, and a serial number, drive object properties include the drive status, health, and flags; the size in bytes; and a bus and slot number.</span></span>

<span data-ttu-id="d9e91-113">A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d9e91-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="d9e91-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9e91-114">Type</span></span>                                              | <span data-ttu-id="d9e91-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="d9e91-115">Element</span></span>                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9e91-116">Interfaces que são sempre expostas por este objeto</span><span class="sxs-lookup"><span data-stu-id="d9e91-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="d9e91-117">**IVdsDrive**</span><span class="sxs-lookup"><span data-stu-id="d9e91-117">**IVdsDrive**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| <span data-ttu-id="d9e91-118">Interfaces que podem ser expostas por este objeto</span><span class="sxs-lookup"><span data-stu-id="d9e91-118">Interfaces that may be exposed by this object</span></span>     | [<span data-ttu-id="d9e91-119">**IVdsMaintenance**</span><span class="sxs-lookup"><span data-stu-id="d9e91-119">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| <span data-ttu-id="d9e91-120">Enumerações associadas</span><span class="sxs-lookup"><span data-stu-id="d9e91-120">Associated enumerations</span></span>                           | <span data-ttu-id="d9e91-121">[**VDS \_ \_Sinalizador de unidade**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**\_ \_ status da unidade VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)e [**\_ \_ extensão da unidade VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent).</span><span class="sxs-lookup"><span data-stu-id="d9e91-121">[**VDS\_DRIVE\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**VDS\_DRIVE\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status), and [**VDS\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent).</span></span> |
| <span data-ttu-id="d9e91-122">Estruturas associadas</span><span class="sxs-lookup"><span data-stu-id="d9e91-122">Associated structures</span></span>                             | <span data-ttu-id="d9e91-123">[**VDS \_ GERAR \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) notificação de [**\_ unidade \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)de prop e VDS.</span><span class="sxs-lookup"><span data-stu-id="d9e91-123">[**VDS\_DRIVE\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) and [**VDS\_DRIVE\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="d9e91-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9e91-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9e91-125">Objetos de provedor de hardware</span><span class="sxs-lookup"><span data-stu-id="d9e91-125">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="d9e91-126">**IVdsSubSystem::QueryDrives**</span><span class="sxs-lookup"><span data-stu-id="d9e91-126">**IVdsSubSystem::QueryDrives**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[<span data-ttu-id="d9e91-127">**IVdsSubSystem:: GetDrive**</span><span class="sxs-lookup"><span data-stu-id="d9e91-127">**IVdsSubSystem::GetDrive**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
