---
description: API EndpointVolume
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: API EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b827045250336aa499e386a8dafedb6ae068b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646412"
---
# <a name="endpointvolume-api"></a><span data-ttu-id="959d4-103">API EndpointVolume</span><span class="sxs-lookup"><span data-stu-id="959d4-103">EndpointVolume API</span></span>

<span data-ttu-id="959d4-104">A API EndpointVolume permite que clientes especializados controlem e monitorem os níveis de volume de [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="959d4-104">The EndpointVolume API enables specialized clients to control and monitor the volume levels of [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="959d4-105">Um cliente Obtém referências às interfaces na API EndpointVolume obtendo a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de um dispositivo de ponto de extremidade de áudio e chamando o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) .</span><span class="sxs-lookup"><span data-stu-id="959d4-105">A client obtains references to the interfaces in the EndpointVolume API by obtaining the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an audio endpoint device and calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method.</span></span>

<span data-ttu-id="959d4-106">O arquivo de cabeçalho Endpointvolume. h define as interfaces na API EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="959d4-106">Header file Endpointvolume.h defines the interfaces in the EndpointVolume API.</span></span>

<span data-ttu-id="959d4-107">Os aplicativos de áudio que usam a [API MMDevice](mmdevice-api.md) e [WASAPI](wasapi.md) normalmente usam a interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) para controlar os níveis de volume por sessão.</span><span class="sxs-lookup"><span data-stu-id="959d4-107">Audio applications that use the [MMDevice API](mmdevice-api.md) and [WASAPI](wasapi.md) typically use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interface to control volume levels on a per-session basis.</span></span> <span data-ttu-id="959d4-108">Somente dois tipos de aplicativos de áudio exigem o uso da API EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="959d4-108">Only two types of audio applications require the use of the EndpointVolume API.</span></span> <span data-ttu-id="959d4-109">Esses tipos de aplicativos são:</span><span class="sxs-lookup"><span data-stu-id="959d4-109">These application types are:</span></span>

-   <span data-ttu-id="959d4-110">Aplicativos que gerenciam os níveis de volume mestre de dispositivos de ponto de extremidade de áudio, semelhantes ao programa de controle de volume do Windows, Sndvol.exe.</span><span class="sxs-lookup"><span data-stu-id="959d4-110">Applications that manage the master volume levels of audio endpoint devices, similar to the Windows volume-control program, Sndvol.exe.</span></span>
-   <span data-ttu-id="959d4-111">Aplicativos de áudio profissional ("áudio pro") que exigem acesso de modo exclusivo a dispositivos de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="959d4-111">Professional audio ("pro audio") applications that require exclusive-mode access to audio endpoint devices.</span></span>

<span data-ttu-id="959d4-112">O uso inadequado da API EndpointVolume pode interferir na política de áudio do Windows e interromper as configurações de volume do sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="959d4-112">Inappropriate use of the EndpointVolume API can interfere with Windows audio policy and disrupt the user's system volume settings.</span></span>

<span data-ttu-id="959d4-113">Se um dispositivo de ponto de extremidade de áudio implementar o volume de hardware e os controles de mudo, a API do EndpointVolume usará esses controles para gerenciar o volume do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="959d4-113">If an audio endpoint device implements hardware volume and mute controls, the EndpointVolume API uses those controls to manage the device volume.</span></span> <span data-ttu-id="959d4-114">Caso contrário, a API EndpointVolume implementa os controles no software, de forma transparente para o cliente.</span><span class="sxs-lookup"><span data-stu-id="959d4-114">Otherwise, the EndpointVolume API implements the controls in software, transparently to the client.</span></span>

