---
description: Gerenciamento de fluxo
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: Gerenciamento de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07180d8b46f4d079c08f4b619cf4a7773a6104d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089321"
---
# <a name="stream-management"></a><span data-ttu-id="f7248-103">Gerenciamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="f7248-103">Stream Management</span></span>

<span data-ttu-id="f7248-104">Depois de enumerar os [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md) no sistema e identificar um dispositivo de processamento ou de captura adequado, a próxima tarefa para um aplicativo cliente de áudio é abrir uma conexão com o dispositivo de ponto de extremidade e gerenciar o fluxo de dados de áudio nessa conexão.</span><span class="sxs-lookup"><span data-stu-id="f7248-104">After enumerating the [audio endpoint devices](audio-endpoint-devices.md) in the system and identifying a suitable rendering or capture device, the next task for an audio client application is to open a connection with the endpoint device and to manage the flow of audio data over that connection.</span></span> <span data-ttu-id="f7248-105">O [WASAPI](wasapi.md) permite que os clientes criem e gerenciem fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="f7248-105">[WASAPI](wasapi.md) enables clients to create and manage audio streams.</span></span>

<span data-ttu-id="f7248-106">O WASAPI implementa várias interfaces para fornecer serviços de gerenciamento de fluxo para clientes de áudio.</span><span class="sxs-lookup"><span data-stu-id="f7248-106">WASAPI implements several interfaces to provide stream-management services to audio clients.</span></span> <span data-ttu-id="f7248-107">A interface principal é [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient).</span><span class="sxs-lookup"><span data-stu-id="f7248-107">The primary interface is [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient).</span></span> <span data-ttu-id="f7248-108">Um cliente obtém a interface **IAudioClient** para um dispositivo de ponto de extremidade de áudio chamando o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (com o parâmetro *IID* definido como **REFIID** IID \_ IAudioClient) no objeto de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f7248-108">A client obtains the **IAudioClient** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioClient) on the endpoint object.</span></span>

<span data-ttu-id="f7248-109">O cliente chama os métodos na interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f7248-109">The client calls the methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to do the following:</span></span>

-   <span data-ttu-id="f7248-110">Descobrir quais formatos de áudio o dispositivo de ponto de extremidade dá suporte.</span><span class="sxs-lookup"><span data-stu-id="f7248-110">Discover which audio formats the endpoint device supports.</span></span>
-   <span data-ttu-id="f7248-111">Obter o tamanho do buffer do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f7248-111">Get the endpoint buffer size.</span></span>
-   <span data-ttu-id="f7248-112">Obtenha o formato e a latência do fluxo.</span><span class="sxs-lookup"><span data-stu-id="f7248-112">Get the stream format and latency.</span></span>
-   <span data-ttu-id="f7248-113">Inicie, pare e redefina o fluxo que flui por meio do dispositivo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f7248-113">Start, stop, and reset the stream that flows through the endpoint device.</span></span>
-   <span data-ttu-id="f7248-114">Acessar serviços de áudio adicionais.</span><span class="sxs-lookup"><span data-stu-id="f7248-114">Access additional audio services.</span></span>

<span data-ttu-id="f7248-115">Para criar um fluxo, um cliente chama o método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="f7248-115">To create a stream, a client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="f7248-116">Por meio desse método, o cliente especifica o formato de dados para o fluxo, o tamanho do buffer de ponto de extremidade e se o fluxo opera no modo compartilhado ou exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f7248-116">Through this method, the client specifies the data format for the stream, the size of the endpoint buffer, and whether the stream operates in shared or exclusive mode.</span></span>

<span data-ttu-id="f7248-117">Os métodos restantes na interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) se enquadram em dois grupos:</span><span class="sxs-lookup"><span data-stu-id="f7248-117">The remaining methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface fall into two groups:</span></span>

