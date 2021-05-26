---
description: Invocar métodos de serviço de forma assíncrona
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Invocar métodos de serviço de forma assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef4f0eb2e75b977b53300bed6eab4c909fa7796
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423846"
---
# <a name="invoking-service-methods-asynchronously"></a>Invocar métodos de serviço de forma assíncrona

O aplicativo WpdServiceApiSample inclui código que demonstra como um aplicativo pode invocar os métodos de serviço de forma assíncrona. Este exemplo usa as interfaces a seguir.



| Interface    | Descrição          |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | Usado para recuperar a interface **IPortableDeviceServiceMethods** para invocar métodos em um determinado serviço.                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | Usado para invocar um método de serviço.                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                                  | Usado para manter os parâmetros de método de saída e os resultados do método de entrada. Isso poderá ser **NULL** se o método não exigir parâmetros ou retornar resultados. |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | Implementado pelo aplicativo para receber os resultados do método quando um método for concluído.                                                                               |



 

Quando o usuário escolhe a opção "10" na linha de comando, o aplicativo invoca o método **InvokeMethodsAsync** encontrado no módulo ServiceMethods.cpp. Observe que, antes de invocar os métodos, o aplicativo de exemplo abre um serviço Contatos em um dispositivo conectado.

Os métodos de serviço encapsulam a funcionalidade que cada serviço define e implementa. Eles são exclusivos para cada tipo de serviço e são representados por um GUID. Por exemplo, o serviço Contatos define um método **BeginSync** que os aplicativos chamam para preparar o dispositivo para sincronizar objetos contact e um **método EndSync** para notificar o dispositivo de que a sincronização foi concluída. Os aplicativos executam um método de serviço de dispositivo portátil chamando [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).

Os métodos de serviço não devem ser confundidos com comandos WPD. Os comandos WPD fazem parte da DDI (interface de driver de dispositivo) Standard WPD e são o mecanismo de comunicação entre um aplicativo WPD e o driver. Os comandos são predefinidos, agrupados por categorias (por exemplo, a **categoria de WPD \_ \_ comum**) e são representados por uma estrutura de **PROPERTYKEY** . Um aplicativo envia comandos para o driver de dispositivo chamando [**IPortableDeviceService:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand). Para obter mais informações, consulte o tópico comandos.

O método **InvokeMethodsAsync** invoca [**IPortableDeviceService:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar uma interface [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Usando essa interface, ela invoca a função auxiliar **InvokeMethodAsync** duas vezes; uma vez para o método **BeginSync** e uma vez para o método **endsync** . Neste exemplo, **InvokeMethodAsync** aguarda indefinidamente por um evento global ser sinalizado quando [**IPortableDeviceServiceMethodCallback:: OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) é chamado.

O código a seguir usa o método **InvokeMethodsAsync** .


```C++
// Invoke methods on the Contacts Service asynchornously.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethodsAsync(IPortableDeviceService* pService)
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

    // Invoke the BeginSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_BeginSync);

        // This method does not take any parameters, so we pass in NULL
        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_BeginSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_EndSync);

        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_EndSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
    }
}
```



A função auxiliar **InvokeMethodAsync** faz o seguinte para cada método que ele invoca:

-   Cria um identificador de evento global que ele monitora para determinar a conclusão do método.
-   Cria um objeto **CMethodCallback** que é fornecido como um argumento para [**IPortableDeviceServiceMethods: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).
-   Chama o método **IPortableDeviceServiceMethods:: InvokeAsync** para invocar o método fornecido.
-   Monitora o identificador de evento global para conclusão.
-   Executa a limpeza.

A classe **CMethodCallback** demonstra como um aplicativo pode implementar o [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback). A implementação de **OnComplete** nessa classe sinaliza um evento para notificar o aplicativo de que o método de serviço foi concluído. Além do método **OnComplete,** essa classe implementa **AddRef,** **QueryInterface** e **Release**, que são usados para manter a contagem de referência do objeto e as interfaces que ele implementa.


```C++
class CMethodCallback : public IPortableDeviceServiceMethodCallback
{
public:
   CMethodCallback () : m_cRef(1)
   {
   }

   ~CMethodCallback ()
   {
   }

public:
    // IPortableDeviceServiceMethodCallback::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE OnComplete(
        HRESULT                 hrStatus,
        IPortableDeviceValues*  /*pResults*/) // We are ignoring results as our methods will not return any results
    {
        printf("** Method completed, status HRESULT = 0x%lx **\n", hrStatus);

        if (g_hMethodCompleteEvent != NULL)
        {
            SetEvent(g_hMethodCompleteEvent);
        }          
        return S_OK;
    }

    // IUnknown::AddRef
    virtual ULONG STDMETHODCALLTYPE AddRef(void)
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    // IUnknown::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceServiceMethodCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            *ppvObj = NULL;
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    // IUnknown::Release
    virtual ULONG STDMETHODCALLTYPE Release(void)
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

private:
    DWORD   m_cRef;
};
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