<span data-ttu-id="959d4-115">Se um dispositivo tiver controles de áudio e volume de hardware, as alterações feitas nas configurações de volume e áudio do dispositivo por meio da API EndpointVolume afetarão o nível de volume no modo compartilhado e no modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="959d4-115">If a device has hardware volume and mute controls, changes made to the device's volume and mute settings through the EndpointVolume API affect the volume level in both shared mode and exclusive mode.</span></span> <span data-ttu-id="959d4-116">Se um dispositivo não tiver controles de áudio e de volume de hardware, as alterações feitas no volume de software e nos controles de áudio por meio da API EndpointVolume afetarão o nível de volume no modo compartilhado, mas não no modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="959d4-116">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through the EndpointVolume API affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="959d4-117">No modo exclusivo, o cliente e o dispositivo trocam dados de áudio diretamente, ignorando os controles de software.</span><span class="sxs-lookup"><span data-stu-id="959d4-117">In exclusive mode, the client and the device exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="959d4-118">Para aplicativos que devem gerenciar o volume de hardware e os controles de mudo, a API do EndpointVolume oferece duas possíveis vantagens sobre a [API do DeviceTopology](devicetopology-api.md).</span><span class="sxs-lookup"><span data-stu-id="959d4-118">For applications that must manage hardware volume and mute controls, the EndpointVolume API offers two potential advantages over the [DeviceTopology API](devicetopology-api.md).</span></span>

<span data-ttu-id="959d4-119">Primeiro, um número de dispositivos de adaptador de áudio não tem controles de volume de hardware.</span><span class="sxs-lookup"><span data-stu-id="959d4-119">First, a number of audio adapter devices lack hardware volume controls.</span></span> <span data-ttu-id="959d4-120">Se um dispositivo não tem um controle de volume de hardware, a interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) na API EndpointVolume implementa automaticamente um controle de volume de software no fluxo para ou desse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="959d4-120">If a device lacks a hardware volume control, the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the EndpointVolume API automatically implements a software volume control on the stream to or from that device.</span></span> <span data-ttu-id="959d4-121">Para um cliente da API EndpointVolume, o resultado é o mesmo se o controle de volume for implementado no hardware pelo dispositivo ou no software pela interface de API do EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="959d4-121">For a client of the EndpointVolume API, the result is the same whether the volume control is implemented in hardware by the device or in software by the EndpointVolume API interface.</span></span>

<span data-ttu-id="959d4-122">Em segundo lugar, mesmo que o dispositivo adaptador implemente controles de volume de hardware, um aplicativo que usa a API DeviceTopology para implementar um algoritmo de passagem de topologia pode falhar ao localizar o controle que ele está procurando.</span><span class="sxs-lookup"><span data-stu-id="959d4-122">Second, even if the adapter device does implement hardware volume controls, an application that uses the DeviceTopology API to implement a topology-traversal algorithm might fail to find the control that it is looking for.</span></span> <span data-ttu-id="959d4-123">Normalmente, esse aplicativo é projetado para atravessar a topologia de hardware de um determinado dispositivo ou de um conjunto de dispositivos relacionados.</span><span class="sxs-lookup"><span data-stu-id="959d4-123">Typically, such an application is designed to traverse the hardware topology of a particular device or set of related devices.</span></span> <span data-ttu-id="959d4-124">Os riscos de aplicativo falham se tentar atravessar a topologia de um dispositivo que não foi especificamente projetado para o ou testado com o.</span><span class="sxs-lookup"><span data-stu-id="959d4-124">The application risks failing if it attempts to traverse the topology of a device that it has not been specifically designed for or tested with.</span></span>

<span data-ttu-id="959d4-125">Somente aplicativos especializados que devem acessar funções de hardware diferentes de controles de volume e sem áudio exigem o uso da API DeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="959d4-125">Only specialized applications that must access hardware functions other than volume and mute controls require the use of the DeviceTopology API.</span></span> <span data-ttu-id="959d4-126">Para aplicativos que exigem controle apenas do nível de volume de um fluxo de modo exclusivo, a API EndpointVolume é mais simples de usar e funciona de forma confiável com uma variedade maior de dispositivos de hardware de áudio.</span><span class="sxs-lookup"><span data-stu-id="959d4-126">For applications that require control only of the volume level of an exclusive-mode stream, the EndpointVolume API is simpler to use and works reliably with a wider range of audio hardware devices.</span></span>

