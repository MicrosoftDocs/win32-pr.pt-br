---
title: Adquirindo licenças
description: Adquirindo licenças
ms.assetid: dde33d57-6c63-4e1a-8398-5db466fb22fa
keywords:
- SDK do Windows Media Format, APIs estendidas do cliente DRM
- SDK do Windows Media Format, APIs estendidas do cliente
- SDK do Windows Media Format, APIs estendidas
- SDK do Windows Media Format, APIs
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- Windows Media Format SDK, adquirindo licenças
- SDK do Windows Media Format, licenças
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), aquisição de licenças
- DRM (gerenciamento de direitos digitais), aquisição de licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- APIs estendidas do cliente DRM, adquirindo licenças
- APIs estendidas do cliente, adquirindo licenças
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c024789823ca0cd1b38959d78535ce71e2514897
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363689"
---
# <a name="acquiring-licenses"></a><span data-ttu-id="1c855-122">Adquirindo licenças</span><span class="sxs-lookup"><span data-stu-id="1c855-122">Acquiring Licenses</span></span>

<span data-ttu-id="1c855-123">Um cenário comum para adquirir licenças é quando um usuário tem um arquivo de mídia do Windows protegido e tenta acessar o conteúdo pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="1c855-123">A common scenario for acquiring licenses is when a user has a protected Windows Media file and tries to access the content for the first time.</span></span> <span data-ttu-id="1c855-124">Como as APIs estendidas do cliente DRM do Windows Media são separadas das rotinas de manipulação de arquivos ASF, o cenário de aquisição de licença básica, embora com suporte, requer mais chamadas à API do que usar o SDK do Windows Media Format e o SDK do Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1c855-124">Because the Windows Media DRM Client Extended APIs are separate from ASF file handling routines, the basic license acquisition scenario, while supported, requires more API calls than using the Windows Media Format SDK and the Media Foundation SDK.</span></span>

<span data-ttu-id="1c855-125">Esta seção descreve como usar as APIs estendidas do cliente DRM do Windows Media para adquirir licenças armazenadas no repositório de licenças local em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="1c855-125">This section describes how to use the Windows Media DRM Client Extended APIs to acquire licenses that are stored in the local license store on a client computer.</span></span> <span data-ttu-id="1c855-126">Ele contém os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="1c855-126">It contains the following topics.</span></span>



| <span data-ttu-id="1c855-127">Tópico</span><span class="sxs-lookup"><span data-stu-id="1c855-127">Topic</span></span>                                                                | <span data-ttu-id="1c855-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c855-128">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c855-129">Aquisição de licença silenciosa</span><span class="sxs-lookup"><span data-stu-id="1c855-129">Silent License Acquisition</span></span>](silent-license-acquisition.md)         | <span data-ttu-id="1c855-130">Descreve como adquirir licenças sem intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="1c855-130">Describes how to acquire licenses without user intervention.</span></span>                                                                               |
| [<span data-ttu-id="1c855-131">Aquisição de licença não silenciosa</span><span class="sxs-lookup"><span data-stu-id="1c855-131">Non-Silent License Acquisition</span></span>](non-silent-license-acquisition.md) | <span data-ttu-id="1c855-132">Descreve como adquirir licenças quando a intervenção do usuário (como pagar pelo conteúdo) é necessária.</span><span class="sxs-lookup"><span data-stu-id="1c855-132">Describes how to acquire licenses when user intervention (such as paying for the content) is required.</span></span>                                     |
| [<span data-ttu-id="1c855-133">Pré-entrega de licença</span><span class="sxs-lookup"><span data-stu-id="1c855-133">License Pre-Delivery</span></span>](license-pre-delivery.md)                     | <span data-ttu-id="1c855-134">Descreve como efetuar pull de licenças de um servidor de licença para um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="1c855-134">Describes how to pull licenses from a license server to a client computer.</span></span>                                                                 |
| [<span data-ttu-id="1c855-135">Criando licenças localmente</span><span class="sxs-lookup"><span data-stu-id="1c855-135">Creating Licenses Locally</span></span>](creating-licenses-locally.md)           | <span data-ttu-id="1c855-136">Descreve como criar suas próprias licenças sem baixá-las de um servidor de licenças e como armazená-las no repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="1c855-136">Describes how to create your own licenses without downloading them from a license server and how to store them in the local license store.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1c855-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c855-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c855-138">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="1c855-138">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




