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
# <a name="audio-events-for-legacy-audio-applications"></a><span data-ttu-id="b681d-103">Eventos de áudio para aplicativos de áudio herdados</span><span class="sxs-lookup"><span data-stu-id="b681d-103">Audio Events for Legacy Audio Applications</span></span>

<span data-ttu-id="b681d-104">APIs de áudio herdadas como DirectSound, DirectShow e as funções **waveOutXxx** permitem que os aplicativos obtenham e definam os níveis de volume de fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="b681d-104">Legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions enable applications to get and set the volume levels of audio streams.</span></span> <span data-ttu-id="b681d-105">Os aplicativos podem usar os recursos de controle de volume nessas APIs para exibir controles deslizantes de volume em suas janelas de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b681d-105">Applications can use the volume-control capabilities in these APIs to display volume sliders in their application windows.</span></span>

<span data-ttu-id="b681d-106">No Windows Vista, o programa de controle de volume do sistema, SNDVOL, permite que os usuários controlem os níveis de volume de áudio para aplicativos individuais.</span><span class="sxs-lookup"><span data-stu-id="b681d-106">In Windows Vista, the system volume-control program, Sndvol, allows users to control the audio volume levels for individual applications.</span></span> <span data-ttu-id="b681d-107">Os controles deslizantes de volume exibidos por aplicativos devem ser vinculados aos controles deslizantes de volume correspondentes no SNDVOL.</span><span class="sxs-lookup"><span data-stu-id="b681d-107">The volume sliders that are displayed by applications should be linked to the corresponding volume sliders in Sndvol.</span></span> <span data-ttu-id="b681d-108">Se um usuário ajustar o volume do aplicativo por meio de um controle deslizante de volume em uma janela de aplicativo, o controle deslizante de volume correspondente em SNDVOL será movido imediatamente para indicar o novo nível de volume.</span><span class="sxs-lookup"><span data-stu-id="b681d-108">If a user adjusts the application volume through a volume slider in an application window, then the corresponding volume slider in Sndvol immediately moves to indicate the new volume level.</span></span> <span data-ttu-id="b681d-109">Por outro lado, se o usuário ajustar o volume do aplicativo por meio de SNDVOL, os controles deslizantes de volume na janela do aplicativo devem ser movidos para indicar o novo nível de volume.</span><span class="sxs-lookup"><span data-stu-id="b681d-109">Conversely, if the user adjusts the application volume through Sndvol, then the volume sliders in the application window should move to indicate the new volume level.</span></span>

<span data-ttu-id="b681d-110">No Windows Vista, o SNDVOL reflete imediatamente as alterações de volume que um aplicativo faz por meio de chamadas para o método **IDirectSoundBuffer:: SetVolume** ou a função **waveOutSetVolume** .</span><span class="sxs-lookup"><span data-stu-id="b681d-110">In Windows Vista, Sndvol immediately reflects volume changes that an application makes through calls to the **IDirectSoundBuffer::SetVolume** method or **waveOutSetVolume** function.</span></span> <span data-ttu-id="b681d-111">No entanto, uma API de áudio herdada, como DirectSound ou as funções **waveOutXxx** , não fornece meios para notificar um aplicativo quando o usuário altera o volume do aplicativo por meio de SNDVOL.</span><span class="sxs-lookup"><span data-stu-id="b681d-111">However, a legacy audio API such as DirectSound or the **waveOutXxx** functions provides no means to notify an application when the user changes the application volume through Sndvol.</span></span> <span data-ttu-id="b681d-112">Se um aplicativo exibir um controle deslizante de volume, mas não receber notificações de alterações de volume, o controle deslizante falhará ao refletir as alterações feitas pelo usuário no SNDVOL.</span><span class="sxs-lookup"><span data-stu-id="b681d-112">If an application displays a volume slider but does not receive notifications of volume changes, then the slider will fail to reflect changes made by the user in Sndvol.</span></span> <span data-ttu-id="b681d-113">Para implementar o comportamento apropriado, o designer de aplicativos deve, de alguma forma, compensar a falta de notificações pela API de áudio herdada.</span><span class="sxs-lookup"><span data-stu-id="b681d-113">To implement the appropriate behavior, the application designer must somehow compensate for the lack of notifications by the legacy audio API.</span></span>