<span data-ttu-id="959d4-127">Para obter exemplos de código que usam as interfaces na API EndpointVolume, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="959d4-127">For code examples that use the interfaces in the EndpointVolume API, see the following topics:</span></span>

-   [<span data-ttu-id="959d4-128">Controles de volume do ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="959d4-128">Endpoint Volume Controls</span></span>](endpoint-volume-controls.md)
-   [<span data-ttu-id="959d4-129">Medidores de pico</span><span class="sxs-lookup"><span data-stu-id="959d4-129">Peak Meters</span></span>](peak-meters.md)

<span data-ttu-id="959d4-130">Para ver um exemplo que usa a API EndpointVolume, consulte [EndpointVolume](endpointvolume.md) no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="959d4-130">To see a sample that uses the EndpointVolume API, see [EndpointVolume](endpointvolume.md) in the Windows SDK.</span></span>

<span data-ttu-id="959d4-131">A API EndpointVolume implementa as interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="959d4-131">The EndpointVolume API implements the following interfaces.</span></span>



| <span data-ttu-id="959d4-132">Interface</span><span class="sxs-lookup"><span data-stu-id="959d4-132">Interface</span></span>                                                | <span data-ttu-id="959d4-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="959d4-133">Description</span></span>                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="959d4-134">**IAudioEndpointVolume**</span><span class="sxs-lookup"><span data-stu-id="959d4-134">**IAudioEndpointVolume**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | <span data-ttu-id="959d4-135">Representa os controles de volume no fluxo de áudio de ou para um dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="959d4-135">Represents the volume controls on the audio stream to or from an audio endpoint device.</span></span> |
| [<span data-ttu-id="959d4-136">**IAudioMeterInformation**</span><span class="sxs-lookup"><span data-stu-id="959d4-136">**IAudioMeterInformation**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | <span data-ttu-id="959d4-137">Representa um medidor de pico no fluxo de áudio de ou para um dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="959d4-137">Represents a peak meter on the audio stream to or from an audio endpoint device.</span></span>        |



 

<span data-ttu-id="959d4-138">Além disso, os clientes da API EndpointVolume que exigem notificação de alterações de volume e de mudo em dispositivos de ponto de extremidade de áudio devem implementar a interface a seguir.</span><span class="sxs-lookup"><span data-stu-id="959d4-138">In addition, clients of the EndpointVolume API that require notification of volume and muting changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="959d4-139">Interface</span><span class="sxs-lookup"><span data-stu-id="959d4-139">Interface</span></span>                                                            | <span data-ttu-id="959d4-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="959d4-140">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="959d4-141">**IAudioEndpointVolumeCallback**</span><span class="sxs-lookup"><span data-stu-id="959d4-141">**IAudioEndpointVolumeCallback**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | <span data-ttu-id="959d4-142">Fornece notificações quando o nível de volume ou estado de mudo de um dispositivo de ponto de extremidade de áudio é alterado.</span><span class="sxs-lookup"><span data-stu-id="959d4-142">Provides notifications when the volume level or muting state of an audio endpoint device changes.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="959d4-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="959d4-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="959d4-144">Controles de volume</span><span class="sxs-lookup"><span data-stu-id="959d4-144">Volume Controls</span></span>](volume-controls.md)
</dt> <dt>

[<span data-ttu-id="959d4-145">**Interface IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="959d4-145">**IMMDevice Interface**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[<span data-ttu-id="959d4-146">**IMMDevice:: ativar**</span><span class="sxs-lookup"><span data-stu-id="959d4-146">**IMMDevice::Activate**</span></span>](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[<span data-ttu-id="959d4-147">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="959d4-147">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[<span data-ttu-id="959d4-148">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="959d4-148">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



