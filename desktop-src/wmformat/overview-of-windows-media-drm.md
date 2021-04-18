---
title: Visão geral do DRM do Windows Media
description: Visão geral do DRM do Windows Media
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- SDK do Windows Media Format, licenças DRM
- SDK do Windows Media Format, licenças para DRM
- DRM (gerenciamento de direitos digitais), sobre
- DRM (gerenciamento de direitos digitais), sobre
- DRM (gerenciamento de direitos digitais), empacotando arquivos de mídia do Windows
- DRM (gerenciamento de direitos digitais), empacotando arquivos de mídia do Windows
- DRM (gerenciamento de direitos digitais), licenciamento de arquivo protegido
- DRM (gerenciamento de direitos digitais), licenciamento de arquivo protegido
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), lendo arquivos protegidos
- DRM (gerenciamento de direitos digitais), lendo arquivos protegidos
- ASF (Advanced Systems Format), DRM (gerenciamento de direitos digitais)
- ASF (formato de sistemas avançados), DRM (gerenciamento de direitos digitais)
- licenças, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14cb76fcf61346aab9bd68746afc7e50a2f146d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105793282"
---
# <a name="overview-of-windows-media-drm"></a><span data-ttu-id="a41b2-119">Visão geral do DRM do Windows Media</span><span class="sxs-lookup"><span data-stu-id="a41b2-119">Overview of Windows Media DRM</span></span>

<span data-ttu-id="a41b2-120">O Windows Media Digital Rights Management (DRM) é um sistema para proteger o conteúdo em arquivos de mídia do Windows para que usuários não autorizados não possam acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="a41b2-120">Windows Media Digital Rights Management (DRM) is a system for protecting the content in Windows Media files so that unauthorized users cannot access it.</span></span> <span data-ttu-id="a41b2-121">Há três fases para o ciclo de DRM básico: empacotamento, licenciamento e leitura.</span><span class="sxs-lookup"><span data-stu-id="a41b2-121">There are three phases to the basic DRM cycle: packaging, licensing, and reading.</span></span>

## <a name="packaging-windows-media-files"></a><span data-ttu-id="a41b2-122">Empacotando Arquivos de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="a41b2-122">Packaging Windows Media Files</span></span>

<span data-ttu-id="a41b2-123">O DRM do Windows Media foi projetado para funcionar com arquivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="a41b2-123">Windows Media DRM is designed to work with Windows Media files.</span></span> <span data-ttu-id="a41b2-124">Um arquivo de mídia do Windows é um arquivo que está em conformidade com a especificação ASF (Advanced Systems Format) e contém apenas áudio e vídeo que foram compactados usando os codecs de áudio e vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a41b2-124">A Windows Media file is a file that conforms to the Advanced Systems Format (ASF) specification and only contains Audio and Video that has been compressed by using the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="a41b2-125">Quando um arquivo ASF é empacotado, uma seção específica de DRM é adicionada ao cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="a41b2-125">When an ASF file is packaged, a DRM-specific section is added to the header.</span></span> <span data-ttu-id="a41b2-126">O cabeçalho DRM contém uma ID de chave, que identifica o conteúdo para fins de licenciamento e uma URL de aquisição de licença, que é o endereço de uma página da Web que pode emitir licenças para ler o conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="a41b2-126">The DRM header contains a Key ID, which identifies the content for the purposes of licensing, and a license acquisition URL, which is the address of a Web page that can issue licenses to read the protected content.</span></span> <span data-ttu-id="a41b2-127">Há muito mais informações que podem ser colocadas no cabeçalho DRM, mas é opcional.</span><span class="sxs-lookup"><span data-stu-id="a41b2-127">There is much more information that can be put in the DRM header, but it is optional.</span></span> <span data-ttu-id="a41b2-128">O cabeçalho DRM é assinado para que o packager possa ser verificado.</span><span class="sxs-lookup"><span data-stu-id="a41b2-128">The DRM header is signed so that the packager can be verified.</span></span>