<span data-ttu-id="b681d-114">Uma solução pode ser para que o aplicativo defina um temporizador para lembrá-lo periodicamente de verificar o nível de volume para ver se ele foi alterado.</span><span class="sxs-lookup"><span data-stu-id="b681d-114">One solution might be for the application to set a timer to periodically remind it to check the volume level to see if it has changed.</span></span>

<span data-ttu-id="b681d-115">Uma solução mais elegante é que o aplicativo use os recursos de notificação de eventos das principais APIs de áudio.</span><span class="sxs-lookup"><span data-stu-id="b681d-115">A more elegant solution is for the application to use the event notification capabilities of the core audio APIs.</span></span> <span data-ttu-id="b681d-116">Em particular, o aplicativo pode registrar uma interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para receber retornos de chamada quando alterações de volume ou outros tipos de eventos de áudio ocorrerem.</span><span class="sxs-lookup"><span data-stu-id="b681d-116">In particular, the application can register an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to receive callbacks when volume changes or other types of audio events occur.</span></span> <span data-ttu-id="b681d-117">Quando o volume é alterado, a rotina de retorno de chamada de alteração de volume pode atualizar imediatamente o controle deslizante de volume do aplicativo para refletir a alteração.</span><span class="sxs-lookup"><span data-stu-id="b681d-117">When the volume changes, the volume-change callback routine can immediately update the application's volume slider to reflect the change.</span></span>

<span data-ttu-id="b681d-118">O exemplo de código a seguir mostra como um aplicativo pode se registrar para receber notificações de alterações de volume e outros eventos de áudio:</span><span class="sxs-lookup"><span data-stu-id="b681d-118">The following code example shows how an application can register to receive notifications of volume changes and other audio events:</span></span>


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



<span data-ttu-id="b681d-119">O exemplo de código anterior implementa uma classe chamada AudioVolumeEvents.</span><span class="sxs-lookup"><span data-stu-id="b681d-119">The preceding code example implements a class named AudioVolumeEvents.</span></span> <span data-ttu-id="b681d-120">Durante a inicialização do programa, o aplicativo de áudio permite notificações de eventos de áudio criando um objeto AudioVolumeEvents.</span><span class="sxs-lookup"><span data-stu-id="b681d-120">During program initialization, the audio application enables audio-event notifications by creating an AudioVolumeEvents object.</span></span> <span data-ttu-id="b681d-121">O construtor para essa classe usa três parâmetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="b681d-121">The constructor for this class takes three input parameters:</span></span>

-   <span data-ttu-id="b681d-122">*Flow*— a direção do fluxo de dados do [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md) (um valor de enumeração [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) ).</span><span class="sxs-lookup"><span data-stu-id="b681d-122">*flow*—the data-flow direction of the [audio endpoint device](audio-endpoint-devices.md) (an [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) enumeration value).</span></span>
-   <span data-ttu-id="b681d-123">*função*— a [função de dispositivo](device-roles.md) atual do dispositivo de ponto de extremidade (um valor de enumeração [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ).</span><span class="sxs-lookup"><span data-stu-id="b681d-123">*role*—the current [device role](device-roles.md) of the endpoint device (an [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration value).</span></span>
-   <span data-ttu-id="b681d-124">*pAudioEvents*— ponteiro para um objeto (uma instância de interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) ) que contém um conjunto de rotinas de retorno de chamada que são implementadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b681d-124">*pAudioEvents*—pointer to an object (an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface instance) that contains a set of callback routines that are implemented by the application.</span></span>

<span data-ttu-id="b681d-125">O construtor fornece os valores de fluxo e função como parâmetros de entrada para o método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) .</span><span class="sxs-lookup"><span data-stu-id="b681d-125">The constructor supplies the flow and role values as input parameters to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method.</span></span> <span data-ttu-id="b681d-126">O método cria um objeto [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) que encapsula o dispositivo de ponto de extremidade de áudio com a direção de fluxo de dados e a função de dispositivo especificadas.</span><span class="sxs-lookup"><span data-stu-id="b681d-126">The method creates an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object that encapsulates the audio endpoint device with the specified data-flow direction and device role.</span></span>

