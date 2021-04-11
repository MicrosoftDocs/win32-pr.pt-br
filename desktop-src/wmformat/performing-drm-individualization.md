---
title: Executando individualização de DRM
description: Executando individualização de DRM
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- SDK do Windows Media Format, APIs estendidas do cliente DRM
- SDK do Windows Media Format, APIs estendidas do cliente
- SDK do Windows Media Format, APIs estendidas
- SDK do Windows Media Format, APIs
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- SDK do Windows Media Format, individualização de DRM
- SDK do Windows Media Format, individualização
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), individualização
- DRM (gerenciamento de direitos digitais), individualização
- DRM (gerenciamento de direitos digitais), individualização de DRM
- DRM (gerenciamento de direitos digitais), individualização de DRM
- APIs estendidas do cliente DRM, individualização
- APIs estendidas do cliente, individualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d8f7f04add4ed626985651d5220e69ea713e4d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292617"
---
# <a name="performing-drm-individualization"></a><span data-ttu-id="fa276-122">Executando individualização de DRM</span><span class="sxs-lookup"><span data-stu-id="fa276-122">Performing DRM Individualization</span></span>

<span data-ttu-id="fa276-123">A individualização é o processo de atualizar o componente DRM no computador cliente, criptografá-lo e torná-lo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="fa276-123">Individualization is the process of updating the DRM component on the client computer, encrypting it, and making it unique.</span></span> <span data-ttu-id="fa276-124">Quando um computador é individualizado, o componente DRM é vinculado ao computador e não será capaz de decodificar o conteúdo em nenhum outro computador.</span><span class="sxs-lookup"><span data-stu-id="fa276-124">When a computer is individualized, the DRM component is tied to the computer and will not be able to decode content on any other computer.</span></span> <span data-ttu-id="fa276-125">As APIs estendidas do cliente Windows Media DRM oferecem suporte para individualizar o componente DRM em computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="fa276-125">The Windows Media DRM Client Extended APIs provide support for individualizing the DRM component on client computers.</span></span>

<span data-ttu-id="fa276-126">A individualização é executada chamando o método [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) .</span><span class="sxs-lookup"><span data-stu-id="fa276-126">Individualization is performed by calling the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method.</span></span> <span data-ttu-id="fa276-127">Você pode chamar **PerformSecurityUpdate** para que ela seja individualizada somente se a versão no servidor for mais recente do que a instalada no computador cliente ou se você puder forçar a individualização sem considerar as versões de segurança relativas.</span><span class="sxs-lookup"><span data-stu-id="fa276-127">You can call **PerformSecurityUpdate** so that it will individualize only if the version on the server is newer than the one installed on the client computer, or you can force individualization without regard to the relative security versions.</span></span> <span data-ttu-id="fa276-128">O sinalizador para a individualização conforme necessário é a \_ segurança do WMDRM \_ Execute \_ indiv.</span><span class="sxs-lookup"><span data-stu-id="fa276-128">The flag for as-needed individualization is WMDRM\_SECURITY\_PERFORM\_INDIV.</span></span> <span data-ttu-id="fa276-129">O sinalizador para individualização forçada é a segurança do WMDRM \_ \_ Execute \_ Force \_ indiv.</span><span class="sxs-lookup"><span data-stu-id="fa276-129">The flag for forced individualization is WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV.</span></span>

<span data-ttu-id="fa276-130">**PerformSecurityUpdate** é uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="fa276-130">**PerformSecurityUpdate** is an asynchronous call.</span></span> <span data-ttu-id="fa276-131">Ele retornará rapidamente e, em seguida, gerará eventos para fornecer informações de status sobre o processo de individualização.</span><span class="sxs-lookup"><span data-stu-id="fa276-131">It will return quickly and then generate events to provide status information about the individualization process.</span></span> <span data-ttu-id="fa276-132">A maioria dos eventos gerados será **MEWMDRMIndividualizationProgress** eventos e cada um terá uma interface [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) associada.</span><span class="sxs-lookup"><span data-stu-id="fa276-132">The majority of the events generated will be **MEWMDRMIndividualizationProgress** events, and each has an associated [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span> <span data-ttu-id="fa276-133">Para obter a interface de status, você deve chamar **IMFMediaEvent:: GetValue** para recuperar um ponteiro **IUnknown** que esteja no mesmo objeto e, em seguida, consultá-lo para **IWMDRMIndividualizationStatus**.</span><span class="sxs-lookup"><span data-stu-id="fa276-133">To get the status interface, you must call **IMFMediaEvent::GetValue** to retrieve an **IUnknown** pointer that is on the same object and then query it for **IWMDRMIndividualizationStatus**.</span></span>

<span data-ttu-id="fa276-134">Você pode obter dados para uma estrutura de [**\_ \_ status de individualização do WM**](drmwm-individualize-status.md) chamando [**IWMDRMIndividualizeStatus:: GetStatus**](iwmdrmindividualizationstatus-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="fa276-134">You can get data for a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure by calling [**IWMDRMIndividualizeStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md).</span></span> <span data-ttu-id="fa276-135">Cada evento gerado tem seu próprio objeto com status, portanto, você deve passar pelo processo de obter o valor do evento e consultar a interface de status a cada vez.</span><span class="sxs-lookup"><span data-stu-id="fa276-135">Each event that is generated has its own object with status, so you must go through the process of getting the event value and querying for the status interface every time.</span></span>

<span data-ttu-id="fa276-136">Dependendo do tamanho do download, pode haver dezenas ou centenas de eventos **MEWMDRMIndividualizationProgress** .</span><span class="sxs-lookup"><span data-stu-id="fa276-136">Depending on the size of the download, there may be dozens or hundreds of **MEWMDRMIndividualizationProgress** events.</span></span> <span data-ttu-id="fa276-137">Quando o processo de individualização é concluído, um evento **MEWMDRMIndividualizationCompleted** é gerado.</span><span class="sxs-lookup"><span data-stu-id="fa276-137">When the individualization process is finished, an **MEWMDRMIndividualizationCompleted** event is generated.</span></span>

<span data-ttu-id="fa276-138">Quando a individualização for concluída, os únicos objetos existentes que refletirão o novo estado individual serão aqueles que herdam de [**IWMDRMSecurity**](iwmdrmsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="fa276-138">When individualization is completed, the only existing objects that will reflect the new individualized state are those that inherit from [**IWMDRMSecurity**](iwmdrmsecurity.md).</span></span> <span data-ttu-id="fa276-139">Todos os outros objetos existentes não serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="fa276-139">All other existing objects will not be updated.</span></span> <span data-ttu-id="fa276-140">Você deve liberar e recriar outros objetos para que eles reflitam o novo estado individual.</span><span class="sxs-lookup"><span data-stu-id="fa276-140">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa276-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa276-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa276-142">**Exemplo de individualização de DRM**</span><span class="sxs-lookup"><span data-stu-id="fa276-142">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="fa276-143">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="fa276-143">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="fa276-144">**Usando o modelo de evento Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="fa276-144">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> <dt>

<span data-ttu-id="fa276-145">[Práticas recomendadas de individualização do Windows Media DRM](/previous-versions/ms867216(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="fa276-145">[Windows Media DRM Individualization Best Practices](/previous-versions/ms867216(v=msdn.10))</span></span>
</dt> </dl>

 

 




