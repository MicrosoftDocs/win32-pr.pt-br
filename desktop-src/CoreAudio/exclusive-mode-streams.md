---
description: Fluxos de Exclusive-Mode
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Fluxos de Exclusive-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7722dd3463346e976f30a77949f56026a2425624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920367"
---
# <a name="exclusive-mode-streams"></a><span data-ttu-id="f1c19-103">Fluxos de Exclusive-Mode</span><span class="sxs-lookup"><span data-stu-id="f1c19-103">Exclusive-Mode Streams</span></span>

<span data-ttu-id="f1c19-104">Conforme explicado anteriormente, se um aplicativo abrir um fluxo em modo exclusivo, o aplicativo terá o uso exclusivo do dispositivo de ponto de extremidade de áudio que reproduz ou registra o fluxo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-104">As explained previously, if an application opens a stream in exclusive mode, the application has exclusive use of the audio endpoint device that plays or records the stream.</span></span> <span data-ttu-id="f1c19-105">Por outro lado, vários aplicativos podem compartilhar um dispositivo de ponto de extremidade de áudio abrindo fluxos de modo compartilhado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-105">In contrast, several applications can share an audio endpoint device by opening shared-mode streams on the device.</span></span>

<span data-ttu-id="f1c19-106">O acesso de modo exclusivo a um dispositivo de áudio pode bloquear sons de sistema cruciais, impedir a interoperabilidade com outros aplicativos e, de outra forma, degradar a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="f1c19-106">Exclusive-mode access to an audio device can block crucial system sounds, prevent interoperability with other applications, and otherwise degrade the user experience.</span></span> <span data-ttu-id="f1c19-107">Para atenuar esses problemas, um aplicativo com um fluxo de modo exclusivo normalmente abandona o controle do dispositivo de áudio quando o aplicativo não é o processo em primeiro plano ou não é transmitido ativamente.</span><span class="sxs-lookup"><span data-stu-id="f1c19-107">To mitigate these problems, an application with an exclusive-mode stream typically relinquishes control of the audio device when the application is not the foreground process or is not actively streaming.</span></span>

<span data-ttu-id="f1c19-108">A latência de fluxo é o atraso que é inerente ao caminho de dados que conecta o buffer de ponto de extremidade de um aplicativo a um dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="f1c19-108">Stream latency is the delay that is inherent in the data path that connects an application's endpoint buffer with an audio endpoint device.</span></span> <span data-ttu-id="f1c19-109">Para um fluxo de renderização, a latência é o atraso máximo desde o momento em que um aplicativo grava um exemplo em um buffer de ponto de extremidade no momento em que o exemplo é ouvido pelos alto-falantes.</span><span class="sxs-lookup"><span data-stu-id="f1c19-109">For a rendering stream, the latency is the maximum delay from the time that an application writes a sample to an endpoint buffer to the time that the sample is heard through the speakers.</span></span> <span data-ttu-id="f1c19-110">Para um fluxo de captura, a latência é o atraso máximo desde o momento em que um som entra no microfone até a hora em que um aplicativo pode ler o exemplo desse som do buffer de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f1c19-110">For a capture stream, the latency is the maximum delay from the time that a sound enters the microphone to the time that an application can read the sample for that sound from the endpoint buffer.</span></span>

<span data-ttu-id="f1c19-111">Os aplicativos que usam fluxos de modo exclusivo geralmente fazem isso porque exigem latências baixas nos caminhos de dados entre os dispositivos de ponto de extremidade de áudio e os threads de aplicativo que acessam os buffers de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f1c19-111">Applications that use exclusive-mode streams often do so because they require low latencies in the data paths between the audio endpoint devices and the application threads that access the endpoint buffers.</span></span> <span data-ttu-id="f1c19-112">Normalmente, esses threads são executados com prioridade relativamente alta e se agendam para serem executados em intervalos periódicos próximos ou iguais ao intervalo periódico que separa as passagens de processamento sucessivas pelo hardware de áudio.</span><span class="sxs-lookup"><span data-stu-id="f1c19-112">Typically, these threads run at relatively high priority and schedule themselves to run at periodic intervals that are close to or the same as the periodic interval that separates successive processing passes by the audio hardware.</span></span> <span data-ttu-id="f1c19-113">Durante cada passagem, o hardware de áudio processa os novos dados nos buffers de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f1c19-113">During each pass, the audio hardware processes the new data in the endpoint buffers.</span></span>

