---
title: Lidando com conteúdo protegido
description: Lidando com conteúdo protegido
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Gerenciador de Dispositivos de mídia do Windows, certificados
- Gerenciador de Dispositivos, certificados
- aplicativos de área de trabalho, certificados
- provedores de serviços, certificados
- Guia de programação, certificados
- certificates
- Windows Media Gerenciador de Dispositivos, provedor de conteúdo seguro (SCP)
- Gerenciador de Dispositivos, provedor de conteúdo seguro (SCP)
- aplicativos de área de trabalho, provedor de conteúdo seguro (SCP)
- provedores de serviços, provedor de conteúdo seguro (SCP)
- Guia de programação, provedor de conteúdo seguro (SCP)
- provedor de conteúdo seguro (SCP)
- SCP (provedor de conteúdo seguro)
- Windows Media Gerenciador de Dispositivos, conteúdo protegido por DRM
- Gerenciador de Dispositivos, conteúdo protegido por DRM
- Guia de programação, conteúdo protegido por DRM
- aplicativos de desktop, conteúdo protegido por DRM
- provedores de serviços, conteúdo protegido por DRM
- Conteúdo protegido por DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd0fb6ab155d08ed19eb84988709695f9ed63fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363859"
---
# <a name="handling-protected-content"></a><span data-ttu-id="2bcc9-122">Lidando com conteúdo protegido</span><span class="sxs-lookup"><span data-stu-id="2bcc9-122">Handling Protected Content</span></span>

<span data-ttu-id="2bcc9-123">Se você estiver criando um aplicativo ou provedor de serviços que consumirá conteúdo protegido pelo DRM (gerenciamento de direitos digitais) do Windows Media, você deverá ter um par de chave/certificado emitido pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-123">If you are building an application or service provider that will consume content protected by Windows Media digital rights management (DRM), you must have a key/certificate pair issued by Microsoft.</span></span> <span data-ttu-id="2bcc9-124">Para saber onde obter esse certificado, consulte [ferramentas para desenvolvimento](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="2bcc9-124">To learn where to get this certificate, see [Tools for Development](tools-for-development.md).</span></span> <span data-ttu-id="2bcc9-125">Se você não pretende manipular o conteúdo protegido, você pode usar a chave fictícia e o certificado fornecido com esse SDK em um arquivo chamado Key. c.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-125">If you do not intend to handle protected content, you can use the dummy key and certificate provided with this SDK in a file named key.c.</span></span>

<span data-ttu-id="2bcc9-126">Para qualquer arquivo protegido pela tecnologia DRM, o Windows Media Gerenciador de Dispositivos requer a presença de um SCP (provedor de conteúdo seguro) para esse formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-126">For any file that is protected by DRM technology, Windows Media Device Manager requires the presence of a secure content provider (SCP) for that file format.</span></span> <span data-ttu-id="2bcc9-127">A Microsoft fornece um módulo SCP para arquivos WMA e WMV.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-127">Microsoft provides an SCP module for WMA and WMV files.</span></span> <span data-ttu-id="2bcc9-128">Se seu aplicativo ou provedor de serviços estiver lidando com conteúdo protegido por DRM de outro formato, você deverá fornecer seu próprio módulo SCP.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-128">If your application or service provider will be handling DRM-protected content of another format, you must provide your own SCP module.</span></span> <span data-ttu-id="2bcc9-129">Um módulo SCP é um objeto COM que implementa todas as [interfaces para provedores de conteúdo seguro](interfaces-for-secure-content-providers.md).</span><span class="sxs-lookup"><span data-stu-id="2bcc9-129">An SCP module is a COM object that implements all the [interfaces for Secure Content Providers](interfaces-for-secure-content-providers.md).</span></span>

<span data-ttu-id="2bcc9-130">Um aplicativo pode enviar conteúdo protegido por DRM para dispositivos criados no Windows Media DRM 10 para dispositivos portáteis ou em um PDDRM (DRM de dispositivo portátil).</span><span class="sxs-lookup"><span data-stu-id="2bcc9-130">An application can send DRM-protected content to devices built on either Windows Media DRM 10 for Portable Devices, or Portable Device DRM (PDDRM).</span></span> <span data-ttu-id="2bcc9-131">No entanto, você só pode criar um provedor de serviços para dispositivos criados em PDDRM; Você não pode criar um provedor de serviços para dispositivos criados no Windows Media DRM 10 para dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-131">However, you can only create a service provider for devices built on PDDRM; you cannot create a service provider for devices built on Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="2bcc9-132">Esses últimos dispositivos só podem usar o provedor de serviços MTP fornecido pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-132">These latter devices can only use the Microsoft-provided MTP service provider.</span></span>

<span data-ttu-id="2bcc9-133">Os dispositivos criados no PDDRM só podem dar suporte a licenças para conteúdo comprado.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-133">Devices built on PDDRM can only support licenses for purchased content.</span></span> <span data-ttu-id="2bcc9-134">As licenças que têm condições de expiração de tempo só têm suporte em dispositivos criados no Windows Media DRM 10 para dispositivos portáteis, que têm requisitos especiais, como um Clock e uma individualização seguros.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-134">Licenses that have time-expiration conditions are only supported by devices built on Windows Media DRM 10 for Portable Devices, which have special requirements such as a secure clock and individualization.</span></span> <span data-ttu-id="2bcc9-135">O SDK do Windows Media DRM 10 para dispositivos portáteis fornece detalhes sobre os requisitos de dispositivo para dar suporte à tecnologia da versão 10.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-135">Windows Media DRM 10 for Portable Devices SDK gives details on device requirements to support version 10 technology.</span></span>

