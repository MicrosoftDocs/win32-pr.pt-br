---
description: Eventos de áudio para aplicativos de áudio herdados
ms.assetid: 91a93b79-2563-4b25-af5d-ca5f7d35d77b
title: Eventos de áudio para aplicativos de áudio herdados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fe99195910b1c1c68c0f3a1b39dd2706dde0be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089634"
---
# <a name="audio-events-for-legacy-audio-applications"></a>Eventos de áudio para aplicativos de áudio herdados

APIs de áudio herdadas como DirectSound, DirectShow e as funções **waveOutXxx** permitem que os aplicativos obtenham e definam os níveis de volume de fluxos de áudio. Os aplicativos podem usar os recursos de controle de volume nessas APIs para exibir controles deslizantes de volume em suas janelas de aplicativos.

No Windows Vista, o programa de controle de volume do sistema, SNDVOL, permite que os usuários controlem os níveis de volume de áudio para aplicativos individuais. Os controles deslizantes de volume exibidos por aplicativos devem ser vinculados aos controles deslizantes de volume correspondentes no SNDVOL. Se um usuário ajustar o volume do aplicativo por meio de um controle deslizante de volume em uma janela de aplicativo, o controle deslizante de volume correspondente em SNDVOL será movido imediatamente para indicar o novo nível de volume. Por outro lado, se o usuário ajustar o volume do aplicativo por meio de SNDVOL, os controles deslizantes de volume na janela do aplicativo devem ser movidos para indicar o novo nível de volume.

No Windows Vista, o SNDVOL reflete imediatamente as alterações de volume que um aplicativo faz por meio de chamadas para o método **IDirectSoundBuffer:: SetVolume** ou a função **waveOutSetVolume** . No entanto, uma API de áudio herdada, como DirectSound ou as funções **waveOutXxx** , não fornece meios para notificar um aplicativo quando o usuário altera o volume do aplicativo por meio de SNDVOL. Se um aplicativo exibir um controle deslizante de volume, mas não receber notificações de alterações de volume, o controle deslizante falhará ao refletir as alterações feitas pelo usuário no SNDVOL. Para implementar o comportamento apropriado, o designer de aplicativos deve, de alguma forma, compensar a falta de notificações pela API de áudio herdada.

Uma solução pode ser para que o aplicativo defina um temporizador para lembrá-lo periodicamente de verificar o nível de volume para ver se ele foi alterado.

Uma solução mais elegante é que o aplicativo use os recursos de notificação de eventos das principais APIs de áudio. Em particular, o aplicativo pode registrar uma interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para receber retornos de chamada quando alterações de volume ou outros tipos de eventos de áudio ocorrerem. Quando o volume é alterado, a rotina de retorno de chamada de alteração de volume pode atualizar imediatamente o controle deslizante de volume do aplicativo para refletir a alteração.

O exemplo de código a seguir mostra como um aplicativo pode se registrar para receber notificações de alterações de volume e outros eventos de áudio:


