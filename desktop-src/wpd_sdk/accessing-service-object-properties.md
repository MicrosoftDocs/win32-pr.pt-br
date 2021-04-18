---
description: Acessando Propriedades de objeto de serviço
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: Acessando Propriedades de objeto de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781205"
---
# <a name="accessing-service-object-properties"></a><span data-ttu-id="03d8d-103">Acessando Propriedades de objeto de serviço</span><span class="sxs-lookup"><span data-stu-id="03d8d-103">Accessing Service Object Properties</span></span>

<span data-ttu-id="03d8d-104">Um aplicativo pode ler e gravar propriedades para um único objeto em um serviço, para vários objetos identificados por identificadores de objeto ou para vários objetos do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="03d8d-104">An application can read and write properties for a single object on a service, for multiple objects identified by object identifiers, or for multiple objects of the same type.</span></span> <span data-ttu-id="03d8d-105">O tópico [Recuperando propriedades do objeto](retrieving-content-object-properties.md) descreve a leitura de propriedades de um único objeto em um serviço.</span><span class="sxs-lookup"><span data-stu-id="03d8d-105">The [Retrieving Object Properties](retrieving-content-object-properties.md) topic describes reading properties for a single object on a service.</span></span> <span data-ttu-id="03d8d-106">O tópico [gravando Propriedades de objeto](writing-content-object-properties.md) descreve a gravação de propriedades para um único objeto em um serviço.</span><span class="sxs-lookup"><span data-stu-id="03d8d-106">The [Writing Object Properties](writing-content-object-properties.md) topic describes writing properties for a single object on a service.</span></span>

<span data-ttu-id="03d8d-107">Consulte a seção [tarefas avançadas](advanced-tasks.md) para obter uma descrição da recuperação de propriedade para vários objetos.</span><span class="sxs-lookup"><span data-stu-id="03d8d-107">Refer to the [Advanced Tasks](advanced-tasks.md) section for a description of property retrieval for multiple objects.</span></span>

## <a name="when-to-use-service-property-definitions"></a><span data-ttu-id="03d8d-108">Quando usar definições de propriedade de serviço</span><span class="sxs-lookup"><span data-stu-id="03d8d-108">When to use Service Property Definitions</span></span>

<span data-ttu-id="03d8d-109">As chamadas à API WPD usadas para recuperar e definir propriedades de objeto para um serviço são as mesmas que as chamadas para recuperar propriedades de objeto para um dispositivo (compare "Recuperando propriedades para um único objeto" para obter um exemplo).</span><span class="sxs-lookup"><span data-stu-id="03d8d-109">The WPD API calls used for retrieving and setting object properties for a service are the same as the calls for retrieving object properties for a device (compare "Retrieving Properties for a Single Object" for an example).</span></span> <span data-ttu-id="03d8d-110">A principal diferença é que um conjunto diferente de PROPERTYKEYs é usado para consultar as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="03d8d-110">The key difference is that a different set of PROPERTYKEYs are used to query object properties.</span></span> <span data-ttu-id="03d8d-111">Para o WpdServiceApiSample, o serviço de dispositivo PROPERTYKEYs é usado (como **PKEY \_ GenericObj \_ Name**); para o WpdApiSample, o PropertyKeys de WPD é usado (como o **\_ \_ nome do objeto WPD**).</span><span class="sxs-lookup"><span data-stu-id="03d8d-111">For the WpdServiceApiSample, device service PROPERTYKEYs are used (such as **PKEY\_GenericObj\_Name**); for the WpdApiSample, WPD PROPERTYKEYs are used (such as **WPD\_OBJECT\_NAME**).</span></span>