<span data-ttu-id="b681d-127">O aplicativo implementa o objeto apontado por *pAudioEvents*.</span><span class="sxs-lookup"><span data-stu-id="b681d-127">The application implements the object pointed to by *pAudioEvents*.</span></span> <span data-ttu-id="b681d-128">(A implementação não é mostrada no exemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="b681d-128">(The implementation is not shown in the preceding code example.</span></span> <span data-ttu-id="b681d-129">Para obter um exemplo de código que implementa uma interface **IAudioSessionEvents** , consulte [eventos de sessão de áudio](audio-session-events.md).) Cada método nessa interface recebe notificações de um determinado tipo de evento de áudio.</span><span class="sxs-lookup"><span data-stu-id="b681d-129">For a code example that implements an **IAudioSessionEvents** interface, see [Audio Session Events](audio-session-events.md).) Each method in this interface receives notifications of a particular type of audio event.</span></span> <span data-ttu-id="b681d-130">Se o aplicativo não estiver interessado em um determinado tipo de evento, o método para esse tipo de evento não deverá fazer nada, mas retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b681d-130">If the application is not interested in a particular event type, then the method for that event type should do nothing but return S\_OK.</span></span>

<span data-ttu-id="b681d-131">O método [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) recebe notificações de alterações de volume.</span><span class="sxs-lookup"><span data-stu-id="b681d-131">The [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) method receives notifications of volume changes.</span></span> <span data-ttu-id="b681d-132">Normalmente, esse método atualiza o controle deslizante de volume do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b681d-132">Typically, this method updates the application's volume slider.</span></span>

<span data-ttu-id="b681d-133">No exemplo de código anterior, o construtor para a classe AudioVolumeEvents é registrado para notificações na [sessão de áudio](audio-sessions.md) específica do processo que é identificada pelo valor GUID de sessão GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="b681d-133">In the preceding code example, the constructor for the AudioVolumeEvents class registers for notifications on the process-specific [audio session](audio-sessions.md) that is identified by session GUID value GUID\_NULL.</span></span> <span data-ttu-id="b681d-134">Por padrão, as APIs de áudio herdadas, como DirectSound, DirectShow e as funções **waveOutXxx** , atribuem seus fluxos a essa sessão.</span><span class="sxs-lookup"><span data-stu-id="b681d-134">By default, legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions assign their streams to this session.</span></span> <span data-ttu-id="b681d-135">No entanto, um aplicativo DirectSound ou DirectShow pode, como uma opção, substituir o comportamento padrão e atribuir seus fluxos a uma sessão de processo cruzado ou a uma sessão identificada por um valor de GUID diferente de GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="b681d-135">However, a DirectSound or DirectShow application can, as an option, override the default behavior and assign its streams to a cross-process session or to a session that is identified by a GUID value other than GUID\_NULL.</span></span> <span data-ttu-id="b681d-136">(No momento, nenhum mecanismo é fornecido para um aplicativo **waveOutXxx** substituir o comportamento padrão de maneira semelhante.) Para obter um exemplo de código de um aplicativo do DirectShow com esse comportamento, consulte [funções de dispositivo para aplicativos do DirectShow](device-roles-for-directshow-applications.md).</span><span class="sxs-lookup"><span data-stu-id="b681d-136">(No mechanism is currently provided for a **waveOutXxx** application to override the default behavior in a similar manner.) For a code example of a DirectShow application with this behavior, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="b681d-137">Para acomodar esse aplicativo, você pode modificar o Construtor no exemplo de código anterior para aceitar dois parâmetros de entrada adicionais — um GUID de sessão e um sinalizador para indicar se a sessão a ser monitorada é uma sessão de processo cruzado ou específica de processo.</span><span class="sxs-lookup"><span data-stu-id="b681d-137">To accommodate such an application, you can modify the constructor in the preceding code example to accept two additional input parameters—a session GUID and a flag to indicate whether the session that is to be monitored is a cross-process or process-specific session.</span></span> <span data-ttu-id="b681d-138">Passe esses parâmetros para a chamada para o método [**IAudioSessionManager:: GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) no construtor.</span><span class="sxs-lookup"><span data-stu-id="b681d-138">Pass these parameters to the call to the [**IAudioSessionManager::GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) method in the constructor.</span></span>

