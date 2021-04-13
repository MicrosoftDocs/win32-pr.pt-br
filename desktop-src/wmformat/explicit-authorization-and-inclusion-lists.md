---
title: Autorização explícita e listas de inclusão
description: Autorização explícita e listas de inclusão
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- SDK do Windows Media Format, exportação de DRM
- SDK do Windows Media Format, exportar
- SDK do Windows Media Format, autorização explícita e listas de inclusão
- SDK do Windows Media Format, listas de autorização
- SDK do Windows Media Format, listas de inclusão
- DRM (gerenciamento de direitos digitais), exportar
- DRM (gerenciamento de direitos digitais), exportar
- DRM (gerenciamento de direitos digitais), autorização explícita e listas de inclusão
- DRM (gerenciamento de direitos digitais), autorização explícita e listas de inclusão
- DRM (gerenciamento de direitos digitais), listas de autorização
- DRM (gerenciamento de direitos digitais), listas de autorização
- DRM (gerenciamento de direitos digitais), listas de inclusão
- DRM (gerenciamento de direitos digitais), listas de inclusão
- APIs estendidas do cliente DRM, autorização explícita e listas de inclusão
- APIs estendidas do cliente, autorização explícita e listas de inclusão
- APIs estendidas do cliente DRM, listas de autorização
- APIs estendidas do cliente, listas de autorização
- APIs estendidas do cliente DRM, listas de inclusão
- APIs estendidas do cliente, listas de inclusão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2309bed28ffd3add2a75c1cd90488b9ef454659b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365547"
---
# <a name="explicit-authorization-and-inclusion-lists"></a><span data-ttu-id="59e16-122">Autorização explícita e listas de inclusão</span><span class="sxs-lookup"><span data-stu-id="59e16-122">Explicit Authorization and Inclusion Lists</span></span>

<span data-ttu-id="59e16-123">As licenças podem conter uma lista de inclusão para autorizar explicitamente a exportação de conteúdo protegido pelo Windows Media DRM para outros esquemas de proteção de conteúdo (CPS).</span><span class="sxs-lookup"><span data-stu-id="59e16-123">Licenses can contain an inclusion list to explicitly authorize the exporting of content protected by Windows Media DRM to other content protection schemes (CPS).</span></span> <span data-ttu-id="59e16-124">De acordo com os termos do contrato de licença que você insere com a Microsoft para habilitar a exportação de DRM, você pode exportar apenas para um CPS válido identificado na lista de inclusão de uma licença.</span><span class="sxs-lookup"><span data-stu-id="59e16-124">As per the terms of the license agreement you enter into with Microsoft to enable DRM Export you can export only to a valid CPS that is identified in the inclusion list of a license.</span></span>

<span data-ttu-id="59e16-125">Uma lista de inclusão é uma matriz vinculada de GUIDs (identificadores globais exclusivos) que cada uma representa um determinado CPS autorizado para o qual o conteúdo pode ser exportado.</span><span class="sxs-lookup"><span data-stu-id="59e16-125">An inclusion list is a bounded array of globally unique identifiers (GUIDs) that each represents a specific authorized CPS to which the content can be exported.</span></span> <span data-ttu-id="59e16-126">Os GUIDs listados em uma lista de inclusão são independentes dos níveis de proteção de saída (OPL) e dos níveis de proteção de conteúdo (CPL).</span><span class="sxs-lookup"><span data-stu-id="59e16-126">The GUIDs listed in an inclusion list are independent of the output protection levels (OPL) and content protection levels (CPL).</span></span> <span data-ttu-id="59e16-127">Impor essas restrições é de responsabilidade do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="59e16-127">Enforcing these restrictions is the responsibility of your application.</span></span>

> [!Note]  
> <span data-ttu-id="59e16-128">Ao executar a exportação do DRM do Windows Media no conteúdo compactado, você acessa a lista de inclusão por meio do método [**IWMDRMLicense:: inclusionlist**](iwmdrmlicense-getinclusionlist.md) .</span><span class="sxs-lookup"><span data-stu-id="59e16-128">When performing Windows Media DRM Export on compressed content, you access the inclusion list through the [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) method.</span></span> <span data-ttu-id="59e16-129">Ao executar a exportação do DRM do Windows Media em conteúdo descompactado, use o método [**IWMDRMReader3:: inclusionlist**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) .</span><span class="sxs-lookup"><span data-stu-id="59e16-129">When performing Windows Media DRM Export on uncompressed content, use the [**IWMDRMReader3::GetInclusionList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) method.</span></span>

 

<span data-ttu-id="59e16-130">Para registrar um novo sistema de proteção de conteúdo como uma exportação do DRM do Windows Media em regras de conformidade de exportação do Windows Media DRM, entre em contato com wmla@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="59e16-130">To register a new content protection system as a Windows Media DRM Permitted Export in the Windows Media DRM export compliance rules, please contact wmla@microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59e16-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="59e16-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59e16-132">**Exportação de DRM**</span><span class="sxs-lookup"><span data-stu-id="59e16-132">**DRM Export**</span></span>](drm-export.md)
</dt> </dl>

 

 




