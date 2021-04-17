---
title: Como recortar com um Axis-Aligned retângulo
description: Mostra como recortar uma região com um retângulo de clipe alinhado por eixo.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9fea904f9df396918d2cdfdb5205f6dd0197d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104570621"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a><span data-ttu-id="51252-103">Como recortar com um Axis-Aligned retângulo</span><span class="sxs-lookup"><span data-stu-id="51252-103">How to Clip with an Axis-Aligned Clip Rectangle</span></span>

<span data-ttu-id="51252-104">Este tópico descreve como recortar uma imagem com um retângulo de clipe alinhado por eixo.</span><span class="sxs-lookup"><span data-stu-id="51252-104">This topic describes how to clip an image with an axis-aligned clip rectangle.</span></span> <span data-ttu-id="51252-105">Essa abordagem produz apenas clipes retangulares, pois os limites de conteúdo são alinhados ao eixo do retângulo.</span><span class="sxs-lookup"><span data-stu-id="51252-105">This approach produces only rectangular clips, because the content bounds are aligned to the axis of the rectangle.</span></span> <span data-ttu-id="51252-106">Essa abordagem é mais eficiente do que usar camadas com os limites de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="51252-106">This approach is more efficient than using layers with the content bounds.</span></span> <span data-ttu-id="51252-107">Para obter mais informações, consulte[visão geral de camadas](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="51252-107">For more information, see[Layers Overview](direct2d-layers-overview.md).</span></span>

<span data-ttu-id="51252-108">**Para recortar com um retângulo de clipe alinhado por eixo**</span><span class="sxs-lookup"><span data-stu-id="51252-108">**To clip with an axis-aligned clip rectangle**</span></span>

1.  <span data-ttu-id="51252-109">Carregar a imagem original de um recurso.</span><span class="sxs-lookup"><span data-stu-id="51252-109">Load the original image from a resource.</span></span> <span data-ttu-id="51252-110">Para obter informações sobre como carregar um bitmap, consulte [como carregar um bitmap de um recurso](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="51252-110">For information on how to load a bitmap, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
2.  <span data-ttu-id="51252-111">Chame [**ID2D1RenderTarget::P ushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) para especificar um retângulo.</span><span class="sxs-lookup"><span data-stu-id="51252-111">Call [**ID2D1RenderTarget::PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) to specify a rectangle.</span></span> <span data-ttu-id="51252-112">Os comandos de renderização são recortados no retângulo.</span><span class="sxs-lookup"><span data-stu-id="51252-112">The rendering commands are clipped to the rectangle.</span></span>

3.  <span data-ttu-id="51252-113">Pinte a imagem original.</span><span class="sxs-lookup"><span data-stu-id="51252-113">Paint the original image.</span></span>
4.  <span data-ttu-id="51252-114">Chame [**ID2D1RenderTarget::P opaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para remover o último clipe alinhado pelo eixo do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="51252-114">Call [**ID2D1RenderTarget::PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the last axis-aligned clip from the render target.</span></span>

<span data-ttu-id="51252-115">Por exemplo, na ilustração a seguir, o bitmap original à esquerda é 200 \* 130 pixels.</span><span class="sxs-lookup"><span data-stu-id="51252-115">For example, in the following illustration, the original bitmap on the left is 200\*130 pixels.</span></span> <span data-ttu-id="51252-116">O bitmap à direita é o bitmap original recortado no retângulo de clipe alinhado ao eixo.</span><span class="sxs-lookup"><span data-stu-id="51252-116">The bitmap on the right is the original bitmap clipped to the axis-aligned clip rectangle.</span></span> <span data-ttu-id="51252-117">As dimensões são (20, 20) a (100, 100).</span><span class="sxs-lookup"><span data-stu-id="51252-117">The dimensions are (20, 20) to (100, 100).</span></span>

![ilustração de um bitmap Goldfish antes e depois que o bitmap é recortado](images/cliparegion-axisalignedclip.png)

<span data-ttu-id="51252-119">Para criar a imagem recortada, crie uma estrutura de retângulo como a área de recorte.</span><span class="sxs-lookup"><span data-stu-id="51252-119">To create the clipped image, create a rectangle structure as the clipping area.</span></span> <span data-ttu-id="51252-120">Chame [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) com a área de recorte e pinte a imagem original.</span><span class="sxs-lookup"><span data-stu-id="51252-120">Call [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) with the clipping area and paint the original image.</span></span> <span data-ttu-id="51252-121">Chame [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para remover o clipe do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="51252-121">Call [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the clip from the render target.</span></span> <span data-ttu-id="51252-122">O código a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="51252-122">The following code shows how to do this.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a><span data-ttu-id="51252-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="51252-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51252-124">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="51252-124">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 