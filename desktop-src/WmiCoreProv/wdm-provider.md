---
description: O provedor WDM (Windows Driver Model) concede acesso às classes, instâncias, métodos e eventos de drivers de hardware que estão em conformidade com o modelo WDM.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: Provedor WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d96ce356214f2788d3608b2ba85943e607394cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647702"
---
# <a name="wdm-provider"></a><span data-ttu-id="84e52-103">Provedor WDM</span><span class="sxs-lookup"><span data-stu-id="84e52-103">WDM Provider</span></span>

<span data-ttu-id="84e52-104">O provedor WDM (Windows Driver Model) concede acesso às classes, instâncias, métodos e eventos de drivers de hardware que estão em conformidade com o modelo WDM.</span><span class="sxs-lookup"><span data-stu-id="84e52-104">The WDM (Windows Driver Model) provider grants access to the classes, instances, methods, and events of hardware drivers that conform to the WDM model.</span></span> <span data-ttu-id="84e52-105">As classes para drivers de hardware residem no "root \\ WMI namespace".</span><span class="sxs-lookup"><span data-stu-id="84e52-105">The classes for hardware drivers reside in the "root\\wmi namespace".</span></span>

<span data-ttu-id="84e52-106">As classes WDM são definidas principalmente no WMI. mof.</span><span class="sxs-lookup"><span data-stu-id="84e52-106">WDM classes are defined primarily in Wmi.mof.</span></span>

<span data-ttu-id="84e52-107">O WDM é uma interface de sistema operacional por meio da qual os componentes de hardware fornecem informações e notificação de eventos.</span><span class="sxs-lookup"><span data-stu-id="84e52-107">WDM is an operating system interface through which hardware components provide information and event notification.</span></span> <span data-ttu-id="84e52-108">O provedor WDM é uma classe, instância, evento e provedor de métodos que permite que os aplicativos de gerenciamento acessem dados e eventos de drivers de dispositivo habilitados para WMI para WDM.</span><span class="sxs-lookup"><span data-stu-id="84e52-108">The WDM provider is a class, instance, event, and method provider that allows management applications access to data and events from WMI-for-WDM enabled device drivers.</span></span> <span data-ttu-id="84e52-109">As classes criadas pelo provedor WDM para representar os dados de driver de dispositivo residem apenas no namespace "root \\ WMI".</span><span class="sxs-lookup"><span data-stu-id="84e52-109">The classes created by the WDM provider to represent device driver data reside only in the "Root\\WMI" namespace.</span></span> <span data-ttu-id="84e52-110">Esse namespace já deve existir antes que o provedor WDM processe os drivers WDM instalados.</span><span class="sxs-lookup"><span data-stu-id="84e52-110">This namespace must already exist before the WDM provider will process the installed WDM drivers.</span></span>

<span data-ttu-id="84e52-111">O provedor WDM registra informações sobre as operações de WDM no arquivo WmiProv. log.</span><span class="sxs-lookup"><span data-stu-id="84e52-111">The WDM provider records information about WDM operations in the WmiProv.log file.</span></span> <span data-ttu-id="84e52-112">Para obter mais informações, consulte [arquivos de log do WMI](/windows/desktop/WmiSdk/wmi-log-files).</span><span class="sxs-lookup"><span data-stu-id="84e52-112">For more information, see [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span>

<span data-ttu-id="84e52-113">Como uma classe, instância, método e provedor de eventos, o provedor WDM implementa a interface [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) padrão, bem como os seguintes métodos de [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) :</span><span class="sxs-lookup"><span data-stu-id="84e52-113">As a class, instance, method, and event provider, the WDM provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the following [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="84e52-114">**CreateClassEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="84e52-114">**CreateClassEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [<span data-ttu-id="84e52-115">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="84e52-115">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="84e52-116">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="84e52-116">**GetObjectAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="84e52-117">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="84e52-117">**ExecMethodAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="84e52-118">**ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="84e52-118">**ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [<span data-ttu-id="84e52-119">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="84e52-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="84e52-120">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="84e52-120">**PutInstanceAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="84e52-121">O provedor WDM dá suporte ao evento [**WmiEvent**](/windows/desktop/WmiCoreProv/wmievent) extrínsecos, que notifica o WMI sobre eventos de drivers baseados em WDM.</span><span class="sxs-lookup"><span data-stu-id="84e52-121">The WDM provider supports the [**WMIEvent**](/windows/desktop/WmiCoreProv/wmievent) extrinsic event, which notifies WMI regarding events from WDM-based drivers.</span></span> <span data-ttu-id="84e52-122">Você pode registrar seus consumidores de eventos para eventos **WmiEvent** como faria com qualquer outro evento.</span><span class="sxs-lookup"><span data-stu-id="84e52-122">You can register your event consumers for **WMIEvent** events as you would any other event.</span></span> <span data-ttu-id="84e52-123">Para obter mais informações, consulte [recebendo um evento WMI](/windows/desktop/WmiSdk/receiving-a-wmi-event).</span><span class="sxs-lookup"><span data-stu-id="84e52-123">For more information, see [Receiving a WMI Event](/windows/desktop/WmiSdk/receiving-a-wmi-event).</span></span> <span data-ttu-id="84e52-124">Nenhum evento de criação de classe é gerado ao iniciar um driver.</span><span class="sxs-lookup"><span data-stu-id="84e52-124">No class creation events are raised when starting a driver.</span></span>

<span data-ttu-id="84e52-125">O provedor WDM dá suporte à seguinte classe:</span><span class="sxs-lookup"><span data-stu-id="84e52-125">The WDM provider supports the following class:</span></span>

-   [<span data-ttu-id="84e52-126">**WMIBinaryMofResource**</span><span class="sxs-lookup"><span data-stu-id="84e52-126">**WMIBinaryMofResource**</span></span>](wmibinarymofresource.md)

## <a name="related-topics"></a><span data-ttu-id="84e52-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="84e52-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84e52-128">Provedores de WMI</span><span class="sxs-lookup"><span data-stu-id="84e52-128">WMI Providers</span></span>](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[<span data-ttu-id="84e52-129">Acessando dados de drivers de dispositivo</span><span class="sxs-lookup"><span data-stu-id="84e52-129">Accessing Data from Device Drivers</span></span>](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
