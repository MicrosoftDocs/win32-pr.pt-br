---
description: Manipulando eventos do dispositivo
ms.assetid: 529a8b7a-08b4-47de-8ed3-28e8fff0ede2
title: Manipulando eventos do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74692b73e39aa83286604408f3c556f5fbeb3f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786282"
---
# <a name="handling-events-from-the-device"></a><span data-ttu-id="4c088-103">Manipulando eventos do dispositivo</span><span class="sxs-lookup"><span data-stu-id="4c088-103">Handling Events from the Device</span></span>

<span data-ttu-id="4c088-104">Outra operação realizada por um aplicativo WPD é a manipulação de eventos que são acionados pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c088-104">Another operation accomplished by a WPD application is the handling of events that are fired by the device.</span></span>

<span data-ttu-id="4c088-105">As operações de manipulação de eventos são realizadas usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c088-105">Event handling operations are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="4c088-106">Interface</span><span class="sxs-lookup"><span data-stu-id="4c088-106">Interface</span></span>                                                                      | <span data-ttu-id="4c088-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c088-107">Description</span></span>                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="4c088-108">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="4c088-108">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                           | <span data-ttu-id="4c088-109">Permite que o aplicativo se registre para receber retornos de chamada assíncronos.</span><span class="sxs-lookup"><span data-stu-id="4c088-109">Lets the application register to receive asynchronous callbacks.</span></span> |
| [<span data-ttu-id="4c088-110">**Interface IPortableDeviceEventCallback**</span><span class="sxs-lookup"><span data-stu-id="4c088-110">**IPortableDeviceEventCallback Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback) | <span data-ttu-id="4c088-111">Contém o manipulador de eventos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4c088-111">Contains the application's event handler.</span></span>                        |



 

<span data-ttu-id="4c088-112">A classe CPortableDeviceEventsCallback no módulo DeviceEvents. cpp do aplicativo de exemplo demonstra como um aplicativo pode implementar o [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback).</span><span class="sxs-lookup"><span data-stu-id="4c088-112">The CPortableDeviceEventsCallback class in the sample application's DeviceEvents.cpp module demonstrates how an application can implement [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback).</span></span> <span data-ttu-id="4c088-113">A implementação do método [**OnEvent**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceeventcallback-onevent) nessa classe grava os parâmetros de qualquer evento na janela do console do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4c088-113">The implementation of the [**OnEvent**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceeventcallback-onevent) method in this class writes the parameters for any event to the application's console window.</span></span> <span data-ttu-id="4c088-114">Além do método OnEvent, essa classe implementa AddRef e Release, que são usados para manter a contagem de referência do objeto.</span><span class="sxs-lookup"><span data-stu-id="4c088-114">In addition to the OnEvent method, this class implements AddRef and Release, which are used to maintain the object's reference count.</span></span>


```C++
class CPortableDeviceEventsCallback : public IPortableDeviceEventCallback
{
public:
    CPortableDeviceEventsCallback() : m_cRef(1)
    {
    }

    ~CPortableDeviceEventsCallback()
    {
    }

    HRESULT __stdcall QueryInterface(
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
            (riid == IID_IPortableDeviceEventCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    ULONG __stdcall AddRef()
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    ULONG __stdcall Release()
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

    HRESULT __stdcall OnEvent(
        IPortableDeviceValues* pEventParameters)
    {
        HRESULT hr = S_OK;

        if (pEventParameters != NULL)
        {
            printf("***************************\n** Device event received **\n***************************\n");
            DisplayStringProperty(pEventParameters, WPD_EVENT_PARAMETER_PNP_DEVICE_ID, L"WPD_EVENT_PARAMETER_PNP_DEVICE_ID");
            DisplayGuidProperty(pEventParameters, WPD_EVENT_PARAMETER_EVENT_ID, L"WPD_EVENT_PARAMETER_EVENT_ID");
        }

        return hr;
    }

    ULONG m_cRef;
};
```



