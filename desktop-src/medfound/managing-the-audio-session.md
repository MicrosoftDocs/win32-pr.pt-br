---
description: Este tópico descreve como controlar o volume de áudio ao usar o MFPlay para reprodução de áudio/vídeo.
ms.assetid: 4cf3dd0f-4c8a-4720-9eb3-d23352f3a85e
title: Gerenciando a sessão de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e5231ca02603279675fabaaac4b96a1cd001906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296180"
---
# <a name="managing-the-audio-session"></a><span data-ttu-id="8db3a-103">Gerenciando a sessão de áudio</span><span class="sxs-lookup"><span data-stu-id="8db3a-103">Managing the Audio Session</span></span>

<span data-ttu-id="8db3a-104">\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="8db3a-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8db3a-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="8db3a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8db3a-106">\]</span><span class="sxs-lookup"><span data-stu-id="8db3a-106">\]</span></span>

<span data-ttu-id="8db3a-107">Este tópico descreve como controlar o volume de áudio ao usar o MFPlay para reprodução de áudio/vídeo.</span><span class="sxs-lookup"><span data-stu-id="8db3a-107">This topic describes how to control audio volume when using MFPlay for audio/video playback.</span></span>

<span data-ttu-id="8db3a-108">O MFPlay fornece os seguintes métodos para controlar o volume de áudio durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="8db3a-108">MFPlay provides the following methods to control the audio volume during playback.</span></span>



