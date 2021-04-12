---
description: Um aplicativo de mídia que deseja fornecer uma experiência de pato personalizada deve escutar as notificações de eventos quando um fluxo de comunicação é aberto ou fechado no sistema.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Obtendo eventos de pato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e45557c25570a89452a39683a0b6732b9632129
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500968"
---
# <a name="getting-ducking-events"></a><span data-ttu-id="e2984-103">Obtendo eventos de pato</span><span class="sxs-lookup"><span data-stu-id="e2984-103">Getting Ducking Events</span></span>

<span data-ttu-id="e2984-104">Um aplicativo de mídia que deseja fornecer uma experiência de pato personalizada deve escutar as notificações de eventos quando um fluxo de comunicação é aberto ou fechado no sistema.</span><span class="sxs-lookup"><span data-stu-id="e2984-104">A media application that wants to provide a customised ducking experience must listen for the event notifications when a communication stream is opened or closed in the system.</span></span> <span data-ttu-id="e2984-105">A implementação personalizada pode ser fornecida usando MediaFoundation, DirectShow ou DirectSound, que usam as APIs de áudio principais.</span><span class="sxs-lookup"><span data-stu-id="e2984-105">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="e2984-106">Um cliente WASAPI direto também pode substituir o tratamento padrão se ele sabe quando a sessão de comunicação começa e termina.</span><span class="sxs-lookup"><span data-stu-id="e2984-106">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="e2984-107">Para fornecer uma implementação personalizada, um aplicativo de mídia precisa obter notificações do sistema quando um aplicativo de comunicação inicia ou termina um fluxo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="e2984-107">To provide a custom implementation, a media application needs to get notifications from the system when a communication application starts or ends a communication stream.</span></span> <span data-ttu-id="e2984-108">O aplicativo de mídia deve implementar a interface [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) e registrar a implementação com o sistema de áudio.</span><span class="sxs-lookup"><span data-stu-id="e2984-108">The media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="e2984-109">Após o registro bem-sucedido, o aplicativo de mídia recebe notificações de eventos na forma de retornos de chamada por meio dos métodos na interface.</span><span class="sxs-lookup"><span data-stu-id="e2984-109">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="e2984-110">Para obter mais informações, consulte [considerações de implementação para notificações de pato](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="e2984-110">For more information, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

<span data-ttu-id="e2984-111">Para enviar notificações de pato, o sistema de áudio deve saber qual sessão de áudio está ouvindo os eventos de pato.</span><span class="sxs-lookup"><span data-stu-id="e2984-111">To send ducking notifications, the audio system must know which audio session is listening for the ducking events.</span></span> <span data-ttu-id="e2984-112">Cada sessão de áudio é identificada exclusivamente com um GUID — identificador de instância de sessão.</span><span class="sxs-lookup"><span data-stu-id="e2984-112">Each audio session is uniquely identified with a GUID—session instance identifier.</span></span> <span data-ttu-id="e2984-113">O Gerenciador de sessão permite que um aplicativo Obtenha informações sobre a sessão, como o título da sessão de áudio, o estado de renderização e o identificador da instância de sessão.</span><span class="sxs-lookup"><span data-stu-id="e2984-113">The session manager allows an application to get information about the session such as title of audio session, the rendering state, and the session instance identifier.</span></span> <span data-ttu-id="e2984-114">O identificador pode ser recuperado usando a interface de controle de política, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).</span><span class="sxs-lookup"><span data-stu-id="e2984-114">The identifier can be retrieved by using the policy control interface, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).</span></span>

<span data-ttu-id="e2984-115">As etapas a seguir resumem o processo de obtenção do identificador de instância de sessão do aplicativo de mídia:</span><span class="sxs-lookup"><span data-stu-id="e2984-115">The following steps summarize the process of getting the session instance identifier of the media application:</span></span>

