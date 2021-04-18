---
description: Objeto de porta do controlador
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: Objeto de porta do controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759817"
---
# <a name="controller-port-object"></a><span data-ttu-id="68d54-103">Objeto de porta do controlador</span><span class="sxs-lookup"><span data-stu-id="68d54-103">Controller Port Object</span></span>

<span data-ttu-id="68d54-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="68d54-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="68d54-105">Um objeto de porta do controlador modela uma porta do controlador em um subsistema.</span><span class="sxs-lookup"><span data-stu-id="68d54-105">A controller port object models a controller port in a subsystem.</span></span> <span data-ttu-id="68d54-106">Os computadores host podem gravar e ler de LUNs por meio de portas do controlador.</span><span class="sxs-lookup"><span data-stu-id="68d54-106">Host computers can write to and read from LUNs through controller ports.</span></span> <span data-ttu-id="68d54-107">As portas do controlador são contidas por controladores em um subsistema.</span><span class="sxs-lookup"><span data-stu-id="68d54-107">Controller ports are contained by controllers in a subsystem.</span></span> <span data-ttu-id="68d54-108">No VDS 1,1 e VDS 2.0, cada uma das portas do controlador de um subsistema é definida como ativa ou inativa em relação a cada um dos LUNs que as superfícies do subsistema.</span><span class="sxs-lookup"><span data-stu-id="68d54-108">In VDS 1.1 and VDS2.0, each of a subsystem's controller ports is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span> <span data-ttu-id="68d54-109">Uma única porta do controlador pode ser definida simultaneamente como ativa para um LUN e inativa para outros.</span><span class="sxs-lookup"><span data-stu-id="68d54-109">A single controller port, then, can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="68d54-110">Uma porta de controlador que está ativa para um determinado LUN transporta a responsabilidade pelo tratamento de entrada e saída do LUN.</span><span class="sxs-lookup"><span data-stu-id="68d54-110">A controller port that is active for a given LUN carries responsibility for handling input to and output from the LUN.</span></span>

<span data-ttu-id="68d54-111">As portas do controlador ativo servem como um dos pontos de extremidade dos caminhos do MPIO em Fibre Channel provedores de hardware, nos quais as políticas de balanceamento de carga podem ser impostas.</span><span class="sxs-lookup"><span data-stu-id="68d54-111">Active controller ports serve as one of the endpoints of MPIO paths in Fibre Channel hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="68d54-112">Use o método [**IVdsControllerControllerPort:: QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) para determinar as portas do controlador que estão contidas em um controlador específico.</span><span class="sxs-lookup"><span data-stu-id="68d54-112">Use the [**IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) method to determine the controller ports that are contained by a specific controller.</span></span> <span data-ttu-id="68d54-113">Os chamadores podem obter um ponteiro para uma porta de controlador específica selecionando o objeto de porta do controlador desejado da enumeração que é retornada pelo método **QueryControllerPorts** .</span><span class="sxs-lookup"><span data-stu-id="68d54-113">Callers can get a pointer to a specific controller port by selecting the desired controller port object from the enumeration that is returned by the **QueryControllerPorts** method.</span></span> <span data-ttu-id="68d54-114">Com um objeto de controlador, um chamador pode definir o status da porta do controlador e a consulta para seus LUNs associados.</span><span class="sxs-lookup"><span data-stu-id="68d54-114">With a controller object, a caller can set the controller port status and query for its associated LUNs.</span></span>

<span data-ttu-id="68d54-115">As propriedades do objeto do controlador incluem um identificador de objeto, um nome, um número de série e o status da porta do controlador.</span><span class="sxs-lookup"><span data-stu-id="68d54-115">Controller object properties include an object identifier, a name, a serial number, and the controller port status.</span></span>

<span data-ttu-id="68d54-116">A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="68d54-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="68d54-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="68d54-117">Type</span></span>                                                                                              | <span data-ttu-id="68d54-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="68d54-118">Element</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68d54-119">Interfaces que são sempre expostas por este objeto no VDS 1,1 e 2,0 Fibre Channel somente provedores</span><span class="sxs-lookup"><span data-stu-id="68d54-119">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="68d54-120">**IVdsControllerPort**</span><span class="sxs-lookup"><span data-stu-id="68d54-120">**IVdsControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| <span data-ttu-id="68d54-121">Enumerações associadas</span><span class="sxs-lookup"><span data-stu-id="68d54-121">Associated enumerations</span></span>                                                                           | [<span data-ttu-id="68d54-122">**\_status da porta VDS \_**</span><span class="sxs-lookup"><span data-stu-id="68d54-122">**VDS\_PORT\_STATUS**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| <span data-ttu-id="68d54-123">Estruturas associadas</span><span class="sxs-lookup"><span data-stu-id="68d54-123">Associated structures</span></span>                                                                             | <span data-ttu-id="68d54-124">[**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) Notificação de porta de porta do [ **VDS \_ \_** e prop](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span><span class="sxs-lookup"><span data-stu-id="68d54-124">[**VDS\_PORT\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="68d54-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68d54-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68d54-126">Objetos de provedor de hardware</span><span class="sxs-lookup"><span data-stu-id="68d54-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="68d54-127">**IVdsControllerControllerPort::QueryControllerPorts**</span><span class="sxs-lookup"><span data-stu-id="68d54-127">**IVdsControllerControllerPort::QueryControllerPorts**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