| <span data-ttu-id="8db3a-109">Método</span><span class="sxs-lookup"><span data-stu-id="8db3a-109">Method</span></span>                                                            | <span data-ttu-id="8db3a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8db3a-110">Description</span></span>                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="8db3a-111">**IMFPMediaPlayer:: setbalance**</span><span class="sxs-lookup"><span data-stu-id="8db3a-111">**IMFPMediaPlayer::SetBalance**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | <span data-ttu-id="8db3a-112">Define o equilíbrio entre os canais esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="8db3a-112">Sets the balance between the left and right channels.</span></span> |
| [<span data-ttu-id="8db3a-113">**IMFPMediaPlayer:: setmudo**</span><span class="sxs-lookup"><span data-stu-id="8db3a-113">**IMFPMediaPlayer::SetMute**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | <span data-ttu-id="8db3a-114">Silencia ou desativa o áudio.</span><span class="sxs-lookup"><span data-stu-id="8db3a-114">Mutes or unmutes the audio.</span></span>                           |
| [<span data-ttu-id="8db3a-115">**IMFPMediaPlayer:: SetVolume**</span><span class="sxs-lookup"><span data-stu-id="8db3a-115">**IMFPMediaPlayer::SetVolume**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | <span data-ttu-id="8db3a-116">Define o nível de volume.</span><span class="sxs-lookup"><span data-stu-id="8db3a-116">Sets the volume level.</span></span>                                |



 

<span data-ttu-id="8db3a-117">Para entender o comportamento desses métodos, você deve saber alguma terminologia da API de sessão de áudio do Windows (WASAPI), que implementa a funcionalidade de áudio de nível baixo usada pelo MFPlay.</span><span class="sxs-lookup"><span data-stu-id="8db3a-117">To understand the behavior of these methods, you must know some terminology from the Windows Audio Session API (WASAPI), which implements the low-level audio functionality used by MFPlay.</span></span>

<span data-ttu-id="8db3a-118">No WASAPI, cada fluxo de áudio pertence a exatamente uma *sessão de áudio*, que é um grupo de fluxos de áudio relacionados.</span><span class="sxs-lookup"><span data-stu-id="8db3a-118">In WASAPI, every audio stream belongs to exactly one *audio session*, which is a group of related audio streams.</span></span> <span data-ttu-id="8db3a-119">Normalmente, um aplicativo mantém uma única sessão de áudio, embora os aplicativos possam criar mais de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="8db3a-119">Typically, an application maintains a single audio session, although applications can create more than one session.</span></span> <span data-ttu-id="8db3a-120">O SNDVOL (programa de controle de volume do sistema) exibe um controle de volume para cada sessão de áudio.</span><span class="sxs-lookup"><span data-stu-id="8db3a-120">The system volume-control program (Sndvol) displays a volume control for each audio session.</span></span> <span data-ttu-id="8db3a-121">Por meio do SNDVOL, um usuário pode ajustar o volume de uma sessão de áudio de fora do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8db3a-121">Through Sndvol, a user can adjust the volume of an audio session from outside of the application.</span></span> <span data-ttu-id="8db3a-122">A imagem a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="8db3a-122">The following image illustrates this process.</span></span>

![diagrama mostrando fluxos de áudio que passam pelo controle de volume no caminho para os alto-falantes; aplicativo e ponto de SNDVOL para controle de volume](images/audio-session.gif)

<span data-ttu-id="8db3a-124">No MFPlay, um item de mídia pode ter um ou mais fluxos de áudio ativos (normalmente apenas um).</span><span class="sxs-lookup"><span data-stu-id="8db3a-124">In MFPlay, a media item can have one or more active audio streams (typically only one).</span></span> <span data-ttu-id="8db3a-125">Internamente, o MFPlay usa o [processamento de áudio de streaming](streaming-audio-renderer.md) (SAR) para renderizar os fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="8db3a-125">Internally, MFPlay uses the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) to render the audio streams.</span></span> <span data-ttu-id="8db3a-126">A menos que você configure-o caso contrário, o SAR ingressará na sessão de áudio padrão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8db3a-126">Unless you configure it otherwise, the SAR joins the application's default audio session.</span></span>

<span data-ttu-id="8db3a-127">Os métodos de áudio MFPlay controlam apenas os fluxos que pertencem ao item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="8db3a-127">The MFPlay audio methods control only the streams that belong to the current media item.</span></span> <span data-ttu-id="8db3a-128">Eles não afetam o volume de nenhum outro fluxo que pertença à mesma sessão de áudio.</span><span class="sxs-lookup"><span data-stu-id="8db3a-128">They do not affect the volume for any other streams that belong to the same audio session.</span></span> <span data-ttu-id="8db3a-129">Em termos de WASAPI, os métodos MFPlay controlam os níveis de volume *por canal* , não o nível de volume mestre.</span><span class="sxs-lookup"><span data-stu-id="8db3a-129">In terms of WASAPI, the MFPlay methods control the *per-channel* volume levels, not the master volume level.</span></span> <span data-ttu-id="8db3a-130">A imagem a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="8db3a-130">The following image illustrates this process.</span></span>

![diagrama semelhante ao anterior, mas o segundo fluxo começa no item de mídia, e o aplicativo aponta para o segundo fluxo e para o controle de volume](images/audio-session02.gif)

<span data-ttu-id="8db3a-132">É importante entender algumas implicações desse recurso do MFPlay.</span><span class="sxs-lookup"><span data-stu-id="8db3a-132">It is important to understand some implications of this feature of MFPlay.</span></span> <span data-ttu-id="8db3a-133">Primeiro, um aplicativo pode ajustar o volume de reprodução sem afetar outros fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="8db3a-133">First, an application can adjust the playback volume without affecting other audio streams.</span></span> <span data-ttu-id="8db3a-134">Você pode usar esse recurso se MFPlay para implementar o esmaecimento cruzado de áudio, criando duas instâncias do objeto MFPlay e ajustando o volume separadamente.</span><span class="sxs-lookup"><span data-stu-id="8db3a-134">You could use this feature if MFPlay to implement audio cross-fading, by creating two instances of the MFPlay object and adjusting the volume separately.</span></span>

<span data-ttu-id="8db3a-135">Se você usar métodos MFPlay para alterar o volume ou o estado de mudo, as alterações não aparecerão em SNDVOL.</span><span class="sxs-lookup"><span data-stu-id="8db3a-135">If you use MFPlay methods to change the volume or mute state, the changes do not appear in Sndvol.</span></span> <span data-ttu-id="8db3a-136">Por exemplo, você pode chamar [**setmudo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) para mudo do áudio, mas o SNDVOL não mostrará a sessão como mudo.</span><span class="sxs-lookup"><span data-stu-id="8db3a-136">For example, you can call [**SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) to mute the audio, but Sndvol will not show the session as muted.</span></span> <span data-ttu-id="8db3a-137">Por outro lado, se SndVol for usado para ajustar o volume da sessão, as alterações não serão refletidas nos valores retornados por [**IMFPMediaPlayer:: GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) ou [**IMFPMediaPlayer:: getmudo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).</span><span class="sxs-lookup"><span data-stu-id="8db3a-137">Conversely, if SndVol is used to adjust the session volume, the changes are not reflected in the values returned by [**IMFPMediaPlayer::GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) or [**IMFPMediaPlayer::GetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).</span></span>

<span data-ttu-id="8db3a-138">Para cada instância do objeto MFPlay Player, o nível de volume efetivo é igual a *fPlayerVolume* × *fSessionVolume*, em que *fPlayerVolume* é o valor retornado por [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume)e *fSessionVolume* é o volume mestre da sessão.</span><span class="sxs-lookup"><span data-stu-id="8db3a-138">For each instance of the MFPlay player object, the effective volume level equals *fPlayerVolume* × *fSessionVolume*, where *fPlayerVolume* is the value returned by [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume), and *fSessionVolume* is the master volume for the session.</span></span>

<span data-ttu-id="8db3a-139">Para cenários de reprodução simples, pode ser preferível usar o WASAPI para controlar o volume de áudio para toda a sessão, em vez de usar os métodos MFPlay.</span><span class="sxs-lookup"><span data-stu-id="8db3a-139">For simple playback scenarios, it might be preferable to use the WASAPI to control the audio volume for the entire session, rather than use the MFPlay methods.</span></span>

## <a name="example-code"></a><span data-ttu-id="8db3a-140">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="8db3a-140">Example Code</span></span>

<span data-ttu-id="8db3a-141">O que vem a seguir é uma classe C++ que manipula as tarefas básicas no WASAPI:</span><span class="sxs-lookup"><span data-stu-id="8db3a-141">What follows is a C++ class that handles the basic tasks in WASAPI:</span></span>

-   <span data-ttu-id="8db3a-142">Controlando o volume e o estado de mudo para a sessão.</span><span class="sxs-lookup"><span data-stu-id="8db3a-142">Controlling the volume and mute state for the session.</span></span>
-   <span data-ttu-id="8db3a-143">Obter notificações sempre que o volume ou o estado de mudo for alterado.</span><span class="sxs-lookup"><span data-stu-id="8db3a-143">Getting notifications whenever the volume or mute state change.</span></span>

### <a name="class-declaration"></a><span data-ttu-id="8db3a-144">Declaração de classe</span><span class="sxs-lookup"><span data-stu-id="8db3a-144">Class Declaration</span></span>

<span data-ttu-id="8db3a-145">A `CAudioSessionVolume` declaração de classe implementa a interface [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) , que é a interface de retorno de chamada para eventos de sessão de áudio.</span><span class="sxs-lookup"><span data-stu-id="8db3a-145">The `CAudioSessionVolume` class declaration implements the [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, which is the callback interface for audio session events.</span></span>


```C++
class CAudioSessionVolume : public IAudioSessionEvents
{
public:
    // Static method to create an instance of the object.
    static HRESULT CreateInstance(
        UINT uNotificationMessage,
        HWND hwndNotification,
        CAudioSessionVolume **ppAudioSessionVolume
    );

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IAudioSessionEvents methods.

    STDMETHODIMP OnSimpleVolumeChanged(
        float NewVolume,
        BOOL NewMute,
        LPCGUID EventContext
        );

    // The remaining audio session events do not require any action.
    STDMETHODIMP OnDisplayNameChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnIconPathChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnChannelVolumeChanged(DWORD,float[],DWORD,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnGroupingParamChanged(LPCGUID,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnStateChanged(AudioSessionState)
    {
        return S_OK;
    }

    STDMETHODIMP OnSessionDisconnected(AudioSessionDisconnectReason)
    {
        return S_OK;
    }

    // Other methods
    HRESULT EnableNotifications(BOOL bEnable);
    HRESULT GetVolume(float *pflVolume);
    HRESULT SetVolume(float flVolume);
    HRESULT GetMute(BOOL *pbMute);
    HRESULT SetMute(BOOL bMute);
    HRESULT SetDisplayName(const WCHAR *wszName);

protected:
    CAudioSessionVolume(UINT uNotificationMessage, HWND hwndNotification);
    ~CAudioSessionVolume();

    HRESULT Initialize();

protected:
    LONG m_cRef;                        // Reference count.
    UINT m_uNotificationMessage;        // Window message to send when an audio event occurs.
    HWND m_hwndNotification;            // Window to receives messages.
    BOOL m_bNotificationsEnabled;       // Are audio notifications enabled?

    IAudioSessionControl    *m_pAudioSession;
    ISimpleAudioVolume      *m_pSimpleAudioVolume;
};
```



<span data-ttu-id="8db3a-146">Quando o `CAudioSessionVolume` objeto recebe um evento de sessão de áudio, ele posta uma mensagem de janela privada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8db3a-146">When the `CAudioSessionVolume` object receives an audio session event, it posts a private window message to the application.</span></span> <span data-ttu-id="8db3a-147">O identificador de janela e a mensagem de janela são fornecidos como parâmetros para o `CAudioSessionVolume::CreateInstance` método estático.</span><span class="sxs-lookup"><span data-stu-id="8db3a-147">The window handle and the window message are given as parameters to the static `CAudioSessionVolume::CreateInstance` method.</span></span>

### <a name="getting-the-wasapi-interface-pointers"></a><span data-ttu-id="8db3a-148">Obtendo os ponteiros de interface WASAPI</span><span class="sxs-lookup"><span data-stu-id="8db3a-148">Getting the WASAPI Interface Pointers</span></span>

<span data-ttu-id="8db3a-149">`CAudioSessionVolume` usa duas interfaces WASAPI principais:</span><span class="sxs-lookup"><span data-stu-id="8db3a-149">`CAudioSessionVolume` uses two main WASAPI interfaces:</span></span>

-   <span data-ttu-id="8db3a-150">O [**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) gerencia a sessão de áudio.</span><span class="sxs-lookup"><span data-stu-id="8db3a-150">[**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) manages the audio session.</span></span>
-   <span data-ttu-id="8db3a-151">[**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) controla o nível de volume e o estado de mudo da sessão.</span><span class="sxs-lookup"><span data-stu-id="8db3a-151">[**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) controls the volume level and mute state of the session.</span></span>

<span data-ttu-id="8db3a-152">Para obter essas interfaces, você deve enumerar o ponto de extremidade de áudio usado pelo SAR.</span><span class="sxs-lookup"><span data-stu-id="8db3a-152">To get these interfaces, you must enumerate the audio endpoint that is used by the SAR.</span></span> <span data-ttu-id="8db3a-153">Um *ponto de extremidade de áudio* é um dispositivo de hardware que captura ou consome dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="8db3a-153">An *audio endpoint* is a hardware device that captures or consumes audio data.</span></span> <span data-ttu-id="8db3a-154">Para reprodução de áudio, um ponto de extremidade é simplesmente um palestrante ou outra saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="8db3a-154">For audio playback, an endpoint is simply a speaker or other audio output.</span></span> <span data-ttu-id="8db3a-155">Por padrão, o SAR usa o ponto de extremidade padrão para a função de dispositivo **eConsole** .</span><span class="sxs-lookup"><span data-stu-id="8db3a-155">By default, the SAR uses the default endpoint for the **eConsole** device role.</span></span> <span data-ttu-id="8db3a-156">Uma *função de dispositivo* é uma função atribuída para um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8db3a-156">A *device role* is an assigned role for an endpoint.</span></span> <span data-ttu-id="8db3a-157">As funções de dispositivo são especificadas pela enumeração [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) , documentada em [APIs de áudio de núcleo](../coreaudio/core-audio-apis-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="8db3a-157">Device roles are specified by the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration, which is documented in [Core Audio APIs](../coreaudio/core-audio-apis-in-windows-vista.md).</span></span>

<span data-ttu-id="8db3a-158">O código a seguir mostra como enumerar o ponto de extremidade e obter as interfaces WASAPI.</span><span class="sxs-lookup"><span data-stu-id="8db3a-158">The following code shows how to enumerate the endpoint and get the WASAPI interfaces.</span></span>


```C++
HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}
```



### <a name="controlling-the-volume"></a><span data-ttu-id="8db3a-159">Controlando o volume</span><span class="sxs-lookup"><span data-stu-id="8db3a-159">Controlling the Volume</span></span>

<span data-ttu-id="8db3a-160">Os `CAudioSessionVolume` métodos que controlam o volume de áudio chamam os métodos [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) equivalentes.</span><span class="sxs-lookup"><span data-stu-id="8db3a-160">The `CAudioSessionVolume` methods that control the audio volume call the equivalent [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) methods.</span></span> <span data-ttu-id="8db3a-161">Por exemplo, `CAudioSessionVolume::SetVolume` chama [**ISimpleAudioVolume:: SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="8db3a-161">For example, `CAudioSessionVolume::SetVolume` calls [**ISimpleAudioVolume::SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), as shown in the following code.</span></span>


```C++
HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}
```



## <a name="complete-caudiosessionvolume-code"></a><span data-ttu-id="8db3a-162">Código completo do CAudioSessionVolume</span><span class="sxs-lookup"><span data-stu-id="8db3a-162">Complete CAudioSessionVolume Code</span></span>

<span data-ttu-id="8db3a-163">Aqui está a listagem completa para os métodos da `CAudioSessionVolume` classe.</span><span class="sxs-lookup"><span data-stu-id="8db3a-163">Here is the complete listing for the methods of the `CAudioSessionVolume` class.</span></span>


```C++
static const GUID AudioSessionVolumeCtx =
{ 0x2715279f, 0x4139, 0x4ba0, { 0x9c, 0xb1, 0xb3, 0x51, 0xf1, 0xb5, 0x8a, 0x4a } };


CAudioSessionVolume::CAudioSessionVolume(
    UINT uNotificationMessage,
    HWND hwndNotification
    )
    : m_cRef(1),
      m_uNotificationMessage(uNotificationMessage),
      m_hwndNotification(hwndNotification),
      m_bNotificationsEnabled(FALSE),
      m_pAudioSession(NULL),
      m_pSimpleAudioVolume(NULL)
{
}

CAudioSessionVolume::~CAudioSessionVolume()
{
    EnableNotifications(FALSE);

    SafeRelease(&m_pAudioSession);
    SafeRelease(&m_pSimpleAudioVolume);
};


//  Creates an instance of the CAudioSessionVolume object.

/* static */
HRESULT CAudioSessionVolume::CreateInstance(
    UINT uNotificationMessage,
    HWND hwndNotification,
    CAudioSessionVolume **ppAudioSessionVolume
    )
{

    CAudioSessionVolume *pAudioSessionVolume = new (std::nothrow)
        CAudioSessionVolume(uNotificationMessage, hwndNotification);

    if (pAudioSessionVolume == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pAudioSessionVolume->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppAudioSessionVolume = pAudioSessionVolume;
    }
    else
    {
        pAudioSessionVolume->Release();
    }

    return hr;
}


//  Initializes the CAudioSessionVolume object.

HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}

STDMETHODIMP CAudioSessionVolume::QueryInterface(REFIID riid, void **ppv)
{
    static const QITAB qit[] =
    {
        QITABENT(CAudioSessionVolume, IAudioSessionEvents),
        { 0 },
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::Release()
{
    LONG cRef = InterlockedDecrement( &m_cRef );
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}


// Enables or disables notifications from the audio session. For example, the
// application is notified if the user mutes the audio through the system
// volume-control program (Sndvol).

HRESULT CAudioSessionVolume::EnableNotifications(BOOL bEnable)
{
    HRESULT hr = S_OK;

    if (m_hwndNotification == NULL || m_pAudioSession == NULL)
    {
        return E_FAIL;
    }

    if (m_bNotificationsEnabled == bEnable)
    {
        // No change.
        return S_OK;
    }

    if (bEnable)
    {
        hr = m_pAudioSession->RegisterAudioSessionNotification(this);
    }
    else
    {
        hr = m_pAudioSession->UnregisterAudioSessionNotification(this);
    }

    if (SUCCEEDED(hr))
    {
        m_bNotificationsEnabled = bEnable;
    }

    return hr;
}


// Gets the session volume level.

HRESULT CAudioSessionVolume::GetVolume(float *pflVolume)
{
    if ( m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMasterVolume(pflVolume);
    }
}

//  Sets the session volume level.
//
//  flVolume: Ranges from 0 (silent) to 1 (full volume)

HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}


//  Gets the muting state of the session.

HRESULT CAudioSessionVolume::GetMute(BOOL *pbMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMute(pbMute);
    }
}

//  Mutes or unmutes the session audio.

HRESULT CAudioSessionVolume::SetMute(BOOL bMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMute(
            bMute,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}

//  Sets the display name for the session audio.

HRESULT CAudioSessionVolume::SetDisplayName(const WCHAR *wszName)
{
    if (m_pAudioSession == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pAudioSession->SetDisplayName(wszName, NULL);
    }
}


//  Called when the session volume level or muting state changes.
//  (Implements IAudioSessionEvents::OnSimpleVolumeChanged.)

HRESULT CAudioSessionVolume::OnSimpleVolumeChanged(
    float NewVolume,
    BOOL NewMute,
    LPCGUID EventContext
    )
{
    // Check if we should post a message to the application.

    if ( m_bNotificationsEnabled &&
        (*EventContext != AudioSessionVolumeCtx) &&
        (m_hwndNotification != NULL)
        )
    {
        // Notifications are enabled, AND
        // We did not trigger the event ourselves, AND
        // We have a valid window handle.

        // Post the message.
        ::PostMessage(
            m_hwndNotification,
            m_uNotificationMessage,
            *((WPARAM*)(&NewVolume)),  // Coerce the float.
            (LPARAM)NewMute
            );
    }
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="8db3a-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8db3a-164">Requirements</span></span>

<span data-ttu-id="8db3a-165">O MFPlay requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8db3a-165">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8db3a-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8db3a-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8db3a-167">Usando o MFPlay para reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="8db3a-167">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
