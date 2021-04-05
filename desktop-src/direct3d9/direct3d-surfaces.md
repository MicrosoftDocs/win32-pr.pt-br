---
description: Uma superfície representa uma área linear da memória de vídeo e geralmente reside na memória de vídeo do cartão de vídeo, embora as superfícies possam existir na memória do sistema. As superfícies são gerenciadas pela interface IDirect3DSurface9.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Superfícies do Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08729cc7252c39ddf71048991a796469f2e8b0b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645624"
---
# <a name="direct3d-surfaces-direct3d-9"></a><span data-ttu-id="5b681-104">Superfícies do Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5b681-104">Direct3D Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="5b681-105">Uma superfície representa uma área linear da memória de vídeo e geralmente reside na memória de vídeo do cartão de vídeo, embora as superfícies possam existir na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="5b681-105">A surface represents a linear area of display memory and usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span> <span data-ttu-id="5b681-106">As superfícies são gerenciadas pela interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="5b681-106">Surfaces are managed by the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span>

-   <span data-ttu-id="5b681-107">Buffer frontal.</span><span class="sxs-lookup"><span data-stu-id="5b681-107">Front Buffer.</span></span> <span data-ttu-id="5b681-108">Um retângulo de memória que é convertido pelo adaptador gráfico e exibido no monitor.</span><span class="sxs-lookup"><span data-stu-id="5b681-108">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span> <span data-ttu-id="5b681-109">No Direct3D, um aplicativo nunca grava diretamente no buffer frontal.</span><span class="sxs-lookup"><span data-stu-id="5b681-109">In Direct3D an application never writes directly to the front buffer.</span></span>
-   <span data-ttu-id="5b681-110">Buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="5b681-110">Back Buffer.</span></span> <span data-ttu-id="5b681-111">Um retângulo de memória no qual um aplicativo pode gravar diretamente.</span><span class="sxs-lookup"><span data-stu-id="5b681-111">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="5b681-112">O buffer de fundo nunca é exibido diretamente no monitor.</span><span class="sxs-lookup"><span data-stu-id="5b681-112">The back buffer is never directly displayed on the monitor.</span></span>
-   <span data-ttu-id="5b681-113">Invertendo superfícies.</span><span class="sxs-lookup"><span data-stu-id="5b681-113">Flipping surfaces.</span></span> <span data-ttu-id="5b681-114">O processo de mover o buffer de fundo para o buffer frontal.</span><span class="sxs-lookup"><span data-stu-id="5b681-114">The process of moving the back buffer to the front buffer.</span></span>
-   <span data-ttu-id="5b681-115">Cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="5b681-115">Swap chain.</span></span> <span data-ttu-id="5b681-116">Uma coleção de um ou mais buffers de back-end que podem ser exibidos em série para o buffer frontal.</span><span class="sxs-lookup"><span data-stu-id="5b681-116">A collection of one or more back buffers that can be serially presented to the front buffer.</span></span>

## <a name="getting-a-surface"></a><span data-ttu-id="5b681-117">Obtendo uma superfície</span><span class="sxs-lookup"><span data-stu-id="5b681-117">Getting a Surface</span></span>

<span data-ttu-id="5b681-118">Crie uma superfície chamando qualquer um destes métodos:</span><span class="sxs-lookup"><span data-stu-id="5b681-118">Create a surface by calling any of these methods:</span></span>

