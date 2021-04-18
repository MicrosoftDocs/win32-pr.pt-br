---
description: Objeto do portal
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: Objeto do portal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01328d8dccfe7a29c0686cde9b531df63d56e63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813258"
---
# <a name="portal-object"></a><span data-ttu-id="93efd-103">Objeto do portal</span><span class="sxs-lookup"><span data-stu-id="93efd-103">Portal Object</span></span>

<span data-ttu-id="93efd-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="93efd-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="93efd-105">Um objeto do portal modela um portal iSCSI que está contido em um subsistema iSCSI.</span><span class="sxs-lookup"><span data-stu-id="93efd-105">A portal object models an iSCSI portal that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="93efd-106">Use o método [**IVdsSubSystemIscsi:: QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) para determinar os portais iSCSI do subsistema.</span><span class="sxs-lookup"><span data-stu-id="93efd-106">Use the [**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) method to determine the iSCSI portals of the subsystem.</span></span> <span data-ttu-id="93efd-107">Os chamadores podem obter um ponteiro para um portal específico selecionando o objeto do portal desejado da enumeração que é retornada pelo método **QueryPortals** .</span><span class="sxs-lookup"><span data-stu-id="93efd-107">Callers can get a pointer to a specific portal by selecting the desired portal object from the enumeration that is returned by the **QueryPortals** method.</span></span> <span data-ttu-id="93efd-108">Com um objeto do portal, você pode definir o status e a consulta do portal para propriedades do portal, grupos de portais associados e o subsistema que contém o Portal.</span><span class="sxs-lookup"><span data-stu-id="93efd-108">With a portal object, you can set the portal status and query for portal properties, associated portal groups, and the subsystem that contains the portal.</span></span>

<span data-ttu-id="93efd-109">Um objeto do portal só pode ser associado a no máximo um grupo de portal de um destino especificado.</span><span class="sxs-lookup"><span data-stu-id="93efd-109">A portal object can only be associated with at most one portal group of a specified target.</span></span>

<span data-ttu-id="93efd-110">Os portais servem como um dos pontos de extremidade dos caminhos do MPIO em provedores de hardware iSCSI, nos quais as políticas de balanceamento de carga podem ser impostas.</span><span class="sxs-lookup"><span data-stu-id="93efd-110">Portals serve as one of the endpoints of MPIO paths in iSCSI hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="93efd-111">As propriedades do objeto do portal incluem um identificador de objeto, um endereço IP e uma porta e o status do Portal.</span><span class="sxs-lookup"><span data-stu-id="93efd-111">Portal object properties include an object identifier, an IP address and port, and the portal status.</span></span>

<span data-ttu-id="93efd-112">A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="93efd-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="93efd-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="93efd-113">Type</span></span>                                                                                      | <span data-ttu-id="93efd-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="93efd-114">Element</span></span>                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93efd-115">Interfaces que são sempre expostas por este objeto somente nos provedores de iSCSI VDS 1,1 e 2,0</span><span class="sxs-lookup"><span data-stu-id="93efd-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="93efd-116">[**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).</span><span class="sxs-lookup"><span data-stu-id="93efd-116">[**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).</span></span>                                                                             |
| <span data-ttu-id="93efd-117">Enumerações associadas</span><span class="sxs-lookup"><span data-stu-id="93efd-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="93efd-118">[**VDS \_ \_ \_ status do portal iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).</span><span class="sxs-lookup"><span data-stu-id="93efd-118">[**VDS\_ISCSI\_PORTAL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).</span></span>                                                          |
| <span data-ttu-id="93efd-119">Estruturas associadas</span><span class="sxs-lookup"><span data-stu-id="93efd-119">Associated structures</span></span>                                                                     | <span data-ttu-id="93efd-120">[**VDS \_ Notificação do portal do ISCSI \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) e da [**\_ porta \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification).</span><span class="sxs-lookup"><span data-stu-id="93efd-120">[**VDS\_ISCSI\_PORTAL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="93efd-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93efd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93efd-122">Objetos de provedor de hardware</span><span class="sxs-lookup"><span data-stu-id="93efd-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="93efd-123">**IVdsSubSystemIscsi::QueryPortals**</span><span class="sxs-lookup"><span data-stu-id="93efd-123">**IVdsSubSystemIscsi::QueryPortals**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
