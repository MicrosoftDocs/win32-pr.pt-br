---
description: Recuperando os eventos com suporte de um dispositivo
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: Recuperando os eventos com suporte de um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a542a34d0938c7e2ff86118818714f18b1224f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506260"
---
# <a name="retrieving-the-events-supported-by-a-device"></a>Recuperando os eventos com suporte de um dispositivo

Alguns drivers WPD dão suporte à notificação de eventos. Isso significa que um aplicativo pode se registrar no driver para receber uma notificação quando ocorrer uma ação específica. Por exemplo, um aplicativo pode se registrar para receber uma notificação quando um objeto é adicionado ou removido.

Há dez eventos predefinidos que um aplicativo pode monitorar. Eles são descritos na tabela a seguir.



| Evento                       | Descrição                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Recursos do dispositivo atualizados | Ocorre quando os recursos do dispositivo foram alterados.                                                                                      |
| Dispositivo removido              | Ocorre quando o dispositivo está desconectado.                                                                                                   |
| Redefinição do dispositivo                | Ocorre quando o dispositivo é redefinido.                                                                                                 |
| Objeto adicionado                | Ocorre depois que um novo objeto é disponibilizado no dispositivo.                                                                             |
| Objeto removido              | Ocorre depois que um objeto é removido do dispositivo.                                                                               |
| Transferência de objeto solicitada   | Indica que uma solicitação foi feita para transferir um objeto.                                                                          |
| Objeto atualizado              | Ocorre após a atualização de um objeto ou de seus filhos. (Os clientes conectados devem atualizar sua exibição do objeto fornecido.) |
| Formato de armazenamento em andamento  | Ocorre quando o armazenamento do dispositivo está sendo formatado.                                                                                     |



 

Para obter uma lista das constantes associadas a esses eventos, consulte o tópico [constantes do evento](event-constants.md) .

A função ListSupportedEvents no módulo DeviceCapabilities. cpp demonstra a recuperação de eventos com suporte em um determinado dispositivo.

Seu aplicativo pode recuperar os identificadores para eventos com suporte de um dispositivo usando as interfaces descritas na tabela a seguir.



| Interface                                                                                      | Descrição                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fornece acesso aos métodos de recuperação de evento com suporte. |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Usado para enumerar e armazenar dados de categoria funcional.     |



 

A primeira tarefa realizada pelo aplicativo de exemplo é a recuperação de um objeto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , que é usado para recuperar os eventos com suporte pelo dispositivo especificado.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pEvents;
DWORD dwNumEvents = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}
```



Os eventos com suporte são recuperados chamando o método [**IPortableDeviceCapabilities:: GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) . Esse método recupera uma coleção de identificadores de eventos para o dispositivo fornecido e os armazena em um objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) apontado pelo argumento pEvents.


```C++
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetSupportedEvents(&pEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get supported events from the device, hr = 0x%lx\n",hr);
    }
}
```



A próxima etapa é recuperar a contagem de eventos com suporte para que o aplicativo possa iterar por meio do objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) e recuperar o identificador de cada um.


```C++
if (SUCCEEDED(hr))
{
    hr = pEvents->GetCount(&dwNumEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Supported Events Found on the device\n\n", dwNumEvents);

// Loop through each event and display its name
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
                // Display the event name
                DisplayEvent(*pv.puuid);
                printf("\n");
                // Display the event options
                DisplayEventOptions(pCapabilities, *pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Constantes de evento**](event-constants.md)
</dt> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