<span data-ttu-id="b681d-139">Depois que o construtor chama o método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) para se registrar para notificações, o aplicativo continua a receber notificações apenas desde que a interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) ou [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) exista.</span><span class="sxs-lookup"><span data-stu-id="b681d-139">After the constructor calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register for notifications, the application continues to receive notifications for only as long as either the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) or [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface exists.</span></span> <span data-ttu-id="b681d-140">O objeto AudioVolumeEvents no exemplo de código anterior mantém referências a essas interfaces até que seu destruidor seja chamado.</span><span class="sxs-lookup"><span data-stu-id="b681d-140">The AudioVolumeEvents object in the preceding code example holds references to these interfaces until its destructor is called.</span></span> <span data-ttu-id="b681d-141">Esse comportamento garante que o aplicativo continuará a receber notificações para o tempo de vida do objeto AudioVolumeEvents.</span><span class="sxs-lookup"><span data-stu-id="b681d-141">This behavior ensures that the application will continue to receive notifications for the lifetime of the AudioVolumeEvents object.</span></span>

<span data-ttu-id="b681d-142">Em vez de selecionar implicitamente um dispositivo de áudio com base em sua função de dispositivo, um aplicativo multimídia DirectSound ou herdado do Windows pode permitir que o usuário selecione explicitamente um dispositivo de uma lista de dispositivos disponíveis que são identificados por seus nomes amigáveis.</span><span class="sxs-lookup"><span data-stu-id="b681d-142">Instead of implicitly selecting an audio device based on its device role, a DirectSound or legacy Windows multimedia application might allow the user to explicitly select a device from a list of available devices that are identified by their friendly names.</span></span> <span data-ttu-id="b681d-143">Para dar suporte a esse comportamento, o exemplo de código anterior deve ser modificado para gerar notificações de evento de áudio para o dispositivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="b681d-143">To support this behavior, the preceding code example must be modified to generate audio-event notifications for the selected device.</span></span> <span data-ttu-id="b681d-144">São necessárias duas modificações.</span><span class="sxs-lookup"><span data-stu-id="b681d-144">Two modifications are required.</span></span> <span data-ttu-id="b681d-145">Primeiro, altere a definição do construtor para aceitar uma [cadeia de caracteres de ID de ponto de extremidade](endpoint-id-strings.md) como um parâmetro de entrada (no lugar dos parâmetros de fluxo e função no exemplo de código).</span><span class="sxs-lookup"><span data-stu-id="b681d-145">First, change the constructor definition to accept an [endpoint ID string](endpoint-id-strings.md) as an input parameter (in place of the flow and role parameters in the code example).</span></span> <span data-ttu-id="b681d-146">Essa cadeia de caracteres identifica o dispositivo de ponto de extremidade de áudio correspondente ao DirectSound ou dispositivo de formato de onda selecionado.</span><span class="sxs-lookup"><span data-stu-id="b681d-146">This string identifies the audio endpoint device that corresponds to the selected DirectSound or legacy waveform device.</span></span> <span data-ttu-id="b681d-147">Em segundo lugar, substitua a chamada para o método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) por uma chamada para o método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="b681d-147">Second, replace the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method with a call to the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="b681d-148">A chamada **GetDevice** usa a cadeia de caracteres de ID de ponto de extremidade como um parâmetro de entrada e cria uma instância do dispositivo de ponto de extremidade que é identificada pela cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b681d-148">The **GetDevice** call takes the endpoint ID string as an input parameter and creates an instance of the endpoint device that is identified by the string.</span></span>

