---
title: Obtendo objetos de serviço
description: Os objetos de dispositivo expõem uma propriedade chamada Serviços que retorna uma coleção de objetos de serviço que contém um objeto de serviço para cada serviço exportado pelo dispositivo.
ms.assetid: 8ef12b6e-cb9b-4406-95be-002117b8fc3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b7fca24bfc79a9458cfb964af28edba813a90ef17924a68fd0d1689e047884c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999566"
---
# <a name="obtaining-service-objects"></a>Obtendo objetos de serviço

Os objetos de dispositivo expõem uma propriedade chamada [**Serviços**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) que retorna uma coleção de objetos de serviço que contém um objeto de serviço para cada serviço exportado pelo dispositivo. Os aplicativos podem percorrer essa coleção sequencialmente ou solicitar um serviço específico usando sua ID de serviço.

## <a name="vbscript-example"></a>Exemplo de VBScript

O exemplo a seguir é o código VBScript que extrai objetos de serviço para dois dos serviços exportados por um dispositivo.


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



A primeira linha extrai a coleção de serviços do objeto Device consultando a [**propriedade**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) Services. As duas linhas a seguir obtém os dois objetos de Serviço desejados da coleção especificando suas IDs de serviço. A coleção de serviços também pode ser percorrido sequencialmente usando um **para cada ... próximo** loop.

## <a name="c-example"></a>Exemplo de C++

O exemplo a seguir mostra o código C++ necessário para obter objetos de serviço de um dispositivo. Primeiro, o código de exemplo consulta a [**propriedade IUPnPDevice::Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) na interface que foi passada para a função. Isso retorna uma coleção de serviços usando a interface [**IUPnPServices.**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) Para obter objetos de serviço individuais, use [**o método Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) e especifique as IDs de serviço solicitadas. Para percorrer a coleção sequencialmente, use os métodos [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)e [**IEnumVARIANT::Skip.**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) Este exemplo é semelhante ao exemplo usado para percorrer a [**coleção IUPnPDevices.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")


HRESULT ExtractServices(IUPnPDevice * pDevice)
{
    // Create a BSTR to hold the service name
    BSTR bstrServiceName = SysAllocString(L"urn:upnp-org:servicId:DVDVideo");
    if (NULL == bstrServiceName)
    {
        return E_OUTOFMEMORY;
    }
    // Get the list of services available on the device
    IUPnPServices * pServices = NULL;
    HRESULT hr = pDevice->get_Services(&pServices);
    if (SUCCEEDED(hr))
    {
        // Retrieve the service we are interested in
        IUPnPService * pAppService = NULL;
        hr = pServices->get_Item(bstrServiceName, &pAppService);
        if (SUCCEEDED(hr))
        {
            // Do something interesting with the service object
            pAppService->Release();
        }
        pServices->Release();
    }
    SysFreeString(bstrServiceName);
    return hr;
}
```



 

 