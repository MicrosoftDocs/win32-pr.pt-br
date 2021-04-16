---
description: Recuperando eventos de serviço com suporte
ms.assetid: 1bf3aa08-7ffc-417f-a67e-9eee042337b9
title: Recuperando eventos de serviço com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f515b65b8ed062c346777224a64539f5229a704a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772611"
---
# <a name="retrieving-supported-service-events"></a>Recuperando eventos de serviço com suporte

O aplicativo WpdServicesApiSample inclui código que demonstra como um aplicativo pode recuperar os eventos com suporte de um determinado serviço Contacts chamando métodos nas interfaces a seguir.



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Interface                                                                            | Descrição                                                                                           |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Usado para recuperar a interface **IPortableDeviceServiceCapabilities** para acessar os eventos com suporte. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Fornece acesso aos eventos e atributos de evento com suporte.                                         |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contém a lista de eventos com suporte.                                                                |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contém os atributos de um determinado evento.                                                            |



 

Quando o usuário escolhe a opção "4" na linha de comando, o aplicativo invoca o método **ListSupportedEvents** encontrado no módulo percapabilities. cpp.

Observe que, antes de recuperar a lista de eventos, o aplicativo de exemplo abre um serviço de contatos em um dispositivo conectado.

Em WPD, um evento é descrito por seu nome, opções e parâmetros. O nome do evento é uma cadeia de caracteres amigável para scripts, por exemplo, "MyCustomEvent". As opções de evento indicam se um determinado evento é transmitido para todos os clientes e se esse evento dá suporte à reprodução automática. Os atributos de parâmetro de evento incluem o PROPERTYKEY e o VARTYPE de um determinado parâmetro.

Quatro métodos no módulo percapabilities. cpp suportam a recuperação de eventos com suporte para o serviço de contatos fornecido: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions** e **DisplayEventParameters**. O método **ListSupportedEvents** recupera uma contagem de eventos com suporte e o identificador GUID para cada evento. O método **DisplayEvent** exibe o nome ou o GUID do evento e, em seguida, chama **DisplayEventOptions** e **DisplayEventParameters** para exibir os dados relacionados ao evento.

O método **ListSupportedEvents** invoca o método [**IPortableDeviceService:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar uma interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Usando essa interface, ele recupera os eventos com suporte chamando o método [**IPortableDeviceServiceCapabilities:: GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) . O método **GetSupportedEvents** recupera os GUIDs de cada evento com suporte pelo serviço e copia esses GUIDs em um objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .

O código a seguir ilustra a recuperação de eventos de serviço com suporte.


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



Depois que o método **ListSupportedEvents** recupera os GUIDs que representam cada evento suportado pelo serviço fornecido, ele invoca o método **DisplayEvent** para recuperar dados específicos do evento. Esses dados incluem o nome do evento, suas opções (difusão ou reprodução automática), GUIDs de parâmetro, tipos de parâmetro e assim por diante.

O método **DisplayEvent** invoca o método [**IPortableDeviceServiceCapabilities:: geteventattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) para recuperar uma coleção de atributos para o evento fornecido. Em seguida, ele chama o método [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) e solicita que o driver retorne um nome amigável para o evento fornecido. Em seguida, **DisplayEvent** chama o [**IPortableDeviceValues:: GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) para recuperar as opções de evento. Por fim, DisplayEvent chama [**IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) para recuperar a lista de parâmetros de evento. Ele passa os dados retornados por esses métodos para as funções auxiliares **DisplayEventOptions** e **DisplayEventParameters** , que renderizam as opções e informações de parâmetro para o evento fornecido.

O código a seguir usa o método **DisplayEvent** .


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



A função auxiliar **DisplayEventOptions** recebe um objeto [**IPortableDeviceValues**](iportabledevicevalues.md) que contém os dados de opção do evento. Em seguida, ele chama o método [**IPortableDeviceValues:: Getboolvalue**](iportabledevicevalues-getboolvalue.md) para recuperar os dados de opções. Usando esses dados, ele renderiza uma cadeia de caracteres que indica se há suporte para as opções de difusão e reprodução automática.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



