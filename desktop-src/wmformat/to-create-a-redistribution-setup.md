---
title: Para criar uma configuração de redistribuição
description: Para criar uma configuração de redistribuição
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- SDK do Windows Media Format, redistribuição de software
- Formato de sistema avançado (ASF), redistribuição de software
- ASF (formato de sistemas avançados), redistribuição de software
- SDK do Windows Media Format, redistribuição
- Formato de sistema avançado (ASF), redistribuição
- ASF (formato de sistemas avançados), redistribuição
- redistribuição de software, criando
- redistribuição de software WMFDist.exe
- redistribuição, criando
- redistribuição, WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0c2f241d8c1ad164bc14608103f423a7aba78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159743"
---
# <a name="to-create-a-redistribution-setup"></a><span data-ttu-id="cdfa6-114">Para criar uma configuração de redistribuição</span><span class="sxs-lookup"><span data-stu-id="cdfa6-114">To Create a Redistribution Setup</span></span>

1.  <span data-ttu-id="cdfa6-115">Faça com que sua rotina de instalação instale os arquivos do aplicativo e faça as configurações necessárias antes de invocar o pacote de redistribuição.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-115">Have your setup routine install your application files and make required settings before invoking the redistribution package.</span></span>
2.  <span data-ttu-id="cdfa6-116">Instale o WMFDist.exe.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-116">Install WMFDist.exe.</span></span> <span data-ttu-id="cdfa6-117">Você pode usar o sinalizador/Q: a para fazer uma instalação silenciosa, autônoma e suprimir a interface do usuário da configuração de redistribuição durante a instalação do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-117">You can use the /Q:A flag to do a quiet, unattended installation and suppress the user interface of the redistribution setup during the installation of your application.</span></span> <span data-ttu-id="cdfa6-118">Sua rotina deve detectar se a reinicialização é necessária no final.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-118">Your routine must then detect whether restarting is needed at the end.</span></span>

    <span data-ttu-id="cdfa6-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="cdfa6-119">For example:</span></span>

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a><span data-ttu-id="cdfa6-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cdfa6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdfa6-121">**Redistribuição de software**</span><span class="sxs-lookup"><span data-stu-id="cdfa6-121">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




