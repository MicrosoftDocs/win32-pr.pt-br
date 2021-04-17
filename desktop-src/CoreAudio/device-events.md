---
description: Eventos de dispositivo
ms.assetid: b31500d6-a79d-4e6e-878e-6bd77055f1ad
title: Eventos de dispositivo (APIs de áudio de núcleo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0513fc49ee5f3cb2bfe95ca2330cb79b74720923
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748850"
---
# <a name="device-events-core-audio-apis"></a><span data-ttu-id="a6565-103">Eventos de dispositivo (APIs de áudio de núcleo)</span><span class="sxs-lookup"><span data-stu-id="a6565-103">Device Events (Core Audio APIs)</span></span>

<span data-ttu-id="a6565-104">Um evento de dispositivo notifica os clientes sobre uma alteração no status de um [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md) no sistema.</span><span class="sxs-lookup"><span data-stu-id="a6565-104">A device event notifies clients of a change in the status of an [audio endpoint device](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="a6565-105">Veja a seguir exemplos de eventos de dispositivo:</span><span class="sxs-lookup"><span data-stu-id="a6565-105">The following are examples of device events:</span></span>

-   <span data-ttu-id="a6565-106">O usuário habilita ou desabilita um dispositivo de ponto de extremidade de áudio de Gerenciador de Dispositivos ou do painel de controle multimídia do Windows Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="a6565-106">The user enables or disables an audio endpoint device from Device Manager or from the Windows multimedia control panel, Mmsys.cpl.</span></span>
-   <span data-ttu-id="a6565-107">O usuário adiciona um adaptador de áudio ao sistema ou remove um adaptador de áudio do sistema.</span><span class="sxs-lookup"><span data-stu-id="a6565-107">The user adds an audio adapter to the system or removes an audio adapter from the system.</span></span>
-   <span data-ttu-id="a6565-108">O usuário conecta um dispositivo de ponto de extremidade de áudio em uma tomada de áudio com detecção de presença de Jack ou remove um dispositivo de ponto de extremidade de áudio desse conector.</span><span class="sxs-lookup"><span data-stu-id="a6565-108">The user plugs an audio endpoint device into an audio jack with jack-presence detection, or removes an audio endpoint device from such a jack.</span></span>
-   <span data-ttu-id="a6565-109">O usuário altera a [função de dispositivo](device-roles.md) atribuída a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6565-109">The user changes the [device role](device-roles.md) that is assigned to a device.</span></span>
-   <span data-ttu-id="a6565-110">O valor de uma [propriedade de um dispositivo](device-properties.md) é alterado.</span><span class="sxs-lookup"><span data-stu-id="a6565-110">The value of a [property of a device](device-properties.md) changes.</span></span>

<span data-ttu-id="a6565-111">A adição ou remoção de um adaptador de áudio gera eventos de dispositivo para todos os dispositivos de ponto de extremidade de áudio que se conectam ao adaptador.</span><span class="sxs-lookup"><span data-stu-id="a6565-111">The addition or removal of an audio adapter generates device events for all of the audio endpoint devices that connect to the adapter.</span></span> <span data-ttu-id="a6565-112">Os primeiros quatro itens na lista anterior são exemplos de alterações de estado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6565-112">The first four items in the preceding list are examples of device state changes.</span></span> <span data-ttu-id="a6565-113">Para obter mais informações sobre os Estados do dispositivo de dispositivos de ponto de extremidade de áudio, consulte [constantes do estado do dispositivo \_ \_ xxx](device-state-xxx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a6565-113">For more information about the device states of audio endpoint devices, see [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).</span></span> <span data-ttu-id="a6565-114">Para obter mais informações sobre a detecção de presença de Jack, consulte [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="a6565-114">For more information about jack-presence detection, see [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="a6565-115">Um cliente pode se registrar para ser notificado quando ocorrerem eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6565-115">A client can register to be notified when device events occur.</span></span> <span data-ttu-id="a6565-116">Em resposta a essas notificações, o cliente pode alterar dinamicamente a forma como ele usa um dispositivo específico ou selecionar um dispositivo diferente a ser usado para uma finalidade específica.</span><span class="sxs-lookup"><span data-stu-id="a6565-116">In response to these notifications, the client can dynamically change the way that it uses a particular device, or select a different device to use for a particular purpose.</span></span>

<span data-ttu-id="a6565-117">Por exemplo, se um aplicativo estiver reproduzindo uma faixa de áudio por meio de um conjunto de alto-falantes USB e o usuário desconectar os alto-falantes do conector USB, o aplicativo receberá uma notificação de evento do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6565-117">For example, if an application is playing an audio track through a set of USB speakers, and the user disconnects the speakers from the USB connector, the application receives a device-event notification.</span></span> <span data-ttu-id="a6565-118">Em resposta ao evento, se o aplicativo detectar que um conjunto de alto-falantes da área de trabalho está conectado ao adaptador de áudio integrado na placa-mãe do sistema, o aplicativo poderá continuar jogando a faixa de áudio nos alto-falantes da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a6565-118">In response to the event, if the application detects that a set of desktop speakers is connected to the integrated audio adapter on the system motherboard, the application can resume playing the audio track through the desktop speakers.</span></span> <span data-ttu-id="a6565-119">Neste exemplo, a transição de alto-falantes USB para alto-falantes de área de trabalho ocorre automaticamente, sem a necessidade de o usuário intervir redirecionando explicitamente o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a6565-119">In this example, the transition from USB speakers to desktop speakers occurs automatically, without requiring the user to intervene by explicitly redirecting the application.</span></span>

<span data-ttu-id="a6565-120">Para se registrar para receber notificações de dispositivo, um cliente chama o método [**IMMDeviceEnumerator:: RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) .</span><span class="sxs-lookup"><span data-stu-id="a6565-120">To register to receive device notifications, a client calls the [**IMMDeviceEnumerator::RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) method.</span></span> <span data-ttu-id="a6565-121">Quando o cliente não requer mais notificações, ele os cancela chamando o método [**IMMDeviceEnumerator:: UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) .</span><span class="sxs-lookup"><span data-stu-id="a6565-121">When the client no longer requires notifications, it cancels them by calling the [**IMMDeviceEnumerator::UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) method.</span></span> <span data-ttu-id="a6565-122">Ambos os métodos usam um parâmetro de entrada, chamado *pNotify*, que é um ponteiro para uma instância de interface [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) .</span><span class="sxs-lookup"><span data-stu-id="a6565-122">Both methods take an input parameter, named *pNotify*, that is a pointer to an [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) interface instance.</span></span>

<span data-ttu-id="a6565-123">A interface **IMMNotificationClient** é implementada por um cliente.</span><span class="sxs-lookup"><span data-stu-id="a6565-123">The **IMMNotificationClient** interface is implemented by a client.</span></span> <span data-ttu-id="a6565-124">A interface contém vários métodos, sendo que cada um serve como uma rotina de retorno de chamada para um determinado tipo de evento de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6565-124">The interface contains several methods, each of which serves as a callback routine for a particular type of device event.</span></span> <span data-ttu-id="a6565-125">Quando um evento de dispositivo ocorre em um dispositivo de ponto de extremidade de áudio, o módulo MMDevice chama o método apropriado na interface **IMMNotificationClient** de cada cliente que está atualmente registrado para receber notificações de eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6565-125">When a device event occurs in an audio endpoint device, the MMDevice module calls the appropriate method in the **IMMNotificationClient** interface of every client that is currently registered to receive device-event notifications.</span></span> <span data-ttu-id="a6565-126">Essas chamadas passam uma descrição do evento para os clientes.</span><span class="sxs-lookup"><span data-stu-id="a6565-126">These calls pass a description of the event to the clients.</span></span> <span data-ttu-id="a6565-127">Para obter mais informações, consulte [**interface IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span><span class="sxs-lookup"><span data-stu-id="a6565-127">For more information, see [**IMMNotificationClient Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span></span>

<span data-ttu-id="a6565-128">Um cliente registrado para receber notificações de eventos de dispositivo receberá notificações de todos os tipos de eventos de dispositivo que ocorrem em todos os dispositivos de ponto de extremidade de áudio no sistema.</span><span class="sxs-lookup"><span data-stu-id="a6565-128">A client that is registered to receive device-event notifications will receive notifications of all types of device events that occur in all of the audio endpoint devices in the system.</span></span> <span data-ttu-id="a6565-129">Se um cliente estiver interessado apenas em determinados tipos de evento ou em determinados dispositivos, os métodos em sua implementação **IMMNotificationClient** deverão filtrar os eventos adequadamente.</span><span class="sxs-lookup"><span data-stu-id="a6565-129">If a client is interested only in certain event types or in certain devices, then the methods in its **IMMNotificationClient** implementation should filter the events appropriately.</span></span>

<span data-ttu-id="a6565-130">O SDK do Windows fornece exemplos que incluem várias implementações para a [**interface IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span><span class="sxs-lookup"><span data-stu-id="a6565-130">The Windows SDK provides samples that include several implementations for the [**IMMNotificationClient Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span></span> <span data-ttu-id="a6565-131">Para obter mais informações, consulte [exemplos de SDK que usam as APIs de áudio de núcleo](sdk-samples-that-use-the-core-audio-apis.md).</span><span class="sxs-lookup"><span data-stu-id="a6565-131">For more information, see [SDK Samples That Use the Core Audio APIs](sdk-samples-that-use-the-core-audio-apis.md).</span></span>

<span data-ttu-id="a6565-132">O exemplo de código a seguir mostra uma implementação possível da interface **IMMNotificationClient** :</span><span class="sxs-lookup"><span data-stu-id="a6565-132">The following code example shows a possible implementation of the **IMMNotificationClient** interface:</span></span>


```C++
//-----------------------------------------------------------
// Example implementation of IMMNotificationClient interface.
// When the status of audio endpoint devices change, the
// MMDevice module calls these methods to notify the client.
//-----------------------------------------------------------

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class CMMNotificationClient : public IMMNotificationClient
{
    LONG _cRef;
    IMMDeviceEnumerator *_pEnumerator;

    // Private function to print device-friendly name
    HRESULT _PrintDeviceName(LPCWSTR  pwstrId);

public:
    CMMNotificationClient() :
        _cRef(1),
        _pEnumerator(NULL)
    {
    }

    ~CMMNotificationClient()
    {
        SAFE_RELEASE(_pEnumerator)
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IMMNotificationClient) == riid)
        {
            AddRef();
            *ppvInterface = (IMMNotificationClient*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback methods for device-event notifications.

    HRESULT STDMETHODCALLTYPE OnDefaultDeviceChanged(
                                EDataFlow flow, ERole role,
                                LPCWSTR pwstrDeviceId)
    {
        char  *pszFlow = "?????";
        char  *pszRole = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (flow)
        {
        case eRender:
            pszFlow = "eRender";
            break;
        case eCapture:
            pszFlow = "eCapture";
            break;
        }

        switch (role)
        {
        case eConsole:
            pszRole = "eConsole";
            break;
        case eMultimedia:
            pszRole = "eMultimedia";
            break;
        case eCommunications:
            pszRole = "eCommunications";
            break;
        }

        printf("  -->New default device: flow = %s, role = %s\n",
               pszFlow, pszRole);
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceAdded(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Added device\n");
        return S_OK;
    };

    HRESULT STDMETHODCALLTYPE OnDeviceRemoved(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Removed device\n");
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceStateChanged(
                                LPCWSTR pwstrDeviceId,
                                DWORD dwNewState)
    {
        char  *pszState = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (dwNewState)
        {
        case DEVICE_STATE_ACTIVE:
            pszState = "ACTIVE";
            break;
        case DEVICE_STATE_DISABLED:
            pszState = "DISABLED";
            break;
        case DEVICE_STATE_NOTPRESENT:
            pszState = "NOTPRESENT";
            break;
        case DEVICE_STATE_UNPLUGGED:
            pszState = "UNPLUGGED";
            break;
        }

        printf("  -->New device state is DEVICE_STATE_%s (0x%8.8x)\n",
               pszState, dwNewState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnPropertyValueChanged(
                                LPCWSTR pwstrDeviceId,
                                const PROPERTYKEY key)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Changed device property "
               "{%8.8x-%4.4x-%4.4x-%2.2x%2.2x-%2.2x%2.2x%2.2x%2.2x%2.2x%2.2x}#%d\n",
               key.fmtid.Data1, key.fmtid.Data2, key.fmtid.Data3,
               key.fmtid.Data4[0], key.fmtid.Data4[1],
               key.fmtid.Data4[2], key.fmtid.Data4[3],
               key.fmtid.Data4[4], key.fmtid.Data4[5],
               key.fmtid.Data4[6], key.fmtid.Data4[7],
               key.pid);
        return S_OK;
    }
};

// Given an endpoint ID string, print the friendly device name.
HRESULT CMMNotificationClient::_PrintDeviceName(LPCWSTR pwstrId)
{
    HRESULT hr = S_OK;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;
    PROPVARIANT varString;

    CoInitialize(NULL);
    PropVariantInit(&varString);

    if (_pEnumerator == NULL)
    {
        // Get enumerator for audio endpoint devices.
        hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                              NULL, CLSCTX_INPROC_SERVER,
                              __uuidof(IMMDeviceEnumerator),
                              (void**)&_pEnumerator);
    }
    if (hr == S_OK)
    {
        hr = _pEnumerator->GetDevice(pwstrId, &pDevice);
    }
    if (hr == S_OK)
    {
        hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    }
    if (hr == S_OK)
    {
        // Get the endpoint device's friendly-name property.
        hr = pProps->GetValue(PKEY_Device_FriendlyName, &varString);
    }
    printf("----------------------\nDevice name: \"%S\"\n"
           "  Endpoint ID string: \"%S\"\n",
           (hr == S_OK) ? varString.pwszVal : L"null device",
           (pwstrId != NULL) ? pwstrId : L"null ID");

    PropVariantClear(&varString);

    SAFE_RELEASE(pProps)
    SAFE_RELEASE(pDevice)
    CoUninitialize();
    return hr;
}
```



<span data-ttu-id="a6565-133">A classe CMMNotificationClient no exemplo de código anterior é uma implementação da interface **IMMNotificationClient** .</span><span class="sxs-lookup"><span data-stu-id="a6565-133">The CMMNotificationClient class in the preceding code example is an implementation of the **IMMNotificationClient** interface.</span></span> <span data-ttu-id="a6565-134">Como **IMMNotificationClient** é herdado de **IUnknown**, a definição de classe contém implementações dos métodos **IUnknown** **AddRef**, **Release** e **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="a6565-134">Because **IMMNotificationClient** inherits from **IUnknown**, the class definition contains implementations of the **IUnknown** methods **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="a6565-135">Os métodos públicos restantes na definição de classe são específicos para a interface **IMMNotificationClient** .</span><span class="sxs-lookup"><span data-stu-id="a6565-135">The remaining public methods in the class definition are specific to the **IMMNotificationClient** interface.</span></span> <span data-ttu-id="a6565-136">Esses métodos são:</span><span class="sxs-lookup"><span data-stu-id="a6565-136">These methods are:</span></span>

-   <span data-ttu-id="a6565-137">**OnDefaultDeviceChanged**, que é chamado quando o usuário altera a função de dispositivo de um dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="a6565-137">**OnDefaultDeviceChanged**, which is called when the user changes the device role of an audio endpoint device.</span></span>
-   <span data-ttu-id="a6565-138">**OnDeviceAdded**, que é chamado quando o usuário adiciona um dispositivo de ponto de extremidade de áudio ao sistema.</span><span class="sxs-lookup"><span data-stu-id="a6565-138">**OnDeviceAdded**, which is called when the user adds an audio endpoint device to the system.</span></span>
-   <span data-ttu-id="a6565-139">**OnDeviceRemoved**, que é chamado quando o usuário remove um dispositivo de ponto de extremidade de áudio do sistema.</span><span class="sxs-lookup"><span data-stu-id="a6565-139">**OnDeviceRemoved**, which is called when the user removes an audio endpoint device from the system.</span></span>
-   <span data-ttu-id="a6565-140">**OnDeviceStateChanged**, que é chamado quando o estado do dispositivo de um dispositivo de ponto de extremidade de áudio é alterado.</span><span class="sxs-lookup"><span data-stu-id="a6565-140">**OnDeviceStateChanged**, which is called when the device state of an audio endpoint device changes.</span></span> <span data-ttu-id="a6565-141">(Para obter mais informações sobre os Estados do dispositivo, consulte [constantes do estado do dispositivo \_ \_ xxx](device-state-xxx-constants.md).)</span><span class="sxs-lookup"><span data-stu-id="a6565-141">(For more information about device states, see [DEVICE\_STATE\_ XXX Constants](device-state-xxx-constants.md).)</span></span>
-   <span data-ttu-id="a6565-142">**Onvalordapropriedadechanged**, que é chamado quando o valor de uma propriedade de um dispositivo de ponto de extremidade de áudio é alterado.</span><span class="sxs-lookup"><span data-stu-id="a6565-142">**OnPropertyValueChanged**, which is called when the value of a property of an audio endpoint device changes.</span></span>

<span data-ttu-id="a6565-143">Cada um desses métodos usa um parâmetro de entrada, *pwstrDeviceId*, que é um ponteiro para uma cadeia de caracteres de ID de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a6565-143">Each of these methods takes an input parameter, *pwstrDeviceId*, that is a pointer to an endpoint ID string.</span></span> <span data-ttu-id="a6565-144">A cadeia de caracteres identifica o dispositivo de ponto de extremidade de áudio no qual o evento do dispositivo ocorreu.</span><span class="sxs-lookup"><span data-stu-id="a6565-144">The string identifies the audio endpoint device in which the device event occurred.</span></span>

<span data-ttu-id="a6565-145">No exemplo de código anterior, \_ printName é um método particular na classe CMMNotificationClient que imprime o nome amigável do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6565-145">In the preceding code example, \_PrintDeviceName is a private method in the CMMNotificationClient class that prints the friendly name of the device.</span></span> <span data-ttu-id="a6565-146">\_O filedevicename usa a cadeia de caracteres de ID do ponto de extremidade como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="a6565-146">\_PrintDeviceName takes the endpoint ID string as an input parameter.</span></span> <span data-ttu-id="a6565-147">Ele passa a cadeia de caracteres para o método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="a6565-147">It passes the string to the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="a6565-148">**GetDevice** cria um objeto de dispositivo de ponto de extremidade para representar o dispositivo e fornece a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="a6565-148">**GetDevice** creates an endpoint device object to represent the device and provides the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface to that object.</span></span> <span data-ttu-id="a6565-149">Em seguida, o \_ Revicename chama o método [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) para recuperar a interface **IPropertyStore** para o armazenamento de propriedades do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6565-149">Next, \_PrintDeviceName calls the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method to retrieve the **IPropertyStore** interface to the device's property store.</span></span> <span data-ttu-id="a6565-150">Por fim, o renome do \_ dispositivo chama o método **IPropertyStore:: GetItem** para obter a propriedade friendly-Name do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6565-150">Finally, \_PrintDeviceName calls the **IPropertyStore::GetItem** method to obtain the friendly-name property of the device.</span></span> <span data-ttu-id="a6565-151">Para obter mais informações sobre o **IPropertyStore**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="a6565-151">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="a6565-152">Além dos eventos de dispositivo, os clientes podem se registrar para receber notificações de eventos de sessão de áudio e eventos de volume de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a6565-152">In addition to device events, clients can register to receive notifications of audio-session events and endpoint-volume events.</span></span> <span data-ttu-id="a6565-153">Para obter mais informações, consulte [**interface IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e [**interface IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).</span><span class="sxs-lookup"><span data-stu-id="a6565-153">For more information, see [**IAudioSessionEvents Interface**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) and [**IAudioEndpointVolumeCallback Interface**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6565-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6565-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6565-155">Dispositivos de ponto de extremidade de áudio</span><span class="sxs-lookup"><span data-stu-id="a6565-155">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> </dl>

 

 