-   <span data-ttu-id="f7248-118">Métodos que podem ser chamados somente após o fluxo ter sido aberto por [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="f7248-118">Methods that can be called only after the stream has been opened by [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="f7248-119">Métodos que podem ser chamados a qualquer momento antes ou depois da chamada de [**inicialização**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="f7248-119">Methods that can be called at any time before or after the [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call.</span></span>

<span data-ttu-id="f7248-120">Os métodos a seguir podem ser chamados somente após a chamada para [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):</span><span class="sxs-lookup"><span data-stu-id="f7248-120">The following methods can be called only after the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):</span></span>

-   [<span data-ttu-id="f7248-121">**IAudioClient:: getbuffersize**</span><span class="sxs-lookup"><span data-stu-id="f7248-121">**IAudioClient::GetBufferSize**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [<span data-ttu-id="f7248-122">**IAudioClient::GetCurrentPadding**</span><span class="sxs-lookup"><span data-stu-id="f7248-122">**IAudioClient::GetCurrentPadding**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [<span data-ttu-id="f7248-123">**IAudioClient:: GetService**</span><span class="sxs-lookup"><span data-stu-id="f7248-123">**IAudioClient::GetService**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [<span data-ttu-id="f7248-124">**IAudioClient::GetStreamLatency**</span><span class="sxs-lookup"><span data-stu-id="f7248-124">**IAudioClient::GetStreamLatency**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [<span data-ttu-id="f7248-125">**IAudioClient:: Reset**</span><span class="sxs-lookup"><span data-stu-id="f7248-125">**IAudioClient::Reset**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [<span data-ttu-id="f7248-126">**IAudioClient:: iniciar**</span><span class="sxs-lookup"><span data-stu-id="f7248-126">**IAudioClient::Start**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [<span data-ttu-id="f7248-127">**IAudioClient:: Stop**</span><span class="sxs-lookup"><span data-stu-id="f7248-127">**IAudioClient::Stop**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

<span data-ttu-id="f7248-128">Os métodos a seguir podem ser chamados antes ou depois da chamada [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) :</span><span class="sxs-lookup"><span data-stu-id="f7248-128">The following methods can be called before or after the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call:</span></span>

-   [<span data-ttu-id="f7248-129">**IAudioClient::GetDevicePeriod**</span><span class="sxs-lookup"><span data-stu-id="f7248-129">**IAudioClient::GetDevicePeriod**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [<span data-ttu-id="f7248-130">**IAudioClient::GetMixFormat**</span><span class="sxs-lookup"><span data-stu-id="f7248-130">**IAudioClient::GetMixFormat**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [<span data-ttu-id="f7248-131">**IAudioClient::IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="f7248-131">**IAudioClient::IsFormatSupported**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

<span data-ttu-id="f7248-132">Para acessar os serviços adicionais de cliente de áudio, o cliente chama o método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="f7248-132">To access the additional audio client services, the client calls the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="f7248-133">Por meio desse método, o cliente pode obter referências às seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="f7248-133">Through this method, the client can obtain references to the following interfaces:</span></span>

-   [<span data-ttu-id="f7248-134">**IAudioRenderClient**</span><span class="sxs-lookup"><span data-stu-id="f7248-134">**IAudioRenderClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    <span data-ttu-id="f7248-135">Grava dados de renderização em um buffer de ponto de extremidade de renderização de áudio.</span><span class="sxs-lookup"><span data-stu-id="f7248-135">Writes rendering data to an audio-rendering endpoint buffer.</span></span>

-   [<span data-ttu-id="f7248-136">**IAudioCaptureClient**</span><span class="sxs-lookup"><span data-stu-id="f7248-136">**IAudioCaptureClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    <span data-ttu-id="f7248-137">Lê dados capturados de um buffer de ponto de extremidade de captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="f7248-137">Reads captured data from an audio-capture endpoint buffer.</span></span>

-   [<span data-ttu-id="f7248-138">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="f7248-138">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    <span data-ttu-id="f7248-139">Comunica-se com o Gerenciador de sessão de áudio para configurar e gerenciar a sessão de áudio associada ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="f7248-139">Communicates with the audio session manager to configure and manage the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="f7248-140">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="f7248-140">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    <span data-ttu-id="f7248-141">Controla o nível de volume da sessão de áudio que está associada ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="f7248-141">Controls the volume level of the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="f7248-142">**IChannelAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="f7248-142">**IChannelAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    <span data-ttu-id="f7248-143">Controla os níveis de volume dos canais individuais na sessão de áudio que está associada ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="f7248-143">Controls the volume levels of the individual channels in the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="f7248-144">**IAudioClock**</span><span class="sxs-lookup"><span data-stu-id="f7248-144">**IAudioClock**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    <span data-ttu-id="f7248-145">Monitora a taxa de dados de fluxo e a posição do fluxo.</span><span class="sxs-lookup"><span data-stu-id="f7248-145">Monitors the stream data rate and stream position.</span></span>

<span data-ttu-id="f7248-146">Além disso, os clientes do WASAPI que exigem a notificação de eventos relacionados à sessão devem implementar a seguinte interface:</span><span class="sxs-lookup"><span data-stu-id="f7248-146">In addition, WASAPI clients that require notification of session-related events should implement the following interface:</span></span>

-   [<span data-ttu-id="f7248-147">**IAudioSessionEvents**</span><span class="sxs-lookup"><span data-stu-id="f7248-147">**IAudioSessionEvents**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    <span data-ttu-id="f7248-148">Para receber notificações de eventos, o cliente passa um ponteiro para sua interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para o método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) como um parâmetro de chamada.</span><span class="sxs-lookup"><span data-stu-id="f7248-148">To receive event notifications, the client passes a pointer to its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method as a call parameter.</span></span>

<span data-ttu-id="f7248-149">Por fim, um cliente pode usar uma API de nível superior para criar um fluxo de áudio, mas também exigir acesso aos controles de sessão e controles de volume para a sessão que contém o fluxo.</span><span class="sxs-lookup"><span data-stu-id="f7248-149">Finally, a client might use a higher-level API to create an audio stream, but also require access to the session controls and volume controls for the session that contains the stream.</span></span> <span data-ttu-id="f7248-150">Uma API de nível superior normalmente não fornece esse acesso.</span><span class="sxs-lookup"><span data-stu-id="f7248-150">A higher-level API typically does not provide this access.</span></span> <span data-ttu-id="f7248-151">O cliente pode obter os controles para uma sessão específica por meio da interface [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) .</span><span class="sxs-lookup"><span data-stu-id="f7248-151">The client can obtain the controls for a particular session through the [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface.</span></span> <span data-ttu-id="f7248-152">Essa interface permite que o cliente obtenha as interfaces [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) e [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) para uma sessão sem exigir que o cliente use a interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) para criar um fluxo e atribuir o fluxo à sessão.</span><span class="sxs-lookup"><span data-stu-id="f7248-152">This interface enables the client to obtain the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) and [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interfaces for a session without requiring the client to use the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to create a stream and to assign the stream to the session.</span></span> <span data-ttu-id="f7248-153">Um cliente obtém a interface **IAudioSessionManager** para um dispositivo de ponto de extremidade de áudio chamando o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (com o parâmetro *IID* definido como **REFIID** IID \_ IAudioSessionManager) no objeto de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f7248-153">A client obtains the **IAudioSessionManager** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioSessionManager) on the endpoint object.</span></span>

<span data-ttu-id="f7248-154">As interfaces [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)e [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) são definidas no arquivo de cabeçalho Audiopolicy. h.</span><span class="sxs-lookup"><span data-stu-id="f7248-154">The [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents), and [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interfaces are defined in header file Audiopolicy.h.</span></span> <span data-ttu-id="f7248-155">Todas as outras interfaces WASAPI são definidas no arquivo de cabeçalho Audioclient. h.</span><span class="sxs-lookup"><span data-stu-id="f7248-155">All other WASAPI interfaces are defined in header file Audioclient.h.</span></span>

<span data-ttu-id="f7248-156">As seções a seguir descrevem como usar o WASAPI para gerenciar fluxos de áudio:</span><span class="sxs-lookup"><span data-stu-id="f7248-156">The following sections describe how to use WASAPI to manage audio streams:</span></span>

-   [<span data-ttu-id="f7248-157">Sobre o WASAPI</span><span class="sxs-lookup"><span data-stu-id="f7248-157">About WASAPI</span></span>](wasapi.md)
-   [<span data-ttu-id="f7248-158">Renderizando um fluxo</span><span class="sxs-lookup"><span data-stu-id="f7248-158">Rendering a Stream</span></span>](rendering-a-stream.md)
-   [<span data-ttu-id="f7248-159">Capturando um fluxo</span><span class="sxs-lookup"><span data-stu-id="f7248-159">Capturing a Stream</span></span>](capturing-a-stream.md)
-   [<span data-ttu-id="f7248-160">Gravação de loopback</span><span class="sxs-lookup"><span data-stu-id="f7248-160">Loopback Recording</span></span>](loopback-recording.md)
-   [<span data-ttu-id="f7248-161">Fluxos de modo exclusivo</span><span class="sxs-lookup"><span data-stu-id="f7248-161">Exclusive-Mode Streams</span></span>](exclusive-mode-streams.md)
-   [<span data-ttu-id="f7248-162">Recuperando de um erro de Invalid-Device</span><span class="sxs-lookup"><span data-stu-id="f7248-162">Recovering from an Invalid-Device Error</span></span>](recovering-from-an-invalid-device-error.md)
-   [<span data-ttu-id="f7248-163">Usando um dispositivo de comunicação</span><span class="sxs-lookup"><span data-stu-id="f7248-163">Using a Communication Device</span></span>](using-the-communication-device.md)
-   [<span data-ttu-id="f7248-164">Roteamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="f7248-164">Stream Routing</span></span>](stream-routing.md)

## <a name="related-topics"></a><span data-ttu-id="f7248-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7248-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7248-166">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="f7248-166">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