<span data-ttu-id="f1c19-114">Para alcançar as menores latências de fluxo, um aplicativo pode exigir hardware de áudio especial e um sistema de computador que está levemente carregado.</span><span class="sxs-lookup"><span data-stu-id="f1c19-114">To achieve the smallest stream latencies, an application might require both special audio hardware, and a computer system that is lightly loaded.</span></span> <span data-ttu-id="f1c19-115">A condução do hardware de áudio além de seus limites de tempo ou o carregamento do sistema com tarefas de alta prioridade concorrentes pode causar uma falha em um fluxo de áudio de baixa latência.</span><span class="sxs-lookup"><span data-stu-id="f1c19-115">Driving the audio hardware beyond its timing limits or loading the system with competing high-priority tasks might cause a glitch in a low-latency audio stream.</span></span> <span data-ttu-id="f1c19-116">Por exemplo, para um fluxo de renderização, pode ocorrer uma falha se o aplicativo não conseguir gravar em um buffer de ponto de extremidade antes de o hardware de áudio ler o buffer ou se o hardware não conseguir ler o buffer antes da hora em que o buffer está agendado para reprodução.</span><span class="sxs-lookup"><span data-stu-id="f1c19-116">For example, for a rendering stream, a glitch can occur if the application fails to write to an endpoint buffer before the audio hardware reads the buffer, or if the hardware fails to read the buffer before the time that the buffer is scheduled to play.</span></span> <span data-ttu-id="f1c19-117">Normalmente, um aplicativo destinado a ser executado em uma ampla variedade de hardwares de áudio e em uma ampla gama de sistemas deve relaxar seus requisitos de tempo suficientes para evitar problemas em todos os ambientes de destino.</span><span class="sxs-lookup"><span data-stu-id="f1c19-117">Typically, an application that is intended to run on a wide variety of audio hardware and in a broad range of systems should relax its timing requirements enough to avoid glitches in all target environments.</span></span>

<span data-ttu-id="f1c19-118">O Windows Vista tem vários recursos para dar suporte a aplicativos que exigem fluxos de áudio de baixa latência.</span><span class="sxs-lookup"><span data-stu-id="f1c19-118">Windows Vista has several features to support applications that require low-latency audio streams.</span></span> <span data-ttu-id="f1c19-119">Conforme discutido nos [componentes de áudio do modo de usuário](user-mode-audio-components.md), os aplicativos que executam operações de tempo crítico podem chamar as funções do serviço do Agendador de classes de multimídia (MMCSS) para aumentar a prioridade do thread sem negar recursos de CPU a aplicativos de prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="f1c19-119">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), applications that perform time-critical operations can call the Multimedia Class Scheduler Service (MMCSS) functions to increase thread priority without denying CPU resources to lower-priority applications.</span></span> <span data-ttu-id="f1c19-120">Além disso, o método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) dá suporte a um \_ sinalizador AUDCLNT STREAMFLAGS \_ EVENTCALLBACK que permite que o thread de serviço de buffer de um aplicativo agende sua execução para ocorrer quando um novo buffer se tornar disponível no dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="f1c19-120">In addition, the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method supports an AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK flag that enables an application's buffer-servicing thread to schedule its execution to occur when a new buffer becomes available from the audio device.</span></span> <span data-ttu-id="f1c19-121">Usando esses recursos, um thread de aplicativo pode reduzir as incertezas sobre quando ele será executado, diminuindo assim o risco de falhas em um fluxo de áudio de baixa latência.</span><span class="sxs-lookup"><span data-stu-id="f1c19-121">By using these features, an application thread can reduce uncertainty about when it will execute, thereby decreasing the risk of glitches in a low-latency audio stream.</span></span>

