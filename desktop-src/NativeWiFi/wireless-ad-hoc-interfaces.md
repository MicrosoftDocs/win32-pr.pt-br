---
description: A interface de programação ad hoc sem fio é composta pelas seguintes interfaces.
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: Interfaces ad hoc sem fio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810301"
---
# <a name="wireless-ad-hoc-interfaces"></a><span data-ttu-id="d668d-103">Interfaces ad hoc sem fio</span><span class="sxs-lookup"><span data-stu-id="d668d-103">Wireless Ad Hoc Interfaces</span></span>

<span data-ttu-id="d668d-104">A interface de programação ad hoc sem fio é composta pelas seguintes interfaces.</span><span class="sxs-lookup"><span data-stu-id="d668d-104">The wireless ad hoc programming interface is composed of the following interfaces.</span></span>



| <span data-ttu-id="d668d-105">Nome da Interface</span><span class="sxs-lookup"><span data-stu-id="d668d-105">Interface Name</span></span>                                                                       | <span data-ttu-id="d668d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d668d-106">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d668d-107">**IDot11AdHocInterface**</span><span class="sxs-lookup"><span data-stu-id="d668d-107">**IDot11AdHocInterface**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | <span data-ttu-id="d668d-108">Representa uma NIC (placa de interface de rede) sem fio.</span><span class="sxs-lookup"><span data-stu-id="d668d-108">Represents a wireless network interface card (NIC).</span></span>                                                    |
| [<span data-ttu-id="d668d-109">**IDot11AdHocInterfaceNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="d668d-109">**IDot11AdHocInterfaceNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | <span data-ttu-id="d668d-110">Define as notificações com suporte pelo [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).</span><span class="sxs-lookup"><span data-stu-id="d668d-110">Defines the notifications supported by [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).</span></span>           |
| [<span data-ttu-id="d668d-111">**IDot11AdHocManager**</span><span class="sxs-lookup"><span data-stu-id="d668d-111">**IDot11AdHocManager**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | <span data-ttu-id="d668d-112">Cria e gerencia redes ad hoc 802,11.</span><span class="sxs-lookup"><span data-stu-id="d668d-112">Creates and manages 802.11 ad hoc networks.</span></span>                                                            |
| [<span data-ttu-id="d668d-113">**IDot11AdHocManagerNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="d668d-113">**IDot11AdHocManagerNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | <span data-ttu-id="d668d-114">Define as notificações com suporte pela interface [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) .</span><span class="sxs-lookup"><span data-stu-id="d668d-114">Defines the notifications supported by the [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) interface.</span></span> |
| [<span data-ttu-id="d668d-115">**IDot11AdHocNetwork**</span><span class="sxs-lookup"><span data-stu-id="d668d-115">**IDot11AdHocNetwork**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | <span data-ttu-id="d668d-116">Representa um destino de rede ad hoc disponível no intervalo de conexão.</span><span class="sxs-lookup"><span data-stu-id="d668d-116">Represents an available ad hoc network destination within connection range.</span></span>                            |
| [<span data-ttu-id="d668d-117">**IDot11AdHocNetworkNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="d668d-117">**IDot11AdHocNetworkNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | <span data-ttu-id="d668d-118">Define as notificações com suporte pela interface [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) .</span><span class="sxs-lookup"><span data-stu-id="d668d-118">Defines the notifications supported by the [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) interface.</span></span> |
| [<span data-ttu-id="d668d-119">**IDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="d668d-119">**IDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | <span data-ttu-id="d668d-120">Especifica as configurações de segurança para uma rede ad hoc sem fio.</span><span class="sxs-lookup"><span data-stu-id="d668d-120">Specifies the security settings for a wireless ad hoc network.</span></span>                                         |
| [<span data-ttu-id="d668d-121">**IEnumDot11AdHocInterfaces**</span><span class="sxs-lookup"><span data-stu-id="d668d-121">**IEnumDot11AdHocInterfaces**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | <span data-ttu-id="d668d-122">Representa a coleção de interfaces de rede ad hoc 802,11 visíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="d668d-122">Represents the collection of currently visible 802.11 ad hoc network interfaces.</span></span>                       |
| [<span data-ttu-id="d668d-123">**IEnumDot11AdHocNetworks**</span><span class="sxs-lookup"><span data-stu-id="d668d-123">**IEnumDot11AdHocNetworks**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | <span data-ttu-id="d668d-124">Representa a coleção de redes ad hoc 802,11 visíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="d668d-124">Represents the collection of currently visible 802.11 ad hoc networks.</span></span>                                 |
| [<span data-ttu-id="d668d-125">**IEnumDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="d668d-125">**IEnumDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | <span data-ttu-id="d668d-126">Representa a coleção de configurações de segurança associadas a cada rede ad hoc sem fio visível.</span><span class="sxs-lookup"><span data-stu-id="d668d-126">Represents the collection of security settings associated with each visible wireless ad hoc network.</span></span>   |



 

> [!Note]  
> <span data-ttu-id="d668d-127">O modo ad hoc pode não estar disponível em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="d668d-127">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="d668d-128">A partir do Windows 8.1 e do Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .</span><span class="sxs-lookup"><span data-stu-id="d668d-128">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

 

 