<span data-ttu-id="b681d-149">A técnica para obter a cadeia de caracteres de ID de ponto de extremidade para um dispositivo DirectSound ou dispositivo de forma de onda herdada é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="b681d-149">The technique for obtaining the endpoint ID string for a DirectSound device or legacy waveform device is as follows.</span></span>

<span data-ttu-id="b681d-150">Primeiro, durante a enumeração do dispositivo, o DirectSound fornece a cadeia de caracteres da ID do ponto de extremidade para cada dispositivo enumerado.</span><span class="sxs-lookup"><span data-stu-id="b681d-150">First, during device enumeration, DirectSound supplies the endpoint ID string for each enumerated device.</span></span> <span data-ttu-id="b681d-151">Para iniciar a enumeração do dispositivo, o aplicativo passa um ponteiro de função de retorno de chamada como um parâmetro de entrada para a função **DirectSoundCreate** ou **DirectSoundCaptureCreate** .</span><span class="sxs-lookup"><span data-stu-id="b681d-151">To begin device enumeration, the application passes a callback function pointer as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span> <span data-ttu-id="b681d-152">A definição da função de retorno de chamada é:</span><span class="sxs-lookup"><span data-stu-id="b681d-152">The definition of the callback function is:</span></span>


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



<span data-ttu-id="b681d-153">No Windows Vista, o parâmetro *lpcstrModule* aponta para a cadeia de caracteres de ID do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="b681d-153">In Windows Vista, the *lpcstrModule* parameter points to the endpoint ID string.</span></span> <span data-ttu-id="b681d-154">(Em versões anteriores do Windows, incluindo o Windows Server 2003, o Windows XP e o Windows 2000, o parâmetro *lpcstrModule* aponta para o nome do módulo do driver para o dispositivo.) O parâmetro *lpcstrDescription* aponta para uma cadeia de caracteres que contém o nome amigável do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b681d-154">(In earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000, the *lpcstrModule* parameter points to the name of the driver module for the device.) The *lpcstrDescription* parameter points to a string that contains the friendly name of the device.</span></span> <span data-ttu-id="b681d-155">Para obter mais informações sobre a enumeração de dispositivo DirectSound, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="b681d-155">For more information about DirectSound device enumeration, see the Windows SDK documentation.</span></span>

<span data-ttu-id="b681d-156">Em segundo lugar, para obter a cadeia de caracteres de ID de ponto de extremidade para um dispositivo de forma de onda herdado, use a função **waveOutMessage** ou **waveInMessage** para enviar uma \_ mensagem QUERYFUNCTIONINSTANCEID drv para o driver de dispositivo de forma</span><span class="sxs-lookup"><span data-stu-id="b681d-156">Second, to obtain the endpoint ID string for a legacy waveform device, use the **waveOutMessage** or **waveInMessage** function to send a DRV\_QUERYFUNCTIONINSTANCEID message to the waveform device driver.</span></span> <span data-ttu-id="b681d-157">Para obter um exemplo de código que mostra o uso dessa mensagem, consulte [funções de dispositivo para aplicativos multimídia herdados do Windows](device-roles-for-legacy-windows-multimedia-applications.md).</span><span class="sxs-lookup"><span data-stu-id="b681d-157">For a code example that shows the use of this message, see [Device Roles for Legacy Windows Multimedia Applications](device-roles-for-legacy-windows-multimedia-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b681d-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b681d-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b681d-159">Interoperabilidade com APIs de áudio herdadas</span><span class="sxs-lookup"><span data-stu-id="b681d-159">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