```C++
//-----------------------------------------------------------
// Register the application to receive notifications when the
// volume level changes on the default process-specific audio
// session (with session GUID value GUID_NULL) on the audio
// endpoint device with the specified data-flow direction
// (eRender or eCapture) and device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class AudioVolumeEvents
{
    HRESULT _hrStatus;
    IAudioSessionManager *_pManager;
    IAudioSessionControl *_pControl;
    IAudioSessionEvents *_pAudioEvents;
public:
    AudioVolumeEvents(EDataFlow, ERole, IAudioSessionEvents*);
    ~AudioVolumeEvents();
    HRESULT GetStatus() { return _hrStatus; };
};

// Constructor
AudioVolumeEvents::AudioVolumeEvents(EDataFlow flow, ERole role,
                                     IAudioSessionEvents *pAudioEvents)
{
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    _hrStatus = S_OK;
    _pManager = NULL;
    _pControl = NULL;
    _pAudioEvents = pAudioEvents;

    if (_pAudioEvents == NULL)
    {
        _hrStatus = E_POINTER;
        return;
    }

    _pAudioEvents->AddRef();

    // Get the enumerator for the audio endpoint devices
    // on this system.
    _hrStatus = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                                 NULL, CLSCTX_INPROC_SERVER,
                                 __uuidof(IMMDeviceEnumerator),
                                 (void**)&pEnumerator);
    EXIT_ON_ERROR(_hrStatus)

    // Get the audio endpoint device with the specified data-flow
    // direction (eRender or eCapture) and device role.
    _hrStatus = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                                     &pDevice);
    EXIT_ON_ERROR(_hrStatus)

    // Get the session manager for the endpoint device.
    _hrStatus = pDevice->Activate(__uuidof(IAudioSessionManager),
                                  CLSCTX_INPROC_SERVER, NULL,
                                  (void**)&_pManager);
    EXIT_ON_ERROR(_hrStatus)

    // Get the control interface for the process-specific audio
    // session with session GUID = GUID_NULL. This is the session
    // that an audio stream for a DirectSound, DirectShow, waveOut,
    // or PlaySound application stream belongs to by default.
    _hrStatus = _pManager->GetAudioSessionControl(NULL, 0, &_pControl);
    EXIT_ON_ERROR(_hrStatus)

    _hrStatus = _pControl->RegisterAudioSessionNotification(_pAudioEvents);
    EXIT_ON_ERROR(_hrStatus)

Exit:
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
}

// Destructor
AudioVolumeEvents::~AudioVolumeEvents()
{
    if (_pControl != NULL)
    {
        _pControl->UnregisterAudioSessionNotification(_pAudioEvents);
    }
    SAFE_RELEASE(_pManager)
    SAFE_RELEASE(_pControl)
    SAFE_RELEASE(_pAudioEvents)
};
```



O exemplo de código anterior implementa uma classe chamada AudioVolumeEvents. Durante a inicialização do programa, o aplicativo de áudio permite notificações de eventos de áudio criando um objeto AudioVolumeEvents. O construtor para essa classe usa três parâmetros de entrada:

-   *Flow*— a direção do fluxo de dados do [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md) (um valor de enumeração [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) ).
-   *função*— a [função de dispositivo](device-roles.md) atual do dispositivo de ponto de extremidade (um valor de enumeração [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ).
-   *pAudioEvents*— ponteiro para um objeto (uma instância de interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) ) que contém um conjunto de rotinas de retorno de chamada que são implementadas pelo aplicativo.

O construtor fornece os valores de fluxo e função como parâmetros de entrada para o método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) . O método cria um objeto [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) que encapsula o dispositivo de ponto de extremidade de áudio com a direção de fluxo de dados e a função de dispositivo especificadas.

O aplicativo implementa o objeto apontado por *pAudioEvents*. (A implementação não é mostrada no exemplo de código anterior. Para obter um exemplo de código que implementa uma interface **IAudioSessionEvents** , consulte [eventos de sessão de áudio](audio-session-events.md).) Cada método nessa interface recebe notificações de um determinado tipo de evento de áudio. Se o aplicativo não estiver interessado em um determinado tipo de evento, o método para esse tipo de evento não deverá fazer nada, mas retornará S \_ OK.

O método [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) recebe notificações de alterações de volume. Normalmente, esse método atualiza o controle deslizante de volume do aplicativo.

