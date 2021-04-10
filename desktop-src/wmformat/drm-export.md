---
title: Exportação de DRM
description: Exportação de DRM
ms.assetid: 0b44f2e5-e63c-4bdb-8123-097a5d5e3756
keywords:
- SDK do Windows Media Format, APIs estendidas do cliente DRM
- SDK do Windows Media Format, APIs estendidas do cliente
- SDK do Windows Media Format, APIs estendidas
- SDK do Windows Media Format, APIs
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- SDK do Windows Media Format, exportação de DRM
- SDK do Windows Media Format, exportar
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), exportar
- DRM (gerenciamento de direitos digitais), exportar
- APIs estendidas do cliente DRM, exportar
- APIs estendidas do cliente, exportar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2917cfd0c9042f4547540618b44ed4c2f324edb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292255"
---
# <a name="drm-export"></a><span data-ttu-id="1172f-120">Exportação de DRM</span><span class="sxs-lookup"><span data-stu-id="1172f-120">DRM Export</span></span>

<span data-ttu-id="1172f-121">A funcionalidade de exportação do DRM do Windows Media permite que você crie aplicativos licenciados que descriptografam o conteúdo protegido pelo DRM do Windows Media e criptografe novamente em um esquema de proteção de conteúdo de saída (CPS) especificado explicitamente pelo emissor de licença associado.</span><span class="sxs-lookup"><span data-stu-id="1172f-121">Windows Media DRM export functionality enables you to create licensed applications that decrypt content protected by Windows Media DRM, and re-encrypt in an output content protection scheme (CPS) explicitly specified by the associated license issuer.</span></span> <span data-ttu-id="1172f-122">O emissor da licença autoriza explicitamente a exportação de conteúdo para um CPS específico por meio de uma lista de inclusão.</span><span class="sxs-lookup"><span data-stu-id="1172f-122">The license issuer explicitly authorizes the export of content to a specific CPS through an inclusion list.</span></span>

> [!Note]  
> <span data-ttu-id="1172f-123">Para acessar a funcionalidade de exportação, você deve se inscrever para um [certificado de aplicativo de exportação](export-application-certificate.md) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1172f-123">To access export functionality, you must apply for an [Export Application Certificate](export-application-certificate.md) from Microsoft.</span></span>

 

<span data-ttu-id="1172f-124">A funcionalidade de exportação do DRM do Windows Media é explicada nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="1172f-124">Windows Media DRM export functionality is explained in the following sections.</span></span>



| <span data-ttu-id="1172f-125">Seção</span><span class="sxs-lookup"><span data-stu-id="1172f-125">Section</span></span>                                                                                      | <span data-ttu-id="1172f-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="1172f-126">Description</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1172f-127">Exportar certificado de aplicativo</span><span class="sxs-lookup"><span data-stu-id="1172f-127">Export Application Certificate</span></span>](export-application-certificate.md)                         | <span data-ttu-id="1172f-128">Descreve um certificado de aplicativo de exportação.</span><span class="sxs-lookup"><span data-stu-id="1172f-128">Describes an export application certificate.</span></span>                                                        |
| [<span data-ttu-id="1172f-129">Autorização explícita e listas de inclusão</span><span class="sxs-lookup"><span data-stu-id="1172f-129">Explicit Authorization and Inclusion Lists</span></span>](explicit-authorization-and-inclusion-lists.md) | <span data-ttu-id="1172f-130">Explica o processo de autorização explícita e como as inclusões de lista funcionam.</span><span class="sxs-lookup"><span data-stu-id="1172f-130">Explains the process of explicit authorization, and how inclusions lists work.</span></span>                      |
| [<span data-ttu-id="1172f-131">Exportando conteúdo compactado</span><span class="sxs-lookup"><span data-stu-id="1172f-131">Exporting Compressed Content</span></span>](exporting-compressed-content.md)                             | <span data-ttu-id="1172f-132">Descreve como exportar conteúdo compactado do conteúdo de áudio ou vídeo protegido por DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1172f-132">Describes how to export compressed content from Windows Media DRM protected audio or video content.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1172f-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1172f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1172f-134">**Autorização explícita e listas de inclusão**</span><span class="sxs-lookup"><span data-stu-id="1172f-134">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="1172f-135">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="1172f-135">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




