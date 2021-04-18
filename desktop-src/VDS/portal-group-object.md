---
description: Objeto de grupo do portal
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: Objeto de grupo do portal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c915e76debac959a1dc7684d87c9770033b4aa34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506227"
---
# <a name="portal-group-object"></a><span data-ttu-id="9bd20-103">Objeto de grupo do portal</span><span class="sxs-lookup"><span data-stu-id="9bd20-103">Portal Group Object</span></span>

<span data-ttu-id="9bd20-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9bd20-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="9bd20-105">Um objeto de grupo de portais modela um grupo de portal iSCSI que está contido em um destino iSCSI.</span><span class="sxs-lookup"><span data-stu-id="9bd20-105">A portal group object models an iSCSI portal group that is contained within an iSCSI target.</span></span>

<span data-ttu-id="9bd20-106">Use o método [**IVdsIscsiTarget:: QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) para determinar os grupos de portal que estão contidos por um destino específico.</span><span class="sxs-lookup"><span data-stu-id="9bd20-106">Use the [**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) method to determine the portal groups that are contained by a specific target.</span></span> <span data-ttu-id="9bd20-107">Use o método [**IVdsIscsiPortal:: QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) para determinar os grupos de portal que estão associados a um portal especificado.</span><span class="sxs-lookup"><span data-stu-id="9bd20-107">Use the [**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) method to determine the portal groups that are associated with a specified portal.</span></span> <span data-ttu-id="9bd20-108">Os chamadores podem obter um ponteiro para um grupo específico do portal selecionando o objeto do grupo do portal desejado da enumeração que é retornada pelo método **QueryPortalGroups** ou o método **QueryAssociatedPortalGroups** .</span><span class="sxs-lookup"><span data-stu-id="9bd20-108">Callers can get a pointer to a specific portal group by selecting the desired portal group object from the enumeration that is returned by the **QueryPortalGroups** method or the **QueryAssociatedPortalGroups** method.</span></span> <span data-ttu-id="9bd20-109">Com um objeto de grupo do portal, você pode adicionar ou remover portais e consultar Propriedades do grupo de portal, portais associados e o destino que contém o grupo do Portal.</span><span class="sxs-lookup"><span data-stu-id="9bd20-109">With a portal group object, you can add or remove portals and query for portal group properties, associated portals, and the target that contains the portal group.</span></span>

<span data-ttu-id="9bd20-110">As propriedades do objeto do grupo de portais incluem um [identificador de objeto](vds-data-types.md) e a marca do grupo do Portal.</span><span class="sxs-lookup"><span data-stu-id="9bd20-110">Portal group object properties include an [object identifier](vds-data-types.md) and the portal group tag.</span></span> <span data-ttu-id="9bd20-111">Para obter mais informações sobre marcas de grupo do portal, consulte a especificação iSCSI em <https://go.microsoft.com/fwlink/p/?linkid=158752> .</span><span class="sxs-lookup"><span data-stu-id="9bd20-111">For more information about portal group tags, see the iSCSI specification at <https://go.microsoft.com/fwlink/p/?linkid=158752>.</span></span>

<span data-ttu-id="9bd20-112">A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9bd20-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="9bd20-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="9bd20-113">Type</span></span>                                                                                      | <span data-ttu-id="9bd20-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="9bd20-114">Element</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bd20-115">Interfaces que são sempre expostas por este objeto somente nos provedores de iSCSI VDS 1,1 e 2,0</span><span class="sxs-lookup"><span data-stu-id="9bd20-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="9bd20-116">[**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).</span><span class="sxs-lookup"><span data-stu-id="9bd20-116">[**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).</span></span>                                                                                              |
| <span data-ttu-id="9bd20-117">Enumerações associadas</span><span class="sxs-lookup"><span data-stu-id="9bd20-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="9bd20-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9bd20-118">None.</span></span>                                                                                                                                              |
| <span data-ttu-id="9bd20-119">Estruturas associadas</span><span class="sxs-lookup"><span data-stu-id="9bd20-119">Associated structures</span></span>                                                                     | <span data-ttu-id="9bd20-120">[**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) Notificação do grupo de portais do portal de propriedades e do [**portal do VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification).</span><span class="sxs-lookup"><span data-stu-id="9bd20-120">[**VDS\_ISCSI\_PORTALGROUP\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) and [**VDS\_PORTAL\_GROUP\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9bd20-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9bd20-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bd20-122">Objetos de provedor de hardware</span><span class="sxs-lookup"><span data-stu-id="9bd20-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="9bd20-123">**IVdsIscsiPortal::QueryAssociatedPortalGroups**</span><span class="sxs-lookup"><span data-stu-id="9bd20-123">**IVdsIscsiPortal::QueryAssociatedPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[<span data-ttu-id="9bd20-124">**IVdsIscsiTarget::QueryPortalGroups**</span><span class="sxs-lookup"><span data-stu-id="9bd20-124">**IVdsIscsiTarget::QueryPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
