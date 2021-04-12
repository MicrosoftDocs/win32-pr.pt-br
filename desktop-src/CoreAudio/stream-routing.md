---
description: O roteamento de fluxo é a capacidade de um aplicativo de mídia alternar fluxos entre dispositivos com interrupção mínima para a sessão de reprodução ou de captura.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Roteamento de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b21cd15a4467cb9b08747119aab999882ae3b5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457060"
---
# <a name="stream-routing"></a><span data-ttu-id="fc463-103">Roteamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="fc463-103">Stream Routing</span></span>

<span data-ttu-id="fc463-104">O *Roteamento de fluxo* é a capacidade de um aplicativo de mídia alternar fluxos entre dispositivos com interrupção mínima para a sessão de reprodução ou de captura.</span><span class="sxs-lookup"><span data-stu-id="fc463-104">*Stream routing* is the ability of a media application to switch streams between devices with minimal interruption to the playback or the capture session.</span></span>

<span data-ttu-id="fc463-105">Um computador pode ter vários dispositivos de renderização e captura.</span><span class="sxs-lookup"><span data-stu-id="fc463-105">A computer can have multiple rendering and capture devices.</span></span> <span data-ttu-id="fc463-106">O sistema lista esses dispositivos no painel de controle **sons** .</span><span class="sxs-lookup"><span data-stu-id="fc463-106">The system lists these devices on the **Sounds** control panel.</span></span> <span data-ttu-id="fc463-107">Nessa lista, um usuário pode definir um dispositivo para ser o dispositivo padrão para cada função: reprodução, gravação ou as quatro funções de comunicação (renderização do console, captura do console, renderização de comunicação ou captura de comunicação).</span><span class="sxs-lookup"><span data-stu-id="fc463-107">From this list, a user can set a device to be the default device for each role: playback, recording, or the four communications roles (console render, console capture, communication render, or communication capture).</span></span> <span data-ttu-id="fc463-108">A lista de dispositivos pode ser modificada dinamicamente, pois alguns desses dispositivos podem estar disponíveis temporariamente, por exemplo, um headset USB.</span><span class="sxs-lookup"><span data-stu-id="fc463-108">The list of devices may be modified dynamically as some of these devices can be available temporarily, for example a USB headset.</span></span> <span data-ttu-id="fc463-109">Quando vários dispositivos estão disponíveis, o usuário pode alterar o padrão para um dispositivo diferente.</span><span class="sxs-lookup"><span data-stu-id="fc463-109">When multiple devices are available, the user can change the default to a different device.</span></span> <span data-ttu-id="fc463-110">O usuário também pode alterar o formato de um dispositivo (taxa de exemplo, bits por amostra e assim por diante) na guia **avançado** para as propriedades do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc463-110">The user can also change the format of a device (sample rate, bits per sample, and so on) on the **Advanced** tab for the device properties.</span></span>

<span data-ttu-id="fc463-111">Considere um cenário no qual um usuário seleciona os **alto-falantes** como o dispositivo padrão para renderizar fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="fc463-111">Consider a scenario in which a user selects **Speakers** as the default device for rendering audio streams.</span></span> <span data-ttu-id="fc463-112">Em seguida, o usuário conecta um headset USB, seleciona o headset como o novo dispositivo padrão e altera a taxa de amostra do dispositivo de 44,1 kHz para 48 kHz.</span><span class="sxs-lookup"><span data-stu-id="fc463-112">The user then connects a USB headset, selects the headset as the new default device, and changes the sample rate of the device from 44.1 kHz to 48 kHz.</span></span> <span data-ttu-id="fc463-113">O usuário deseja reproduzir o fluxo de áudio no headset na nova taxa de amostra com interrupção mínima para a sessão de streaming.</span><span class="sxs-lookup"><span data-stu-id="fc463-113">The user wants to play the audio stream on the headset at the new sample rate with minimal interruption to the streaming session.</span></span>

<span data-ttu-id="fc463-114">Nesse cenário, há dois casos que o aplicativo de mídia deve manipular:</span><span class="sxs-lookup"><span data-stu-id="fc463-114">In this scenario, there are two cases that the media application must handle:</span></span>

