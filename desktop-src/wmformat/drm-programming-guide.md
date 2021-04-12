---
title: Guia de programação do cliente Microsoft Windows Media DRM
description: Guia de programação do cliente Microsoft Windows Media DRM
ms.assetid: e7b179b3-ed14-4ea0-9a00-9d96557a2e2e
keywords:
- SDK do Windows Media Format, APIs estendidas do cliente DRM
- SDK do Windows Media Format, APIs estendidas do cliente
- SDK do Windows Media Format, APIs estendidas
- SDK do Windows Media Format, APIs
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- SDK do Windows Media Format, guia de programação
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), guia de programação
- DRM (gerenciamento de direitos digitais), guia de programação
- APIs estendidas do cliente DRM, sobre
- APIs estendidas do cliente, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b338ea6ebd9cb132c8e6b1c76c8e1d7f6c6aa182
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454536"
---
# <a name="microsoft-windows-media-drm-client-programming-guide"></a><span data-ttu-id="03fdd-119">Guia de programação do cliente Microsoft Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="03fdd-119">Microsoft Windows Media DRM Client Programming Guide</span></span>

<span data-ttu-id="03fdd-120">Este guia fornece informações sobre como usar os recursos das APIs estendidas do cliente DRM do Windows Media em seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="03fdd-120">This guide provides information about using the features of the Windows Media DRM Client Extended APIs in your applications.</span></span> <span data-ttu-id="03fdd-121">As seções a seguir explicam, em detalhes, as etapas envolvidas na implementação de recursos DRM.</span><span class="sxs-lookup"><span data-stu-id="03fdd-121">The following sections explain, in detail, the steps involved in implementing DRM features.</span></span>



| <span data-ttu-id="03fdd-122">Seção</span><span class="sxs-lookup"><span data-stu-id="03fdd-122">Section</span></span>                                                                                                                          | <span data-ttu-id="03fdd-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="03fdd-123">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03fdd-124">Introdução</span><span class="sxs-lookup"><span data-stu-id="03fdd-124">Getting Started</span></span>](drm-getting-started.md)                                                                                       | <span data-ttu-id="03fdd-125">Fornece informações sobre como configurar projetos C++ que usam as APIs estendidas do cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="03fdd-125">Provides information about setting up C++ projects that use the Windows Media DRM Client Extended APIs.</span></span>    |
| [<span data-ttu-id="03fdd-126">Adquirindo licenças</span><span class="sxs-lookup"><span data-stu-id="03fdd-126">Acquiring Licenses</span></span>](acquiring-licenses.md)                                                                                     | <span data-ttu-id="03fdd-127">Descreve como obter licenças no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="03fdd-127">Describes how to get licenses on the client computer.</span></span>                                                      |
| [<span data-ttu-id="03fdd-128">Obtendo informações de licenças no repositório de licenças local</span><span class="sxs-lookup"><span data-stu-id="03fdd-128">Getting Information from Licenses in the Local License Store</span></span>](getting-information-from-licenses-in-the-local-license-store.md) | <span data-ttu-id="03fdd-129">Descreve como obter informações sobre direitos de conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="03fdd-129">Describes how to get information about rights for protected content.</span></span>                                       |
| [<span data-ttu-id="03fdd-130">Executando individualização de DRM</span><span class="sxs-lookup"><span data-stu-id="03fdd-130">Performing DRM Individualization</span></span>](performing-drm-individualization.md)                                                         | <span data-ttu-id="03fdd-131">Descreve como atualizar e individualizar o componente DRM no computador cliente para torná-lo mais seguro.</span><span class="sxs-lookup"><span data-stu-id="03fdd-131">Describes how to update and individualize the DRM component on the client computer to make it more secure.</span></span> |
| [<span data-ttu-id="03fdd-132">Exportação de DRM</span><span class="sxs-lookup"><span data-stu-id="03fdd-132">DRM Export</span></span>](drm-export.md)                                                                                                     | <span data-ttu-id="03fdd-133">Descreve como exportar conteúdo protegido pelo Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="03fdd-133">Describes how to export content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="03fdd-134">Importação de DRM</span><span class="sxs-lookup"><span data-stu-id="03fdd-134">DRM Import</span></span>](drm-import.md)                                                                                                     | <span data-ttu-id="03fdd-135">Descreve como importar conteúdo protegido pelo Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="03fdd-135">Describes how to import content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="03fdd-136">Revogação de licença</span><span class="sxs-lookup"><span data-stu-id="03fdd-136">License Revocation</span></span>](drm-license-revocation.md)                                                                                 | <span data-ttu-id="03fdd-137">Descreve como remover licenças do repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="03fdd-137">Describes how to remove licenses from the local license store.</span></span>                                             |
| [<span data-ttu-id="03fdd-138">Revogação e renovação de componentes automatizados</span><span class="sxs-lookup"><span data-stu-id="03fdd-138">Automated Component Revocation and Renewal</span></span>](automated-component-revocation-and-renewal.md)                                     | <span data-ttu-id="03fdd-139">Descreve o sistema de revogação automatizada e renovação do Windows Media DRM usando os habilitadores de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="03fdd-139">Describes the Windows Media DRM automated revocation and renewal system using content enablers.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="03fdd-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03fdd-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03fdd-141">**APIs estendidas do cliente DRM do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="03fdd-141">**Windows Media DRM Client Extended APIs**</span></span>](windows-media-drm-client-extended-apis.md)
</dt> <dt>

<span data-ttu-id="03fdd-142">[SDK do Windows Media Rights Manager](/previous-versions/ms986509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="03fdd-142">[Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10))</span></span>
</dt> </dl>

 

 
