---
title: Importando e exportando conteúdo protegido por DRM
description: Importando e exportando conteúdo protegido por DRM
ms.assetid: 1c0520dd-b698-4174-a70e-32f43e2395b1
keywords:
- SDK do Windows Media Format, APIs estendidas do cliente DRM
- SDK do Windows Media Format, APIs estendidas do cliente
- SDK do Windows Media Format, APIs estendidas
- SDK do Windows Media Format, APIs
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- SDK do Windows Media Format, importar
- SDK do Windows Media Format, exportar
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), importando conteúdo protegido
- DRM (gerenciamento de direitos digitais), importando conteúdo protegido
- DRM (gerenciamento de direitos digitais), exportando conteúdo protegido
- DRM (gerenciamento de direitos digitais), exportando conteúdo protegido
- APIs estendidas do cliente DRM, sobre
- APIs estendidas do cliente, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f368417b62c9746b6d2c9e331b9cd849455b8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636856"
---
# <a name="importing-and-exporting-drm-protected-content"></a><span data-ttu-id="5438a-122">Importando e exportando conteúdo protegido por DRM</span><span class="sxs-lookup"><span data-stu-id="5438a-122">Importing and Exporting DRM Protected Content</span></span>

<span data-ttu-id="5438a-123">Uma das principais funções das novas APIs estendidas do cliente DRM do Windows Media é habilitar a importação e a exportação de conteúdo protegido por DRM para sistemas de gerenciamento de direitos de terceiros.</span><span class="sxs-lookup"><span data-stu-id="5438a-123">One of the primary roles of the new Windows Media DRM Client Extended APIs is to enable the import and export of DRM-protected content to third-party rights management systems.</span></span>

<span data-ttu-id="5438a-124">O principal desafio de importar e exportar dados protegidos em seu aplicativo é compartilhar robustamente os exemplos de dados ASF entre o sistema e o subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="5438a-124">The primary challenge of importing and exporting protected data in your application is to robustly share ASF data samples between your system and the DRM subsystem.</span></span> <span data-ttu-id="5438a-125">Quando seu aplicativo manipula amostras de dados, ele precisa garantir que determinados padrões de robustez sejam atendidos para evitar o potencial para que o mecanismo de proteção seja burlado.</span><span class="sxs-lookup"><span data-stu-id="5438a-125">When your application handles data samples it has to assure that certain robustness standards are met to avoid the potential for the protection mechanism to be circumvented.</span></span> <span data-ttu-id="5438a-126">Esses padrões são descritos nas regras de robustez e de conformidade que você concorda ao licenciar o DRM.</span><span class="sxs-lookup"><span data-stu-id="5438a-126">These standards are outlined in the robustness and compliance rules that you agree to when you license DRM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5438a-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5438a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5438a-128">**Sobre as APIs estendidas do cliente DRM do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5438a-128">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




