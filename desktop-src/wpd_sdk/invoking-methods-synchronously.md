---
description: Invocando métodos de serviço
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Invocando métodos de serviço
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0553e1490a6f8d0903756767397c30c2e1137a16a80609ed3a22da69188f799e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843103"
---
# <a name="invoking-service-methods"></a>Invocando métodos de serviço

O aplicativo WpdServicesApiSample inclui código que demonstra como um aplicativo pode invocar os métodos com suporte de um determinado serviço Contacts de forma síncrona. Este exemplo usa as seguintes interfaces



| Interface    | Descrição    |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Usado para recuperar a interface **IPortableDeviceServiceMethods** para invocar métodos em um determinado serviço.                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | Usado para invocar um método de serviço.                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | Usado para manter os parâmetros do método de saída e os resultados do método de entrada. Isso poderá ser **nulo** se o método não exigir nenhum parâmetro ou retornar nenhum resultado. |



 

Quando o usuário escolhe a opção "9" na linha de comando, o aplicativo invoca o método **invokemethods** que é encontrado no módulo permethods. cpp. Observe que, antes de invocar os métodos, o aplicativo de exemplo abre um serviço de contatos em um dispositivo conectado.

Os métodos de serviço encapsulam a funcionalidade que cada serviço define e implementa. Eles são exclusivos de cada tipo de serviço e são representados por um GUID. Por exemplo, o serviço de contatos define um método **BeginSync** que os aplicativos chamam para preparar o dispositivo para sincronizar objetos de contato e um método **endsync** para notificar o dispositivo de que a sincronização foi concluída. Os aplicativos executam um método chamando [**IPortableDeviceServiceMethods:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).

Os métodos de serviço não devem ser confundidos com comandos WPD. Os comandos WPD fazem parte da DDI (interface de driver de dispositivo) Standard WPD e são o mecanismo de comunicação entre um aplicativo WPD e o driver. Os comandos são predefinidos, agrupados por categorias, por exemplo, a **categoria de WPD \_ \_ comum** e são representados por uma estrutura **PROPERTYKEY** . Um aplicativo envia comandos para o driver de dispositivo chamando [**IPortableDeviceService:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand). Para obter mais informações, consulte o tópico comandos.

O método **invokemethods** invoca o método [**IPortableDeviceService:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar uma interface [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Usando essa interface, ele invoca os métodos **BeginSync** e **endsync** chamando o método [**IPortableDeviceServiceMethods:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) . Cada vez que chama **Invoke**, o aplicativo fornece o REFGUID para o método que é invocado.

O código a seguir usa o método **invokemethods** .


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



