---
title: Funções de buffer
description: Para copiar o conteúdo de um buffer fora da tela para um buffer na tela, chame SwapBuffers.
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- Funções WGL, buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a93858b8085171a9139bc5ab329e531ddbb699
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105757750"
---
# <a name="buffer-functions"></a><span data-ttu-id="d611d-104">Funções de buffer</span><span class="sxs-lookup"><span data-stu-id="d611d-104">Buffer Functions</span></span>

<span data-ttu-id="d611d-105">Para copiar o conteúdo de um buffer fora da tela para um buffer na tela, chame [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="d611d-105">To copy the contents of an off-screen buffer to an on-screen buffer, call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="d611d-106">A função **SwapBuffers** usa um identificador para um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d611d-106">The **SwapBuffers** function takes a handle to a device context.</span></span> <span data-ttu-id="d611d-107">O formato de pixel atual para o contexto de dispositivo especificado deve incluir um buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="d611d-107">The current pixel format for the specified device context must include a back buffer.</span></span> <span data-ttu-id="d611d-108">Por padrão, o buffer de fundo está fora da tela e o buffer frontal está na tela.</span><span class="sxs-lookup"><span data-stu-id="d611d-108">By default, the back buffer is off-screen, and the front buffer is on-screen.</span></span>

> [!Note]  
> <span data-ttu-id="d611d-109">A função **SwapBuffers** não troca de fato o conteúdo dos dois buffers, mas copia o conteúdo de um buffer para outro.</span><span class="sxs-lookup"><span data-stu-id="d611d-109">The **SwapBuffers** function does not really swap the contents of the two buffers, but rather copies the contents of one buffer to another.</span></span> <span data-ttu-id="d611d-110">O conteúdo do buffer fora da tela é indefinido após uma chamada para **SwapBuffers**.</span><span class="sxs-lookup"><span data-stu-id="d611d-110">The contents of the off-screen buffer are undefined after a call to **SwapBuffers**.</span></span> <span data-ttu-id="d611d-111">Assim, o resultado de duas chamadas consecutivas para **SwapBuffers** é indefinido.</span><span class="sxs-lookup"><span data-stu-id="d611d-111">Thus, the result of two consecutive calls to **SwapBuffers** is undefined.</span></span>

 

<span data-ttu-id="d611d-112">A ilustração a seguir mostra como o conteúdo dos buffers é copiado ao chamar **SwapBuffers**.</span><span class="sxs-lookup"><span data-stu-id="d611d-112">The following illustration shows how the contents of the buffers are copied when calling **SwapBuffers**.</span></span>

![Diagrama mostrando os resultados indefinidos de chamadas consecutivas para a função SwapBuffers.](images/opengl00.png)

<span data-ttu-id="d611d-114">Várias funções de núcleo OpenGL também gerenciam buffers.</span><span class="sxs-lookup"><span data-stu-id="d611d-114">Several OpenGL core functions also manage buffers.</span></span> <span data-ttu-id="d611d-115">A função [**glDrawBuffer**](gldrawbuffer.md) é a mais relevante para o buffer duplo; Ele especifica o framebuffer ou os buffers que o OpenGL desenha.</span><span class="sxs-lookup"><span data-stu-id="d611d-115">The [**glDrawBuffer**](gldrawbuffer.md) function is the one most relevant to double buffering; it specifies the framebuffer or buffers that OpenGL draws into.</span></span>

<span data-ttu-id="d611d-116">As funções a seguir também afetam os buffers:</span><span class="sxs-lookup"><span data-stu-id="d611d-116">The following functions also affect buffers:</span></span>

-   [<span data-ttu-id="d611d-117">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="d611d-117">**glReadBuffer**</span></span>](glreadbuffer.md)
-   [<span data-ttu-id="d611d-118">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="d611d-118">**glReadPixels**</span></span>](glreadpixels.md)
-   [<span data-ttu-id="d611d-119">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="d611d-119">**glCopyPixels**</span></span>](glcopypixels.md)
-   [<span data-ttu-id="d611d-120">**glAccum**</span><span class="sxs-lookup"><span data-stu-id="d611d-120">**glAccum**</span></span>](glaccum.md)
-   [<span data-ttu-id="d611d-121">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="d611d-121">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="d611d-122">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="d611d-122">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="d611d-123">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="d611d-123">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="d611d-124">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="d611d-124">**glStencilMask**</span></span>](glstencilmask.md)
-   [<span data-ttu-id="d611d-125">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="d611d-125">**glClearAccum**</span></span>](glclearaccum.md)
-   [<span data-ttu-id="d611d-126">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="d611d-126">**glClearColor**</span></span>](glclearcolor.md)
-   [<span data-ttu-id="d611d-127">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="d611d-127">**glClearDepth**</span></span>](glcleardepth.md)
-   [<span data-ttu-id="d611d-128">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="d611d-128">**glClearIndex**</span></span>](glclearindex.md)
-   [<span data-ttu-id="d611d-129">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="d611d-129">**glClearStencil**</span></span>](glclearstencil.md)

 

 