<span data-ttu-id="4c088-115">O aplicativo de exemplo instancia a classe CPortableDeviceEventsCallback em sua função auxiliar RegisterForEventNotifications.</span><span class="sxs-lookup"><span data-stu-id="4c088-115">The sample application instantiates the CPortableDeviceEventsCallback class in its RegisterForEventNotifications helper function.</span></span> <span data-ttu-id="4c088-116">Essa função cria uma instância do objeto de retorno de chamada usando o novo operador.</span><span class="sxs-lookup"><span data-stu-id="4c088-116">This function creates an instance of the callback object using the new operator.</span></span> <span data-ttu-id="4c088-117">Em seguida, ele chama o método [**IPortableDevice:: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) para registrar o retorno de chamada e começar a receber eventos.</span><span class="sxs-lookup"><span data-stu-id="4c088-117">It then calls the [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) method to register the callback and begin receiving events.</span></span>


```C++
void RegisterForEventNotifications(IPortableDevice* pDevice)
{
    HRESULT                        hr = S_OK;
    LPWSTR                         wszEventCookie = NULL;
    CPortableDeviceEventsCallback* pCallback = NULL;

    if (pDevice == NULL)
    {
        return;
    }

    // Check to see if we already have an event registration cookie.  If so,
    // then avoid registering again.
    // NOTE: An application can register for events as many times as they want.
    //       This sample only keeps a single registration cookie around for
    //       simplicity.
    if (g_strEventRegistrationCookie.GetLength() > 0)
    {
        printf("This application has already registered to receive device events.\n");
        return;
    }

    // Create an instance of the callback object.  This will be called when events
    // are received.
    if (hr == S_OK)
    {
        pCallback = new CPortableDeviceEventsCallback();
        if (pCallback == NULL)
        {
            hr = E_OUTOFMEMORY;
            printf("Failed to allocate memory for IPortableDeviceEventsCallback object, hr = 0x%lx\n",hr);
        }
    }

    // Call Advise to register the callback and receive events.
    if (hr == S_OK)
    {
        hr = pDevice->Advise(0, pCallback, NULL, &wszEventCookie);
        if (FAILED(hr))
        {
            printf("! Failed to register for device events, hr = 0x%lx\n",hr);
        }
    }

    // Save the event registration cookie if event registration was successful.
    if (hr == S_OK)
    {
        g_strEventRegistrationCookie = wszEventCookie;
    }

    // Free the event registration cookie, if one was returned.
    if (wszEventCookie != NULL)
    {
        CoTaskMemFree(wszEventCookie);
        wszEventCookie = NULL;
    }

    if (hr == S_OK)
    {
        printf("This application has registered for device event notifications and was returned the registration cookie '%ws'", g_strEventRegistrationCookie.GetString());
    }

    // If a failure occurs, remember to delete the allocated callback object, if one exists.
    if (pCallback != NULL)
    {
        pCallback->Release();
    }
```



<span data-ttu-id="4c088-118">Quando o aplicativo de exemplo estiver por meio do recebimento de eventos, ele chamará a função auxiliar UnregisterForEventNotifications.</span><span class="sxs-lookup"><span data-stu-id="4c088-118">Once the sample application is through receiving events, it calls the UnregisterForEventNotifications helper function.</span></span> <span data-ttu-id="4c088-119">Essa função, por sua vez, chama o método [**IPortableDevice:: Unadvise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-unadvise) para cancelar o registro do retorno de chamada do recebimento de eventos.</span><span class="sxs-lookup"><span data-stu-id="4c088-119">This function, in turn, calls the [**IPortableDevice::Unadvise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-unadvise) method to unregister the callback from receiving events.</span></span>


```C++
void UnregisterForEventNotifications(IPortableDevice* pDevice)
{
    HRESULT hr = S_OK;

    if (pDevice == NULL)
    {
        return;
    }

    hr = pDevice->Unadvise(g_strEventRegistrationCookie);
    if (FAILED(hr))
    {
        printf("! Failed to unregister for device events using registration cookie '%ws', hr = 0x%lx\n",g_strEventRegistrationCookie.GetString(), hr);
    }

    if (hr == S_OK)
    {
        printf("This application used the registration cookie '%ws' to unregister from receiving device event notifications", g_strEventRegistrationCookie.GetString());
    }

    g_strEventRegistrationCookie = L"";
}
```



## <a name="related-topics"></a><span data-ttu-id="4c088-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c088-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c088-121">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="4c088-121">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="4c088-122">**Interface IPortableDeviceEventCallback**</span><span class="sxs-lookup"><span data-stu-id="4c088-122">**IPortableDeviceEventCallback Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)
</dt> <dt>

[<span data-ttu-id="4c088-123">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="4c088-123">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



