---
description: Invocando métodos de serviço
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Invocando métodos de serviço
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b9540cf7378e13d56af2611d6216897c6750f6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424196"
---
# <a name="invoking-service-methods"></a><span data-ttu-id="35b7b-103">Invocando métodos de serviço</span><span class="sxs-lookup"><span data-stu-id="35b7b-103">Invoking Service Methods</span></span>

<span data-ttu-id="35b7b-104">O aplicativo WpdServicesApiSample inclui código que demonstra como um aplicativo pode invocar os métodos com suporte de um determinado serviço Contacts de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="35b7b-104">The WpdServicesApiSample application includes code that demonstrates how an application can invoke the methods supported by a given Contacts service synchronously..</span></span> <span data-ttu-id="35b7b-105">Este exemplo usa as seguintes interfaces</span><span class="sxs-lookup"><span data-stu-id="35b7b-105">This sample uses the following interfaces</span></span>



| <span data-ttu-id="35b7b-106">Interface</span><span class="sxs-lookup"><span data-stu-id="35b7b-106">Interface</span></span>    | <span data-ttu-id="35b7b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="35b7b-107">Description</span></span>    |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35b7b-108">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="35b7b-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="35b7b-109">Usado para recuperar a interface **IPortableDeviceServiceMethods** para invocar métodos em um determinado serviço.</span><span class="sxs-lookup"><span data-stu-id="35b7b-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="35b7b-110">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="35b7b-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | <span data-ttu-id="35b7b-111">Usado para invocar um método de serviço.</span><span class="sxs-lookup"><span data-stu-id="35b7b-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="35b7b-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="35b7b-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="35b7b-113">Usado para manter os parâmetros do método de saída e os resultados do método de entrada.</span><span class="sxs-lookup"><span data-stu-id="35b7b-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="35b7b-114">Isso poderá ser **nulo** se o método não exigir nenhum parâmetro ou retornar nenhum resultado.</span><span class="sxs-lookup"><span data-stu-id="35b7b-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |



 

<span data-ttu-id="35b7b-115">Quando o usuário escolhe a opção "9" na linha de comando, o aplicativo invoca o método **invokemethods** que é encontrado no módulo permethods. cpp.</span><span class="sxs-lookup"><span data-stu-id="35b7b-115">When the user chooses option "9" at the command line, the application invokes the **InvokeMethods** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="35b7b-116">Observe que, antes de invocar os métodos, o aplicativo de exemplo abre um serviço de contatos em um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="35b7b-116">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="35b7b-117">Os métodos de serviço encapsulam a funcionalidade que cada serviço define e implementa.</span><span class="sxs-lookup"><span data-stu-id="35b7b-117">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="35b7b-118">Eles são exclusivos de cada tipo de serviço e são representados por um GUID.</span><span class="sxs-lookup"><span data-stu-id="35b7b-118">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="35b7b-119">Por exemplo, o serviço de contatos define um método **BeginSync** que os aplicativos chamam para preparar o dispositivo para sincronizar objetos de contato e um método **endsync** para notificar o dispositivo de que a sincronização foi concluída.</span><span class="sxs-lookup"><span data-stu-id="35b7b-119">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="35b7b-120">Os aplicativos executam um método chamando [**IPortableDeviceServiceMethods:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span><span class="sxs-lookup"><span data-stu-id="35b7b-120">Applications execute a method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="35b7b-121">Os métodos de serviço não devem ser confundidos com comandos WPD.</span><span class="sxs-lookup"><span data-stu-id="35b7b-121">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="35b7b-122">Os comandos WPD fazem parte da DDI (interface de driver de dispositivo) Standard WPD e são o mecanismo de comunicação entre um aplicativo WPD e o driver.</span><span class="sxs-lookup"><span data-stu-id="35b7b-122">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="35b7b-123">Os comandos são predefinidos, agrupados por categorias, por exemplo, **WPD \_ CATEGORY \_ COMMON** e são representados por uma **estrutura PROPERTYKEY.**</span><span class="sxs-lookup"><span data-stu-id="35b7b-123">Commands are predefined, grouped by categories, for example, **WPD\_CATEGORY\_COMMON**, and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="35b7b-124">Um aplicativo envia comandos para o driver de dispositivo chamando [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="35b7b-124">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="35b7b-125">Para obter mais informações, consulte o tópico Comandos.</span><span class="sxs-lookup"><span data-stu-id="35b7b-125">For more information, see the Commands topic.</span></span>

<span data-ttu-id="35b7b-126">O **método InvokeMethods** invoca o método [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar uma interface [**IPortableDeviceServiceMethods.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)</span><span class="sxs-lookup"><span data-stu-id="35b7b-126">The **InvokeMethods** method invokes the [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="35b7b-127">Usando essa interface, ele invoca os métodos **BeginSync** e **EndSync** chamando o [**método IPortableDeviceServiceMethods::Invoke.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods)</span><span class="sxs-lookup"><span data-stu-id="35b7b-127">Using this interface, it invokes the **BeginSync** and **EndSync** methods by calling the [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="35b7b-128">Sempre que ele chama **Invoke**, o aplicativo fornece o REFGUID para o método invocado.</span><span class="sxs-lookup"><span data-stu-id="35b7b-128">Each time it calls **Invoke**, the application supplies the REFGUID for the method that is invoked.</span></span>

<span data-ttu-id="35b7b-129">O código a seguir usa **o método InvokeMethods.**</span><span class="sxs-lookup"><span data-stu-id="35b7b-129">The following code uses the **InvokeMethods** method.</span></span>


```C++
// Invoke methods on the Contacts Service.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethods(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke() the BeginSync method
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_BeginSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_EndSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        } 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="35b7b-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35b7b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35b7b-131">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="35b7b-131">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="35b7b-132">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="35b7b-132">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="35b7b-133">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="35b7b-133">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