<span data-ttu-id="03d8d-112">O serviço de dispositivo PROPERTYKEYs é definido em BridgeDeviceServices. h (incluído por cada arquivo de cabeçalho de serviço) e representa o conjunto comum de PROPERTYKEYS empregado por aplicativos de serviços de dispositivo e a implementação de firmware no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03d8d-112">Device service PROPERTYKEYs are defined in BridgeDeviceServices.h (included by each service header file), and represent the common set of PROPERTYKEYS employed by both device services applications and the firmware implementation on the device.</span></span> <span data-ttu-id="03d8d-113">Isso permite um conjunto consistente de definições em toda a pilha de dispositivos com a tradução mínima, agrupa o PROPERTYKEYs com base no serviço e permite que novos serviços sejam definidos com mais facilidade sem a necessidade de atualizar o esquema WPD.</span><span class="sxs-lookup"><span data-stu-id="03d8d-113">This allows a consistent set of definitions throughout the device stack with minimal translation, groups PROPERTYKEYs based on the service, and enables new services to be more easily defined without having to update the WPD schema.</span></span>

<span data-ttu-id="03d8d-114">O conjunto de PROPERTYKEYs usado dependerá das necessidades do seu aplicativo:</span><span class="sxs-lookup"><span data-stu-id="03d8d-114">The set of PROPERTYKEYs used will depend on your application's needs:</span></span>

-   <span data-ttu-id="03d8d-115">Se seu aplicativo estiver se comunicando com o dispositivo chamando [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), use o PROPERTYKEYs definido em PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="03d8d-115">If your application is communicating with the device by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), use the PROPERTYKEYs defined in PortableDevice.h.</span></span> <span data-ttu-id="03d8d-116">Um exemplo desse tipo de aplicativo é o WpdApiSample.</span><span class="sxs-lookup"><span data-stu-id="03d8d-116">An example of such an application is the WpdApiSample.</span></span>
-   <span data-ttu-id="03d8d-117">Se seu aplicativo estiver se comunicando com os serviços de dispositivo chamando [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), use o PROPERTYKEYS definido em BridgeDeviceServices. h.</span><span class="sxs-lookup"><span data-stu-id="03d8d-117">If your application is communicating with device services by calling [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), use the PROPERTYKEYS defined in BridgeDeviceServices.h.</span></span> <span data-ttu-id="03d8d-118">Um exemplo desse tipo de aplicativo é o WpdServicesApiSample.</span><span class="sxs-lookup"><span data-stu-id="03d8d-118">An example of such an application is the WpdServicesApiSample.</span></span>
-   <span data-ttu-id="03d8d-119">Se você estiver escrevendo um aplicativo complexo que precisa dar suporte a um híbrido de serviços de dispositivo e ao dispositivo (isso significa que seu aplicativo chama **IPortableDevice:: Open** e **IPortableDeviceService:: Open**), você precisará usar o PROPERTYKEYs WPD ao usar IPortableDevice e suas interfaces derivadas e o serviço de dispositivo PROPERTYKEYs ao usar [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) e suas interfaces derivadas.</span><span class="sxs-lookup"><span data-stu-id="03d8d-119">If you are writing a complex application that needs to support a hybrid of both device services and the device (this means your application calls both **IPortableDevice::Open** and **IPortableDeviceService::Open**), you will need to use the WPD PROPERTYKEYs when using IPortableDevice and its derived interfaces, and device service PROPERTYKEYs when using [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) and its derived interfaces.</span></span>

<span data-ttu-id="03d8d-120">A maioria dos aplicativos WPD deve enquadrar-se na primeira ou segunda categoria.</span><span class="sxs-lookup"><span data-stu-id="03d8d-120">Most WPD applications should fall into the first or second category.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03d8d-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03d8d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03d8d-122">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="03d8d-122">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="03d8d-123">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="03d8d-123">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="03d8d-124">Recuperando propriedades do objeto</span><span class="sxs-lookup"><span data-stu-id="03d8d-124">Retrieving Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="03d8d-125">Gravando Propriedades do objeto</span><span class="sxs-lookup"><span data-stu-id="03d8d-125">Writing Object Properties</span></span>](writing-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="03d8d-126">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="03d8d-126">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