<span data-ttu-id="f1c19-122">Os drivers para adaptadores de áudio mais antigos provavelmente usarão a DDI (interface de driver de dispositivo) WaveCyclic ou WavePci, enquanto os drivers para adaptadores de áudio mais novos têm maior probabilidade de oferecer suporte à DDI WaveRT.</span><span class="sxs-lookup"><span data-stu-id="f1c19-122">The drivers for older audio adapters are likely to use the WaveCyclic or WavePci device driver interface (DDI), whereas the drivers for newer audio adapters are more likely to support the WaveRT DDI.</span></span> <span data-ttu-id="f1c19-123">Para aplicativos de modo exclusivo, os drivers WaveRT podem fornecer melhor desempenho que os drivers WaveCyclic ou WavePci, mas os drivers de WaveRT exigem recursos de hardware adicionais.</span><span class="sxs-lookup"><span data-stu-id="f1c19-123">For exclusive-mode applications, WaveRT drivers can provide better performance than WaveCyclic or WavePci drivers, but WaveRT drivers require additional hardware capabilities.</span></span> <span data-ttu-id="f1c19-124">Esses recursos incluem a capacidade de compartilhar buffers de hardware diretamente com aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f1c19-124">These capabilities include the ability to share hardware buffers directly with applications.</span></span> <span data-ttu-id="f1c19-125">Com o compartilhamento direto, nenhuma intervenção do sistema é necessária para transferir dados entre um aplicativo de modo exclusivo e o hardware de áudio.</span><span class="sxs-lookup"><span data-stu-id="f1c19-125">With direct sharing, no system intervention is required to transfer data between an exclusive-mode application and the audio hardware.</span></span> <span data-ttu-id="f1c19-126">Por outro lado, os drivers WaveCyclic e WavePci são adequados para adaptadores de áudio mais antigos e com menos capacidade.</span><span class="sxs-lookup"><span data-stu-id="f1c19-126">In contrast, WaveCyclic and WavePci drivers are suitable for older, less capable audio adapters.</span></span> <span data-ttu-id="f1c19-127">Esses adaptadores dependem do software do sistema para transportar blocos de dados (anexados a pacotes de solicitação de e/s do sistema ou IRPs) entre buffers de aplicativo e buffers de hardware.</span><span class="sxs-lookup"><span data-stu-id="f1c19-127">These adapters rely on system software to transport blocks of data (attached to system I/O request packets, or IRPs) between application buffers and hardware buffers.</span></span> <span data-ttu-id="f1c19-128">Além disso, os dispositivos de áudio USB dependem do software do sistema para transportar dados entre buffers de aplicativo e buffers de hardware.</span><span class="sxs-lookup"><span data-stu-id="f1c19-128">In addition, USB audio devices rely on system software to transport data between application buffers and hardware buffers.</span></span> <span data-ttu-id="f1c19-129">Para melhorar o desempenho de aplicativos de modo exclusivo que se conectam a dispositivos de áudio que dependem do sistema para o transporte de dados, o WASAPI aumenta automaticamente a prioridade dos threads do sistema que transferem dados entre os aplicativos e o hardware.</span><span class="sxs-lookup"><span data-stu-id="f1c19-129">To improve the performance of exclusive-mode applications that connect to audio devices that rely on the system for data transport, WASAPI automatically increases the priority of the system threads that transfer data between the applications and the hardware.</span></span> <span data-ttu-id="f1c19-130">O WASAPI usa o MMCSS para aumentar a prioridade do thread.</span><span class="sxs-lookup"><span data-stu-id="f1c19-130">WASAPI uses MMCSS to increase the thread priority.</span></span> <span data-ttu-id="f1c19-131">No Windows Vista, se um thread do sistema gerencia o transporte de dados para um fluxo de reprodução de áudio de modo exclusivo com um formato PCM e um período de dispositivo inferior a 10 milissegundos, o WASAPI atribui o nome da tarefa do MMCSS "áudio pro" ao thread.</span><span class="sxs-lookup"><span data-stu-id="f1c19-131">In Windows Vista, if a system thread manages data transport for an exclusive-mode audio playback stream with a PCM format and a device period of less than 10 milliseconds, WASAPI assigns the MMCSS task name "Pro Audio" to the thread.</span></span> <span data-ttu-id="f1c19-132">Se o período do dispositivo do fluxo for maior ou igual a 10 milissegundos, o WASAPI atribuirá o nome da tarefa do MMCSS "áudio" ao thread.</span><span class="sxs-lookup"><span data-stu-id="f1c19-132">If the device period of the stream is greater than or equal to 10 milliseconds, WASAPI assigns the MMCSS task name "Audio" to the thread.</span></span> <span data-ttu-id="f1c19-133">Para obter mais informações sobre WaveCyclic, WavePci e WaveRT DDIs, consulte a documentação do Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="f1c19-133">For more information about the WaveCyclic, WavePci, and WaveRT DDIs, see the Windows DDK documentation.</span></span> <span data-ttu-id="f1c19-134">Para obter informações sobre como selecionar um período de dispositivo apropriado, consulte [**IAudioClient:: GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span><span class="sxs-lookup"><span data-stu-id="f1c19-134">For information about selecting an appropriate device period, see [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span></span>

