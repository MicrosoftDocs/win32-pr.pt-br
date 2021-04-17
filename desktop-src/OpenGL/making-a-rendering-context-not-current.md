---
title: Fazendo um contexto de renderização não atual
description: Para desanexar um contexto de renderização de um thread, torne-o não atual. Você pode fazer isso chamando a função wglMakeCurrent com os parâmetros definidos como NULL. Veja a seguir um exemplo dessa tarefa simples.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL no Windows, contextos de renderização
- contextos de renderização OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12b3e0184a606faef7792b990d674054c5ddf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292067"
---
# <a name="making-a-rendering-context-not-current"></a><span data-ttu-id="00ecd-107">Fazendo um contexto de renderização não atual</span><span class="sxs-lookup"><span data-stu-id="00ecd-107">Making a Rendering Context Not Current</span></span>

<span data-ttu-id="00ecd-108">Para desanexar um contexto de renderização de um thread, torne-o não atual.</span><span class="sxs-lookup"><span data-stu-id="00ecd-108">To detach a rendering context from a thread, make it not current.</span></span> <span data-ttu-id="00ecd-109">Você pode fazer isso chamando a função [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) com os parâmetros definidos como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="00ecd-109">You can do this by calling the [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) function with the parameters set to **NULL**.</span></span> <span data-ttu-id="00ecd-110">Veja a seguir um exemplo dessa tarefa simples.</span><span class="sxs-lookup"><span data-stu-id="00ecd-110">The following is a sample of this simple task.</span></span>

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




