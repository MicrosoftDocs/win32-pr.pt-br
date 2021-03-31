---
title: Como usar um bitmap como uma máscara de opacidade
description: Mostra como recortar uma região com máscaras de bitmap.
ms.assetid: d6ad53a6-5e84-49d0-ab2c-5d6ad9428f9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2106f43a6845cd724204fbf3e5aa1ec2b866bf46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917548"
---
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a><span data-ttu-id="eeea7-103">Como usar um bitmap como uma máscara de opacidade</span><span class="sxs-lookup"><span data-stu-id="eeea7-103">How to Use a Bitmap as an Opacity Mask</span></span>

<span data-ttu-id="eeea7-104">Este tópico descreve como usar um bitmap como uma máscara opacty chamando o método [**ID2D1Factory:: FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) .</span><span class="sxs-lookup"><span data-stu-id="eeea7-104">This topic describes how to use a bitmap as an opacty mask by calling the [**ID2D1Factory::FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) method.</span></span> <span data-ttu-id="eeea7-105">A máscara de opacidade é um bitmap que fornece as informações de cobertura representadas pelo canal alfa, que controla a transparência do conteúdo que é processado.</span><span class="sxs-lookup"><span data-stu-id="eeea7-105">The opacity mask is a bitmap that supplies the coverage information that is represented by the alpha channel, which controls the transparency of the content that is rendered.</span></span> <span data-ttu-id="eeea7-106">Essa abordagem é mais eficiente do que usar camadas com uma máscara de opacidade.</span><span class="sxs-lookup"><span data-stu-id="eeea7-106">This approach is more efficient than using layers with an opacity mask.</span></span> <span data-ttu-id="eeea7-107">Para obter mais informações, consulte [visão geral de camadas](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eeea7-107">For more information, see [Layers Overview](direct2d-layers-overview.md).</span></span>

<span data-ttu-id="eeea7-108">**Para recortar uma região**</span><span class="sxs-lookup"><span data-stu-id="eeea7-108">**To clip a region**</span></span>

1.  <span data-ttu-id="eeea7-109">Carregue o bitmap original de um recurso.</span><span class="sxs-lookup"><span data-stu-id="eeea7-109">Load the original bitmap from a resource.</span></span> <span data-ttu-id="eeea7-110">Para obter informações sobre como carregar um bitmap, consulte [como carregar um bitmap de um recurso](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="eeea7-110">For information on how to load a bitmap, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
2.  <span data-ttu-id="eeea7-111">Carregar a máscara de bitmap de um recurso.</span><span class="sxs-lookup"><span data-stu-id="eeea7-111">Load the bitmap mask from a resource.</span></span>
3.  <span data-ttu-id="eeea7-112">Crie um pincel de bitmap com o bitmap original.</span><span class="sxs-lookup"><span data-stu-id="eeea7-112">Create a bitmap brush with the original bitmap.</span></span> <span data-ttu-id="eeea7-113">Para obter informações sobre como criar um pincel de bitmap, consulte [como criar um pincel de bitmap](how-to-create-a-bitmap-brush.md).</span><span class="sxs-lookup"><span data-stu-id="eeea7-113">For information on how to create a bitmap brush, see [How to Create a Bitmap Brush](how-to-create-a-bitmap-brush.md).</span></span>
4.  <span data-ttu-id="eeea7-114">Chame [**ID2D1Factory:: SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para definir o modo de antialias no destino de renderização para o \_ modo de antialias d2d1 com \_ \_ alias para [**ID2D1Factory:: FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) para funcionar.</span><span class="sxs-lookup"><span data-stu-id="eeea7-114">Call [**ID2D1Factory::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set antialias mode on the render target to D2D1\_ANTIALIAS\_MODE\_ALIASED for [**ID2D1Factory::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) to work.</span></span>
5.  <span data-ttu-id="eeea7-115">Chame [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) com a máscara de bitmap e o pincel de bitmap no destino de renderização para preencher o clipe.</span><span class="sxs-lookup"><span data-stu-id="eeea7-115">Call [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) with the bitmap mask and the bitmap brush on the render target to fill the clip.</span></span>

<span data-ttu-id="eeea7-116">A ilustração a seguir mostra o bitmap original à esquerda, a máscara de bitmap no centro e o bitmap recortados para a máscara à direita.</span><span class="sxs-lookup"><span data-stu-id="eeea7-116">The following illustration shows the original bitmap on the left, the bitmap mask in the center, and the bitmap clipped to the mask on the right.</span></span>

![ilustração de um bitmap goldfish, uma máscara em formato de peixe que é criada a partir do bitmap e o bitmap em forma de peixe resultante após a máscara](images/cliparegion-opacitymask.png)

<span data-ttu-id="eeea7-118">O código a seguir mostra como recortar a região com a máscara mostrada na ilustração anterior.</span><span class="sxs-lookup"><span data-stu-id="eeea7-118">The following code shows how to clip the region with the mask shown in the preceding illustration.</span></span> <span data-ttu-id="eeea7-119">Ele primeiro carrega o bitmap original e a máscara de bitmap.</span><span class="sxs-lookup"><span data-stu-id="eeea7-119">It first loads the original bitmap and the bitmap mask.</span></span> <span data-ttu-id="eeea7-120">E, em seguida, cria um pincel de bitmap com o bitmap original.</span><span class="sxs-lookup"><span data-stu-id="eeea7-120">And then creates a bitmap brush with the original bitmap.</span></span>


```C++
// Create the bitmap to be used by the bitmap brush
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFish",
        L"Image",
        &m_pOrigBitmap
        );
}

if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFishMask",
        L"Image",
        &m_pBitmapMask
        );
}

if (SUCCEEDED(hr))
{
    D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = D2D1::BitmapBrushProperties(
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
        );

    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pOrigBitmap,
        propertiesXClampYClamp,
        &m_pOriginalBitmapBrush
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateBitmapBrush(
            m_pBitmapMask,
            propertiesXClampYClamp,
            &m_pBitmapMaskBrush
            );
    }
}
```



<span data-ttu-id="eeea7-121">Em seguida, ele chama [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para definir o modo AntiAlias.</span><span class="sxs-lookup"><span data-stu-id="eeea7-121">It then calls [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set the antialias mode.</span></span> <span data-ttu-id="eeea7-122">Chame [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) para usar uma máscara de bitmap para recortar o bitmap original.</span><span class="sxs-lookup"><span data-stu-id="eeea7-122">Call [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) to use a bitmap mask to clip the original bitmap.</span></span>


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



<span data-ttu-id="eeea7-123">Para obter mais informações sobre máscaras de opacidade, consulte a [visão geral das máscaras de opacidade](opacity-masks-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eeea7-123">For more information about opacity masks, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eeea7-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eeea7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeea7-125">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="eeea7-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 