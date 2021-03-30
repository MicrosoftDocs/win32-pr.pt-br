---
title: Importação de DRM
description: Importação de DRM
ms.assetid: 5e67a721-830b-4d99-9f90-4cb2d7c61104
keywords:
- SDK do Windows Media Format, APIs estendidas do cliente DRM
- SDK do Windows Media Format, APIs estendidas do cliente
- SDK do Windows Media Format, APIs estendidas
- SDK do Windows Media Format, APIs
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- SDK do Windows Media Format, importação de DRM
- SDK do Windows Media Format, importar
- SDK do Windows Media Format, CPS (sistema de proteção de conteúdo)
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), CPS (sistema de proteção de conteúdo)
- DRM (gerenciamento de direitos digitais), CPS (sistema de proteção de conteúdo)
- APIs estendidas do cliente DRM, importar
- APIs estendidas do cliente, importar
- APIs estendidas do cliente DRM, CPS (sistema de proteção de conteúdo)
- APIs estendidas do cliente, CPS (sistema de proteção de conteúdo)
- sistema de proteção de conteúdo (CPS)
- CPS (sistema de proteção de conteúdo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fc20cfd682df975c10a8f39785c0e8d69610d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636111"
---
# <a name="drm-import"></a><span data-ttu-id="dba37-127">Importação de DRM</span><span class="sxs-lookup"><span data-stu-id="dba37-127">DRM Import</span></span>

<span data-ttu-id="dba37-128">As seções a seguir explicam como converter o conteúdo de mídia de um sistema de proteção de conteúdo (CPS) de terceiros para o DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dba37-128">The following sections explain how to convert media content from a third-party content protection system (CPS) to Windows Media DRM.</span></span> <span data-ttu-id="dba37-129">Esse processo é conhecido como importação de DRM e consiste basicamente nas seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="dba37-129">This process is known as DRM Import and consists essentially of the following steps:</span></span>

1.  <span data-ttu-id="dba37-130">Criando o arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="dba37-130">Creating the ASF file.</span></span>
2.  <span data-ttu-id="dba37-131">Criando a licença.</span><span class="sxs-lookup"><span data-stu-id="dba37-131">Creating the license.</span></span>
3.  <span data-ttu-id="dba37-132">Opcionalmente, excluindo a licença.</span><span class="sxs-lookup"><span data-stu-id="dba37-132">Optionally deleting the license.</span></span>

<span data-ttu-id="dba37-133">A importação de DRM é explicada nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="dba37-133">DRM Import is explained in the following sections.</span></span>



| <span data-ttu-id="dba37-134">Seção</span><span class="sxs-lookup"><span data-stu-id="dba37-134">Section</span></span>                                                                              | <span data-ttu-id="dba37-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="dba37-135">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="dba37-136">Importando a licença e o material da chave</span><span class="sxs-lookup"><span data-stu-id="dba37-136">Importing License and Key Material</span></span>](importing-license-and-key-material.md)         | <span data-ttu-id="dba37-137">Descreve como emitir licenças localmente e importá-las para o Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="dba37-137">Describes how to issue licenses locally and import them into Windows Media DRM.</span></span>      |
| [<span data-ttu-id="dba37-138">Verificando revogação de certificado</span><span class="sxs-lookup"><span data-stu-id="dba37-138">Checking Certificate Revocation</span></span>](checking-certificate-revocation.md)               | <span data-ttu-id="dba37-139">Descreve como verificar a revogação de certificado.</span><span class="sxs-lookup"><span data-stu-id="dba37-139">Describes how to check certificate revocation.</span></span>                                       |
| [<span data-ttu-id="dba37-140">Criando uma licença do XMR</span><span class="sxs-lookup"><span data-stu-id="dba37-140">Building an XMR License</span></span>](building-an-xmr-license.md)                               | <span data-ttu-id="dba37-141">Descreve como criar uma licença do XMR e passá-la para o subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="dba37-141">Describes how to create an XMR license and pass it to the DRM subsystem.</span></span>             |
| [<span data-ttu-id="dba37-142">Criando e inicializando um gravador de DRM</span><span class="sxs-lookup"><span data-stu-id="dba37-142">Creating and Initializing a DRM Writer</span></span>](creating-and-initializing-a-drm-writer.md) | <span data-ttu-id="dba37-143">Descreve como inicializar um objeto do gravador ASF para se preparar para a importação de DRM.</span><span class="sxs-lookup"><span data-stu-id="dba37-143">Describes how to initialize an ASF writer object to prepare for DRM Import.</span></span>          |
| [<span data-ttu-id="dba37-144">Criptografando e importando amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="dba37-144">Encrypting and Importing Media Samples</span></span>](encrypting-and-importing-media-samples.md) | <span data-ttu-id="dba37-145">Descreve como criptografar e importar exemplos de mídia individuais no Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="dba37-145">Describes how to encrypt and import individual media samples into Windows Media DRM.</span></span> |
| [<span data-ttu-id="dba37-146">Exclusão de licenças</span><span class="sxs-lookup"><span data-stu-id="dba37-146">License Deletion</span></span>](license-deletion.md)                                             | <span data-ttu-id="dba37-147">Descreve como excluir licenças criadas localmente.</span><span class="sxs-lookup"><span data-stu-id="dba37-147">Describes how to delete locally created licenses.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="dba37-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dba37-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dba37-149">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="dba37-149">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




