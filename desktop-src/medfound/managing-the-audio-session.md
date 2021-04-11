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
# <a name="managing-the-audio-session"></a>Gerenciando a sessão de áudio

\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. \]

Este tópico descreve como controlar o volume de áudio ao usar o MFPlay para reprodução de áudio/vídeo.

O MFPlay fornece os seguintes métodos para controlar o volume de áudio durante a reprodução.



| Método                                                            | Descrição                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [**IMFPMediaPlayer:: setbalance**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | Define o equilíbrio entre os canais esquerdo e direito. |
| [**IMFPMediaPlayer:: setmudo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | Silencia ou desativa o áudio.                           |
| [**IMFPMediaPlayer:: SetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | Define o nível de volume.                                |



 

Para entender o comportamento desses métodos, você deve saber alguma terminologia da API de sessão de áudio do Windows (WASAPI), que implementa a funcionalidade de áudio de nível baixo usada pelo MFPlay.

No WASAPI, cada fluxo de áudio pertence a exatamente uma *sessão de áudio*, que é um grupo de fluxos de áudio relacionados. Normalmente, um aplicativo mantém uma única sessão de áudio, embora os aplicativos possam criar mais de uma sessão. O SNDVOL (programa de controle de volume do sistema) exibe um controle de volume para cada sessão de áudio. Por meio do SNDVOL, um usuário pode ajustar o volume de uma sessão de áudio de fora do aplicativo. A imagem a seguir ilustra esse processo.

![diagrama mostrando fluxos de áudio que passam pelo controle de volume no caminho para os alto-falantes; aplicativo e ponto de SNDVOL para controle de volume](images/audio-session.gif)

No MFPlay, um item de mídia pode ter um ou mais fluxos de áudio ativos (normalmente apenas um). Internamente, o MFPlay usa o [processamento de áudio de streaming](streaming-audio-renderer.md) (SAR) para renderizar os fluxos de áudio. A menos que você configure-o caso contrário, o SAR ingressará na sessão de áudio padrão do aplicativo.

Os métodos de áudio MFPlay controlam apenas os fluxos que pertencem ao item de mídia atual. Eles não afetam o volume de nenhum outro fluxo que pertença à mesma sessão de áudio. Em termos de WASAPI, os métodos MFPlay controlam os níveis de volume *por canal* , não o nível de volume mestre. A imagem a seguir ilustra esse processo.

![diagrama semelhante ao anterior, mas o segundo fluxo começa no item de mídia, e o aplicativo aponta para o segundo fluxo e para o controle de volume](images/audio-session02.gif)

É importante entender algumas implicações desse recurso do MFPlay. Primeiro, um aplicativo pode ajustar o volume de reprodução sem afetar outros fluxos de áudio. Você pode usar esse recurso se MFPlay para implementar o esmaecimento cruzado de áudio, criando duas instâncias do objeto MFPlay e ajustando o volume separadamente.

Se você usar métodos MFPlay para alterar o volume ou o estado de mudo, as alterações não aparecerão em SNDVOL. Por exemplo, você pode chamar [**setmudo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) para mudo do áudio, mas o SNDVOL não mostrará a sessão como mudo. Por outro lado, se SndVol for usado para ajustar o volume da sessão, as alterações não serão refletidas nos valores retornados por [**IMFPMediaPlayer:: GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) ou [**IMFPMediaPlayer:: getmudo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).

Para cada instância do objeto MFPlay Player, o nível de volume efetivo é igual a *fPlayerVolume* × *fSessionVolume*, em que *fPlayerVolume* é o valor retornado por [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume)e *fSessionVolume* é o volume mestre da sessão.

Para cenários de reprodução simples, pode ser preferível usar o WASAPI para controlar o volume de áudio para toda a sessão, em vez de usar os métodos MFPlay.

## <a name="example-code"></a>Código de exemplo

O que vem a seguir é uma classe C++ que manipula as tarefas básicas no WASAPI:

-   Controlando o volume e o estado de mudo para a sessão.
-   Obter notificações sempre que o volume ou o estado de mudo for alterado.

### <a name="class-declaration"></a>Declaração de classe

A `CAudioSessionVolume` declaração de classe implementa a interface [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) , que é a interface de retorno de chamada para eventos de sessão de áudio.


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



Quando o `CAudioSessionVolume` objeto recebe um evento de sessão de áudio, ele posta uma mensagem de janela privada para o aplicativo. O identificador de janela e a mensagem de janela são fornecidos como parâmetros para o `CAudioSessionVolume::CreateInstance` método estático.

### <a name="getting-the-wasapi-interface-pointers"></a>Obtendo os ponteiros de interface WASAPI

`CAudioSessionVolume` usa duas interfaces WASAPI principais:

-   O [**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) gerencia a sessão de áudio.
-   [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) controla o nível de volume e o estado de mudo da sessão.

Para obter essas interfaces, você deve enumerar o ponto de extremidade de áudio usado pelo SAR. Um *ponto de extremidade de áudio* é um dispositivo de hardware que captura ou consome dados de áudio. Para reprodução de áudio, um ponto de extremidade é simplesmente um palestrante ou outra saída de áudio. Por padrão, o SAR usa o ponto de extremidade padrão para a função de dispositivo **eConsole** . Uma *função de dispositivo* é uma função atribuída para um ponto de extremidade. As funções de dispositivo são especificadas pela enumeração [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) , documentada em [APIs de áudio de núcleo](../coreaudio/core-audio-apis-in-windows-vista.md).

O código a seguir mostra como enumerar o ponto de extremidade e obter as interfaces WASAPI.


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



### <a name="controlling-the-volume"></a>Controlando o volume

Os `CAudioSessionVolume` métodos que controlam o volume de áudio chamam os métodos [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) equivalentes. Por exemplo, `CAudioSessionVolume::SetVolume` chama [**ISimpleAudioVolume:: SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), conforme mostrado no código a seguir.


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



## <a name="complete-caudiosessionvolume-code"></a>Código completo do CAudioSessionVolume

Aqui está a listagem completa para os métodos da `CAudioSessionVolume` classe.


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



## <a name="requirements"></a>Requisitos

O MFPlay requer o Windows 7.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o MFPlay para reprodução de áudio/vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
