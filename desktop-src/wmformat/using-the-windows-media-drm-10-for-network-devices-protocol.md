---
title: Usando o protocolo Windows Media DRM 10 para dispositivos de rede
description: Usando o protocolo Windows Media DRM 10 para dispositivos de rede
ms.assetid: dec88d72-718c-42ab-8d48-eddf906051ef
keywords:
- SDK do Windows Media Format, Windows Media DRM 10 para dispositivos de rede
- SDK do Windows Media Format, DRM 10 para dispositivos de rede
- ASF (Advanced Systems Format), Windows Media DRM 10 para dispositivos de rede
- ASF (formato de sistemas avançados), Windows Media DRM 10 para dispositivos de rede
- Formato de sistema avançado (ASF), DRM 10 para dispositivos de rede
- Formato ASF 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), Windows Media DRM 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), Windows Media DRM 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), DRM 10 para dispositivos de rede
- DRM (gerenciamento de direitos digitais), DRM 10 para dispositivos de rede
- Windows Media DRM 10 para dispositivos de rede, protocolos
- DRM 10 para dispositivos de rede, protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73908c66dbffe7f50f4f28beb520861611d59962
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292112"
---
# <a name="using-the-windows-media-drm-10-for-network-devices-protocol"></a><span data-ttu-id="8699e-115">Usando o protocolo Windows Media DRM 10 para dispositivos de rede</span><span class="sxs-lookup"><span data-stu-id="8699e-115">Using the Windows Media DRM 10 for Network Devices Protocol</span></span>

<span data-ttu-id="8699e-116">O Windows Media Format SDK fornece alguns recursos para dar suporte ao protocolo de dispositivo de rede seguro, Windows Media DRM 10 para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="8699e-116">The Windows Media Format SDK provides some features to support the secure network device protocol, Windows Media DRM 10 for Network Devices.</span></span> <span data-ttu-id="8699e-117">Esse protocolo define as mensagens enviadas entre um dispositivo de reprodução de mídia digital, como um player de vídeo de conjunto superior e o computador que atende aos dados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8699e-117">This protocol defines the messages sent between a digital media playback device, such as a set-top video player, and the computer that serves data to the device.</span></span> <span data-ttu-id="8699e-118">Os dados de mídia enviados entre o servidor e o dispositivo são criptografados para protegê-lo da interceptação.</span><span class="sxs-lookup"><span data-stu-id="8699e-118">The media data sent between server and device is encrypted to protect it from interception.</span></span>

<span data-ttu-id="8699e-119">A comunicação entre o aplicativo e os dispositivos que dão suporte ao Windows Media DRM 10 para dispositivos de rede pode usar quaisquer protocolos de rede que você preferir.</span><span class="sxs-lookup"><span data-stu-id="8699e-119">The communication between your application and devices that support Windows Media DRM 10 for Network Devices can use whatever networking protocols you prefer.</span></span> <span data-ttu-id="8699e-120">O Windows Media Format SDK não fornece nenhum objeto que execute as comunicações de rede para você.</span><span class="sxs-lookup"><span data-stu-id="8699e-120">The Windows Media Format SDK does not provide any objects that perform the network communications for you.</span></span> <span data-ttu-id="8699e-121">Em vez disso, os objetos desse SDK processam algumas mensagens do Windows Media DRM 10 para dispositivos de rede depois que seu aplicativo as recebeu.</span><span class="sxs-lookup"><span data-stu-id="8699e-121">Instead, the objects of this SDK process some Windows Media DRM 10 for Network Devices messages after your application has received them.</span></span>

<span data-ttu-id="8699e-122">Os recursos que dão suporte ao Windows Media DRM 10 para dispositivos de rede são o registro de dispositivo, a detecção de proximidade e a conversão de arquivos protegidos por DRM.</span><span class="sxs-lookup"><span data-stu-id="8699e-122">The features that support Windows Media DRM 10 for Network Devices are device registration, proximity detection, and converting DRM-protected files.</span></span> <span data-ttu-id="8699e-123">Esses recursos são descritos nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="8699e-123">These features are described in the following sections.</span></span>



| <span data-ttu-id="8699e-124">Seção</span><span class="sxs-lookup"><span data-stu-id="8699e-124">Section</span></span>                                                                                                                                                                          | <span data-ttu-id="8699e-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="8699e-125">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8699e-126">Registro de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8699e-126">Device Registration</span></span>](device-registration.md)                                                                                                                                   | <span data-ttu-id="8699e-127">Descreve como processar mensagens de solicitação de registro de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8699e-127">Describes how to process registration request messages from devices.</span></span>                                                                       |
| [<span data-ttu-id="8699e-128">Executando detecção de proximidade</span><span class="sxs-lookup"><span data-stu-id="8699e-128">Performing Proximity Detection</span></span>](performing-proximity-detection.md)                                                                                                             | <span data-ttu-id="8699e-129">Descreve o processo de detecção de proximidade.</span><span class="sxs-lookup"><span data-stu-id="8699e-129">Describes the proximity detection process.</span></span>                                                                                                 |
| [<span data-ttu-id="8699e-130">Convertendo um arquivo de DRM-Protected em um fluxo do Windows Media DRM 10 para dispositivos de rede</span><span class="sxs-lookup"><span data-stu-id="8699e-130">Converting a DRM-Protected File to a Windows Media DRM 10 for Network Devices Stream</span></span>](converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream.md) | <span data-ttu-id="8699e-131">Descreve como converter um arquivo protegido por DRM em um fluxo que pode ser enviado para um dispositivo que usa o Windows Media DRM 10 para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="8699e-131">Describes how to convert a DRM-protected file to a stream that can be sent to a device that uses Windows Media DRM 10 for Network Devices.</span></span> |



 

> [!Note]  
> <span data-ttu-id="8699e-132">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="8699e-132">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8699e-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8699e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8699e-134">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="8699e-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




