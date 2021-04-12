---
title: Executando detecção de proximidade
description: Executando detecção de proximidade
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- SDK do Windows Media Format, executando detecção de proximidade
- SDK do Windows Media Format, detecção de proximidade
- ASF (Advanced Systems Format), executando detecção de proximidade
- ASF (formato de sistemas avançados), executando detecção de proximidade
- ASF (Advanced Systems Format), detecção de proximidade
- ASF (formato de sistemas avançados), detecção de proximidade
- DRM (gerenciamento de direitos digitais), executando detecção de proximidade
- DRM (gerenciamento de direitos digitais), executando detecção de proximidade
- DRM (gerenciamento de direitos digitais), detecção de proximidade
- DRM (gerenciamento de direitos digitais), detecção de proximidade
- detecção de proximidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9628a6c33832b56858e5c457f15fd0935c2c436
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365523"
---
# <a name="performing-proximity-detection"></a><span data-ttu-id="82a33-114">Executando detecção de proximidade</span><span class="sxs-lookup"><span data-stu-id="82a33-114">Performing Proximity Detection</span></span>

<span data-ttu-id="82a33-115">Antes de poder transmitir dados criptografados para um dispositivo registrado no protocolo Windows Media DRM 10 para dispositivos de rede, você deve executar um processo chamado detecção de proximidade (também chamado de validação).</span><span class="sxs-lookup"><span data-stu-id="82a33-115">Before you can stream encrypted data to a registered device in the Windows Media DRM 10 for Network Devices protocol, you must perform a process called proximity detection (also called validation).</span></span> <span data-ttu-id="82a33-116">Esse processo envolve o envio de mensagens para o dispositivo e o recebimento de respostas.</span><span class="sxs-lookup"><span data-stu-id="82a33-116">This process involves sending messages to the device and receiving responses.</span></span> <span data-ttu-id="82a33-117">O tempo necessário para receber uma resposta é usado para determinar se o dispositivo é "próximo" o suficiente para o computador na rede para receber dados seguros.</span><span class="sxs-lookup"><span data-stu-id="82a33-117">The time it takes to receive a response is used to determine whether the device is "near" enough to the computer on the network to receive secure data.</span></span> <span data-ttu-id="82a33-118">A confirmação de que o dispositivo está fisicamente perto do computador cliente na rede ajuda a impedir falsificação e outro acesso não autorizado.</span><span class="sxs-lookup"><span data-stu-id="82a33-118">Confirming that the device is physically close to the client computer on the network helps to prevent spoofing and other unauthorized access.</span></span>

<span data-ttu-id="82a33-119">Quando a detecção de proximidade for concluída com êxito, o dispositivo será considerado válido.</span><span class="sxs-lookup"><span data-stu-id="82a33-119">When proximity detection is successfully completed, the device is said to be valid.</span></span> <span data-ttu-id="82a33-120">Você pode verificar se um dispositivo é válido chamando o método [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) .</span><span class="sxs-lookup"><span data-stu-id="82a33-120">You can check whether a device is valid by calling the [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) method.</span></span> <span data-ttu-id="82a33-121">Os dispositivos devem ser validados a cada 48 horas.</span><span class="sxs-lookup"><span data-stu-id="82a33-121">Devices must be validated every 48 hours.</span></span> <span data-ttu-id="82a33-122">Um dispositivo que foi validado mais de 48 horas antes da execução do programa deve ser revalidado executando o processo de detecção de proximidade novamente.</span><span class="sxs-lookup"><span data-stu-id="82a33-122">A device that was validated more than 48 hours before your program runs must be revalidated by performing the proximity detection process again.</span></span>

<span data-ttu-id="82a33-123">Para executar a detecção de proximidade, você deve estabelecer comunicações com o dispositivo e, em seguida, chamar o método [**IWMProximityDetection:: StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) .</span><span class="sxs-lookup"><span data-stu-id="82a33-123">To perform proximity detection, you must establish communications with the device and then call the [**IWMProximityDetection::StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) method.</span></span> <span data-ttu-id="82a33-124">O processo de detecção é concluído de forma assíncrona pelos componentes DRM internos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="82a33-124">The detection process is completed asynchronously by the internal DRM components of the Windows Media Format SDK.</span></span> <span data-ttu-id="82a33-125">Seu aplicativo deve incluir uma implementação da interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) para processar mensagens de detecção de proximidade.</span><span class="sxs-lookup"><span data-stu-id="82a33-125">Your application must include an implementation of the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface to process proximity detection messages.</span></span>

<span data-ttu-id="82a33-126">Há duas mensagens enviadas pelo processo de detecção de proximidade: uma mensagem de resultado e uma mensagem de conclusão.</span><span class="sxs-lookup"><span data-stu-id="82a33-126">There are two messages that are sent by the proximity detection process: a result message and a completion message.</span></span>

<span data-ttu-id="82a33-127">A mensagem de resultado, \_ resultado de proximidade WMT \_ , é enviada quando o processo de detecção é concluído.</span><span class="sxs-lookup"><span data-stu-id="82a33-127">The result message, WMT\_PROXIMITY\_RESULT, is sent when the detection process is completed.</span></span> <span data-ttu-id="82a33-128">O parâmetro *HR* do método de retorno de chamada [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) indica se o dispositivo foi considerado quase o suficiente para o computador cliente.</span><span class="sxs-lookup"><span data-stu-id="82a33-128">The *hr* parameter of the [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method indicates whether the device was found to be near enough to the client computer.</span></span> <span data-ttu-id="82a33-129">Se o parâmetro *HR* da mensagem de resultado indicar êxito *, o parâmetro* 1h conterá um **DWORD** especificando a latência medida para o dispositivo em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="82a33-129">If the *hr* parameter of the result message indicates success, the *pValue* parameter contains a **DWORD** specifying the measured latency to the device in milliseconds.</span></span>

<span data-ttu-id="82a33-130">A mensagem de conclusão, \_ proximidade de WMT \_ concluída, é enviada quando a detecção é finalizada.</span><span class="sxs-lookup"><span data-stu-id="82a33-130">The completion message, WMT\_PROXIMITY\_COMPLETED, is sent when the detection is finalized.</span></span> <span data-ttu-id="82a33-131">Você deve liberar a interface [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) somente depois de receber essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="82a33-131">You should release the [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) interface only after receiving this message.</span></span>

<span data-ttu-id="82a33-132">Quando a detecção de proximidade de um dispositivo é realizada com sucesso, o banco de dados de registro de dispositivo é atualizado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="82a33-132">When proximity detection for a device succeeds, the device registration database is automatically updated.</span></span> <span data-ttu-id="82a33-133">As chamadas subsequentes para [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) retornará **TRUE** até que 48 horas tenham passado e o dispositivo precise ser revalidado.</span><span class="sxs-lookup"><span data-stu-id="82a33-133">Subsequent calls to [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) will return **TRUE** until 48 hours have passed and the device needs to be revalidated.</span></span>

<span data-ttu-id="82a33-134">**Observação** O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="82a33-134">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82a33-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82a33-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82a33-136">**Usando o protocolo Windows Media DRM 10 para dispositivos de rede**</span><span class="sxs-lookup"><span data-stu-id="82a33-136">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




