---
title: Ferramentas para desenvolvimento
description: Ferramentas para desenvolvimento
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Media Gerenciador de Dispositivos, ferramentas de desenvolvimento
- Gerenciador de Dispositivos, ferramentas de desenvolvimento
- Gerenciador de Dispositivos de mídia do Windows, certificados
- Gerenciador de Dispositivos, certificados
- Gerenciador de Dispositivos de mídia do Windows, chaves
- Gerenciador de Dispositivos, chaves
- Gerenciador de Dispositivos de mídia do Windows, bibliotecas
- Gerenciador de Dispositivos, bibliotecas
- Windows Media Gerenciador de Dispositivos, Software Development Kit (SDK)
- Gerenciador de Dispositivos, Software Development Kit (SDK)
- SDK do Windows Media Gerenciador de Dispositivos
- SDK do Gerenciador de Dispositivos
- SDK do Windows Media Player
- SDK do Windows Media Format
- SDK do Windows Media Rights Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45a3e419b87c56a447ad2412234a80432b1598e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "105811361"
---
# <a name="tools-for-development"></a><span data-ttu-id="d9c12-118">Ferramentas para desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="d9c12-118">Tools for Development</span></span>

<span data-ttu-id="d9c12-119">Esta seção descreve os vários certificados e chaves, bibliotecas e SDKs que você precisará programar usando o SDK do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d9c12-119">This section describes the various certificates and keys, libraries, and SDKs you will need to program using the Windows Media Device Manager SDK.</span></span>

<span data-ttu-id="d9c12-120">Certificados e chaves</span><span class="sxs-lookup"><span data-stu-id="d9c12-120">Certificates and Keys</span></span>

<span data-ttu-id="d9c12-121">O SDK do Windows Media Gerenciador de Dispositivos é fornecido com um par de chave/certificado de teste (no arquivo Key. c) que pode ser usado por um aplicativo ou um provedor de serviços para usar os métodos do Windows Media Gerenciador de Dispositivos em conteúdo desprotegido.</span><span class="sxs-lookup"><span data-stu-id="d9c12-121">The Windows Media Device Manager SDK ships with a test key/certificate pair (in the key.c file) that can be used by an application or a service provider to use Windows Media Device Manager methods on unprotected content.</span></span> <span data-ttu-id="d9c12-122">Esse par de chave/certificado permite que o aplicativo ou provedor de serviços use a maior parte da funcionalidade do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d9c12-122">This key/certificate pair allows the application or service provider to use most of the Windows Media Device Manager functionality.</span></span>

