---
title: Compartilhando listas de exibição
description: Quando você cria um contexto de renderização, ele tem seu próprio espaço de lista de exibição.
ms.assetid: 8ace5684-a27b-4d6e-a80b-58a0b7064879
keywords:
- OpenGL no Windows, compartilhando listas de exibição
- compartilhando listas de exibição OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d8d012e8e04455f76ca5d7bfe74229ac0b0ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292704"
---
# <a name="sharing-display-lists"></a><span data-ttu-id="7d0d4-105">Compartilhando listas de exibição</span><span class="sxs-lookup"><span data-stu-id="7d0d4-105">Sharing Display Lists</span></span>

<span data-ttu-id="7d0d4-106">Quando você cria um contexto de renderização, ele tem seu próprio espaço de lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="7d0d4-106">When you create a rendering context, it has its own display-list space.</span></span> <span data-ttu-id="7d0d4-107">A função [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) permite que um contexto de renderização Compartilhe o espaço da lista de exibição de outro contexto de renderização.</span><span class="sxs-lookup"><span data-stu-id="7d0d4-107">The [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) function enables a rendering context to share the display-list space of another rendering context.</span></span> <span data-ttu-id="7d0d4-108">Qualquer número de contextos de renderização pode compartilhar um único espaço de lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="7d0d4-108">Any number of rendering contexts can share a single display-list space.</span></span>

 

 




