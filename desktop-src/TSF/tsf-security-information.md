---
title: Estrutura de serviços de texto de considerações sobre segurança
description: Estrutura de serviços de texto de considerações sobre segurança
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- TSF (estrutura de serviços de texto), segurança
- TSF (estrutura de serviços de texto), segurança
- serviços de texto, segurança
- Aplicativos habilitados para TSF, segurança
- segurança para TSF
- TSF (estrutura de serviços de texto), práticas recomendadas
- TSF (estrutura de serviços de texto), práticas recomendadas
- Aplicativos habilitados para TSF, práticas recomendadas
- serviços de texto, práticas recomendadas
- práticas recomendadas para TSF
- TSF (estrutura de serviços de texto), verificação de erros
- TSF (estrutura de serviços de texto), verificação de erros
- Aplicativos habilitados para TSF, verificação de erros
- serviços de texto, verificação de erros
- verificação de erros
- TSF (estrutura de serviços de texto), assinaturas digitais
- TSF (estrutura de serviços de texto), assinaturas digitais
- serviços de texto, assinaturas digitais
- Aplicativos habilitados para TSF, assinaturas digitais
- assinaturas digitais
- TSF (estrutura de serviços de texto), chamadas LoadLibrary
- TSF (estrutura de serviços de texto), chamadas LoadLibrary
- serviços de texto, chamadas LoadLibrary
- Aplicativos habilitados para TSF, chamadas LoadLibrary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d71966106cde0f59d39442f7e2bf9b2a216cd94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105758123"
---
# <a name="security-considerations-text-services-framework"></a><span data-ttu-id="08bd7-127">Considerações de segurança: estrutura de serviços de texto</span><span class="sxs-lookup"><span data-stu-id="08bd7-127">Security Considerations: Text Services Framework</span></span>

## <a name="best-practices-for-developing-with-tsf"></a><span data-ttu-id="08bd7-128">Práticas recomendadas para o desenvolvimento com o TSF</span><span class="sxs-lookup"><span data-stu-id="08bd7-128">Best Practices for Developing with TSF</span></span>

-   <span data-ttu-id="08bd7-129">**Assinaturas digitais:** Os provedores de serviço de texto devem fornecer assinaturas digitais com seus executáveis binários.</span><span class="sxs-lookup"><span data-stu-id="08bd7-129">**Digital Signatures:** Text service providers should provide digital signatures with their binary executables.</span></span> <span data-ttu-id="08bd7-130">Um serviço de texto registrado tem acesso a threads do sistema e pode expor informações que, de outra forma, não seriam acessíveis.</span><span class="sxs-lookup"><span data-stu-id="08bd7-130">A registered text service has access to system threads and could expose information that would otherwise not be accessible.</span></span> <span data-ttu-id="08bd7-131">Para ajudar a garantir uma operação estável e segura, o usuário deve verificar a assinatura digital de um serviço de texto antes que o serviço de texto tenha permissão para ser carregado.</span><span class="sxs-lookup"><span data-stu-id="08bd7-131">To help ensure stable and secure operation, the user should verify the digital signature of a text service before the text service is allowed to load.</span></span> <span data-ttu-id="08bd7-132">Consulte [introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) para obter o procedimento adequado para criar uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="08bd7-132">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) for the proper procedure to create a digital signature.</span></span>
-   <span data-ttu-id="08bd7-133">**Verificação de erro:** Cada método ou chamada de função deve ser verificada em busca de sucesso.</span><span class="sxs-lookup"><span data-stu-id="08bd7-133">**Error Checking:** Each method or function call should be checked for success.</span></span> <span data-ttu-id="08bd7-134">Em caso de falha, o método ou as chamadas de função restantes devem ser ignorados.</span><span class="sxs-lookup"><span data-stu-id="08bd7-134">In the event of failure, the remaining method or function calls should be skipped.</span></span> <span data-ttu-id="08bd7-135">A maioria dos exemplos de código nesta documentação tem verificação de erro limitada, ou nenhum, para evitar o disfarce do ponto a ser ilustrado.</span><span class="sxs-lookup"><span data-stu-id="08bd7-135">Most of the code examples in this documentation have limited error checking, or none at all, to avoid obscuring the point to be illustrated.</span></span> <span data-ttu-id="08bd7-136">Você não deve colar exemplos da documentação diretamente no código de produção; em vez disso, você deve aprimorar os exemplos adicionando sua própria verificação de erro.</span><span class="sxs-lookup"><span data-stu-id="08bd7-136">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

-   <span data-ttu-id="08bd7-137">**Chamadas LoadLibrary:** Para obter um ponteiro para qualquer uma das [funções de TSF](text-services-framework-functions.md), você precisará usar [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="08bd7-137">**LoadLibrary Calls:** To obtain a pointer to any of the [TSF functions](text-services-framework-functions.md), you will need to use [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="08bd7-138">No entanto, é importante seguir os procedimentos para formatar o nome do caminho da DLL, conforme fornecido na documentação **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="08bd7-138">However, it is important to follow procedures for formatting the DLL path name, as given in **LoadLibrary** documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08bd7-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08bd7-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08bd7-140">Práticas recomendadas de segurança</span><span class="sxs-lookup"><span data-stu-id="08bd7-140">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

<span data-ttu-id="08bd7-141">[Introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08bd7-141">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="08bd7-142">Funções de TSF</span><span class="sxs-lookup"><span data-stu-id="08bd7-142">TSF functions</span></span>](text-services-framework-functions.md)
</dt> <dt>

[<span data-ttu-id="08bd7-143">LoadLibrary</span><span class="sxs-lookup"><span data-stu-id="08bd7-143">LoadLibrary</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="08bd7-144">GetProcAddress</span><span class="sxs-lookup"><span data-stu-id="08bd7-144">GetProcAddress</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 