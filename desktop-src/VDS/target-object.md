---
description: Objeto de Destino
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Objeto de Destino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1e81ea94a2f608378eba069defc83a721e0fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770587"
---
# <a name="target-object"></a><span data-ttu-id="2cc9c-103">Objeto de Destino</span><span class="sxs-lookup"><span data-stu-id="2cc9c-103">Target Object</span></span>

<span data-ttu-id="2cc9c-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2cc9c-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="2cc9c-105">Um objeto de destino modela um destino iSCSI que está contido em um subsistema iSCSI.</span><span class="sxs-lookup"><span data-stu-id="2cc9c-105">A target object models an iSCSI target that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="2cc9c-106">Use o método [**IVdsSubSystemIscsi:: QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) para determinar os destinos iSCSI do subsistema.</span><span class="sxs-lookup"><span data-stu-id="2cc9c-106">Use the [**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) method to determine the iSCSI targets of the subsystem.</span></span> <span data-ttu-id="2cc9c-107">Os chamadores podem obter um ponteiro para um destino específico selecionando o objeto de destino desejado da enumeração que é retornada pelo método **QueryTargets** .</span><span class="sxs-lookup"><span data-stu-id="2cc9c-107">Callers can get a pointer to a specific target by selecting the desired target object from the enumeration that is returned by the **QueryTargets** method.</span></span> <span data-ttu-id="2cc9c-108">Com um objeto de destino, você pode definir o nome amigável e a consulta do destino para propriedades de destino, LUNs associados e o subsistema que contém o destino.</span><span class="sxs-lookup"><span data-stu-id="2cc9c-108">With a target object, you can set the target's friendly name and query for target properties, associated LUNs, and the subsystem that contains the target.</span></span>

<span data-ttu-id="2cc9c-109">Os computadores host devem fazer logon nos destinos para acessar seus LUNs associados.</span><span class="sxs-lookup"><span data-stu-id="2cc9c-109">Host computers must log on to targets to access their associated LUNs.</span></span> <span data-ttu-id="2cc9c-110">Para executar um logon em um destino, o destino deve ter pelo menos um portal associado em um de seus grupos de Portal.</span><span class="sxs-lookup"><span data-stu-id="2cc9c-110">To perform a logon to a target, the target must have at least one associated portal in one of its portal groups.</span></span> <span data-ttu-id="2cc9c-111">A entrada e a saída de LUNs associados são manipuladas por meio desta sessão de logon.</span><span class="sxs-lookup"><span data-stu-id="2cc9c-111">Input to and output from associated LUNs is handled through this logon session.</span></span>

<span data-ttu-id="2cc9c-112">As propriedades do objeto de destino incluem um identificador de objeto, um nome de iSCSI, um nome amigável e um sinalizador habilitado para CHAP.</span><span class="sxs-lookup"><span data-stu-id="2cc9c-112">Target object properties include an object identifier, an iSCSI name, a friendly name, and a CHAP-enabled flag.</span></span>

<span data-ttu-id="2cc9c-113">A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2cc9c-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="2cc9c-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="2cc9c-114">Type</span></span>                                                                                      | <span data-ttu-id="2cc9c-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="2cc9c-115">Element</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc9c-116">Interfaces que são sempre expostas por este objeto somente nos provedores de iSCSI VDS 1,1 e 2,0</span><span class="sxs-lookup"><span data-stu-id="2cc9c-116">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="2cc9c-117">[**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).</span><span class="sxs-lookup"><span data-stu-id="2cc9c-117">[**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).</span></span>                                                                                 |
| <span data-ttu-id="2cc9c-118">Enumerações associadas</span><span class="sxs-lookup"><span data-stu-id="2cc9c-118">Associated enumerations</span></span>                                                                   | <span data-ttu-id="2cc9c-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2cc9c-119">None.</span></span>                                                                                                                       |
| <span data-ttu-id="2cc9c-120">Estruturas associadas</span><span class="sxs-lookup"><span data-stu-id="2cc9c-120">Associated structures</span></span>                                                                     | <span data-ttu-id="2cc9c-121">[**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) Notificação de destino do [**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_target_notification)e da prop de destino iSCSI.</span><span class="sxs-lookup"><span data-stu-id="2cc9c-121">[**VDS\_ISCSI\_TARGET\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) and [**VDS\_TARGET\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_target_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2cc9c-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2cc9c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cc9c-123">Objetos de provedor de hardware</span><span class="sxs-lookup"><span data-stu-id="2cc9c-123">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="2cc9c-124">**IVdsSubSystemIscsi::QueryTargets**</span><span class="sxs-lookup"><span data-stu-id="2cc9c-124">**IVdsSubSystemIscsi::QueryTargets**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