No exemplo de código anterior, o construtor para a classe AudioVolumeEvents é registrado para notificações na [sessão de áudio](audio-sessions.md) específica do processo que é identificada pelo valor GUID de sessão GUID \_ NULL. Por padrão, as APIs de áudio herdadas, como DirectSound, DirectShow e as funções **waveOutXxx** , atribuem seus fluxos a essa sessão. No entanto, um aplicativo DirectSound ou DirectShow pode, como uma opção, substituir o comportamento padrão e atribuir seus fluxos a uma sessão de processo cruzado ou a uma sessão identificada por um valor de GUID diferente de GUID \_ NULL. (No momento, nenhum mecanismo é fornecido para um aplicativo **waveOutXxx** substituir o comportamento padrão de maneira semelhante.) Para obter um exemplo de código de um aplicativo do DirectShow com esse comportamento, consulte [funções de dispositivo para aplicativos do DirectShow](device-roles-for-directshow-applications.md). Para acomodar esse aplicativo, você pode modificar o Construtor no exemplo de código anterior para aceitar dois parâmetros de entrada adicionais — um GUID de sessão e um sinalizador para indicar se a sessão a ser monitorada é uma sessão de processo cruzado ou específica de processo. Passe esses parâmetros para a chamada para o método [**IAudioSessionManager:: GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) no construtor.

Depois que o construtor chama o método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) para se registrar para notificações, o aplicativo continua a receber notificações apenas desde que a interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) ou [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) exista. O objeto AudioVolumeEvents no exemplo de código anterior mantém referências a essas interfaces até que seu destruidor seja chamado. Esse comportamento garante que o aplicativo continuará a receber notificações para o tempo de vida do objeto AudioVolumeEvents.

Em vez de selecionar implicitamente um dispositivo de áudio com base em sua função de dispositivo, um aplicativo multimídia DirectSound ou herdado do Windows pode permitir que o usuário selecione explicitamente um dispositivo de uma lista de dispositivos disponíveis que são identificados por seus nomes amigáveis. Para dar suporte a esse comportamento, o exemplo de código anterior deve ser modificado para gerar notificações de evento de áudio para o dispositivo selecionado. São necessárias duas modificações. Primeiro, altere a definição do construtor para aceitar uma [cadeia de caracteres de ID de ponto de extremidade](endpoint-id-strings.md) como um parâmetro de entrada (no lugar dos parâmetros de fluxo e função no exemplo de código). Essa cadeia de caracteres identifica o dispositivo de ponto de extremidade de áudio correspondente ao DirectSound ou dispositivo de formato de onda selecionado. Em segundo lugar, substitua a chamada para o método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) por uma chamada para o método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . A chamada **GetDevice** usa a cadeia de caracteres de ID de ponto de extremidade como um parâmetro de entrada e cria uma instância do dispositivo de ponto de extremidade que é identificada pela cadeia de caracteres.

A técnica para obter a cadeia de caracteres de ID de ponto de extremidade para um dispositivo DirectSound ou dispositivo de forma de onda herdada é a seguinte.

Primeiro, durante a enumeração do dispositivo, o DirectSound fornece a cadeia de caracteres da ID do ponto de extremidade para cada dispositivo enumerado. Para iniciar a enumeração do dispositivo, o aplicativo passa um ponteiro de função de retorno de chamada como um parâmetro de entrada para a função **DirectSoundCreate** ou **DirectSoundCaptureCreate** . A definição da função de retorno de chamada é:


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



No Windows Vista, o parâmetro *lpcstrModule* aponta para a cadeia de caracteres de ID do ponto de extremidade. (Em versões anteriores do Windows, incluindo o Windows Server 2003, o Windows XP e o Windows 2000, o parâmetro *lpcstrModule* aponta para o nome do módulo do driver para o dispositivo.) O parâmetro *lpcstrDescription* aponta para uma cadeia de caracteres que contém o nome amigável do dispositivo. Para obter mais informações sobre a enumeração de dispositivo DirectSound, consulte a documentação do SDK do Windows.

Em segundo lugar, para obter a cadeia de caracteres de ID de ponto de extremidade para um dispositivo de forma de onda herdado, use a função **waveOutMessage** ou **waveInMessage** para enviar uma \_ mensagem QUERYFUNCTIONINSTANCEID drv para o driver de dispositivo de forma Para obter um exemplo de código que mostra o uso dessa mensagem, consulte [funções de dispositivo para aplicativos multimídia herdados do Windows](device-roles-for-legacy-windows-multimedia-applications.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interoperabilidade com APIs de áudio herdadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



