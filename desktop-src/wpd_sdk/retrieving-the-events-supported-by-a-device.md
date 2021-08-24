---
description: Recuperando os eventos com suporte por um dispositivo
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: Recuperando os eventos com suporte por um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e0e24b5a4424d03c916ca73fd0192f9b6de0a80b6a2e2e67a129deb832f7bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119263116"
---
# <a name="retrieving-the-events-supported-by-a-device"></a>Recuperando os eventos com suporte por um dispositivo

Alguns drivers WPD são suportados pela notificação de eventos. Isso significa que um aplicativo pode se registrar com o driver para receber uma notificação quando ocorre uma ação específica. Por exemplo, um aplicativo pode se registrar para receber uma notificação quando um objeto é adicionado ou removido.

Há dez eventos predefinidos que um aplicativo pode monitorar. Eles são descritos na tabela a seguir.



| Evento                       | Descrição                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Funcionalidades do dispositivo atualizadas | Ocorre quando as funcionalidades do dispositivo foram alteradas.                                                                                      |
| Dispositivo removido              | Ocorre quando o dispositivo é desconectado.                                                                                                   |
| Redefinição do dispositivo                | Ocorre quando o dispositivo foi redefinido.                                                                                                 |
| Objeto adicionado                | Ocorre depois que um novo objeto fica disponível no dispositivo.                                                                             |
| Objeto removido              | Ocorre depois que um objeto foi removido do dispositivo.                                                                               |
| Transferência de objeto solicitada   | Indica que foi feita uma solicitação para transferir um objeto .                                                                          |
| Objeto atualizado              | Ocorre depois que um objeto ou seus filhos foram atualizados. (Os clientes conectados devem atualizar a exibição do objeto determinado.) |
| Armazenamento formato em andamento  | Ocorre quando o armazenamento do dispositivo está sendo formatado.                                                                                     |



 

Para ver uma lista das constantes associadas a esses eventos, consulte o [tópico Constantes de](event-constants.md) Evento.

A função ListSupportedEvents no módulo DeviceCapabilities.cpp demonstra a recuperação de eventos com suporte por um determinado dispositivo.

Seu aplicativo pode recuperar os identificadores de eventos com suporte por um dispositivo usando as interfaces descritas na tabela a seguir.



| Interface                                                                                      | Descrição                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [**IPortableDeviceCapabilities Interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fornece acesso aos métodos de recuperação de eventos com suporte. |
| [**IPortableDevicePropVariantCollection Interface**](iportabledevicepropvariantcollection.md) | Usado para enumerar e armazenar dados de categoria funcional.     |



 

A primeira tarefa realizada pelo aplicativo de exemplo é a recuperação de um objeto [**IPortableDeviceCapabilities,**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) que é usado para recuperar os eventos com suporte pelo dispositivo determinado.


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



Os eventos com suporte são recuperados chamando o [**método IPortableDeviceCapabilities::GetSupportedEvents.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) Esse método recupera uma coleção de identificadores de evento para o dispositivo determinado e os armazena em um [**objeto IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) apontado pelo argumento pEvents.


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



A próxima etapa é recuperar a contagem de eventos com suporte para que o aplicativo possa iterar pelo objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) e recuperar o identificador de cada um.


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

[**IPortableDevice Interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceCapabilities Interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**IPortableDevicePropVariantCollection Interface**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



