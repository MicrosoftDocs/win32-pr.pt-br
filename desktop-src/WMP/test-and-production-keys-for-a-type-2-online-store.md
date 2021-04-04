---
title: Chaves de teste e de produção para uma loja online tipo 2
description: Chaves de teste e de produção para uma loja online tipo 2
ms.assetid: 4fce47e2-d73d-4484-9bda-48257268ed96
keywords:
- Armazenamentos online do Windows Media Player, chaves de teste
- lojas online, chaves de teste
- tipo 2 lojas online, chaves de teste
- Lojas online do Windows Media Player, chaves de produção
- lojas online, chaves de produção
- tipo 2 lojas online, chaves de produção
- Repositórios online do Windows Media Player, documento do serviceInfo
- repositórios online, documento do serviceInfo
- tipo 2 lojas online, documento do serviceInfo
- chaves de teste
- chaves de produção
- Documento do serviceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f009e1b0ca58a66820e193e3b66f8ca50ccadc43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916545"
---
# <a name="test-and-production-keys-for-a-type-2-online-store"></a><span data-ttu-id="5abc9-115">Chaves de teste e de produção para uma loja online tipo 2</span><span class="sxs-lookup"><span data-stu-id="5abc9-115">Test and Production Keys for a Type 2 Online Store</span></span>

<span data-ttu-id="5abc9-116">Quando você começa o desenvolvimento de sua loja online, a Microsoft fornece duas chaves numéricas: uma chave de teste e uma chave de produção.</span><span class="sxs-lookup"><span data-stu-id="5abc9-116">When you begin development of your online store, Microsoft provides you with two numeric keys: a test key and a production key.</span></span> <span data-ttu-id="5abc9-117">Ao mesmo tempo, você deve fornecer à Microsoft duas URLs: uma que aponte para o documento de informações de teste e outra que aponte para seu documento de informações de produção.</span><span class="sxs-lookup"><span data-stu-id="5abc9-117">At the same time, you must provide Microsoft with two URLs: one that points to your test ServiceInfo document and one that points to your production ServiceInfo document.</span></span>

<span data-ttu-id="5abc9-118">Durante o estágio de desenvolvimento e teste, sua loja online ficará visível no Windows Media Player somente se sua chave de teste ou sua chave de produção estiver no registro no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="5abc9-118">During the development and testing stage, your online store is visible in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="5abc9-119">Se a chave de teste estiver no registro, o Windows Media Player recuperará seu documento de informações de teste, que aponta para o plug-in, as páginas da Web e as imagens que pertencem ao seu repositório de teste.</span><span class="sxs-lookup"><span data-stu-id="5abc9-119">If your test key is in the registry, Windows Media Player retrieves your test ServiceInfo document, which points to the plug-in, webpages, and images that belong to your test store.</span></span> <span data-ttu-id="5abc9-120">Se a chave de produção estiver no registro, o Windows Media Player recuperará o documento de informações de produção, que aponta para o plug-in, as páginas da Web e as imagens que pertencem à sua loja de produção.</span><span class="sxs-lookup"><span data-stu-id="5abc9-120">If your production key is in the registry, Windows Media Player retrieves your production ServiceInfo document, which points to the plug-in, webpages, and images that belong to your production store.</span></span>

<span data-ttu-id="5abc9-121">Você pode usar seus armazenamentos de teste e produção de qualquer maneira que achar útil.</span><span class="sxs-lookup"><span data-stu-id="5abc9-121">You can use your test and production stores in any way you find useful.</span></span> <span data-ttu-id="5abc9-122">Normalmente, no entanto, a distinção é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="5abc9-122">Typically, however, the distinction is as follows:</span></span>

-   <span data-ttu-id="5abc9-123">Seu repositório de teste é o local onde você faz alterações diárias em seu plug-in, páginas da Web, imagens e outros componentes do seu serviço.</span><span class="sxs-lookup"><span data-stu-id="5abc9-123">Your test store is the place where you make daily changes to your plug-in, webpages, images, and other components of your service.</span></span>
-   <span data-ttu-id="5abc9-124">Sua loja de produção é o local onde você mantém uma liberação estável do seu serviço, que inclui seu plug-in, páginas da Web, imagens e outros componentes.</span><span class="sxs-lookup"><span data-stu-id="5abc9-124">Your production store is the place where you keep a stable release of your service, which includes your plug-in, webpages, images, and other components.</span></span>

<span data-ttu-id="5abc9-125">Antes que sua loja online possa ser publicada no Windows Media Player, a Microsoft deve validar que o serviço é executado corretamente.</span><span class="sxs-lookup"><span data-stu-id="5abc9-125">Before your online store can be published in Windows Media Player, Microsoft must validate that your service performs correctly.</span></span> <span data-ttu-id="5abc9-126">Durante a fase de validação, a Microsoft usa sua chave de produção.</span><span class="sxs-lookup"><span data-stu-id="5abc9-126">During the validation phase, Microsoft uses your production key.</span></span> <span data-ttu-id="5abc9-127">A Microsoft não usa sua chave de teste durante a fase de validação.</span><span class="sxs-lookup"><span data-stu-id="5abc9-127">Microsoft does not use your test key during the validation phase.</span></span>

<span data-ttu-id="5abc9-128">Quando seu armazenamento online de produção conclui com êxito o processo de validação, a Microsoft publica sua loja, o que significa que sua loja de produção aparece no Windows Media Player para todos os usuários, não apenas aqueles que têm sua chave de produção no registro.</span><span class="sxs-lookup"><span data-stu-id="5abc9-128">When your production online store successfully completes the validation process, Microsoft publishes your store, which means that your production store appears in Windows Media Player for all users, not just the ones who have your production key in the registry.</span></span> <span data-ttu-id="5abc9-129">Depois que o armazenamento é publicado, as chaves de teste e de produção não são mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="5abc9-129">After your store is published, the test and production keys are no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="5abc9-130">Os usuários podem adivinhar a chave de teste ou de produção para sua loja online e exibir sua loja enquanto ela está sendo desenvolvida.</span><span class="sxs-lookup"><span data-stu-id="5abc9-130">Users might be able to guess the test or production key for your online store and view your store while it is being developed.</span></span> <span data-ttu-id="5abc9-131">Você deve ter cuidado ao expor os recursos que deseja manter secretos até a liberação pública.</span><span class="sxs-lookup"><span data-stu-id="5abc9-131">You should be careful about exposing features that you want to keep secret until public release.</span></span>

 

<span data-ttu-id="5abc9-132">Para obter informações detalhadas sobre onde colocar suas chaves de produção e teste no registro do usuário, consulte [chaves e entradas do registro para uma loja online tipo 2](registry-keys-and-entries-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="5abc9-132">For detailed information about where to put your production and test keys in the user's registry, see [Registry Keys and Entries for a Type 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5abc9-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5abc9-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5abc9-134">**Sobre as lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="5abc9-134">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="5abc9-135">**Tipo 2 amostras de loja online**</span><span class="sxs-lookup"><span data-stu-id="5abc9-135">**Type 2 Online Store Samples**</span></span>](type-2-online-store-samples.md)
</dt> </dl>

 

 