<span data-ttu-id="f1c19-135">Conforme descrito em [controles de volume de sessão](session-volume-controls.md), o [WASAPI](wasapi.md) fornece as interfaces [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) para controlar os níveis de volume de fluxos de áudio de modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="f1c19-135">As described in [Session Volume Controls](session-volume-controls.md), [WASAPI](wasapi.md) provides the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces for controlling the volume levels of shared-mode audio streams.</span></span> <span data-ttu-id="f1c19-136">No entanto, os controles nessas interfaces não têm nenhum efeito em fluxos de modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-136">However, the controls in these interfaces have no effect on exclusive-mode streams.</span></span> <span data-ttu-id="f1c19-137">Em vez disso, os aplicativos que gerenciam fluxos de modo exclusivo normalmente usam a interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) na [API EndpointVolume](endpointvolume-api.md) para controlar os níveis de volume desses fluxos.</span><span class="sxs-lookup"><span data-stu-id="f1c19-137">Instead, applications that manage exclusive-mode streams typically use the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the [EndpointVolume API](endpointvolume-api.md) to control the volume levels of those streams.</span></span> <span data-ttu-id="f1c19-138">Para obter informações sobre essa interface, consulte [controles de volume do ponto de extremidade](endpoint-volume-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f1c19-138">For information about this interface, see [Endpoint Volume Controls](endpoint-volume-controls.md).</span></span>

<span data-ttu-id="f1c19-139">Para cada dispositivo de reprodução e dispositivo de captura no sistema, o usuário pode controlar se o dispositivo pode ser usado em modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-139">For each playback device and capture device in the system, the user can control whether the device can be used in exclusive mode.</span></span> <span data-ttu-id="f1c19-140">Se o usuário desabilitar o uso de modo exclusivo do dispositivo, o dispositivo poderá ser usado para reproduzir ou gravar somente fluxos de modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="f1c19-140">If the user disables exclusive-mode use of the device, the device can be used to play or record only shared-mode streams.</span></span>

<span data-ttu-id="f1c19-141">Se o usuário habilitar o uso de modo exclusivo do dispositivo, o usuário também poderá controlar se uma solicitação por um aplicativo para usar o dispositivo em modo exclusivo tomará a preempção do uso do dispositivo por aplicativos que podem estar atualmente em execução ou gravando fluxos de modo compartilhado por meio do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-141">If the user enables exclusive-mode use of the device, the user can also control whether a request by an application to use the device in exclusive mode will preempt the use of the device by applications that might currently be playing or recording shared-mode streams through the device.</span></span> <span data-ttu-id="f1c19-142">Se a preempção estiver habilitada, uma solicitação por um aplicativo para assumir o controle exclusivo do dispositivo terá êxito se o dispositivo não estiver em uso no momento ou se o dispositivo estiver sendo usado no modo compartilhado, mas a solicitação falhará se outro aplicativo já tiver controle exclusivo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-142">If preemption is enabled, a request by an application to take exclusive control of the device succeeds if the device is currently not in use, or if the device is being used in shared mode, but the request fails if another application already has exclusive control of the device.</span></span> <span data-ttu-id="f1c19-143">Se a preempção estiver desabilitada, uma solicitação por um aplicativo para assumir o controle exclusivo do dispositivo terá êxito se o dispositivo não estiver em uso no momento, mas a solicitação falhará se o dispositivo já estiver sendo usado no modo compartilhado ou em modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-143">If preemption is disabled, a request by an application to take exclusive control of the device succeeds if the device is not currently in use, but the request fails if the device is already being used either in shared mode or in exclusive mode.</span></span>

<span data-ttu-id="f1c19-144">No Windows Vista, as configurações padrão para um dispositivo de ponto de extremidade de áudio são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="f1c19-144">In Windows Vista, the default settings for an audio endpoint device are the following:</span></span>

-   <span data-ttu-id="f1c19-145">O dispositivo pode ser usado para reproduzir ou registrar fluxos de modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-145">The device can be used to play or record exclusive-mode streams.</span></span>
-   <span data-ttu-id="f1c19-146">Uma solicitação para usar um dispositivo para reproduzir ou gravar um fluxo de modo exclusivo preempção de qualquer fluxo de modo compartilhado que esteja sendo reproduzido ou registrado por meio do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-146">A request to use a device to play or record an exclusive-mode stream preempts any shared-mode stream that is currently being played or recorded through the device.</span></span>

<span data-ttu-id="f1c19-147">**Para alterar as configurações de modo exclusivo de um dispositivo de reprodução ou de gravação**</span><span class="sxs-lookup"><span data-stu-id="f1c19-147">**To change the exclusive-mode settings of a playback or recording device**</span></span>

