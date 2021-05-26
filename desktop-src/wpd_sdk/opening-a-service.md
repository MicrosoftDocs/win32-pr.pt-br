---
description: Abrindo um serviço
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: Abrindo um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b273b8709a4d750085f14075d605f88ed0faa6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423916"
---
# <a name="opening-a-service"></a>Abrindo um serviço

Antes que seu aplicativo possa executar operações em um serviço, por exemplo, enumerando conteúdo ou recuperando descrições de eventos ou métodos com suporte, ele deve abrir o serviço. No aplicativo WpdServicesApiSample, essa tarefa é demonstrada no módulo do inenumeration. cpp usando as interfaces descritas na tabela a seguir.



| Interface                                                              | Descrição                                        |
|------------------------------------------------------------------------|----------------------------------------------------|
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | Usado para enumerar os serviços em um dispositivo.        |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Usado para abrir uma conexão com um serviço de dispositivo.     |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | Usado para manter as informações do cliente do aplicativo. |



 

O método que abre um serviço é [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open). Esse método usa dois argumentos: um identificador de plug-and-Play (PnP) para o serviço e um objeto [**IPortableDeviceValues**](iportabledevicevalues.md) que contém as informações do cliente do aplicativo.

Para obter um identificador de PnP para um determinado serviço, seu aplicativo chama o método [**IPortableDeviceServiceManager:: Getdeviceservices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) . Esse método recupera uma matriz de identificadores PnP para serviços de um GUID de categoria de serviço (por exemplo, contatos de serviço).

O aplicativo de serviço de exemplo recupera um identificador PnP para serviços de contatos dentro do método **EnumerateContactsServices** no módulo Service Enumeration. cpp. O exemplo de código a seguir é obtido deste método.


```C++
// For each device found, find the contacts service
for (dwIndex = 0; dwIndex < cPnpDeviceIDs; dwIndex++)
{
    DWORD   cPnpServiceIDs = 0;
    PWSTR   pPnpServiceID  = NULL;

    // First, pass NULL as the PWSTR array pointer to get the total number
    // of contacts services (SERVICE_Contacts) found on the device.
    // To find the total number of all services on the device, use GUID_DEVINTERFACE_WPD_SERVICE.
    hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, NULL, &cPnpServiceIDs);
    
    if (SUCCEEDED(hr) && (cPnpServiceIDs > 0))
    {                               
        // For simplicity, we are only using the first contacts service on each device
        cPnpServiceIDs = 1;
        hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, &pPnpServiceID, &cPnpServiceIDs);

        if (SUCCEEDED(hr))
        {
            // We've found the service, display it and save its PnP Identifier
            ContactsServicePnpIDs.Add(pPnpServiceID);

            printf("[%d] ", static_cast<DWORD>(ContactsServicePnpIDs.GetCount()-1));

            // Display information about the device that contains this service.
            DisplayDeviceInformation(pServiceManager, pPnpServiceID);

            // ContactsServicePnpIDs now owns the memory for this string
            pPnpServiceID = NULL;
        }
        else
        {
            printf("! Failed to get the first contacts service from '%ws, hr = 0x%lx\n",pPnpDeviceIDs[dwIndex],hr);
        }
    }
}
```



Depois que o aplicativo recupera o identificador PnP para o serviço, ele pode configurar as informações do cliente e chamar [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).

No aplicativo de exemplo, esse método é chamado dentro de **ChooseDeviceService** no módulo do inenumeration. cpp.

O [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) dá suporte a dois CLSIDs para **CoCreateInstance**. **CLSID \_ PortableDeviceService** retorna um ponteiro **IPortableDeviceService** que não agrega o marshaler de thread livre; **CLSID \_ PortableDeviceServiceFTM** é um novo CLSID que retorna um ponteiro **IPortableDeviceService** que agrega o marshaler de thread livre. Caso contrário, ambos os ponteiros darão suporte à mesma funcionalidade.

Os aplicativos que agem em Single Threaded Apartments devem usar **CLSID \_ PortableDeviceServiceFTM,** pois isso elimina a sobrecarga do marshaling de ponteiro de interface. **CLSID \_ PortableDeviceService** ainda tem suporte para aplicativos herdados.


```C++
hr = CoCreateInstance(CLSID_PortableDeviceServiceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pService));
if (SUCCEEDED(hr))
{
    hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the service for Read Write access, will open it for Read-only access instead\n");

            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);

            hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);

            if (FAILED(hr))
            {
                printf("! Failed to Open the service for Read access, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            printf("! Failed to Open the service, hr = 0x%lx\n",hr);
        }
    }
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPortableDeviceService Interface**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceServiceManager Interface**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



