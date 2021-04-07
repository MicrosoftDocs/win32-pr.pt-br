---
title: Obtendo objetos de serviço
description: Os objetos de dispositivo expõem uma propriedade chamada serviços que retorna uma coleção de objetos de serviço que contém um objeto de serviço para cada serviço exportado pelo dispositivo.
ms.assetid: 8ef12b6e-cb9b-4406-95be-002117b8fc3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf951c9c620c23c2d4919dc4a8bcf082159fa7a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823905"
---
# <a name="obtaining-service-objects"></a><span data-ttu-id="4283a-103">Obtendo objetos de serviço</span><span class="sxs-lookup"><span data-stu-id="4283a-103">Obtaining Service Objects</span></span>

<span data-ttu-id="4283a-104">Os objetos de dispositivo expõem uma propriedade chamada [**Serviços**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) que retorna uma coleção de objetos de serviço que contém um objeto de serviço para cada serviço exportado pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4283a-104">Device objects expose a property called [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) that returns a collection of Service objects that contains one service object for each service exported by the device.</span></span> <span data-ttu-id="4283a-105">Os aplicativos podem atravessar essa coleção sequencialmente ou solicitar um serviço específico usando sua ID de serviço.</span><span class="sxs-lookup"><span data-stu-id="4283a-105">Applications are able to traverse this collection sequentially, or request a particular service by using its service ID.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="4283a-106">Exemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="4283a-106">VBScript Example</span></span>

<span data-ttu-id="4283a-107">O exemplo a seguir é um código VBScript que extrai objetos de serviço para dois dos serviços exportados por um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4283a-107">The following example is VBScript code that extracts Service objects for two of the services exported by a device.</span></span>


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



<span data-ttu-id="4283a-108">A primeira linha extrai a coleção de serviços do objeto de dispositivo consultando a propriedade [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) .</span><span class="sxs-lookup"><span data-stu-id="4283a-108">The first line extracts the services collection from the Device object by querying the [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property.</span></span> <span data-ttu-id="4283a-109">As duas próximas linhas obtêm os dois objetos de serviço desejados da coleção, especificando suas IDs de serviço.</span><span class="sxs-lookup"><span data-stu-id="4283a-109">The next two lines obtain the two desired Service objects from the collection by specifying their service IDs.</span></span> <span data-ttu-id="4283a-110">A coleção de serviços também pode ser atravessada sequencialmente usando um **para cada... próximo** loop.</span><span class="sxs-lookup"><span data-stu-id="4283a-110">The services collection can also be traversed sequentially by using a **for each … next** loop.</span></span>

## <a name="c-example"></a><span data-ttu-id="4283a-111">Exemplo de C++</span><span class="sxs-lookup"><span data-stu-id="4283a-111">C++ Example</span></span>

<span data-ttu-id="4283a-112">O exemplo a seguir mostra o código C++ necessário para obter objetos de serviço de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4283a-112">The following example shows the C++ code required to obtain Service objects from a device.</span></span> <span data-ttu-id="4283a-113">Primeiro, o código de exemplo consulta a propriedade [**IUPnPDevice:: Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) na interface que foi passada para a função.</span><span class="sxs-lookup"><span data-stu-id="4283a-113">First, the sample code queries the [**IUPnPDevice::Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property on the interface that was passed to the function.</span></span> <span data-ttu-id="4283a-114">Isso retorna uma coleção de serviços usando a interface [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) .</span><span class="sxs-lookup"><span data-stu-id="4283a-114">This returns a service collection using the [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) interface.</span></span> <span data-ttu-id="4283a-115">Para obter objetos de serviço individuais, use o método [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) e especifique as IDs de serviço solicitadas.</span><span class="sxs-lookup"><span data-stu-id="4283a-115">To obtain individual Service objects, use the [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) method, and specify the requested service IDs.</span></span> <span data-ttu-id="4283a-116">Para percorrer a coleção sequencialmente, use os métodos [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)e [**IEnumVARIANT:: Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) .</span><span class="sxs-lookup"><span data-stu-id="4283a-116">To traverse the collection sequentially, use the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next), and [**IEnumVARIANT::Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) methods.</span></span> <span data-ttu-id="4283a-117">Este exemplo é semelhante ao exemplo usado para percorrer a coleção [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="4283a-117">This example is similar to the example used to traverse the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) collection.</span></span>


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



 

 