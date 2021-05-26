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
# <a name="invoking-service-methods-asynchronously"></a><span data-ttu-id="a870e-103">Invocar métodos de serviço de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="a870e-103">Invoking Service Methods Asynchronously</span></span>

<span data-ttu-id="a870e-104">O aplicativo WpdServiceApiSample inclui código que demonstra como um aplicativo pode invocar os métodos de serviço de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a870e-104">The WpdServiceApiSample application includes code that demonstrates how an application can invoke the service methods asynchronously.</span></span> <span data-ttu-id="a870e-105">Este exemplo usa as interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="a870e-105">This sample uses the following interfaces.</span></span>



| <span data-ttu-id="a870e-106">Interface</span><span class="sxs-lookup"><span data-stu-id="a870e-106">Interface</span></span>    | <span data-ttu-id="a870e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a870e-107">Description</span></span>          |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a870e-108">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="a870e-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | <span data-ttu-id="a870e-109">Usado para recuperar a interface **IPortableDeviceServiceMethods** para invocar métodos em um determinado serviço.</span><span class="sxs-lookup"><span data-stu-id="a870e-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="a870e-110">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="a870e-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | <span data-ttu-id="a870e-111">Usado para invocar um método de serviço.</span><span class="sxs-lookup"><span data-stu-id="a870e-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="a870e-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="a870e-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                                  | <span data-ttu-id="a870e-113">Usado para manter os parâmetros de método de saída e os resultados do método de entrada.</span><span class="sxs-lookup"><span data-stu-id="a870e-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="a870e-114">Isso poderá ser **NULL** se o método não exigir parâmetros ou retornar resultados.</span><span class="sxs-lookup"><span data-stu-id="a870e-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |
| [<span data-ttu-id="a870e-115">**IPortableDeviceServiceMethodCallback**</span><span class="sxs-lookup"><span data-stu-id="a870e-115">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | <span data-ttu-id="a870e-116">Implementado pelo aplicativo para receber os resultados do método quando um método for concluído.</span><span class="sxs-lookup"><span data-stu-id="a870e-116">Implemented by the application to receive the method results when a method has completed.</span></span>                                                                               |



 

<span data-ttu-id="a870e-117">Quando o usuário escolhe a opção "10" na linha de comando, o aplicativo invoca o método **InvokeMethodsAsync** encontrado no módulo ServiceMethods.cpp.</span><span class="sxs-lookup"><span data-stu-id="a870e-117">When the user chooses option "10" at the command line, the application invokes the **InvokeMethodsAsync** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="a870e-118">Observe que, antes de invocar os métodos, o aplicativo de exemplo abre um serviço Contatos em um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="a870e-118">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="a870e-119">Os métodos de serviço encapsulam a funcionalidade que cada serviço define e implementa.</span><span class="sxs-lookup"><span data-stu-id="a870e-119">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="a870e-120">Eles são exclusivos para cada tipo de serviço e são representados por um GUID.</span><span class="sxs-lookup"><span data-stu-id="a870e-120">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="a870e-121">Por exemplo, o serviço Contatos define um método **BeginSync** que os aplicativos chamam para preparar o dispositivo para sincronizar objetos contact e um **método EndSync** para notificar o dispositivo de que a sincronização foi concluída.</span><span class="sxs-lookup"><span data-stu-id="a870e-121">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="a870e-122">Os aplicativos executam um método de serviço de dispositivo portátil chamando [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span><span class="sxs-lookup"><span data-stu-id="a870e-122">Applications execute a portable device service method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="a870e-123">Os métodos de serviço não devem ser confundidos com comandos WPD.</span><span class="sxs-lookup"><span data-stu-id="a870e-123">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="a870e-124">Os comandos WPD fazem parte da DDI (interface de driver de dispositivo) Standard WPD e são o mecanismo de comunicação entre um aplicativo WPD e o driver.</span><span class="sxs-lookup"><span data-stu-id="a870e-124">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="a870e-125">Os comandos são predefinidos, agrupados por categorias (por exemplo, a **categoria de WPD \_ \_ comum**) e são representados por uma estrutura de **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="a870e-125">Commands are predefined, grouped by categories (for example, **WPD\_CATEGORY\_COMMON**), and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="a870e-126">Um aplicativo envia comandos para o driver de dispositivo chamando [**IPortableDeviceService:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="a870e-126">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="a870e-127">Para obter mais informações, consulte o tópico comandos.</span><span class="sxs-lookup"><span data-stu-id="a870e-127">For more information, see the Commands topic.</span></span>

<span data-ttu-id="a870e-128">O método **InvokeMethodsAsync** invoca [**IPortableDeviceService:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar uma interface [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="a870e-128">The **InvokeMethodsAsync** method invokes [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="a870e-129">Usando essa interface, ela invoca a função auxiliar **InvokeMethodAsync** duas vezes; uma vez para o método **BeginSync** e uma vez para o método **endsync** .</span><span class="sxs-lookup"><span data-stu-id="a870e-129">Using this interface, it invokes the **InvokeMethodAsync** helper function twice; once for the **BeginSync** method and once for the **EndSync** method.</span></span> <span data-ttu-id="a870e-130">Neste exemplo, **InvokeMethodAsync** aguarda indefinidamente por um evento global ser sinalizado quando [**IPortableDeviceServiceMethodCallback:: OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) é chamado.</span><span class="sxs-lookup"><span data-stu-id="a870e-130">In this example, , **InvokeMethodAsync** waits indefinitely for a global event to be signaled when [**IPortableDeviceServiceMethodCallback::OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) is called.</span></span>

<span data-ttu-id="a870e-131">O código a seguir usa o método **InvokeMethodsAsync** .</span><span class="sxs-lookup"><span data-stu-id="a870e-131">The following code uses the **InvokeMethodsAsync** method.</span></span>


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



<span data-ttu-id="a870e-132">A função auxiliar **InvokeMethodAsync** faz o seguinte para cada método que ele invoca:</span><span class="sxs-lookup"><span data-stu-id="a870e-132">The **InvokeMethodAsync** helper function does the following for each method that it invokes:</span></span>

-   <span data-ttu-id="a870e-133">Cria um identificador de evento global que ele monitora para determinar a conclusão do método.</span><span class="sxs-lookup"><span data-stu-id="a870e-133">Creates a global event handle that it monitors to determine method completion.</span></span>
-   <span data-ttu-id="a870e-134">Cria um objeto **CMethodCallback** que é fornecido como um argumento para [**IPortableDeviceServiceMethods: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).</span><span class="sxs-lookup"><span data-stu-id="a870e-134">Creates a **CMethodCallback** object that is supplied as an argument to [**IPortableDeviceServiceMethods:InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).</span></span>
-   <span data-ttu-id="a870e-135">Chama o método **IPortableDeviceServiceMethods:: InvokeAsync** para invocar o método fornecido.</span><span class="sxs-lookup"><span data-stu-id="a870e-135">Calls the **IPortableDeviceServiceMethods::InvokeAsync** method to invoke the given method.</span></span>
-   <span data-ttu-id="a870e-136">Monitora o identificador de evento global para conclusão.</span><span class="sxs-lookup"><span data-stu-id="a870e-136">Monitors the global event handle for completion.</span></span>
-   <span data-ttu-id="a870e-137">Executa a limpeza.</span><span class="sxs-lookup"><span data-stu-id="a870e-137">Performs cleanup.</span></span>

<span data-ttu-id="a870e-138">A classe **CMethodCallback** demonstra como um aplicativo pode implementar o [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback).</span><span class="sxs-lookup"><span data-stu-id="a870e-138">The **CMethodCallback** class demonstrates how an application can implement [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback).</span></span> <span data-ttu-id="a870e-139">A implementação de **OnComplete** nessa classe sinaliza um evento para notificar o aplicativo de que o método de serviço foi concluído.</span><span class="sxs-lookup"><span data-stu-id="a870e-139">The implementation of **OnComplete** in this class signals an event to notify the application that the service method has completed.</span></span> <span data-ttu-id="a870e-140">Além do método **OnComplete,** essa classe implementa **AddRef,** **QueryInterface** e **Release**, que são usados para manter a contagem de referência do objeto e as interfaces que ele implementa.</span><span class="sxs-lookup"><span data-stu-id="a870e-140">In addition to the **OnComplete** method, this class implements **AddRef**, **QueryInterface**, and **Release**, which are used to maintain the object's reference count and the interfaces that it implements.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a870e-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a870e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a870e-142">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="a870e-142">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="a870e-143">**IPortableDeviceServiceMethodCallback**</span><span class="sxs-lookup"><span data-stu-id="a870e-143">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[<span data-ttu-id="a870e-144">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="a870e-144">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="a870e-145">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="a870e-145">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