<span data-ttu-id="2bcc9-136">Antes de enviar conteúdo de DRM para o dispositivo, um aplicativo deve verificar várias coisas:</span><span class="sxs-lookup"><span data-stu-id="2bcc9-136">Before sending DRM content to the device, an application should verify several things:</span></span>

-   <span data-ttu-id="2bcc9-137">Se o dispositivo dá suporte à tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-137">That the device supports DRM technology.</span></span>
-   <span data-ttu-id="2bcc9-138">A qual versão da tecnologia DRM ela dá suporte (versão 10 ou anterior).</span><span class="sxs-lookup"><span data-stu-id="2bcc9-138">What version of DRM technology it supports (version 10 or earlier).</span></span>
-   <span data-ttu-id="2bcc9-139">Se o dispositivo for criado na versão 10, se todos os seus componentes estiverem atualizados (como o relógio seguro e quaisquer requisitos de individualização).</span><span class="sxs-lookup"><span data-stu-id="2bcc9-139">If the device is built on version 10, that all its components are up to date (such as the secure clock and any individualization requirements).</span></span>

<span data-ttu-id="2bcc9-140">Todas as chamadas de método para responder a essas perguntas são feitas pelo cliente e manipuladas pelo Windows Media Gerenciador de Dispositivos e pelo componente do provedor de conteúdo seguro; o provedor de serviços não lida com nenhuma dessas chamadas.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-140">All method calls to answer these questions are made by the client and handled by Windows Media Device Manager and the secure content provider component; the service provider does not handle any of these calls.</span></span>

<span data-ttu-id="2bcc9-141">Se o dispositivo não oferecer suporte ao Windows Media DRM 10 para dispositivos portáteis, ele ainda poderá consumir conteúdo protegido (dependendo da licença de conteúdo e do design do dispositivo), mas qualquer conteúdo enviado a ele terá uma licença de uso simplificada com direitos limitados (por exemplo, sem expiração de tempo).</span><span class="sxs-lookup"><span data-stu-id="2bcc9-141">If the device does not support Windows Media DRM 10 for Portable Devices, it might still be able to consume protected content (depending on the content license and the device design), but any content sent to it will have a simplified use license with limited rights (for example, no time expiration).</span></span>

-   <span data-ttu-id="2bcc9-142">Para obter exemplos que demonstram como um aplicativo verifica se um dispositivo pode lidar com conteúdo protegido e se precisa atualizar seus componentes DRM, consulte [lidando com conteúdo protegido no aplicativo](handling-protected-content-in-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="2bcc9-142">For examples demonstrating how an application verifies whether a device can handle protected content, and whether it needs to update its DRM components, see [Handling Protected Content in the Application](handling-protected-content-in-the-application.md).</span></span>
-   <span data-ttu-id="2bcc9-143">Para obter mais informações sobre como criar um provedor de serviços que possa lidar com conteúdo protegido, consulte [lidando com conteúdo protegido no provedor de serviços](handling-protected-content-in-the-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2bcc9-143">For more information about building a service provider that can handle protected content, see [Handling Protected Content in the Service Provider](handling-protected-content-in-the-service-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="2bcc9-144">Muitos direitos de transferência de arquivo do Windows Media Gerenciador de Dispositivos ou os métodos de solicitação de permissão falharão (geralmente com um valor de **HRESULT** misterioso) ao manipular arquivos protegidos por DRM com um depurador anexado.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-144">Many Windows Media Device Manager file transfer or rights requesting methods will fail (often with a mysterious **HRESULT** value) when handling DRM-protected files with a debugger attached.</span></span> <span data-ttu-id="2bcc9-145">Portanto, você deve usar maneiras alternativas para depurar seu código, como as saídas de log para um formulário do Windows ou um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-145">Therefore, you must use alternate ways to debug your code, such as logging outputs to a Windows form or a log file.</span></span> <span data-ttu-id="2bcc9-146">Para obter mais informações sobre opções de log, consulte [habilitando o log](enabling-logging.md).</span><span class="sxs-lookup"><span data-stu-id="2bcc9-146">For more information on logging options, see [Enabling Logging](enabling-logging.md).</span></span> <span data-ttu-id="2bcc9-147">Se você estiver executando um depurador no conteúdo protegido, um método retornará um dos códigos de erro listados na seção DRM códigos de [erro](error-codes.md)ou, possivelmente, um código de erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-147">If you are running a debugger on protected content, a method will return one of the error codes listed in the DRM section [Error Codes](error-codes.md), or possibly an unknown error code.</span></span> <span data-ttu-id="2bcc9-148">Se você obtiver um valor misterioso de **HRESULT** ao executar um depurador em um conteúdo ou métodos protegidos, a proteção de DRM poderá ser a causa.</span><span class="sxs-lookup"><span data-stu-id="2bcc9-148">If you get mysterious **HRESULT** values when running a debugger on protected content or methods, DRM protection might be the cause.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2bcc9-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2bcc9-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bcc9-150">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="2bcc9-150">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




