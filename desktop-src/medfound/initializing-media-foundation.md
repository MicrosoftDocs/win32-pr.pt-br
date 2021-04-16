---
description: Inicializando Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Inicializando Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb876ec3493d6c4fac1c2f6d6757ef647c511a98
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105768613"
---
# <a name="initializing-media-foundation"></a><span data-ttu-id="4ebbc-103">Inicializando Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ebbc-103">Initializing Media Foundation</span></span>

<span data-ttu-id="4ebbc-104">Antes de usar qualquer Microsoft Media Foundation objetos ou interfaces, você deve chamar a função [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .</span><span class="sxs-lookup"><span data-stu-id="4ebbc-104">Before using any Microsoft Media Foundation objects or interfaces, you must call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="4ebbc-105">Passe a versão constante **MF \_**.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-105">Pass in the constant **MF\_VERSION**.</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



<span data-ttu-id="4ebbc-106">A função [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) Inicializa a plataforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-106">The [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function initializes the Media Foundation platform.</span></span> <span data-ttu-id="4ebbc-107">Se **MFStartup** retornar MF \_ e \_ \_ versão de inicialização inválida \_ , significa que seu aplicativo foi compilado usando uma versão dos cabeçalhos de Media Foundation que não corresponde ao Media Foundation DLLs no seu sistema.</span><span class="sxs-lookup"><span data-stu-id="4ebbc-107">If **MFStartup** returns MF\_E\_BAD\_STARTUP\_VERSION, it means your application was compiled using a version of the Media Foundation headers that does not match the Media Foundation DLLs on your system.</span></span>

<span data-ttu-id="4ebbc-108">Para cada chamada para [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), seu aplicativo deve chamar [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="4ebbc-108">For every call to [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), your application must call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>


```C++
MFShutdown();
```



## <a name="related-topics"></a><span data-ttu-id="4ebbc-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4ebbc-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ebbc-110">Arquitetura Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ebbc-110">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="4ebbc-111">APIs da plataforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ebbc-111">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



