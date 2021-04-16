---
description: Objeto do controlador
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: Objeto do controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104567372"
---
# <a name="controller-object"></a><span data-ttu-id="ffd42-103">Objeto do controlador</span><span class="sxs-lookup"><span data-stu-id="ffd42-103">Controller Object</span></span>

<span data-ttu-id="ffd42-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ffd42-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="ffd42-105">Um objeto de controlador modela um controlador em um subsistema.</span><span class="sxs-lookup"><span data-stu-id="ffd42-105">A controller object models a controller in a subsystem.</span></span> <span data-ttu-id="ffd42-106">Os controladores são contidos por subsistemas, e cada controlador tem uma ou mais portas de controlador por meio das quais o computador host pode gravar e ler de LUNs.</span><span class="sxs-lookup"><span data-stu-id="ffd42-106">Controllers are contained by subsystems, and each controller has one or more controller ports through which the host computer can write to and read from LUNs.</span></span> <span data-ttu-id="ffd42-107">Um único controlador pode ser definido simultaneamente como ativo para um LUN e inativo para outros.</span><span class="sxs-lookup"><span data-stu-id="ffd42-107">A single controller can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="ffd42-108">Um controlador que está ativo para um LUN especificado carrega a responsabilidade de lidar com a entrada e a saída do LUN.</span><span class="sxs-lookup"><span data-stu-id="ffd42-108">A controller that is active for a specified LUN carries the responsibility for handling input to and output from the LUN.</span></span> <span data-ttu-id="ffd42-109">A figura a seguir ilustra essa ideia.</span><span class="sxs-lookup"><span data-stu-id="ffd42-109">The following figure illustrates this idea.</span></span>

![Diagrama que mostra um "controlador" com um LUN ativo à esquerda e dois LUNs ativos à direita.](images/vdscontroller.png)

<span data-ttu-id="ffd42-111">**VDS 1,0:** Cada um dos controladores de um subsistema é definido como ativo ou inativo em relação a cada um dos LUNs das superfícies do subsistema.</span><span class="sxs-lookup"><span data-stu-id="ffd42-111">**VDS 1.0:** Each of a subsystem's controllers is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span>

<span data-ttu-id="ffd42-112">Os aplicativos VDS usam o método [**IVdsSubSystem:: QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) para determinar os controladores contidos em um subsistema específico.</span><span class="sxs-lookup"><span data-stu-id="ffd42-112">VDS applications use the [**IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) method to determine the controllers that are contained by a specific subsystem.</span></span> <span data-ttu-id="ffd42-113">Os chamadores podem obter um ponteiro para um controlador específico selecionando o objeto do controlador desejado da enumeração que é retornada pelo método **QueryControllers** .</span><span class="sxs-lookup"><span data-stu-id="ffd42-113">Callers can get a pointer to a specific controller by selecting the desired controller object from the enumeration that is returned by the **QueryControllers** method.</span></span> <span data-ttu-id="ffd42-114">Com um objeto de controlador, um chamador pode definir o status do controlador, consultar seus LUNs associados, consultar suas portas do controlador e liberar e invalidar o cache.</span><span class="sxs-lookup"><span data-stu-id="ffd42-114">With a controller object, a caller can set the controller status, query for its associated LUNs, query for its controller ports, and flush and invalidate the cache.</span></span>

<span data-ttu-id="ffd42-115">Além de um identificador de objeto, um nome e um número de série, as propriedades do objeto do controlador incluem o status e a integridade do controlador e uma contagem das portas.</span><span class="sxs-lookup"><span data-stu-id="ffd42-115">In addition to an object identifier, a name, and a serial number, controller object properties include the controller status and health, and a count of the ports.</span></span>

<span data-ttu-id="ffd42-116">A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ffd42-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="ffd42-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffd42-117">Type</span></span>                                                                                              | <span data-ttu-id="ffd42-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="ffd42-118">Element</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd42-119">Interfaces que são sempre expostas por este objeto</span><span class="sxs-lookup"><span data-stu-id="ffd42-119">Interfaces that are always exposed by this object</span></span>                                                 | [<span data-ttu-id="ffd42-120">**IVdsController**</span><span class="sxs-lookup"><span data-stu-id="ffd42-120">**IVdsController**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| <span data-ttu-id="ffd42-121">Interfaces que são sempre expostas por este objeto no VDS 1,1 e 2,0 Fibre Channel somente provedores</span><span class="sxs-lookup"><span data-stu-id="ffd42-121">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="ffd42-122">**IVdsControllerControllerPort**</span><span class="sxs-lookup"><span data-stu-id="ffd42-122">**IVdsControllerControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| <span data-ttu-id="ffd42-123">Interfaces que podem ser expostas por este objeto</span><span class="sxs-lookup"><span data-stu-id="ffd42-123">Interfaces that may be exposed by this object</span></span>                                                     | [<span data-ttu-id="ffd42-124">**IVdsMaintenance**</span><span class="sxs-lookup"><span data-stu-id="ffd42-124">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| <span data-ttu-id="ffd42-125">Enumerações associadas</span><span class="sxs-lookup"><span data-stu-id="ffd42-125">Associated enumerations</span></span>                                                                           | <span data-ttu-id="ffd42-126">[**VDS \_ \_status do controlador**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).</span><span class="sxs-lookup"><span data-stu-id="ffd42-126">[**VDS\_CONTROLLER\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).</span></span>                                                                      |
| <span data-ttu-id="ffd42-127">Estruturas associadas</span><span class="sxs-lookup"><span data-stu-id="ffd42-127">Associated structures</span></span>                                                                             | <span data-ttu-id="ffd42-128">[**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) [**\_ \_ Notificação**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)de controlador do VDS e de prop.</span><span class="sxs-lookup"><span data-stu-id="ffd42-128">[**VDS\_CONTROLLER\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) and [**VDS\_CONTROLLER\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ffd42-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ffd42-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffd42-130">Objetos de provedor de hardware</span><span class="sxs-lookup"><span data-stu-id="ffd42-130">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="ffd42-131">**IVdsSubSystem::QueryControllers**</span><span class="sxs-lookup"><span data-stu-id="ffd42-131">**IVdsSubSystem::QueryControllers**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
