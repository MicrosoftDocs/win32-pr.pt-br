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
# <a name="describing-devices"></a>Descrevendo dispositivos

Há duas maneiras de obter objetos de dispositivo:

-   Usando a interface [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) . A interface **IUPnPDescriptionDocument** é a única interface que é segura para scripts.
-   Usando a interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) para obter uma interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .

Os dois métodos retornam coleções de dispositivos. Em seguida, os aplicativos usam os métodos de dispositivo para recuperar propriedades sobre dispositivos.

Os aplicativos são capazes de recuperar os seguintes tipos de informações:

-   Informações de hierarquia de dispositivo, incluindo dispositivos raiz, dispositivos pai e dispositivos filho.
-   Propriedades do dispositivo, incluindo UDNs, identificadores de recursos uniformes (URIs) e nomes legíveis pelo usuário.
-   Informações do fabricante, incluindo nomes e páginas da Web relacionadas.
-   Informações de modelo, incluindo nome, número, UPC, números de série e descrições de dispositivo.
-   Exiba informações, incluindo a URL para controlar o dispositivo e URLs das quais ícones são baixados.
-   Serviços fornecidos por um determinado dispositivo.

Os aplicativos também obtêm a URL do documento de descrição do dispositivo usando a interface [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) . Em seguida, o aplicativo carrega o documento de descrição e trabalha com as propriedades de dispositivo e serviço que não são expostas pela interface [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) . Essa interface não pode ser usada no script, pois não é a interface padrão.

## <a name="visual-basic-example"></a>Exemplo de Visual Basic

O código de exemplo a seguir mostra o uso de [**IUPnPDeviceDocumentAccess:: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).


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



## <a name="c-example"></a>Exemplo de C++

O código de exemplo a seguir mostra o uso de [**IUPnPDeviceDocumentAccess:: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).


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



 

 