1.  <span data-ttu-id="e2984-116">Instancie o enumerador de dispositivo e use-o para obter uma referência ao ponto de extremidade do dispositivo que o aplicativo de mídia está usando para renderizar o fluxo de não comunicação.</span><span class="sxs-lookup"><span data-stu-id="e2984-116">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="e2984-117">Ative o Gerenciador de sessão no ponto de extremidade do dispositivo e obtenha uma referência para a interface [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) do Gerenciador de sessão.</span><span class="sxs-lookup"><span data-stu-id="e2984-117">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="e2984-118">Usando o ponteiro [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , obtenha uma referência à interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) do Gerenciador de sessão.</span><span class="sxs-lookup"><span data-stu-id="e2984-118">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="e2984-119">Consulte o [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) da interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .</span><span class="sxs-lookup"><span data-stu-id="e2984-119">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="e2984-120">Chame [**IAudioSessionControl2:: GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) e recupere uma cadeia de caracteres que contém o identificador de sessão para a sessão de áudio atual.</span><span class="sxs-lookup"><span data-stu-id="e2984-120">Call [**IAudioSessionControl2::GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) and retrieve a string that contains the session identifier for the current audio session.</span></span>

<span data-ttu-id="e2984-121">Para obter notificações de patos sobre fluxos de comunicação, o aplicativo de mídia chama [**IAudioSessionManager2:: RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification).</span><span class="sxs-lookup"><span data-stu-id="e2984-121">To get ducking notifications about communication streams, the media application calls [**IAudioSessionManager2::RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification).</span></span> <span data-ttu-id="e2984-122">O aplicativo de mídia fornece seu identificador de instância de sessão para o sistema de áudio e um ponteiro para a implementação de [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) .</span><span class="sxs-lookup"><span data-stu-id="e2984-122">The media application supplies its session instance identifier to the audio system and a pointer to the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) implementation.</span></span> <span data-ttu-id="e2984-123">O aplicativo agora pode receber notificação de eventos quando um fluxo é aberto no dispositivo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="e2984-123">The application can now receive event notification when a stream opened on the communication device.</span></span> <span data-ttu-id="e2984-124">Para parar de receber a notificação, o aplicativo de mídia deve chamar [**IAudioSessionManager2:: UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).</span><span class="sxs-lookup"><span data-stu-id="e2984-124">To stop getting notification, the media application must call [**IAudioSessionManager2::UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).</span></span>

<span data-ttu-id="e2984-125">O código a seguir mostra como um aplicativo pode se registrar para obter notificações de pato.</span><span class="sxs-lookup"><span data-stu-id="e2984-125">The following code shows how an application can register to get ducking notifications.</span></span> <span data-ttu-id="e2984-126">A classe CMediaPlayer é definida em [considerações de implementação para as notificações de pato](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="e2984-126">The CMediaPlayer class is defined in [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span> <span data-ttu-id="e2984-127">O exemplo [DuckingMediaPlayer](duckingmediaplayer.md) implementa essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="e2984-127">The [DuckingMediaPlayer](duckingmediaplayer.md) sample implements this functionality.</span></span>


```C++
////////////////////////////////////////////////////////////////////
//Description: Registers for duck notifications depending on the 
//             the ducking options specified by the caller.
//Parameters: 
//    If DuckingOptOutChecked is TRUE, the client is registered for
//    to receive ducking notifications; 
//    FALSE, the client's registration is deleted.
////////////////////////////////////////////////////////////////////

HRESULT CMediaPlayer::DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;

    LPWSTR sessionId = NULL;

    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(
              eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate the session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>
                                 (&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(
                                  NULL, 0, &pSessionControl);
        
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                               IID_PPV_ARGS(&pSessionControl2));
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    // Get the session instance identifier.
    
    if (SUCCEEDED(hr))
    {
        hr = pSessionControl2->GetSessionInstanceIdentifier(
                                 sessionId);
                
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }

    //  Register for ducking events depending on 
    //  the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionManager2->RegisterDuckNotification(
                                    sessionId, this);
        }
        else
        {
            hr = pSessionManager2->UnregisterDuckNotification
                                      (FALSE);
        }
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e2984-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2984-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2984-129">Usando um dispositivo de comunicação</span><span class="sxs-lookup"><span data-stu-id="e2984-129">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="e2984-130">Experiência de pato padrão</span><span class="sxs-lookup"><span data-stu-id="e2984-130">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="e2984-131">Desabilitando a experiência de pato padrão</span><span class="sxs-lookup"><span data-stu-id="e2984-131">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="e2984-132">Fornecendo um comportamento personalizado de pato</span><span class="sxs-lookup"><span data-stu-id="e2984-132">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="e2984-133">Considerações de implementação para notificações de pato</span><span class="sxs-lookup"><span data-stu-id="e2984-133">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