<span data-ttu-id="a41b2-129">O conteúdo no arquivo ASF é criptografado durante o processo de empacotamento.</span><span class="sxs-lookup"><span data-stu-id="a41b2-129">The content in the ASF file is encrypted during the packing process.</span></span> <span data-ttu-id="a41b2-130">No entanto, as seguintes informações no arquivo empacotado estão disponíveis até mesmo para clientes que não têm uma licença:</span><span class="sxs-lookup"><span data-stu-id="a41b2-130">However, the following information in the packaged file is available even to clients that do not have a license:</span></span>

-   <span data-ttu-id="a41b2-131">Metadados que são armazenados no cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="a41b2-131">Metadata that is stored in the ASF header.</span></span>
-   <span data-ttu-id="a41b2-132">Alguns metadados armazenados no cabeçalho DRM (por exemplo, você sempre pode obter a URL de aquisição de licença).</span><span class="sxs-lookup"><span data-stu-id="a41b2-132">Some metadata that is stored in the DRM header (for example, you can always get the license acquisition URL).</span></span>

## <a name="licensing-protected-files"></a><span data-ttu-id="a41b2-133">Licenciamento de arquivos protegidos</span><span class="sxs-lookup"><span data-stu-id="a41b2-133">Licensing Protected Files</span></span>

<span data-ttu-id="a41b2-134">Para que um arquivo empacotado seja lido, uma licença deve ser emitida para o computador cliente.</span><span class="sxs-lookup"><span data-stu-id="a41b2-134">For a packaged file to be read, a license must be issued to the client computer.</span></span> <span data-ttu-id="a41b2-135">Uma licença é um conjunto de dados que descreve as condições sob as quais os dados nos arquivos protegidos podem ser lidos.</span><span class="sxs-lookup"><span data-stu-id="a41b2-135">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="a41b2-136">Geralmente, uma licença é emitida para um arquivo protegido em resposta ao usuário que está tentando executar alguma operação no arquivo.</span><span class="sxs-lookup"><span data-stu-id="a41b2-136">Most often, a license is issued for a protected file in response to the user trying to perform some operation on the file.</span></span> <span data-ttu-id="a41b2-137">Também é possível, no entanto, que um emissor de licença entregue licenças a um cliente antes que ele seja explicitamente solicitado.</span><span class="sxs-lookup"><span data-stu-id="a41b2-137">It is also possible, however, for a license issuer to deliver licenses to a client before it is explicitly requested.</span></span> <span data-ttu-id="a41b2-138">Para obter mais informações sobre licenças, consulte [licenças](licenses.md).</span><span class="sxs-lookup"><span data-stu-id="a41b2-138">For more information about licenses, see [Licenses](licenses.md).</span></span>

## <a name="reading-data-from-protected-files"></a><span data-ttu-id="a41b2-139">Lendo dados de arquivos protegidos</span><span class="sxs-lookup"><span data-stu-id="a41b2-139">Reading Data from Protected Files</span></span>

<span data-ttu-id="a41b2-140">Quando um usuário tenta executar uma operação em um arquivo protegido (reproduzir, gravar em CD, copiar para um dispositivo e assim por diante), o aplicativo deve verificar se há licenças para o conteúdo no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="a41b2-140">When a user tries to perform an operation on a protected file (play, burn to CD, copy to a device, and so on), the application must check for licenses for the content on the client computer.</span></span> <span data-ttu-id="a41b2-141">Se houver uma licença válida no computador cliente, a operação poderá continuar.</span><span class="sxs-lookup"><span data-stu-id="a41b2-141">If a valid license exists on the client computer, the operation can proceed.</span></span> <span data-ttu-id="a41b2-142">Se não houver uma licença para o conteúdo ou se nenhuma licença para o conteúdo que está no computador cliente permitir a ação solicitada, uma licença deverá ser adquirida.</span><span class="sxs-lookup"><span data-stu-id="a41b2-142">If there isn't a license for the content, or if no license for the content that is on the client computer allows the requested action, then a license must be acquired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a41b2-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a41b2-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a41b2-144">**Sobre as APIs estendidas do cliente DRM do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a41b2-144">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




