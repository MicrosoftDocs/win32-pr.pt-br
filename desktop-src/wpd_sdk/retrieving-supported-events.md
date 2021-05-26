---
description: Recuperando eventos de serviço com suporte
ms.assetid: 1bf3aa08-7ffc-417f-a67e-9eee042337b9
title: Recuperando eventos de serviço com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc1df4c8255a4dc2a1297ae99216437ac3b4c9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423466"
---
# <a name="retrieving-supported-service-events"></a><span data-ttu-id="de6d8-103">Recuperando eventos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="de6d8-103">Retrieving Supported Service Events</span></span>

<span data-ttu-id="de6d8-104">O aplicativo WpdServicesApiSample inclui código que demonstra como um aplicativo pode recuperar os eventos com suporte por um determinado serviço Contacts chamando métodos nas interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="de6d8-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the events supported by a given Contacts service by calling methods on the following interfaces.</span></span>



| <span data-ttu-id="de6d8-105">Interface</span><span class="sxs-lookup"><span data-stu-id="de6d8-105">Interface</span></span>                | <span data-ttu-id="de6d8-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="de6d8-106">Description</span></span>    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de6d8-107">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="de6d8-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="de6d8-108">Usado para recuperar a interface **IPortableDeviceServiceCapabilities** para acessar os eventos com suporte.</span><span class="sxs-lookup"><span data-stu-id="de6d8-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="de6d8-109">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="de6d8-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="de6d8-110">Fornece acesso aos eventos e atributos de evento com suporte.</span><span class="sxs-lookup"><span data-stu-id="de6d8-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="de6d8-111">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="de6d8-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="de6d8-112">Contém a lista de eventos com suporte.</span><span class="sxs-lookup"><span data-stu-id="de6d8-112">Contains the list of supported events.</span></span>                                                                |
| [<span data-ttu-id="de6d8-113">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="de6d8-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="de6d8-114">Contém os atributos de um determinado evento.</span><span class="sxs-lookup"><span data-stu-id="de6d8-114">Contains the attributes for a given event.</span></span>                                                            |



 

<span data-ttu-id="de6d8-115">Quando o usuário escolhe a opção "4" na linha de comando, o aplicativo invoca o **método ListSupportedEvents** encontrado no módulo ServiceCapabilities.cpp.</span><span class="sxs-lookup"><span data-stu-id="de6d8-115">When the user chooses option "4" at the command line, the application invokes the **ListSupportedEvents** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="de6d8-116">Observe que, antes de recuperar a lista de eventos, o aplicativo de exemplo abre um serviço Contatos em um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="de6d8-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="de6d8-117">No WPD, um evento é descrito por seu nome, opções e parâmetros.</span><span class="sxs-lookup"><span data-stu-id="de6d8-117">In WPD, an event is described by its name, options, and parameters.</span></span> <span data-ttu-id="de6d8-118">O nome do evento é uma cadeia de caracteres amigável para script, por exemplo, "MyCustomEvent".</span><span class="sxs-lookup"><span data-stu-id="de6d8-118">The event name is a script-friendly string, for example, "MyCustomEvent".</span></span> <span data-ttu-id="de6d8-119">As opções de evento indicam se um determinado evento é transmitido para todos os clientes e se esse evento dá suporte à reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="de6d8-119">The event options indicate whether a given event is broadcast to all clients and whether that event supports autoplay.</span></span> <span data-ttu-id="de6d8-120">Os atributos de parâmetro de evento incluem PROPERTYKEY e VARTYPE de um determinado parâmetro.</span><span class="sxs-lookup"><span data-stu-id="de6d8-120">The event parameter attributes includes a given parameter's PROPERTYKEY and VARTYPE.</span></span>

<span data-ttu-id="de6d8-121">Quatro métodos no módulo ServiceCapabilities.cpp são compatíveis com a recuperação de eventos com suporte para o serviço Contacts determinado: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions** e **DisplayEventParameters**.</span><span class="sxs-lookup"><span data-stu-id="de6d8-121">Four methods in the ServiceCapabilities.cpp module support the retrieval of supported events for the given Contacts service: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions**, and **DisplayEventParameters**.</span></span> <span data-ttu-id="de6d8-122">O **método ListSupportedEvents** recupera uma contagem de eventos com suporte e o identificador guid para cada evento.</span><span class="sxs-lookup"><span data-stu-id="de6d8-122">The **ListSupportedEvents** method retrieves a count of supported events and the GUID identifier for each event.</span></span> <span data-ttu-id="de6d8-123">O método **DisplayEvent** exibe o nome ou o GUID do evento e, em seguida, chama **DisplayEventOptions** e **DisplayEventParameters** para exibir os dados relacionados ao evento.</span><span class="sxs-lookup"><span data-stu-id="de6d8-123">The **DisplayEvent** method displays the event name or GUID, and then calls **DisplayEventOptions** and **DisplayEventParameters** to display the event-related data.</span></span>

<span data-ttu-id="de6d8-124">O método **ListSupportedEvents** invoca o método [**IPortableDeviceService:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar uma interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="de6d8-124">The **ListSupportedEvents** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="de6d8-125">Usando essa interface, ele recupera os eventos com suporte chamando o método [**IPortableDeviceServiceCapabilities:: GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) .</span><span class="sxs-lookup"><span data-stu-id="de6d8-125">Using this interface, it retrieves the supported events by calling the [**IPortableDeviceServiceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="de6d8-126">O método **GetSupportedEvents** recupera os GUIDs de cada evento com suporte pelo serviço e copia esses GUIDs em um objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="de6d8-126">The **GetSupportedEvents** method retrieves the GUIDs for each event supported by the service and copies those GUIDs into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="de6d8-127">O código a seguir ilustra a recuperação de eventos de serviço com suporte.</span><span class="sxs-lookup"><span data-stu-id="de6d8-127">The following code illustrates retrieving supported service events.</span></span>


```C++
// List all supported events on the service
void ListSupportedEvents(
    IPortableDeviceService* pService)
{
    HRESULT hr          = S_OK;
    DWORD   dwNumEvents = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pEvents;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all events supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedEvents(&pEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get supported events from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported events found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pEvents->GetCount(&dwNumEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Events Found on the service\n\n", dwNumEvents);

    // Loop through each event and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pEvents->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have an event.  It is assumed that
                // events are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayEvent(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



<span data-ttu-id="de6d8-128">Depois que o método **ListSupportedEvents** recupera os GUIDs que representam cada evento suportado pelo serviço fornecido, ele invoca o método **DisplayEvent** para recuperar dados específicos do evento.</span><span class="sxs-lookup"><span data-stu-id="de6d8-128">After the **ListSupportedEvents** method retrieves the GUIDs representing each event supported by the given service, it invokes the **DisplayEvent** method to retrieve event-specific data.</span></span> <span data-ttu-id="de6d8-129">Esses dados incluem o nome do evento, suas opções (difusão ou reprodução automática), GUIDs de parâmetro, tipos de parâmetro e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="de6d8-129">This data includes the event name, its options (broadcast or autoplay), parameter GUIDs, parameter types, and so on.</span></span>

<span data-ttu-id="de6d8-130">O método **DisplayEvent** invoca o método [**IPortableDeviceServiceCapabilities:: geteventattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) para recuperar uma coleção de atributos para o evento fornecido.</span><span class="sxs-lookup"><span data-stu-id="de6d8-130">The **DisplayEvent** method invokes the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method to retrieve a collection of attributes for the given event.</span></span> <span data-ttu-id="de6d8-131">Em seguida, ele chama o método [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) e solicita que o driver retorne um nome amigável para o evento fornecido.</span><span class="sxs-lookup"><span data-stu-id="de6d8-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a user-friendly name for the given event.</span></span> <span data-ttu-id="de6d8-132">Em seguida, **DisplayEvent** chama o [**IPortableDeviceValues:: GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) para recuperar as opções de evento.</span><span class="sxs-lookup"><span data-stu-id="de6d8-132">Next, **DisplayEvent** calls the [**IPortableDeviceValues::GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) to retrieve the event options.</span></span> <span data-ttu-id="de6d8-133">Por fim, DisplayEvent chama [**IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) para recuperar a lista de parâmetros de evento.</span><span class="sxs-lookup"><span data-stu-id="de6d8-133">Finally, DisplayEvent calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the list of event parameters.</span></span> <span data-ttu-id="de6d8-134">Ele passa os dados retornados por esses métodos para as funções auxiliares **DisplayEventOptions** e **DisplayEventParameters** , que renderizam as opções e informações de parâmetro para o evento fornecido.</span><span class="sxs-lookup"><span data-stu-id="de6d8-134">It passes the data returned by these methods to the **DisplayEventOptions** and the **DisplayEventParameters** helper functions, which render the options and parameter information for the given event.</span></span>

<span data-ttu-id="de6d8-135">O código a seguir usa o método **DisplayEvent** .</span><span class="sxs-lookup"><span data-stu-id="de6d8-135">The following code uses the **DisplayEvent** method.</span></span>


```C++
// Display basic information about an event
void DisplayEvent(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Event)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the event attributes which describe the event
    HRESULT hr = pCapabilities->GetEventAttributes(Event, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the event attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the event if it is available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_EVENT_ATTRIBUTE_NAME, &pszFormatName);
        if (SUCCEEDED(hr))
        {
            printf("%ws\n", pszFormatName);
        }
        else
        {
            printf("%ws\n", (PWSTR)CGuidToString(Event));
        }       

        // Display the event options
        hr = pAttributes->GetIPortableDeviceValuesValue(WPD_EVENT_ATTRIBUTE_OPTIONS, &pOptions);
        if (SUCCEEDED(hr))
        {
            DisplayEventOptions(pOptions);
        }
        else
        {
            printf("! Failed to get the event options, hr = 0x%lx\n", hr);
        }       

        // Display the event parameters
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_EVENT_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayEventParameters(pCapabilities, Event, pParameters);
        }
        else
        {
            printf("! Failed to get the event parameters, hr = 0x%lx\n", hr);
        }       
        
        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



<span data-ttu-id="de6d8-136">A **função auxiliar DisplayEventOptions** recebe um [**objeto IPortableDeviceValues**](iportabledevicevalues.md) que contém os dados de opção do evento.</span><span class="sxs-lookup"><span data-stu-id="de6d8-136">The **DisplayEventOptions** helper function receives an [**IPortableDeviceValues**](iportabledevicevalues.md) object which contains the event's option data.</span></span> <span data-ttu-id="de6d8-137">Em seguida, ele chama [**o método IPortableDeviceValues::GetBoolValue**](iportabledevicevalues-getboolvalue.md) para recuperar os dados de opções.</span><span class="sxs-lookup"><span data-stu-id="de6d8-137">It then calls the [**IPortableDeviceValues::GetBoolValue**](iportabledevicevalues-getboolvalue.md) method to retrieve the options data.</span></span> <span data-ttu-id="de6d8-138">Usando esses dados, ele renderiza uma cadeia de caracteres que indica se há suporte para as opções de transmissão e reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="de6d8-138">Using this data, it renders a string indicating whether the broadcast and autoplay options are supported.</span></span>


```C++
// Display the basic event options.
void DisplayEventOptions(
    IPortableDeviceValues* pOptions)
{
    printf("\tEvent Options:\n");
    // Read the WPD_EVENT_OPTION_IS_BROADCAST_EVENT value to see if the event is
    // a broadcast event. If the read fails, assume FALSE
    BOOL  bIsBroadcastEvent = FALSE;
    pOptions->GetBoolValue(WPD_EVENT_OPTION_IS_BROADCAST_EVENT, &bIsBroadcastEvent);
    printf("\tWPD_EVENT_OPTION_IS_BROADCAST_EVENT = %ws\n",bIsBroadcastEvent ? L"TRUE" : L"FALSE");
}
```



## <a name="related-topics"></a><span data-ttu-id="de6d8-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de6d8-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de6d8-140">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="de6d8-140">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="de6d8-141">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="de6d8-141">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="de6d8-142">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="de6d8-142">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="de6d8-143">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="de6d8-143">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="de6d8-144">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="de6d8-144">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