1.  <span data-ttu-id="f1c19-148">Clique com o botão direito do mouse no ícone do orador na área de notificação, que está localizada no lado direito da barra de tarefas e selecione **dispositivos de reprodução** ou **dispositivos de gravação**.</span><span class="sxs-lookup"><span data-stu-id="f1c19-148">Right-click the speaker icon in the notification area, which is located on the right side of the taskbar, and select **Playback Devices** or **Recording Devices**.</span></span> <span data-ttu-id="f1c19-149">(Como alternativa, execute o painel de controle multimídia do Windows Mmsys.cpl, em uma janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="f1c19-149">(As an alternative, run the Windows multimedia control panel, Mmsys.cpl, from a Command Prompt window.</span></span> <span data-ttu-id="f1c19-150">Para obter mais informações, consulte comentários [nas \_ constantes do estado do dispositivo \_ xxx](device-state-xxx-constants.md).)</span><span class="sxs-lookup"><span data-stu-id="f1c19-150">For more information, see Remarks in [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).)</span></span>
2.  <span data-ttu-id="f1c19-151">Depois que a janela de **som** for exibida, selecione **reprodução** ou **gravação**.</span><span class="sxs-lookup"><span data-stu-id="f1c19-151">After the **Sound** window appears, select **Playback** or **Recording**.</span></span> <span data-ttu-id="f1c19-152">Em seguida, selecione uma entrada na lista de nomes de dispositivo e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="f1c19-152">Next, select an entry in the list of device names, and click **Properties**.</span></span>
3.  <span data-ttu-id="f1c19-153">Depois que a janela **Propriedades** for exibida, clique em **avançado**.</span><span class="sxs-lookup"><span data-stu-id="f1c19-153">After the **Properties** window appears, click **Advanced**.</span></span>
4.  <span data-ttu-id="f1c19-154">Para permitir que os aplicativos usem o dispositivo em modo exclusivo, marque a caixa rotulada **permitir que os aplicativos assumam o controle exclusivo desse dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="f1c19-154">To enable applications to use the device in exclusive mode, check the box labeled **Allow applications to take exclusive control of this device**.</span></span> <span data-ttu-id="f1c19-155">Para desabilitar o uso de modo exclusivo do dispositivo, desmarque a caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="f1c19-155">To disable exclusive-mode use of the device, clear the check box.</span></span>
5.  <span data-ttu-id="f1c19-156">Se o uso de modo exclusivo do dispositivo estiver habilitado, você poderá especificar se uma solicitação de controle exclusivo do dispositivo terá sucesso se o dispositivo estiver atualmente em execução ou gravando fluxos de modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="f1c19-156">If exclusive-mode use of the device is enabled, you can specify whether a request for exclusive control of the device will succeed if the device is currently playing or recording shared-mode streams.</span></span> <span data-ttu-id="f1c19-157">Para dar prioridade aos aplicativos de modo exclusivo sobre aplicativos de modo compartilhado, marque a caixa rotulada **fornecer prioridade de aplicativos em modo exclusivo**.</span><span class="sxs-lookup"><span data-stu-id="f1c19-157">To give exclusive-mode applications priority over shared-mode applications, check the box labeled **Give exclusive mode applications priority**.</span></span> <span data-ttu-id="f1c19-158">Para negar a prioridade de aplicativos de modo exclusivo em aplicativos de modo compartilhado, desmarque a caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="f1c19-158">To deny exclusive-mode applications priority over shared-mode applications, clear the check box.</span></span>

<span data-ttu-id="f1c19-159">O exemplo de código a seguir mostra como reproduzir um fluxo de áudio de baixa latência em um dispositivo de renderização de áudio configurado para uso no modo exclusivo:</span><span class="sxs-lookup"><span data-stu-id="f1c19-159">The following code example shows how to play a low-latency audio stream on an audio-rendering device that is configured for use in exclusive mode:</span></span>


