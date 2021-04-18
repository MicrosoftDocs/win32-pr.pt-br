---
description: Objetos de provedor de hardware
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Objetos de provedor de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1aaebf61e97487b48a6b8bf0dbd91cc6aa3e0bd
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "105770588"
---
# <a name="hardware-provider-objects"></a><span data-ttu-id="3353e-103">Objetos de provedor de hardware</span><span class="sxs-lookup"><span data-stu-id="3353e-103">Hardware Provider Objects</span></span>

<span data-ttu-id="3353e-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3353e-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="3353e-105">O modelo de objeto do VDS inclui um conjunto de objetos para consultar e configurar entidades de provedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="3353e-105">The VDS object model includes a set of objects to query and configure hardware provider entities.</span></span> <span data-ttu-id="3353e-106">(Observe que, embora o VDS inclua um provedor de software, você deve adquirir um provedor de hardware e o hardware associado separadamente para tirar proveito dos objetos de provedor de hardware.) Esses objetos de provedor de hardware representam dispositivos físicos (como subsistemas, unidades e controladores) e dispositivos virtuais (como LUNs e plexes de LUN).</span><span class="sxs-lookup"><span data-stu-id="3353e-106">(Note that while VDS includes a software provider, you must purchase a hardware provider and the associated hardware separately to take advantage of the hardware provider objects.) These hardware provider objects represent physical devices (such as subsystems, drives, and controllers) and virtual devices (such as LUNs and LUN plexes).</span></span>

<span data-ttu-id="3353e-107">Um provedor de hardware deve criar um objeto COM para cada dispositivo físico ou virtual.</span><span class="sxs-lookup"><span data-stu-id="3353e-107">A hardware provider should create one COM object for each physical or virtual device.</span></span>

<span data-ttu-id="3353e-108">A ilustração a seguir mostra a relação entre o objeto de provedor e o conjunto de objetos de provedor de hardware, bem como a relação entre os vários objetos de provedor de hardware em si.</span><span class="sxs-lookup"><span data-stu-id="3353e-108">The illustration that follows shows the relationship between the provider object and the set of hardware provider objects, as well as the relationship between the various hardware provider objects themselves.</span></span>

![<span data-ttu-id="3353e-109">Diagrama que mostra a relação entre o ' provedor ' e o ' subsistema ', ' controlador ', ' LUN ', ' LUN Plex ', ' unidade ' e ' eixo '.</span><span class="sxs-lookup"><span data-stu-id="3353e-109">Diagram that shows the relationship between the 'Provider' and 'Subsystem', 'Controller', 'LUN', 'LUN plex', 'Drive', and 'Spindle'.</span></span> ](images/vdshwobjects.png)

<span data-ttu-id="3353e-110">Um objeto de provedor pode conter qualquer número de subsistemas.</span><span class="sxs-lookup"><span data-stu-id="3353e-110">A provider object can contain any number of subsystems.</span></span> <span data-ttu-id="3353e-111">Todos os provedores de hardware são capazes de gerenciar várias instâncias do mesmo modelo de subsistema.</span><span class="sxs-lookup"><span data-stu-id="3353e-111">All hardware providers are capable of managing multiple instances of the same subsystem model.</span></span> <span data-ttu-id="3353e-112">Muitos provedores de hardware também são capazes de gerenciar várias instâncias de diferentes modelos de subsistema.</span><span class="sxs-lookup"><span data-stu-id="3353e-112">Many hardware providers are also capable of managing multiple instances of different subsystem models.</span></span> <span data-ttu-id="3353e-113">Um único computador pode hospedar qualquer número de provedores de hardware.</span><span class="sxs-lookup"><span data-stu-id="3353e-113">A single computer can host any number of hardware providers.</span></span>

<span data-ttu-id="3353e-114">Um objeto de subsistema pode conter qualquer número de controladores e unidades e pode trazer qualquer número de LUNs.</span><span class="sxs-lookup"><span data-stu-id="3353e-114">A subsystem object can contain any number of controllers and drives, and can surface any number of LUNs.</span></span> <span data-ttu-id="3353e-115">Um objeto de LUN é composto de pelo menos um plex de LUN e cada Plex de LUN é mapeado para uma ou mais unidades, dependendo do tipo de plex.</span><span class="sxs-lookup"><span data-stu-id="3353e-115">A LUN object comprises of at least one LUN plex, and each LUN plex maps to one or more drives, depending on the plex type.</span></span> <span data-ttu-id="3353e-116">Os objetos do controlador podem gerenciar a entrada/saída de dados para qualquer número de objetos de LUN.</span><span class="sxs-lookup"><span data-stu-id="3353e-116">Controller objects can manage data input/output for any number of LUN objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3353e-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3353e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3353e-118">Modelo de objeto VDS</span><span class="sxs-lookup"><span data-stu-id="3353e-118">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