-   <span data-ttu-id="fc463-115">O fluxo deve ser transferido para o novo dispositivo padrão com interrupção mínima para reprodução.</span><span class="sxs-lookup"><span data-stu-id="fc463-115">The stream must be transferred to the new default device with minimal interruption to playback.</span></span>
-   <span data-ttu-id="fc463-116">O novo dispositivo deve retomar a reprodução no novo formato (ou seja, o usuário pode alterar mais do que a taxa de amostra).</span><span class="sxs-lookup"><span data-stu-id="fc463-116">The new device must resume playback in the new format (that is, the user can change more than the sample rate).</span></span>

<span data-ttu-id="fc463-117">No Windows Vista, para dar suporte a esse cenário, o aplicativo de mídia tinha que fornecer a implementação para o roteamento de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fc463-117">In Windows Vista, to support this scenario, the media application had to provide the implementation for stream routing.</span></span> <span data-ttu-id="fc463-118">O aplicativo foi responsável por encerrar os fluxos existentes e reiniciar os fluxos no novo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc463-118">The application was responsible for terminating existing streams and restarting the streams on the new device.</span></span> <span data-ttu-id="fc463-119">Se o usuário alterou o dispositivo padrão ou seu formato Mix foi alterado, todas as sessões associadas foram fechadas e o aplicativo tinha que lidar com a recuperação.</span><span class="sxs-lookup"><span data-stu-id="fc463-119">If the user changed the default device or its mix format changed, then all of the associated sessions were closed and the application had to handle the recovery.</span></span>

<span data-ttu-id="fc463-120">No Windows 7, um aplicativo pode transferir diretamente um fluxo de um dispositivo padrão existente para um novo ponto de extremidade de áudio padrão.</span><span class="sxs-lookup"><span data-stu-id="fc463-120">In Windows 7, an application can seamlessly transfer a stream from an existing default device to a new default audio endpoint.</span></span> <span data-ttu-id="fc463-121">Os conjuntos de API de áudio de alto nível, como as APIs Media Foundation, DirectSound e WAVE, implementam o recurso de roteamento de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fc463-121">High-level audio API sets such as Media Foundation, DirectSound, and WAVE APIs implement the stream routing feature.</span></span> <span data-ttu-id="fc463-122">Os aplicativos de mídia que usam esses conjuntos de API para reproduzir ou capturar um fluxo do dispositivo padrão usam a implementação padrão e não precisarão modificar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc463-122">Media applications that use these API sets to play or capture a stream from the default device use the default implementation and will not have to modify the application.</span></span> <span data-ttu-id="fc463-123">No entanto, se seu aplicativo de mídia usar MMDeviceAPI ou WASAPI diretamente, o aplicativo precisará fornecer a implementação de roteamento de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fc463-123">However, if your media application uses MMDeviceAPI or WASAPI directly, the application needs to provide the stream routing implementation.</span></span>

> [!Note]  
> <span data-ttu-id="fc463-124">MMDeviceAPI e WASAPI são componentes principais de API de áudio que um aplicativo pode usar para renderizar ou capturar um fluxo em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc463-124">MMDeviceAPI and WASAPI are Core Audio API components that an application can use to render or capture a stream on a device.</span></span> <span data-ttu-id="fc463-125">O MMDeviceAPI descobre o novo dispositivo de ponto de extremidade de áudio e o WASAPI gerencia o fluxo de dados de áudio entre um aplicativo de mídia e o dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="fc463-125">The MMDeviceAPI discovers the new audio endpoint device, and WASAPI manages the flow of audio data between a media application and the audio endpoint device.</span></span>

 

<span data-ttu-id="fc463-126">Para implementar o recurso de roteamento de fluxo, o aplicativo deve escutar as notificações enviadas por MMDeviceAPI e WASAPI quando:</span><span class="sxs-lookup"><span data-stu-id="fc463-126">To implement the stream routing feature, the application must listen for the notifications sent by MMDeviceAPI and WASAPI when:</span></span>

