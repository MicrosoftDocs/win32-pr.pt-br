---
title: Implementando a revogação de licenças
description: Implementando a revogação de licenças
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- SDK do Windows Media Format, implementando a revogação de licença
- SDK do Windows Media Format, revogação de licença
- SDK do Windows Media Format, revogação de licenças
- ASF (Advanced Systems Format), implementando a revogação de licenças
- ASF (formato de sistemas avançados), implementando a revogação de licenças
- ASF (Advanced Systems Format), revogação de licença
- ASF (formato de sistemas avançados), revogação de licença
- ASF (Advanced Systems Format), revogação de licenças
- ASF (formato de sistemas avançados), revogação de licenças
- DRM (gerenciamento de direitos digitais), implementando a revogação de licenças
- DRM (gerenciamento de direitos digitais), implementando a revogação de licenças
- DRM (gerenciamento de direitos digitais), revogação de licença
- DRM (gerenciamento de direitos digitais), revogação de licença
- DRM (gerenciamento de direitos digitais), revogação de licenças
- DRM (gerenciamento de direitos digitais), revogação de licenças
- revogação de licença, implementando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83bfb1a512b031f5b7c297ecede4ed33fba8f2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640163"
---
# <a name="implementing-license-revocation"></a><span data-ttu-id="0af78-119">Implementando a revogação de licenças</span><span class="sxs-lookup"><span data-stu-id="0af78-119">Implementing License Revocation</span></span>

<span data-ttu-id="0af78-120">O SDK do Windows Media Rights Manager 10 inclui um recurso chamado revogação de licenças.</span><span class="sxs-lookup"><span data-stu-id="0af78-120">The Windows Media Rights Manager 10 SDK includes a feature called license revocation.</span></span> <span data-ttu-id="0af78-121">Esse recurso permite que os servidores de licenças solicitem que as licenças sejam removidas do computador cliente.</span><span class="sxs-lookup"><span data-stu-id="0af78-121">This feature enables license servers to request that licenses be removed from the client computer.</span></span> <span data-ttu-id="0af78-122">O Windows Media Format SDK fornece métodos que processam mensagens de revogação e removem as licenças do armazenamento de licença local.</span><span class="sxs-lookup"><span data-stu-id="0af78-122">The Windows Media Format SDK provides methods that process revocation messages and remove the licenses from the local license store.</span></span>

<span data-ttu-id="0af78-123">O processo de revogação de licença é iniciado por um serviço fornecido pelo emissor da licença.</span><span class="sxs-lookup"><span data-stu-id="0af78-123">The license revocation process is initiated by a service provided by the license issuer.</span></span> <span data-ttu-id="0af78-124">Seu aplicativo pode hospedar esse serviço ou pode ser um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="0af78-124">Your application can host this service, or it can be a Web application.</span></span> <span data-ttu-id="0af78-125">Em ambos os casos, seu aplicativo deve ser capaz de receber um desafio de licença criado pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="0af78-125">In either case, your application must be able to receive a license challenge created by the service.</span></span>

<span data-ttu-id="0af78-126">Para remover licenças do repositório de licenças, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="0af78-126">To remove licenses from the license store, perform the following steps:</span></span>

1.  <span data-ttu-id="0af78-127">Após receber um desafio de licença do emissor da licença, chame a função [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) para criar um objeto do agente de revogação de licença e obter um ponteiro para a interface [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .</span><span class="sxs-lookup"><span data-stu-id="0af78-127">Upon receiving a license challenge from the license issuer, call the [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) function to create a license revocation agent object and obtain a pointer to the [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) interface.</span></span>
2.  <span data-ttu-id="0af78-128">Chame o método [**IWMLicenseRevocationAgent:: GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) para gerar a resposta de desafio.</span><span class="sxs-lookup"><span data-stu-id="0af78-128">Call the [**IWMLicenseRevocationAgent::GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) method to generate the challenge response.</span></span>
3.  <span data-ttu-id="0af78-129">Envie a resposta de desafio de volta para o componente de serviço de licença do qual você recebeu o desafio.</span><span class="sxs-lookup"><span data-stu-id="0af78-129">Send the challenge response back to the license service component from which you received the challenge.</span></span>
4.  <span data-ttu-id="0af78-130">O componente de serviço de licença envia um LRB (blob de revogação de licença assinada) para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0af78-130">The license service component sends a signed license revocation blob (LRB) to your application.</span></span> <span data-ttu-id="0af78-131">Quando você o receber, chame o método [**IWMLicenseRevocationAgent::P rocesslrb**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) .</span><span class="sxs-lookup"><span data-stu-id="0af78-131">When you receive it, call the [**IWMLicenseRevocationAgent::ProcessLRB**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) method.</span></span> <span data-ttu-id="0af78-132">O **ProcessLRB** cria uma mensagem de confirmação que você deve enviar de volta ao serviço de licença para verificar se as licenças foram removidas.</span><span class="sxs-lookup"><span data-stu-id="0af78-132">**ProcessLRB** creates an acknowledgement message that you must send back to the license service to verify that the licenses were removed.</span></span>

> [!Note]  
> <span data-ttu-id="0af78-133">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="0af78-133">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0af78-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0af78-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0af78-135">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="0af78-135">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="0af78-136">**Interface IWMLicenseRevocationAgent**</span><span class="sxs-lookup"><span data-stu-id="0af78-136">**IWMLicenseRevocationAgent Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




