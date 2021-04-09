---
description: Um usuário pode desabilitar a experiência de pato padrão fornecida pelo sistema usando as opções disponíveis na guia comunicações do painel de controle multimídia do Windows, Mmsys.cpl.
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: Desabilitando a experiência de pato padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed33fa7d9473cb5c68a018b98bff8a826612387e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089630"
---
# <a name="disabling-the-default-ducking-experience"></a><span data-ttu-id="18192-103">Desabilitando a experiência de pato padrão</span><span class="sxs-lookup"><span data-stu-id="18192-103">Disabling the Default Ducking Experience</span></span>

<span data-ttu-id="18192-104">Um usuário pode desabilitar a [experiência de pato padrão](stream-attenuation.md) fornecida pelo sistema usando as opções disponíveis na guia **comunicações** do painel de controle multimídia do Windows, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="18192-104">A user can disable the [Default Ducking Experience](stream-attenuation.md) provided by the system by using the options that are available on the **Communications** tab of the Windows multimedia control panel, Mmsys.cpl.</span></span>

<span data-ttu-id="18192-105">Quando o pato é aplicado, um efeito de esmaecimento e esmaecimento é usado por um período de 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="18192-105">When ducking is applied, a fade-out and fade-in effect is used for a period of 1 second.</span></span> <span data-ttu-id="18192-106">Um aplicativo de jogo pode não querer que o fluxo de comunicação interfira no áudio do jogo.</span><span class="sxs-lookup"><span data-stu-id="18192-106">A game application might not want the communication stream to interfere with the game audio.</span></span> <span data-ttu-id="18192-107">Alguns aplicativos de mídia podem descobrir que a experiência de reprodução é dissonante quando a música esmaece de volta.</span><span class="sxs-lookup"><span data-stu-id="18192-107">Some media applications might find that the playback experience is jarring when music fades back in.</span></span> <span data-ttu-id="18192-108">Esses tipos de aplicativos podem optar por não participar da experiência de pato.</span><span class="sxs-lookup"><span data-stu-id="18192-108">These types of applications can choose not to participate in the ducking experience.</span></span>

<span data-ttu-id="18192-109">Programaticamente, um cliente WASAPI direto pode recusar usando o Gerenciador de sessão para a sessão de áudio que fornece controle de volume para os fluxos que não são de comunicação.</span><span class="sxs-lookup"><span data-stu-id="18192-109">Programmatically, a direct WASAPI client can opt out by using the session manager for the audio session that provides volume control for the non-communication streams.</span></span> <span data-ttu-id="18192-110">Observe que, mesmo que um cliente não esteja no pato, ele ainda recebe notificações de pato do sistema.</span><span class="sxs-lookup"><span data-stu-id="18192-110">Note that even if an client opts out of ducking, it still receives ducking notifications from the system.</span></span>

<span data-ttu-id="18192-111">Para recusar o pato, o cliente deve obter uma referência à interface [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) do Gerenciador de sessão.</span><span class="sxs-lookup"><span data-stu-id="18192-111">To opt out of ducking, the client must get a reference to the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) interface of the session manager.</span></span> <span data-ttu-id="18192-112">Para recusar a experiência de pato, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="18192-112">To opt out of the ducking experience, use the following steps:</span></span>

1.  <span data-ttu-id="18192-113">Instancie o enumerador de dispositivo e use-o para obter uma referência ao ponto de extremidade do dispositivo que o aplicativo de mídia está usando para renderizar o fluxo de não comunicação.</span><span class="sxs-lookup"><span data-stu-id="18192-113">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="18192-114">Ative o Gerenciador de sessão no ponto de extremidade do dispositivo e obtenha uma referência para a interface [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) do Gerenciador de sessão.</span><span class="sxs-lookup"><span data-stu-id="18192-114">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="18192-115">Usando o ponteiro [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , obtenha uma referência à interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) do Gerenciador de sessão.</span><span class="sxs-lookup"><span data-stu-id="18192-115">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="18192-116">Consulte o [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) da interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .</span><span class="sxs-lookup"><span data-stu-id="18192-116">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="18192-117">Chame [**IAudioSessionControl2:: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) e passe **true** ou **false** para especificar a preferência de pato.</span><span class="sxs-lookup"><span data-stu-id="18192-117">Call [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) and pass **TRUE** or **FALSE** to specify the ducking preference.</span></span> <span data-ttu-id="18192-118">A preferência especificada pode ser alterada dinamicamente durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="18192-118">The specified preference can be changed dynamically during the session.</span></span> <span data-ttu-id="18192-119">Observe que a alteração de recusa não tem efeito até que o fluxo seja interrompido e iniciado novamente.</span><span class="sxs-lookup"><span data-stu-id="18192-119">Note that the opt-out change does not take effect until the stream is stopped and started again.</span></span>

<span data-ttu-id="18192-120">O código a seguir mostra como um aplicativo pode especificar sua preferência de pato.</span><span class="sxs-lookup"><span data-stu-id="18192-120">The following code shows how an application can specify its ducking preference.</span></span> <span data-ttu-id="18192-121">O chamador da função deve passar **true** ou **false** no parâmetro DuckingOptOutChecked.</span><span class="sxs-lookup"><span data-stu-id="18192-121">The caller of the function must pass **TRUE** or **FALSE** in the DuckingOptOutChecked parameter.</span></span> <span data-ttu-id="18192-122">Dependendo do valor passado, o pato está habilitado ou desabilitado por meio de [**IAudioSessionControl2:: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).</span><span class="sxs-lookup"><span data-stu-id="18192-122">Depending on the value passed, ducking is enabled or disabled through the [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).</span></span>


```C++
////////////////////////////////////////////////////////////////////
//Description: Specifies the ducking options for the application.
//Parameters: 
//    If DuckingOptOutChecked is TRUE system ducking is disabled; 
//    FALSE, system ducking is enabled.
////////////////////////////////////////////////////////////////////

HRESULT DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;


    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>(&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(NULL, 0, &pSessionControl);
        
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                  __uuidof(IAudioSessionControl2),
                  (void**)&pSessionControl2);
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    //  Sync the ducking state with the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionControl2->SetDuckingPreference(TRUE);
        }
        else
        {
            hr = pSessionControl2->SetDuckingPreference(FALSE);
        }
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="18192-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18192-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18192-124">Usando um dispositivo de comunicação</span><span class="sxs-lookup"><span data-stu-id="18192-124">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="18192-125">Experiência de pato padrão</span><span class="sxs-lookup"><span data-stu-id="18192-125">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="18192-126">Fornecendo um comportamento personalizado de pato</span><span class="sxs-lookup"><span data-stu-id="18192-126">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="18192-127">Considerações de implementação para notificações de pato</span><span class="sxs-lookup"><span data-stu-id="18192-127">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="18192-128">Obtendo eventos de pato</span><span class="sxs-lookup"><span data-stu-id="18192-128">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