-   [<span data-ttu-id="5b681-119">**CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="5b681-119">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="5b681-120">**CreateOffscreenPlainSurface**</span><span class="sxs-lookup"><span data-stu-id="5b681-120">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [<span data-ttu-id="5b681-121">**CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="5b681-121">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

<span data-ttu-id="5b681-122">Os formatos de superfície determinam como os dados de cada pixel na memória da superfície são interpretados.</span><span class="sxs-lookup"><span data-stu-id="5b681-122">Surface formats determine how data for each pixel in surface memory is interpreted.</span></span> <span data-ttu-id="5b681-123">O Direct3D usa o membro [D3DFORMAT](d3dformat.md) da [**estrutura \_ desc de D3DSURFACE**](d3dsurface-desc.md) para descrever o formato da superfície.</span><span class="sxs-lookup"><span data-stu-id="5b681-123">Direct3D uses the [D3DFORMAT](d3dformat.md) member of the [**D3DSURFACE\_DESC**](d3dsurface-desc.md) structure to describe the surface format.</span></span> <span data-ttu-id="5b681-124">Você pode recuperar o formato de uma superfície existente chamando o método [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) .</span><span class="sxs-lookup"><span data-stu-id="5b681-124">You can retrieve the format of an existing surface by calling the [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) method.</span></span>

<span data-ttu-id="5b681-125">Depois que uma superfície é criada, você pode obter um ponteiro para ela chamando qualquer um destes métodos:</span><span class="sxs-lookup"><span data-stu-id="5b681-125">Once a surface is created, you can get a pointer to it by calling any of these methods:</span></span>

-   [<span data-ttu-id="5b681-126">**GetCubeMapSurface**</span><span class="sxs-lookup"><span data-stu-id="5b681-126">**GetCubeMapSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [<span data-ttu-id="5b681-127">**GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="5b681-127">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="5b681-128">**GetDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="5b681-128">**GetDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [<span data-ttu-id="5b681-129">**GetFrontBufferData**</span><span class="sxs-lookup"><span data-stu-id="5b681-129">**GetFrontBufferData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [<span data-ttu-id="5b681-130">**GetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="5b681-130">**GetRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [<span data-ttu-id="5b681-131">**GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="5b681-131">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="5b681-132">**GetSurfaceLevel**</span><span class="sxs-lookup"><span data-stu-id="5b681-132">**GetSurfaceLevel**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

<span data-ttu-id="5b681-133">A interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) permite que você acesse a memória indiretamente por meio do método [**UpdateSurface**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="5b681-133">The [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface enables you to indirectly access memory through the [**UpdateSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="5b681-134">Esse método permite copiar uma região retangular de pixels de uma interface **IDirect3DSurface9** para outra interface **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="5b681-134">This method allows you to copy a rectangular region of pixels from one **IDirect3DSurface9** interface to another **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="5b681-135">A interface de superfície também tem métodos para acessar diretamente a memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5b681-135">The surface interface also has methods to directly access display memory.</span></span> <span data-ttu-id="5b681-136">Por exemplo, você pode usar o método [**LockRect**](/windows/desktop/api) para bloquear uma região retangular de memória de exibição.</span><span class="sxs-lookup"><span data-stu-id="5b681-136">For example, you can use the [**LockRect**](/windows/desktop/api) method to lock a rectangular region of display memory.</span></span> <span data-ttu-id="5b681-137">É importante chamar [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) depois que você terminar de trabalhar com a região retangular bloqueada na superfície.</span><span class="sxs-lookup"><span data-stu-id="5b681-137">It is important to call [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) after you are done working with the locked rectangular region on the surface.</span></span>

## <a name="additional-surface-topics"></a><span data-ttu-id="5b681-138">Tópicos de superfície adicionais</span><span class="sxs-lookup"><span data-stu-id="5b681-138">Additional Surface Topics</span></span>

<span data-ttu-id="5b681-139">Saiba mais sobre como usar superfícies com qualquer um destes tópicos:</span><span class="sxs-lookup"><span data-stu-id="5b681-139">Find out more about how to use surfaces with any of these topics:</span></span>

-   [<span data-ttu-id="5b681-140">Formatos de superfície (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5b681-140">Surface Formats (Direct3D 9)</span></span>](surface-formats.md)
-   [<span data-ttu-id="5b681-141">O que é uma cadeia de permuta? (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5b681-141">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
-   [<span data-ttu-id="5b681-142">Largura vs. pitch (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5b681-142">Width vs. Pitch (Direct3D 9)</span></span>](width-vs--pitch.md)
-   [<span data-ttu-id="5b681-143">Invertendo superfícies (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5b681-143">Flipping Surfaces (Direct3D 9)</span></span>](flipping-surfaces.md)
-   [<span data-ttu-id="5b681-144">Inversão de página e buffer de fundo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5b681-144">Page Flipping and Back Buffering (Direct3D 9)</span></span>](page-flipping-and-back-buffering.md)
-   [<span data-ttu-id="5b681-145">Copiando para superfícies (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5b681-145">Copying to Surfaces (Direct3D 9)</span></span>](copying-to-surfaces.md)
-   [<span data-ttu-id="5b681-146">Copiando superfícies (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5b681-146">Copying Surfaces (Direct3D 9)</span></span>](copying-surfaces.md)
-   [<span data-ttu-id="5b681-147">Acessando a memória da superfície diretamente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5b681-147">Accessing Surface Memory Directly (Direct3D 9)</span></span>](accessing-surface-memory-directly.md)
-   [<span data-ttu-id="5b681-148">Dados de superfície privada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5b681-148">Private Surface Data (Direct3D 9)</span></span>](private-surface-data.md)
-   [<span data-ttu-id="5b681-149">Controles gama (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5b681-149">Gamma Controls (Direct3D 9)</span></span>](gamma-controls.md)

## <a name="related-topics"></a><span data-ttu-id="5b681-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b681-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b681-151">Introdução</span><span class="sxs-lookup"><span data-stu-id="5b681-151">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
