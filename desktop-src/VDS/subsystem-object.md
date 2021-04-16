---
description: Objeto de subsistema
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: Objeto de subsistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8314a798ea809b3175377bc5484f19629094db
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104550310"
---
# <a name="subsystem-object"></a><span data-ttu-id="f0ad4-103">Objeto de subsistema</span><span class="sxs-lookup"><span data-stu-id="f0ad4-103">Subsystem Object</span></span>

<span data-ttu-id="f0ad4-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f0ad4-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="f0ad4-105">Um objeto de subsistema modela um subsistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-105">A subsystem object models a storage subsystem.</span></span> <span data-ttu-id="f0ad4-106">Um subsistema é um compartimento RAID ou uma placa PCI RAID.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-106">A subsystem is either a RAID enclosure or a PCI RAID card.</span></span> <span data-ttu-id="f0ad4-107">Um único computador host pode ser conectado a qualquer número de subsistemas.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-107">A single host computer can be connected to any number of subsystems.</span></span> <span data-ttu-id="f0ad4-108">Cada subsistema é gerenciado por exatamente um provedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-108">Each subsystem is managed by exactly one hardware provider.</span></span> <span data-ttu-id="f0ad4-109">Em uma configuração de SAN, a classe de subsistema representa um compartimento de armazenamento de SAN.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-109">In a SAN configuration, the subsystem class represents a SAN storage enclosure.</span></span>

<span data-ttu-id="f0ad4-110">Um subsistema pode conter qualquer número de controladores e unidades e pode trazer a superfície (remover máscara) de qualquer número de LUNs para o computador no qual o provedor de hardware está em execução.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-110">A subsystem can contain any number of controllers and drives, and can surface (unmask) any number of LUNs to the computer on which the hardware provider is running.</span></span> <span data-ttu-id="f0ad4-111">Subsistemas de extremidade superior podem remover a máscara de LUNs para outros computadores na rede.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-111">Higher-end subsystems can unmask LUNs to other computers on the network.</span></span> <span data-ttu-id="f0ad4-112">Cada unidade de disco em um subsistema está conectada a um barramento e ocupa um slot no barramento.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-112">Each disk drive within a subsystem is connected to a bus and occupies a slot in the bus.</span></span> <span data-ttu-id="f0ad4-113">Cada controlador em um subsistema tem uma ou mais portas do controlador.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-113">Each controller within a subsystem has one or more controller ports.</span></span>

<span data-ttu-id="f0ad4-114">A ilustração a seguir mostra os dispositivos físicos contidos em um subsistema (LUNs não são mostrados) e as relações entre eles.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-114">The illustration that follows shows the physical devices contained in a subsystem (LUNs are not shown) and the relationships among them.</span></span>

![Diagrama que mostra um subsistema começando com ' portas ' à esquerda, movendo para ' controladores ' e, em seguida, um ' barramento ' com ' Slots ' que levam a ' unidades ' individuais.](images/vdssubsystem.png)

<span data-ttu-id="f0ad4-116">Os aplicativos VDS usam o método [**IVdsHwProvider:: QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) para consultar os subsistemas que pertencem a um provedor de hardware específico.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-116">VDS applications use the [**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) method to query the subsystems that belong to a specific hardware provider.</span></span> <span data-ttu-id="f0ad4-117">Os chamadores podem obter um ponteiro para um subsistema específico selecionando o objeto subsistema desejado da enumeração que é retornada pelo método **QuerySubSystems** .</span><span class="sxs-lookup"><span data-stu-id="f0ad4-117">Callers can get a pointer to a specific subsystem by selecting the desired subsystem object from the enumeration that is returned by the **QuerySubSystems** method.</span></span> <span data-ttu-id="f0ad4-118">Com um objeto de subsistema, você pode definir o status do subsistema, criar LUNs, substituir unidades e consultar controladores, unidades e LUNs.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-118">With a subsystem object, you can set the subsystem status, create LUNs, replace drives, and query for controllers, drives, and LUNs.</span></span>

<span data-ttu-id="f0ad4-119">Além de um identificador de objeto, um nome e um número de série, as propriedades de objeto do subsistema incluem o status, a integridade e os sinalizadores do subsistema; uma contagem de controladores, slots e barramentos; e uma configuração de prioridade de recriação.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-119">In addition to an object identifier, a name, and a serial number, subsystem object properties include the subsystem status, health, and flags; a count of the controllers, slots, and buses; and a rebuild priority setting.</span></span>

<span data-ttu-id="f0ad4-120">A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-120">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="f0ad4-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0ad4-121">Type</span></span>                                                                                      | <span data-ttu-id="f0ad4-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="f0ad4-122">Element</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ad4-123">Interfaces que são sempre expostas por este objeto</span><span class="sxs-lookup"><span data-stu-id="f0ad4-123">Interfaces that are always exposed by this object</span></span>                                         | <span data-ttu-id="f0ad4-124">[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).</span><span class="sxs-lookup"><span data-stu-id="f0ad4-124">[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).</span></span>                                                                                          |
| <span data-ttu-id="f0ad4-125">Interfaces que são sempre expostas por este objeto somente nos provedores de iSCSI VDS 1,1 e 2,0</span><span class="sxs-lookup"><span data-stu-id="f0ad4-125">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="f0ad4-126">[**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) e [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).</span><span class="sxs-lookup"><span data-stu-id="f0ad4-126">[**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) and [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).</span></span>             |
| <span data-ttu-id="f0ad4-127">Interfaces que podem ser expostas por este objeto</span><span class="sxs-lookup"><span data-stu-id="f0ad4-127">Interfaces that may be exposed by this object</span></span>                                             | <span data-ttu-id="f0ad4-128">[**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) e [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).</span><span class="sxs-lookup"><span data-stu-id="f0ad4-128">[**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) and [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).</span></span>                               |
| <span data-ttu-id="f0ad4-129">Enumerações associadas</span><span class="sxs-lookup"><span data-stu-id="f0ad4-129">Associated enumerations</span></span>                                                                   | <span data-ttu-id="f0ad4-130">[**VDS \_ \_ \_ Sinalizador de subsistema**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) e [**\_ \_ \_ status de subsistema VDS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).</span><span class="sxs-lookup"><span data-stu-id="f0ad4-130">[**VDS\_SUB\_SYSTEM\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) and [**VDS\_SUB\_SYSTEM\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).</span></span>             |
| <span data-ttu-id="f0ad4-131">Estruturas associadas</span><span class="sxs-lookup"><span data-stu-id="f0ad4-131">Associated structures</span></span>                                                                     | <span data-ttu-id="f0ad4-132">[**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) [**\_ \_ \_ Notificação de subsistema**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification)e de prop-Subsystem de subsistema.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-132">[**VDS\_SUB\_SYSTEM\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) and [**VDS\_SUB\_SYSTEM\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f0ad4-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0ad4-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0ad4-134">Objetos de provedor de hardware</span><span class="sxs-lookup"><span data-stu-id="f0ad4-134">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="f0ad4-135">**IVdsHwProvider::QuerySubSystems**</span><span class="sxs-lookup"><span data-stu-id="f0ad4-135">**IVdsHwProvider::QuerySubSystems**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
