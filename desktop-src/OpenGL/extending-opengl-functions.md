---
title: Estendendo funções OpenGL
description: A biblioteca OpenGL dá suporte a várias implementações de suas funções.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL no Windows, funções de extensão
- funções de extensão OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcbb59aa15a9690ac05728548f0d8073a334a2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916534"
---
# <a name="extending-opengl-functions"></a><span data-ttu-id="e0e25-105">Estendendo funções OpenGL</span><span class="sxs-lookup"><span data-stu-id="e0e25-105">Extending OpenGL Functions</span></span>

<span data-ttu-id="e0e25-106">A biblioteca OpenGL dá suporte a várias implementações de suas funções.</span><span class="sxs-lookup"><span data-stu-id="e0e25-106">The OpenGL library supports multiple implementations of its functions.</span></span> <span data-ttu-id="e0e25-107">Não há suporte necessariamente para funções de extensão com suporte em um contexto de renderização em um contexto de renderização diferente.</span><span class="sxs-lookup"><span data-stu-id="e0e25-107">Extension functions supported in one rendering context aren't necessarily supported in a different rendering context.</span></span> <span data-ttu-id="e0e25-108">Para um determinado contexto de renderização em um aplicativo usando funções de extensão, use apenas os endereços de função retornados pela função [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e0e25-108">For a given rendering context in an application using extension functions, use only the function addresses returned by the [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) function.</span></span>

 

 