-   <span data-ttu-id="fc463-127">O dispositivo padrão é alterado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="fc463-127">The default device is changed by the user.</span></span>
-   <span data-ttu-id="fc463-128">O dispositivo padrão existente é removido e um novo dispositivo padrão é adicionado.</span><span class="sxs-lookup"><span data-stu-id="fc463-128">The existing default device is removed and a new default device is added.</span></span>
-   <span data-ttu-id="fc463-129">O formato do dispositivo é alterado.</span><span class="sxs-lookup"><span data-stu-id="fc463-129">The device format is changed.</span></span>

<span data-ttu-id="fc463-130">Ao lidar com essas notificações, um aplicativo pode executar as operações de gerenciamento de fluxo necessárias ao transferir o fluxo para o novo dispositivo padrão.</span><span class="sxs-lookup"><span data-stu-id="fc463-130">By handling these notifications, an application can perform the necessary stream management operations while transferring the stream to the new default device.</span></span> <span data-ttu-id="fc463-131">Além disso, o aplicativo pode renderizar ou capturar fluxos existentes usando o novo formato especificado pelo usuário enquanto uma sessão de renderização está ativa.</span><span class="sxs-lookup"><span data-stu-id="fc463-131">In addition, the application can render or capture existing streams by using the new format specified by the user while a rendering session is active.</span></span>

<span data-ttu-id="fc463-132">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="fc463-132">This section contains the following topics:</span></span>

-   [<span data-ttu-id="fc463-133">Obtendo o ponto de extremidade do dispositivo para roteamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="fc463-133">Getting the Device Endpoint for Stream Routing</span></span>](getting-the-default-device-endpoint-for-stream-routing.md)
-   [<span data-ttu-id="fc463-134">Notificações relevantes para roteamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="fc463-134">Relevant Notifications for Stream Routing</span></span>](relevant-device-notifications-for-stream-routing.md)
-   [<span data-ttu-id="fc463-135">Considerações de implementação de roteamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="fc463-135">Stream Routing Implementation Considerations</span></span>](stream-routing-implementation-considerations.md)

<span data-ttu-id="fc463-136">Os exemplos a seguir, incluídos no SDK do Windows, demonstram como um aplicativo pode lidar com notificações de roteamento de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fc463-136">The following samples, included in the Windows SDK, demonstrate how an application can handle stream routing notifications.</span></span>

-   [<span data-ttu-id="fc463-137">RenderSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="fc463-137">RenderSharedTimerDriven</span></span>](rendersharedtimerdriven.md)
-   [<span data-ttu-id="fc463-138">RenderSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="fc463-138">RenderSharedEventDriven</span></span>](rendersharedeventdriven.md)
-   [<span data-ttu-id="fc463-139">RenderExclusiveTimerDriven</span><span class="sxs-lookup"><span data-stu-id="fc463-139">RenderExclusiveTimerDriven</span></span>](renderexclusivetimerdriven.md)
-   [<span data-ttu-id="fc463-140">RenderExclusiveEventDriven</span><span class="sxs-lookup"><span data-stu-id="fc463-140">RenderExclusiveEventDriven</span></span>](renderexclusiveeventdriven.md)
-   [<span data-ttu-id="fc463-141">CaptureSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="fc463-141">CaptureSharedTimerDriven</span></span>](capturesharedtimerdriven.md)
-   [<span data-ttu-id="fc463-142">CaptureSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="fc463-142">CaptureSharedEventDriven</span></span>](capturesharedeventdriven.md)

## <a name="related-topics"></a><span data-ttu-id="fc463-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc463-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc463-144">Gerenciamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="fc463-144">Stream Management</span></span>](stream-management.md)
</dt> <dt>

[<span data-ttu-id="fc463-145">Sobre a API do MMDevice</span><span class="sxs-lookup"><span data-stu-id="fc463-145">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="fc463-146">Sobre o WASAPI</span><span class="sxs-lookup"><span data-stu-id="fc463-146">About WASAPI</span></span>](wasapi.md)
</dt> </dl>

 

 