```C++
//-----------------------------------------------------------
// Play an exclusive-mode stream on the default audio
// rendering device. The PlayExclusiveStream function uses
// event-driven buffering and MMCSS to play the stream at
// the minimum latency supported by the device.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayExclusiveStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = 0;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    HANDLE hEvent = NULL;
    HANDLE hTask = NULL;
    UINT32 bufferFrameCount;
    BYTE *pData;
    DWORD flags = 0;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    // Call a helper function to negotiate with the audio
    // device for an exclusive-mode stream format.
    hr = GetStreamFormat(pAudioClient, &pwfx);
    EXIT_ON_ERROR(hr)

    // Initialize the stream to play at the minimum latency.
    hr = pAudioClient->GetDevicePeriod(NULL, &hnsRequestedDuration);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_EXCLUSIVE,
                         AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
                         hnsRequestedDuration,
                         hnsRequestedDuration,
                         pwfx,
                         NULL);
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Create an event handle and register it for
    // buffer-event notifications.
    hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = E_FAIL;
        goto Exit;
    }

    hr = pAudioClient->SetEventHandle(hEvent);
    EXIT_ON_ERROR(hr);

    // Get the actual size of the two allocated buffers.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // To reduce latency, load the first buffer with data
    // from the audio source before starting the stream.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Ask MMCSS to temporarily boost the thread priority
    // to reduce glitches while the low-latency stream plays.
    DWORD taskIndex = 0;
    hTask = AvSetMmThreadCharacteristics(TEXT("Pro Audio"), &taskIndex);
    if (hTask == NULL)
    {
        hr = E_FAIL;
        EXIT_ON_ERROR(hr)
    }

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills one of the two buffers.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Wait for next buffer event to be signaled.
        DWORD retval = WaitForSingleObject(hEvent, 2000);
        if (retval != WAIT_OBJECT_0)
        {
            // Event handle timed out after a 2-second wait.
            pAudioClient->Stop();
            hr = ERROR_TIMEOUT;
            goto Exit;
        }

        // Grab the next empty buffer from the audio device.
        hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
        EXIT_ON_ERROR(hr)

        // Load the buffer with data from the audio source.
        hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for the last buffer to play before stopping.
    Sleep((DWORD)(hnsRequestedDuration/REFTIMES_PER_MILLISEC));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    if (hEvent != NULL)
    {
        CloseHandle(hEvent);
    }
    if (hTask != NULL)
    {
        AvRevertMmThreadCharacteristics(hTask);
    }
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



<span data-ttu-id="f1c19-160">No exemplo de código anterior, a função PlayExclusiveStream é executada no thread do aplicativo que Services armazena os buffers de ponto de extremidade enquanto um fluxo de renderização é reproduzido.</span><span class="sxs-lookup"><span data-stu-id="f1c19-160">In the preceding code example, the PlayExclusiveStream function runs in the application thread that services the endpoint buffers while a rendering stream is playing.</span></span> <span data-ttu-id="f1c19-161">A função usa um único parâmetro, pMySource, que é um ponteiro para um objeto que pertence a uma classe definida pelo cliente, myaudioname.</span><span class="sxs-lookup"><span data-stu-id="f1c19-161">The function takes a single parameter, pMySource, which is a pointer to an object that belongs to a client-defined class, MyAudioSource.</span></span> <span data-ttu-id="f1c19-162">Essa classe tem duas funções de membro, LoadData e SetFormat, que são chamadas no exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="f1c19-162">This class has two member functions, LoadData and SetFormat, that are called in the code example.</span></span> <span data-ttu-id="f1c19-163">Myaudioname é descrito na [renderização de um fluxo](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="f1c19-163">MyAudioSource is described in [Rendering a Stream](rendering-a-stream.md).</span></span>

<span data-ttu-id="f1c19-164">A função PlayExclusiveStream chama uma função auxiliar, GetStreamFormat, que negocia com o dispositivo de processamento padrão para determinar se o dispositivo dá suporte a um formato de fluxo de modo exclusivo que é adequado para uso pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-164">The PlayExclusiveStream function calls a helper function, GetStreamFormat, that negotiates with the default rendering device to determine whether the device supports an exclusive-mode stream format that is suitable for use by the application.</span></span> <span data-ttu-id="f1c19-165">O código para a função GetStreamFormat não aparece no exemplo de código; Isso ocorre porque os detalhes de sua implementação dependem inteiramente dos requisitos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-165">The code for the GetStreamFormat function does not appear in the code example; that is because the details of its implementation depend entirely on the requirements of the application.</span></span> <span data-ttu-id="f1c19-166">No entanto, a operação da função GetStreamFormat pode ser descrita simplesmente — chama o método [**IAudioClient:: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) uma ou mais vezes para determinar se o dispositivo dá suporte a um formato adequado.</span><span class="sxs-lookup"><span data-stu-id="f1c19-166">However, the operation of the GetStreamFormat function can be described simply—it calls the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method one or more times to determine whether the device supports a suitable format.</span></span> <span data-ttu-id="f1c19-167">Os requisitos do aplicativo ditam quais formatos o GetStreamFormat apresenta ao método **IsFormatSupported** e a ordem em que ele os apresenta.</span><span class="sxs-lookup"><span data-stu-id="f1c19-167">The requirements of the application dictate which formats GetStreamFormat presents to the **IsFormatSupported** method and the order in which it presents them.</span></span> <span data-ttu-id="f1c19-168">Para obter mais informações sobre **IsFormatSupported**, consulte [formatos de dispositivo](device-formats.md).</span><span class="sxs-lookup"><span data-stu-id="f1c19-168">For more information about **IsFormatSupported**, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="f1c19-169">Após a chamada GetStreamFormat, a função PlayExclusiveStream chama o método [**IAudioClient:: GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) para obter o período mínimo de dispositivos com suporte pelo hardware de áudio.</span><span class="sxs-lookup"><span data-stu-id="f1c19-169">After the GetStreamFormat call, the PlayExclusiveStream function calls the [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) method to obtain the minimum device period supported by the audio hardware.</span></span> <span data-ttu-id="f1c19-170">Em seguida, a função chama o método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) para solicitar uma duração de buffer igual ao período mínimo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-170">Next, the function calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method to request a buffer duration equal to the minimum period.</span></span> <span data-ttu-id="f1c19-171">Se a chamada for realizada com sucesso, o método **Initialize** alocará dois buffers de ponto de extremidade, cada um deles com duração igual ao período mínimo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-171">If the call succeeds, the **Initialize** method allocates two endpoint buffers, each of which is equal in duration to the minimum period.</span></span> <span data-ttu-id="f1c19-172">Posteriormente, quando o fluxo de áudio começar a ser executado, o hardware de aplicativo e de áudio compartilhará os dois buffers na maneira "pingue-pongue", ou seja, enquanto o aplicativo grava em um buffer, o hardware lê do outro buffer.</span><span class="sxs-lookup"><span data-stu-id="f1c19-172">Later, when the audio stream begins running, the application and audio hardware will share the two buffers in "ping-pong" fashion—that is, while the application writes to one buffer, the hardware reads from the other buffer.</span></span>

<span data-ttu-id="f1c19-173">Antes de iniciar o fluxo, a função PlayExclusiveStream faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f1c19-173">Before starting the stream, the PlayExclusiveStream function does the following:</span></span>

-   <span data-ttu-id="f1c19-174">Cria e registra o identificador de evento por meio do qual ele receberá notificações quando os buffers estiverem prontos para preenchimento.</span><span class="sxs-lookup"><span data-stu-id="f1c19-174">Creates and registers the event handle through which it will receive notifications when buffers become ready to fill.</span></span>
-   <span data-ttu-id="f1c19-175">Preenche o primeiro buffer com dados da fonte de áudio para reduzir o atraso de quando o fluxo começa a ser executado quando o som inicial é ouvido.</span><span class="sxs-lookup"><span data-stu-id="f1c19-175">Fills the first buffer with data from the audio source to reduce the delay from when the stream starts running to when the initial sound is heard.</span></span>
-   <span data-ttu-id="f1c19-176">Chama a função **AvSetMmThreadCharacteristics** para solicitar que o MMCSS aumente a prioridade do thread no qual o PlayExclusiveStream é executado.</span><span class="sxs-lookup"><span data-stu-id="f1c19-176">Calls the **AvSetMmThreadCharacteristics** function to request that MMCSS increase the priority of the thread in which PlayExclusiveStream executes.</span></span> <span data-ttu-id="f1c19-177">(Quando o fluxo para a execução, a chamada de função **AvRevertMmThreadCharacteristics** restaura a prioridade do thread original.)</span><span class="sxs-lookup"><span data-stu-id="f1c19-177">(When the stream stops running, the **AvRevertMmThreadCharacteristics** function call restores the original thread priority.)</span></span>

<span data-ttu-id="f1c19-178">Para obter mais informações sobre **AvSetMmThreadCharacteristics** e **AvRevertMmThreadCharacteristics**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="f1c19-178">For more information about **AvSetMmThreadCharacteristics** and **AvRevertMmThreadCharacteristics**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="f1c19-179">Enquanto o fluxo está em execução, cada iteração do loop **while** no exemplo de código anterior preenche um buffer de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f1c19-179">While the stream is running, each iteration of the **while**-loop in the preceding code example fills one endpoint buffer.</span></span> <span data-ttu-id="f1c19-180">Entre as iterações, a chamada de função **WaitForSingleObject** aguarda o identificador de evento ser sinalizado.</span><span class="sxs-lookup"><span data-stu-id="f1c19-180">Between iterations, the **WaitForSingleObject** function call waits for the event handle to be signaled.</span></span> <span data-ttu-id="f1c19-181">Quando o identificador é sinalizado, o corpo do loop faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f1c19-181">When the handle is signaled, the loop body does the following:</span></span>

1.  <span data-ttu-id="f1c19-182">Chama o método [**IAudioRenderClient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) para obter o próximo buffer.</span><span class="sxs-lookup"><span data-stu-id="f1c19-182">Calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method to get the next buffer.</span></span>
2.  <span data-ttu-id="f1c19-183">Preenche o buffer.</span><span class="sxs-lookup"><span data-stu-id="f1c19-183">Fills the buffer.</span></span>
3.  <span data-ttu-id="f1c19-184">Chama o método [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) para liberar o buffer.</span><span class="sxs-lookup"><span data-stu-id="f1c19-184">Calls the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method to release the buffer.</span></span>

<span data-ttu-id="f1c19-185">Para obter mais informações sobre o **WaitForSingleObject**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="f1c19-185">For more information about **WaitForSingleObject**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="f1c19-186">Se o adaptador de áudio for controlado por um driver WaveRT, a sinalização do identificador de evento será vinculada às notificações de transferência de DMA do hardware de áudio.</span><span class="sxs-lookup"><span data-stu-id="f1c19-186">If the audio adapter is controlled by a WaveRT driver, the signaling of the event handle is tied to the DMA-transfer notifications from the audio hardware.</span></span> <span data-ttu-id="f1c19-187">Para um dispositivo de áudio USB, ou para um dispositivo de áudio que é controlado por um driver WaveCyclic ou WavePci, a sinalização do identificador de evento é vinculada a conclusões do IRPs que transferem dados do buffer de aplicativo para o buffer de hardware.</span><span class="sxs-lookup"><span data-stu-id="f1c19-187">For a USB audio device, or for an audio device that is controlled by a WaveCyclic or WavePci driver, the signaling of the event handle is tied to completions of the IRPs that transfer data from the application buffer to the hardware buffer.</span></span>

<span data-ttu-id="f1c19-188">O exemplo de código anterior envia por push o hardware de áudio e o sistema de computador para seus limites de desempenho.</span><span class="sxs-lookup"><span data-stu-id="f1c19-188">The preceding code example pushes the audio hardware and the computer system to their performance limits.</span></span> <span data-ttu-id="f1c19-189">Primeiro, para reduzir a latência do fluxo, o aplicativo agenda seu thread de serviço de buffer para usar o período mínimo do dispositivo ao qual o hardware de áudio dará suporte.</span><span class="sxs-lookup"><span data-stu-id="f1c19-189">First, to reduce the stream latency, the application schedules its buffer-servicing thread to use the minimum device period that the audio hardware will support.</span></span> <span data-ttu-id="f1c19-190">Em segundo lugar, para garantir que o thread seja executado de forma confiável em cada período do dispositivo, a chamada de função **AvSetMmThreadCharacteristics** define o parâmetro TaskName como "Pro Audio", que é, no Windows Vista, o nome da tarefa padrão com a prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="f1c19-190">Second, to ensure that the thread reliably executes within each device period, the **AvSetMmThreadCharacteristics** function call sets the TaskName parameter to "Pro Audio", which is, in Windows Vista, the default task name with the highest priority.</span></span> <span data-ttu-id="f1c19-191">Considere se os requisitos de tempo de seu aplicativo podem ser relaxados sem comprometer sua utilidade.</span><span class="sxs-lookup"><span data-stu-id="f1c19-191">Consider whether the timing requirements of your application might be relaxed without compromising its usefulness.</span></span> <span data-ttu-id="f1c19-192">Por exemplo, o aplicativo pode agendar seu thread de serviço de buffer para usar um período maior que o mínimo.</span><span class="sxs-lookup"><span data-stu-id="f1c19-192">For example, the application might schedule its buffer-servicing thread to use a period that is longer than the minimum.</span></span> <span data-ttu-id="f1c19-193">Um período mais longo pode permitir com segurança o uso de uma prioridade de thread inferior.</span><span class="sxs-lookup"><span data-stu-id="f1c19-193">A longer period might safely allow the use of a lower thread priority.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1c19-194">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1c19-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1c19-195">Gerenciamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="f1c19-195">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 



