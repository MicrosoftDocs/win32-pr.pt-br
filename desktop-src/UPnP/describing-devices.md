---
title: Descrevendo dispositivos
description: Há duas maneiras de obter objetos de dispositivo.
ms.assetid: a83fbf21-586e-4b92-9875-476d820c377d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abc84f15f6b52328585e05abfd95503087124b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822882"
---
# <a name="describing-devices"></a><span data-ttu-id="09121-103">Descrevendo dispositivos</span><span class="sxs-lookup"><span data-stu-id="09121-103">Describing Devices</span></span>

<span data-ttu-id="09121-104">Há duas maneiras de obter objetos de dispositivo:</span><span class="sxs-lookup"><span data-stu-id="09121-104">There are two ways to obtain device objects:</span></span>

-   <span data-ttu-id="09121-105">Usando a interface [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) .</span><span class="sxs-lookup"><span data-stu-id="09121-105">Using the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) interface.</span></span> <span data-ttu-id="09121-106">A interface **IUPnPDescriptionDocument** é a única interface que é segura para scripts.</span><span class="sxs-lookup"><span data-stu-id="09121-106">The **IUPnPDescriptionDocument** interface is the only interface that is safe for scripting.</span></span>
-   <span data-ttu-id="09121-107">Usando a interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) para obter uma interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="09121-107">Using the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface to obtain an [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface.</span></span>

<span data-ttu-id="09121-108">Os dois métodos retornam coleções de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="09121-108">Both methods return Devices collections.</span></span> <span data-ttu-id="09121-109">Em seguida, os aplicativos usam os métodos de dispositivo para recuperar propriedades sobre dispositivos.</span><span class="sxs-lookup"><span data-stu-id="09121-109">Applications then use the Device methods to retrieve properties about devices.</span></span>

<span data-ttu-id="09121-110">Os aplicativos são capazes de recuperar os seguintes tipos de informações:</span><span class="sxs-lookup"><span data-stu-id="09121-110">Applications are able to retrieve the following types of information:</span></span>

-   <span data-ttu-id="09121-111">Informações de hierarquia de dispositivo, incluindo dispositivos raiz, dispositivos pai e dispositivos filho.</span><span class="sxs-lookup"><span data-stu-id="09121-111">Device hierarchy information, including root devices, parent devices, and child devices.</span></span>
-   <span data-ttu-id="09121-112">Propriedades do dispositivo, incluindo UDNs, identificadores de recursos uniformes (URIs) e nomes legíveis pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="09121-112">Device properties, including UDNs, uniform resource identifiers (URIs), and user-readable names.</span></span>
-   <span data-ttu-id="09121-113">Informações do fabricante, incluindo nomes e páginas da Web relacionadas.</span><span class="sxs-lookup"><span data-stu-id="09121-113">Manufacturer information, including names and related Web pages.</span></span>
-   <span data-ttu-id="09121-114">Informações de modelo, incluindo nome, número, UPC, números de série e descrições de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09121-114">Model information, including the name, number, UPC, serial numbers and device descriptions.</span></span>
-   <span data-ttu-id="09121-115">Exiba informações, incluindo a URL para controlar o dispositivo e URLs das quais ícones são baixados.</span><span class="sxs-lookup"><span data-stu-id="09121-115">Display information, including the URL to control the device, and URLs from which icons are downloaded.</span></span>
-   <span data-ttu-id="09121-116">Serviços fornecidos por um determinado dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09121-116">Services provided by a particular device.</span></span>

<span data-ttu-id="09121-117">Os aplicativos também obtêm a URL do documento de descrição do dispositivo usando a interface [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) .</span><span class="sxs-lookup"><span data-stu-id="09121-117">Applications also obtain the URL of the device description document using the [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) interface.</span></span> <span data-ttu-id="09121-118">Em seguida, o aplicativo carrega o documento de descrição e trabalha com as propriedades de dispositivo e serviço que não são expostas pela interface [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) .</span><span class="sxs-lookup"><span data-stu-id="09121-118">The application then load the description document and work with device and service properties that are not exposed by the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface.</span></span> <span data-ttu-id="09121-119">Essa interface não pode ser usada no script, pois não é a interface padrão.</span><span class="sxs-lookup"><span data-stu-id="09121-119">This interface cannot be used in scripting, because it is not the default interface.</span></span>

## <a name="visual-basic-example"></a><span data-ttu-id="09121-120">Exemplo de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="09121-120">Visual Basic Example</span></span>

<span data-ttu-id="09121-121">O código de exemplo a seguir mostra o uso de [**IUPnPDeviceDocumentAccess:: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span><span class="sxs-lookup"><span data-stu-id="09121-121">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```VB
Sub GetDocumentURL()
Dim pDescDoc As IUPnPDeviceDocumentAccess
Dim strDescDocURL As String

'currentDevice is UPnPDevice object containing the current UPnP Device 
'We are trying to get IUPnPDeviceDocumentAccess interface in the UPnP Device object
Set pDescDoc = currentDevice

If Not (pDescDoc is Nothing) Then
  'Description Document URL is got from device
  strDescDocURL = pDescDoc.GetDocumentURL 
End If
```



## <a name="c-example"></a><span data-ttu-id="09121-122">Exemplo de C++</span><span class="sxs-lookup"><span data-stu-id="09121-122">C++ Example</span></span>

<span data-ttu-id="09121-123">O código de exemplo a seguir mostra o uso de [**IUPnPDeviceDocumentAccess:: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span><span class="sxs-lookup"><span data-stu-id="09121-123">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

int GetDeviceDocumentUrl () 
{
  HRESULT hr = S_OK;
  // List of interfaces needed
  IUPnPDeviceFinder *pDevFinder=NULL;
  IUPnPDevice *pDevice =NULL;
  IUPnPDeviceDocumentAccess* pDeviceDocument=NULL;
  BSTR bstrDeviceUDN =NULL;
  BSTR bstrDeviceDocumentURL = NULL; 

  bstrDeviceUDN = SysAllocString(L"uuid:234324234324");
  if(bstrDeviceUDN == NULL){
    printf("ERROR: Could not allocate memory\n");
    return -1;
  }  

  //CoInitialize the program so that we can create COM objects
  CoInitializeEx(NULL, COINIT_MULTITHREADED);

  //now try to instantiate the DeviceFinder object
  hr = CoCreateInstance(  CLSID_UPnPDeviceFinder, 
              NULL,
              CLSCTX_INPROC_SERVER,
              IID_IUPnPDeviceFinder,
              (LPVOID *) &pDevFinder); 

  if(!SUCCEEDED(hr)){
    printf("\nERROR: CoCreateInstance on IUPnPDeviceFinder returned HRESULT %x",hr);
    goto cleanup;
  }

  printf("\nGot a pointer to the IUPnPDeviceFinder Interface");

  printf("\n Finding the device of given UDN\n");
  hr =pDevFinder->FindByUDN(bstrDeviceUDN, &pDevice);
  if(hr!=S_OK)
  {
    printf("\nERROR: FindByUDN for %S returned HRESULT %x", bstrDeviceUDN, hr);
    goto cleanup;
  }

  printf("\n\tFindByUDN for device of UDN %S succeeded", bstrDeviceUDN);
  //Now query pDevice for IUPnPDeviceDocumentAccess
  hr = pDevice->QueryInterface(IID_IUPnPDeviceDocumentAccess, (VOID **)&pDeviceDocument);
  if(SUCCEEDED(hr)){
    // We have got a pointer to the IUPnPDeviceDocumentAccess interface.
    // GetDocumentURL is available only in Windows XP. 
    hr = pDeviceDocument->GetDocumentURL(&bstrDeviceDocumentURL);
    if(SUCCEEDED(hr))
      printf("\nThe Device Document URL is %S \n", bstrDeviceDocumentURL);
  }
    
cleanup:
  //release references to all interfaces 
  if(pDevFinder)
    pDevFinder->Release();
  if(pDevice)
    pDevice->Release();
  if(pDeviceDocument)
    pDeviceDocument->Release();
  
  // Free the bstr strings
  if(bstrDeviceDocumentURL)
    SysFreeString(bstrDeviceDocumentURL);
  if(bstrDeviceUDN)
    SysFreeString(bstrDeviceUDN);
  CoUninitialize();
  return 0;
}
```



 

 