<span data-ttu-id="d9c12-123">No entanto, para desenvolver um aplicativo ou provedor de serviços que possa lidar com conteúdo protegido por DRM, você deve solicitar um ou mais certificados (cada um com uma chave) na [página de licenciamento do Windows Media](https://www.microsoft.com/licensing/default).</span><span class="sxs-lookup"><span data-stu-id="d9c12-123">However, to develop an application or service provider that can handle DRM-protected content, you must request one or more certificates (each with a key) from the [Windows Media Licensing Page](https://www.microsoft.com/licensing/default).</span></span> <span data-ttu-id="d9c12-124">Os certificados são necessários para os seguintes aplicativos ou objetos:</span><span class="sxs-lookup"><span data-stu-id="d9c12-124">Certificates are required for the following applications or objects:</span></span>

-   <span data-ttu-id="d9c12-125">Provedores de serviço que manipulam conteúdo protegido por DRM exigem um certificado (e chave) do provedor de serviços do Windows Media Gerenciador de Dispositivos</span><span class="sxs-lookup"><span data-stu-id="d9c12-125">Service Providers that handle DRM-protected content require a Windows Media Device Manager Service Provider Certificate (and key)</span></span>
-   <span data-ttu-id="d9c12-126">Os aplicativos que transferem conteúdo protegido por DRM exigem um certificado (e chave) de transferência do Windows Media Gerenciador de Dispositivos</span><span class="sxs-lookup"><span data-stu-id="d9c12-126">Applications that transfer DRM-protected content require a Windows Media Device Manager Transfer Certificate (and key)</span></span>
-   <span data-ttu-id="d9c12-127">Os aplicativos que executam conteúdo protegido por DRM exigem um certificado DRM (e chave).</span><span class="sxs-lookup"><span data-stu-id="d9c12-127">Applications that play DRM-protected content require a DRM Certificate (and key).</span></span>
-   <span data-ttu-id="d9c12-128">Os componentes de medição de licença exigem um certificado de medição.</span><span class="sxs-lookup"><span data-stu-id="d9c12-128">License metering components require a metering certificate.</span></span> <span data-ttu-id="d9c12-129">Isso é fornecido por um serviço de medição de licença criado no SDK do Windows Media Rights Manager, que pode ser solicitado na página de licenciamento do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d9c12-129">This is provided by a license metering service built on the Windows Media Rights Manager SDK, which can be requested on the Windows Media Licensing Page.</span></span>

<span data-ttu-id="d9c12-130">Bibliotecas e cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="d9c12-130">Libraries and Headers</span></span>

<span data-ttu-id="d9c12-131">Além das bibliotecas e dos cabeçalhos mencionados nos [arquivos de biblioteca e de cabeçalho necessários para um aplicativo](required-library-and-header-files-for-an-application.md) ou [bibliotecas e cabeçalhos necessários para um provedor de serviços](required-libraries-and-headers-for-a-service-provider.md), qualquer aplicativo ou plug-in que tenha sido vinculado anteriormente a WMDRMSDK. lib para chamar as funções do Windows Media Format SDK agora deve vincular a WMDRMSDKStub. lib.</span><span class="sxs-lookup"><span data-stu-id="d9c12-131">In addition to the libraries and headers mentioned in [Required Library and Header Files for an Application](required-library-and-header-files-for-an-application.md) or [Required Libraries and Headers for a Service Provider](required-libraries-and-headers-for-a-service-provider.md), any application or plug-in that formerly linked to WMDRMSDK.lib to call Windows Media Format SDK functions should now instead link to WMDRMSDKStub.Lib.</span></span> <span data-ttu-id="d9c12-132">Esse arquivo de biblioteca é usado para acessar arquivos protegidos por DRM.</span><span class="sxs-lookup"><span data-stu-id="d9c12-132">This library file is used to access DRM-protected files.</span></span> <span data-ttu-id="d9c12-133">Você também pode solicitar essa biblioteca na página de licenciamento do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d9c12-133">You can request this library from the Windows Media Licensing Page as well.</span></span>

<span data-ttu-id="d9c12-134">SDKs relacionados</span><span class="sxs-lookup"><span data-stu-id="d9c12-134">Related SDKs</span></span>

<span data-ttu-id="d9c12-135">Os SDKs da Microsoft a seguir fornecem elementos que podem ser necessários na criação de soluções para dispositivos de mídia portáteis.</span><span class="sxs-lookup"><span data-stu-id="d9c12-135">The following Microsoft SDKs provide elements you may need in designing solutions for portable media devices.</span></span>



| <span data-ttu-id="d9c12-136">SDK necessário</span><span class="sxs-lookup"><span data-stu-id="d9c12-136">SDK Required</span></span>                     | <span data-ttu-id="d9c12-137">Necessário para...</span><span class="sxs-lookup"><span data-stu-id="d9c12-137">Required for...</span></span>                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9c12-138">SDK do Windows Media Gerenciador de Dispositivos</span><span class="sxs-lookup"><span data-stu-id="d9c12-138">Windows Media Device Manager SDK</span></span> | <span data-ttu-id="d9c12-139">Aplicativos de player de mídia de desktop que se comunicam com dispositivos portáteis</span><span class="sxs-lookup"><span data-stu-id="d9c12-139">Desktop media player applications that communicate with portable devices</span></span><br/> <span data-ttu-id="d9c12-140">Aplicativos de área de trabalho que podem trocar arquivos ou informações com dispositivos portáteis</span><span class="sxs-lookup"><span data-stu-id="d9c12-140">Desktop applications that can exchange files or information with portable devices</span></span><br/> <span data-ttu-id="d9c12-141">Objetos COM de medição do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="d9c12-141">Windows Media Player metering COM objects</span></span><br/> |
| <span data-ttu-id="d9c12-142">SDK do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="d9c12-142">Windows Media Player SDK</span></span>         | <span data-ttu-id="d9c12-143">Plug-ins do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="d9c12-143">Windows Media Player plug-ins</span></span><br/> <span data-ttu-id="d9c12-144">Objetos COM de medição do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="d9c12-144">Windows Media Player metering COM objects</span></span><br/> <span data-ttu-id="d9c12-145">Capas do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="d9c12-145">Windows Media Player skins</span></span><br/>                                                                                                   |
| <span data-ttu-id="d9c12-146">SDK do Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="d9c12-146">Windows Media Format SDK</span></span>         | <span data-ttu-id="d9c12-147">Players de áudio ou vídeo que podem criar ou reproduzir arquivos (particularmente arquivos ASF)</span><span class="sxs-lookup"><span data-stu-id="d9c12-147">Audio or video players that can create or play files (particularly ASF files)</span></span><br/> <span data-ttu-id="d9c12-148">Aplicativos de edição de áudio ou vídeo</span><span class="sxs-lookup"><span data-stu-id="d9c12-148">Audio or video editing applications</span></span><br/>                                                                                               |
| <span data-ttu-id="d9c12-149">SDK do Windows Media Rights Manager</span><span class="sxs-lookup"><span data-stu-id="d9c12-149">Windows Media Rights Manager SDK</span></span> | <span data-ttu-id="d9c12-150">Aplicativos ou plug-ins que o medidor de execução conta no desktop ou dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9c12-150">Applications or plug-ins that meter play counts on the desktop or device.</span></span>                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="d9c12-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9c12-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9c12-152">**Introdução**</span><span class="sxs-lookup"><span data-stu-id="d9c12-152">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 





