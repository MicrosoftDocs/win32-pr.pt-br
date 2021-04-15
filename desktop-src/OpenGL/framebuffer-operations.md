---
title: Operações de framebuffer
description: Para selecionar o buffer no qual os valores de cores são gravados, use glDrawBuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Pipeline de processamento OpenGL, operações framebuffer
- framebuffers, operações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6199700d00a6628548404870dd6ef6ce3e2c825
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498647"
---
# <a name="framebuffer-operations"></a><span data-ttu-id="74d79-105">Operações de framebuffer</span><span class="sxs-lookup"><span data-stu-id="74d79-105">Framebuffer Operations</span></span>

<span data-ttu-id="74d79-106">Para selecionar o buffer no qual os valores de cores são gravados, use [**glDrawBuffer**](gldrawbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="74d79-106">To select the buffer into which color values are written, use [**glDrawBuffer**](gldrawbuffer.md).</span></span> <span data-ttu-id="74d79-107">Você usa quatro funções diferentes para mascarar a gravação de bits para cada um dos framebuffers lógicos após a execução de todas as operações por fragmento:</span><span class="sxs-lookup"><span data-stu-id="74d79-107">You use four different functions to mask the writing of bits to each of the logical framebuffers after all per-fragment operations have been performed:</span></span>

-   [<span data-ttu-id="74d79-108">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="74d79-108">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="74d79-109">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="74d79-109">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="74d79-110">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="74d79-110">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="74d79-111">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="74d79-111">**glStencilMask**</span></span>](glstencilmask.md)

<span data-ttu-id="74d79-112">A função [**glAccum**](glaccum.md) controla a operação do buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="74d79-112">The [**glAccum**](glaccum.md) function controls the operation of the accumulation buffer.</span></span> <span data-ttu-id="74d79-113">Por fim [**, glClear**](glclear.md) define cada pixel em um subconjunto especificado dos buffers para o valor especificado com [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)ou [**glClearAccum**](glclearaccum.md).</span><span class="sxs-lookup"><span data-stu-id="74d79-113">Finally, [**glClear**](glclear.md) sets every pixel in a specified subset of the buffers to the value specified with [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), or [**glClearAccum**](glclearaccum.md).</span></span>

 

 




