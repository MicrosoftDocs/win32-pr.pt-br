---
title: Visão geral de máscaras da opacidade
description: 'Este tópico descreve como usar bitmaps e pincéis para definir máscaras de opacidade. Ele contém as seguintes seções:'
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a4757a30247da465e0ae5226bd923219e3e665
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104569212"
---
# <a name="opacity-masks-overview"></a><span data-ttu-id="08264-104">Visão geral de máscaras da opacidade</span><span class="sxs-lookup"><span data-stu-id="08264-104">Opacity Masks Overview</span></span>

<span data-ttu-id="08264-105">Este tópico descreve como usar bitmaps e pincéis para definir máscaras de opacidade.</span><span class="sxs-lookup"><span data-stu-id="08264-105">This topic describes how to use bitmaps and brushes to define opacity masks.</span></span> <span data-ttu-id="08264-106">Ele contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="08264-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="08264-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="08264-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="08264-108">O que é uma máscara de opacidade?</span><span class="sxs-lookup"><span data-stu-id="08264-108">What Is an Opacity Mask?</span></span>](#what-is-an-opacity-mask)
-   [<span data-ttu-id="08264-109">Usar um bitmap como uma máscara de opacidade com o método FillOpacityMask</span><span class="sxs-lookup"><span data-stu-id="08264-109">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [<span data-ttu-id="08264-110">Usar um pincel como uma máscara de opacidade com o método FillGeometry</span><span class="sxs-lookup"><span data-stu-id="08264-110">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [<span data-ttu-id="08264-111">Usar um pincel de gradiente linear como uma máscara de opacidade</span><span class="sxs-lookup"><span data-stu-id="08264-111">Use an Linear Gradient Brush as an Opacity Mask</span></span>](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [<span data-ttu-id="08264-112">Usar um pincel de gradiente radial como uma máscara de opacidade</span><span class="sxs-lookup"><span data-stu-id="08264-112">Use a Radial Gradient Brush as an Opacity Mask</span></span>](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [<span data-ttu-id="08264-113">Aplicar uma máscara de opacidade a uma camada</span><span class="sxs-lookup"><span data-stu-id="08264-113">Apply an Opacity Mask to a Layer</span></span>](#apply-an-opacity-mask-to-a-layer)
-   [<span data-ttu-id="08264-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08264-114">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="08264-115">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="08264-115">Prerequisites</span></span>

<span data-ttu-id="08264-116">Esta visão geral pressupõe que você esteja familiarizado com as operações básicas de desenho Direct2D, conforme descrito no passo a passo [criando um aplicativo Direct2D simples](direct2d-quickstart.md) .</span><span class="sxs-lookup"><span data-stu-id="08264-116">This overview assumes that you are familiar with basic Direct2D drawing operations, as described in the [Creating a Simple Direct2D Application](direct2d-quickstart.md) walkthrough.</span></span> <span data-ttu-id="08264-117">Você também deve estar familiarizado com os diferentes tipos de pincéis, conforme descrito na [visão geral de pincéis](direct2d-brushes-overview.md).</span><span class="sxs-lookup"><span data-stu-id="08264-117">You should also be familiar with the different types of brushes, as described in the [Brushes Overview](direct2d-brushes-overview.md).</span></span>

## <a name="what-is-an-opacity-mask"></a><span data-ttu-id="08264-118">O que é uma máscara de opacidade?</span><span class="sxs-lookup"><span data-stu-id="08264-118">What Is an Opacity Mask?</span></span>

<span data-ttu-id="08264-119">Uma máscara de opacidade é uma máscara, descrita por um pincel ou bitmap, que é aplicada a outro objeto para tornar esse objeto parcial ou completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="08264-119">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="08264-120">Uma máscara de opacidade usa informações de canal alfa para especificar como os pixels de origem do objeto são mesclados no destino final de destino.</span><span class="sxs-lookup"><span data-stu-id="08264-120">An opacity mask uses alpha channel information to specify how the source pixels of the object are blended into the final destination target.</span></span> <span data-ttu-id="08264-121">As partes transparentes da máscara indicam as áreas em que a imagem subjacente está oculta, enquanto as partes opacas da máscara indicam onde o objeto mascarado está visível.</span><span class="sxs-lookup"><span data-stu-id="08264-121">The transparent portions of the mask indicate the areas where the underlying image is hidden, whereas the opaque portions of the mask indicate where the masked object is visible.</span></span>

<span data-ttu-id="08264-122">Há várias maneiras de aplicar uma máscara de opacidade:</span><span class="sxs-lookup"><span data-stu-id="08264-122">There are several ways to apply an opacity mask:</span></span>

-   <span data-ttu-id="08264-123">Use o método [**ID2D1RenderTarget:: FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) .</span><span class="sxs-lookup"><span data-stu-id="08264-123">Use the [**ID2D1RenderTarget::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method.</span></span> <span data-ttu-id="08264-124">O método **FillOpacityMask** pinta uma região retangular de um destino de renderização e, em seguida, aplica uma máscara de opacidade, definida por um bitmap.</span><span class="sxs-lookup"><span data-stu-id="08264-124">The **FillOpacityMask** method paints a rectangular region of a render target and then applies an opacity mask, defined by a bitmap.</span></span> <span data-ttu-id="08264-125">Use esse método quando sua máscara de opacidade for um bitmap e você quiser preencher uma região retangular.</span><span class="sxs-lookup"><span data-stu-id="08264-125">Use this method when your opacity mask is a bitmap and you want to fill a rectangular region.</span></span>
-   <span data-ttu-id="08264-126">Use o método [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="08264-126">Use the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="08264-127">O método **FillGeometry** pinta o interior de geometry com o [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)especificado e, em seguida, aplica uma máscara de opacidade, definida por um pincel.</span><span class="sxs-lookup"><span data-stu-id="08264-127">The **FillGeometry** method paints the interior of geometry with the specified [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), then applies an opacity mask, defined by a brush.</span></span> <span data-ttu-id="08264-128">Use esse método quando desejar aplicar uma máscara de opacidade a uma geometria ou se desejar usar um pincel como uma máscara de opacidade.</span><span class="sxs-lookup"><span data-stu-id="08264-128">Use this method when you want to apply an opacity mask to a geometry or you want to use a brush as an opacity mask.</span></span>
-   <span data-ttu-id="08264-129">Use um [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) para aplicar uma máscara de opacidade.</span><span class="sxs-lookup"><span data-stu-id="08264-129">Use an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) to apply an opacity mask.</span></span> <span data-ttu-id="08264-130">Use essa abordagem quando desejar aplicar uma máscara de opacidade a um grupo de conteúdo de desenho, não apenas uma única forma ou imagem.</span><span class="sxs-lookup"><span data-stu-id="08264-130">Use this approach when you want to apply an opacity mask to a group of drawing content, not just a single shape or image.</span></span> <span data-ttu-id="08264-131">Para obter detalhes, consulte a [visão geral de camadas](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="08264-131">For details, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a><span data-ttu-id="08264-132">Usar um bitmap como uma máscara de opacidade com o método FillOpacityMask</span><span class="sxs-lookup"><span data-stu-id="08264-132">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>

<span data-ttu-id="08264-133">O método [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) pinta uma região retangular de um destino de renderização e, em seguida, aplica uma máscara de opacidade, definida por um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="08264-133">The [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method paints a rectangular region of a render target and then applies an opacity mask, defined by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="08264-134">Use esse método quando você tiver um bitmap que deseja usar como uma máscara de opacidade para uma região retangular.</span><span class="sxs-lookup"><span data-stu-id="08264-134">Use this method when you have a bitmap that you want to use as an opacity mask for a rectangular region.</span></span>

<span data-ttu-id="08264-135">O diagrama a seguir mostra um efeito de aplicar a máscara de opacidade (um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) com uma imagem de uma flor) a um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) com uma imagem de uma fábrica de Fern.</span><span class="sxs-lookup"><span data-stu-id="08264-135">The following diagram shows an effect of applying the opacity mask (an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with an image of a flower) to an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with an image of a fern plant.</span></span> <span data-ttu-id="08264-136">A imagem resultante é um bitmap de uma planta recortada para a forma flor.</span><span class="sxs-lookup"><span data-stu-id="08264-136">The resulting image is a bitmap of a plant clipped to the flower shape.</span></span>

![diagrama de um bitmap flor usado como uma máscara de opacidade em uma imagem de uma planta Fern](images/brushes-ovw-bitmapopacity.png)

<span data-ttu-id="08264-138">Os exemplos de código a seguir mostram como isso é feito.</span><span class="sxs-lookup"><span data-stu-id="08264-138">The following code examples shows how this is accomplished.</span></span>

<span data-ttu-id="08264-139">O primeiro exemplo carrega o bitmap a seguir, *m \_ pBitmapMask*, para uso como uma máscara de bitmap.</span><span class="sxs-lookup"><span data-stu-id="08264-139">The first example loads the following bitmap, *m\_pBitmapMask*, for use as a bitmap mask.</span></span> <span data-ttu-id="08264-140">A ilustração a seguir mostra a saída produzida.</span><span class="sxs-lookup"><span data-stu-id="08264-140">The following illustration shows the output that is produced.</span></span> <span data-ttu-id="08264-141">Observe que, embora a parte opaca do bitmap pareça preta, as informações de cor no bitmap não têm efeito sobre a máscara de opacidade; somente as informações de opacidade de cada pixel no bitmap são usadas.</span><span class="sxs-lookup"><span data-stu-id="08264-141">Note that, although the opaque portion of the bitmap appears black, the color information in the bitmap has no effect on the opacity mask; only the opacity information of each pixel in the bitmap is used.</span></span> <span data-ttu-id="08264-142">Os pixels totalmente opacos neste bitmap foram coloridos em preto apenas para fins ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="08264-142">The fully opaque pixels in this bitmap have been colored black for illustrative purposes only.</span></span>

![ilustração da máscara de bitmap flor](images/bitmapmask.png)

<span data-ttu-id="08264-144">Neste exemplo, o [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) é carregado por um método auxiliar, LoadResourceBitmap, definido em outro lugar no exemplo.</span><span class="sxs-lookup"><span data-stu-id="08264-144">In this example, the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is loaded by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"BitmapMask",
                    L"Image",
                    &m_pBitmapMask
                    );
            }
```



<span data-ttu-id="08264-145">O exemplo a seguir define o Brush, *m \_ pFernBitmapBrush*, ao qual a máscara de opacidade é aplicada.</span><span class="sxs-lookup"><span data-stu-id="08264-145">The next example defines the brush, *m\_pFernBitmapBrush*, to which the opacity mask is applied.</span></span> <span data-ttu-id="08264-146">Este exemplo usa um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) que contém uma imagem de um Fern, mas você pode usar um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)ou [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="08264-146">This example uses an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that contains an image of a fern, but you could use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) instead.</span></span> <span data-ttu-id="08264-147">A ilustração a seguir mostra a saída produzida.</span><span class="sxs-lookup"><span data-stu-id="08264-147">The following illustration shows the output that is produced.</span></span>

![ilustração do bitmap usado pelo pincel de bitmap](images/fern.png)


```C++
            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
                hr = m_pRenderTarget->CreateBitmapBrush(
                    m_pFernBitmap,
                    propertiesXClampYClamp,
                    &m_pFernBitmapBrush
                    );


            }
```





<span data-ttu-id="08264-149">Agora que a máscara de opacidade e o pincel estão definidos, você pode usar o método [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) no método de renderização do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="08264-149">Now that opacity mask and the brush are defined, you can use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method in your application's rendering method.</span></span> <span data-ttu-id="08264-150">Ao chamar o método **FillOpacityMask** , você deve especificar o tipo de máscara de opacidade que está usando: **d2d1 \_ de \_ \_ conteúdo máscara \_ de opacidade**, **d2d1 \_ opacidade \_ mascarar \_ \_ texto conteúdo \_ natural** e **d2d1 \_ opacidade \_ máscara texto de \_ conteúdo \_ \_ \_ compatível com GDI**.</span><span class="sxs-lookup"><span data-stu-id="08264-150">When you call the **FillOpacityMask** method, you must specify the type of opacity mask you are using: **D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**, **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_NATURAL**, and **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_GDI\_COMPATIBLE**.</span></span> <span data-ttu-id="08264-151">Para os significados desses três tipos, consulte [**conteúdo da \_ \_ máscara de \_ opacidade do d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).</span><span class="sxs-lookup"><span data-stu-id="08264-151">For the meanings of these three types, see [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).</span></span>

> [!Note]  
> <span data-ttu-id="08264-152">A partir do Windows 8, [**o \_ \_ \_ conteúdo da máscara de opacidade d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) não é necessário.</span><span class="sxs-lookup"><span data-stu-id="08264-152">Starting with Windows 8, the [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) is not required.</span></span> <span data-ttu-id="08264-153">Consulte o método [**ID2D1DeviceContext:: FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) , que não tem um parâmetro de **conteúdo de \_ \_ máscara \_ de opacidade d2d1** .</span><span class="sxs-lookup"><span data-stu-id="08264-153">See the [**ID2D1DeviceContext::FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) method, which has no **D2D1\_OPACITY\_MASK\_CONTENT** parameter.</span></span>

 

<span data-ttu-id="08264-154">O exemplo a seguir define o modo de anti-aliasing do destino de renderização para o [**\_ modo AntiAlias d2d1 com \_ \_ alias**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) para que a máscara de opacidade funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="08264-154">The next example sets the render target's antialiasing mode to [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) so that the opacity mask will work properly.</span></span> <span data-ttu-id="08264-155">Em seguida, ele chama o método [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) e passa-o para a máscara de opacidade (*m \_ pBitmapMask*), o pincel ao qual a máscara de opacidade é aplicada (*m \_ pFernBitmapBrush*), o tipo de conteúdo dentro da máscara de opacidade ([**d2d1 de \_ opacidade \_ \_ \_ máscara**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)e a área a ser pintada.</span><span class="sxs-lookup"><span data-stu-id="08264-155">It then calls the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method and passes it the opacity mask (*m\_pBitmapMask*), the brush to which the opacity mask is applied (*m\_pFernBitmapBrush*), the type of content inside the opacity mask ([**D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)), and the area to paint.</span></span> <span data-ttu-id="08264-156">A ilustração a seguir mostra a saída produzida.</span><span class="sxs-lookup"><span data-stu-id="08264-156">The following illustration shows the output that is produced.</span></span>

![ilustração da imagem da planta Fern com uma máscara de opacidade aplicada](images/opacitymaskoutput.png)


```C++
        D2D1_RECT_F rcBrushRect = D2D1::RectF(5, 5, 155, 155);


        // D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask to function properly
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);
        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);
```





<span data-ttu-id="08264-158">O código foi omitido neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="08264-158">Code has been omitted from this example.</span></span>

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a><span data-ttu-id="08264-159">Usar um pincel como uma máscara de opacidade com o método FillGeometry</span><span class="sxs-lookup"><span data-stu-id="08264-159">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>

<span data-ttu-id="08264-160">A seção anterior descreveu como usar um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) como uma máscara de opacidade.</span><span class="sxs-lookup"><span data-stu-id="08264-160">The preceding section described how to use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) as an opacity mask.</span></span> <span data-ttu-id="08264-161">Direct2D também fornece o método [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , que permite especificar, opcionalmente, o Brush como uma máscara de opacidade quando você preenche um [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry).</span><span class="sxs-lookup"><span data-stu-id="08264-161">Direct2D also provides the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, which enables you to optionally specify brush as an opacity mask when you fill an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry).</span></span> <span data-ttu-id="08264-162">Isso permite que você crie máscaras de opacidade a partir de gradientes (usando [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) ou [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) e bitmaps (usando **ID2D1Bitmap**).</span><span class="sxs-lookup"><span data-stu-id="08264-162">This enables you to create opacity masks from gradients (using [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) and bitmaps (using **ID2D1Bitmap**).</span></span>

<span data-ttu-id="08264-163">O método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) usa três parâmetros:</span><span class="sxs-lookup"><span data-stu-id="08264-163">The [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method takes three parameters:</span></span>

-   <span data-ttu-id="08264-164">O primeiro parâmetro, um [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), define a forma de pintura.</span><span class="sxs-lookup"><span data-stu-id="08264-164">The first parameter, an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), defines the shape to paint.</span></span>
-   <span data-ttu-id="08264-165">O segundo parâmetro, um [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), especifica o pincel usado para pintar a geometria.</span><span class="sxs-lookup"><span data-stu-id="08264-165">The second parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies the brush used to paint the geometry.</span></span> <span data-ttu-id="08264-166">Esse parâmetro deve ser um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) que tenha os modos x-e y-Extend definidos como [**d2d1 \_ modo estendido \_ \_ fixe**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="08264-166">This parameter must be an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that has its x- and y-extend modes set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>
-   <span data-ttu-id="08264-167">O terceiro parâmetro, um [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), especifica um pincel a ser usado como a máscara de opacidade.</span><span class="sxs-lookup"><span data-stu-id="08264-167">The third parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies a brush to use as the opacity mask.</span></span> <span data-ttu-id="08264-168">Esse pincel pode ser um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)ou um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="08264-168">This brush may be an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), or an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span> <span data-ttu-id="08264-169">(Tecnicamente, você pode usar um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), mas usar um pincel de cor sólida como uma máscara de opacidade não produz resultados interessantes.)</span><span class="sxs-lookup"><span data-stu-id="08264-169">(Technically, you may use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), but using a solid color brush as an opacity mask doesn't produce interesting results.)</span></span>

<span data-ttu-id="08264-170">As seções a seguir descrevem como usar objetos [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) e [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) como máscaras de opacidade.</span><span class="sxs-lookup"><span data-stu-id="08264-170">The following sections describe how to use [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) and [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) objects as opacity masks.</span></span>

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="08264-171">Usar um pincel de gradiente linear como uma máscara de opacidade</span><span class="sxs-lookup"><span data-stu-id="08264-171">Use an Linear Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="08264-172">O diagrama a seguir mostra o efeito de aplicar um pincel de gradiente linear a um retângulo que é preenchido com um bitmap de flores.</span><span class="sxs-lookup"><span data-stu-id="08264-172">The following diagram shows the effect of applying a linear gradient brush to a rectangle that is filled with a bitmap of flowers.</span></span>

![diagrama de um bitmap de flor com um pincel de gradiente linear aplicado](images/brushes-ovw-lineargradient-opacitymask.png)

<span data-ttu-id="08264-174">As etapas a seguir descrevem como recriar esse efeito.</span><span class="sxs-lookup"><span data-stu-id="08264-174">The steps that follow describe how to re-create this effect.</span></span>

1.  <span data-ttu-id="08264-175">Defina o conteúdo a ser mascarado.</span><span class="sxs-lookup"><span data-stu-id="08264-175">Define the content to be masked.</span></span> <span data-ttu-id="08264-176">O exemplo a seguir cria um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pLinearFadeFlowersBitmap*.</span><span class="sxs-lookup"><span data-stu-id="08264-176">The following example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pLinearFadeFlowersBitmap*.</span></span> <span data-ttu-id="08264-177">O modo Extend x-e y-para *m \_ pLinearFadeFlowersBitmap* são definidos como [**d2d1 \_ \_ modo Extend \_ fixe**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) para que ele possa ser usado com uma máscara de opacidade pelo método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="08264-177">The extend mode x- and y- for *m\_pLinearFadeFlowersBitmap* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) so that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

    ```cpp
    if (SUCCEEDED(hr))
    {
        // Create the bitmap to be used by the bitmap brush.
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"LinearFadeFlowers",
            L"Image",
            &m_pLinearFadeFlowersBitmap
            );
    }
 
    if (SUCCEEDED(hr))
        {
            D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                D2D1::BitmapBrushProperties(
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                );
    ```

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="08264-178">C++</span><span class="sxs-lookup"><span data-stu-id="08264-178">C++</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>                if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateBitmapBrush(
                            m_pLinearFadeFlowersBitmap,
                            propertiesXClampYClamp,
                            &m_pLinearFadeFlowersBitmapBrush
                            );
                    }</code></pre></td>
    </tr>
    </tbody>
    </table>

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="08264-179">C++</span><span class="sxs-lookup"><span data-stu-id="08264-179">C++</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  <span data-ttu-id="08264-180">Defina a máscara de opacidade.</span><span class="sxs-lookup"><span data-stu-id="08264-180">Define the opacity mask.</span></span> <span data-ttu-id="08264-181">O próximo exemplo de código cria um pincel de gradiente linear diagonal (*m \_ pLinearGradientBrush*) que desaparece de preto totalmente opaco na posição 0 para branco completamente transparente na posição 1.</span><span class="sxs-lookup"><span data-stu-id="08264-181">The next code example creates a diagonal linear gradient brush (*m\_pLinearGradientBrush*) that fades from fully opaque black at position 0 to completely transparent white at position 1.</span></span>
```C++
                if (SUCCEEDED(hr))
                {
                    ID2D1GradientStopCollection *pGradientStops = NULL;

                    static const D2D1_GRADIENT_STOP gradientStops[] =
                    {
                        {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                        {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                    };

                    hr = m_pRenderTarget->CreateGradientStopCollection(
                        gradientStops,
                        2,
                        &pGradientStops);


                    if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateLinearGradientBrush(
                            D2D1::LinearGradientBrushProperties(
                                D2D1::Point2F(0, 0),
                                D2D1::Point2F(150, 150)),
                            pGradientStops,
                            &m_pLinearGradientBrush);
                    }

    
                pGradientStops->Release();
                }
```



    

3.  <span data-ttu-id="08264-182">Use o método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="08264-182">Use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="08264-183">O exemplo final usa o método **FillGeometry** para o pincel de conteúdo para preencher [**um ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) com um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pLinearFadeFlowersBitmap*) e aplica uma máscara de opacidade (*m \_ pLinearGradientBrush*).</span><span class="sxs-lookup"><span data-stu-id="08264-183">The final example uses the **FillGeometry** method to the content brush to fill a [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*) with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pLinearFadeFlowersBitmap*) and applies an opacity mask (*m\_pLinearGradientBrush*).</span></span>
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

<span data-ttu-id="08264-184">O código foi omitido neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="08264-184">Code has been omitted from this example.</span></span>

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="08264-185">Usar um pincel de gradiente radial como uma máscara de opacidade</span><span class="sxs-lookup"><span data-stu-id="08264-185">Use a Radial Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="08264-186">O diagrama a seguir mostra o efeito visual de aplicar um pincel de gradiente radial a um retângulo que é preenchido com um bitmap de folhagem.</span><span class="sxs-lookup"><span data-stu-id="08264-186">The following diagram shows the visual effect of applying a radial gradient brush to a rectangle that is filled with a bitmap of foliage.</span></span>

![diagrama de um bitmap folhagem com um pincel de gradiente radial aplicado](images/brushes-ovw-radialgradient-opacitymask.png)

<span data-ttu-id="08264-188">O primeiro exemplo cria um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pRadialFadeFlowersBitmapBrush*.</span><span class="sxs-lookup"><span data-stu-id="08264-188">The first example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pRadialFadeFlowersBitmapBrush*.</span></span> <span data-ttu-id="08264-189">Para que ele possa ser usado com uma máscara de opacidade pelo método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , o modo Extend x-e y-para *m \_ PRadialFadeFlowersBitmapBrush* é definido como [**d2d1 \_ Extend \_ mode \_ fixe**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="08264-189">So that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, the extend mode x- and y- for *m\_pRadialFadeFlowersBitmapBrush* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                // Create the bitmap to be used by the bitmap brush.
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"RadialFadeFlowers",
                    L"Image",
                    &m_pRadialFadeFlowersBitmap
                    );
            }


            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08264-190">C++</span><span class="sxs-lookup"><span data-stu-id="08264-190">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateBitmapBrush(
                        m_pLinearFadeFlowersBitmap,
                        propertiesXClampYClamp,
                        &m_pLinearFadeFlowersBitmapBrush
                        );
                }</code></pre></td>
</tr>
</tbody>
</table>

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08264-191">C++</span><span class="sxs-lookup"><span data-stu-id="08264-191">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="08264-192">O exemplo a seguir define o pincel de gradiente radial que será usado como a máscara de opacidade.</span><span class="sxs-lookup"><span data-stu-id="08264-192">The next example defines the radial gradient brush that will be used as the opacity mask.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                ID2D1GradientStopCollection *pGradientStops = NULL;

                static const D2D1_GRADIENT_STOP gradientStops[] =
                {
                    {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                    {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                };

                hr = m_pRenderTarget->CreateGradientStopCollection(
                    gradientStops,
                    2,
                    &pGradientStops);




                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateRadialGradientBrush(
                        D2D1::RadialGradientBrushProperties(
                            D2D1::Point2F(75, 75),
                            D2D1::Point2F(0, 0),
                            75,
                            75),
                        pGradientStops,
                        &m_pRadialGradientBrush);
                }
                pGradientStops->Release();
            }
```





<span data-ttu-id="08264-193">O exemplo de código final usa o [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pRadialFadeFlowersBitmapBrush*) e a máscara de opacidade (*m \_ pRadialGradientBrush*) para preencher um [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*).</span><span class="sxs-lookup"><span data-stu-id="08264-193">The final code example uses the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pRadialFadeFlowersBitmapBrush*) and the opacity mask (*m\_pRadialGradientBrush*) to fill an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*).</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



<span data-ttu-id="08264-194">O código foi omitido neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="08264-194">Code has been omitted from this example.</span></span>

## <a name="apply-an-opacity-mask-to-a-layer"></a><span data-ttu-id="08264-195">Aplicar uma máscara de opacidade a uma camada</span><span class="sxs-lookup"><span data-stu-id="08264-195">Apply an Opacity Mask to a Layer</span></span>

<span data-ttu-id="08264-196">Ao chamar [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) para enviar por push um [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) para um destino de renderização, você pode usar a estrutura de [**\_ \_ parâmetros de camada d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) para aplicar um pincel como uma máscara de opacidade.</span><span class="sxs-lookup"><span data-stu-id="08264-196">When you call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) to push an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) onto an render target, you can use the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to apply a brush as an opacity mask.</span></span> <span data-ttu-id="08264-197">O exemplo de código a seguir usa um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) como uma máscara de opacidade.</span><span class="sxs-lookup"><span data-stu-id="08264-197">The following code example uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) as an opacity mask.</span></span>


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



<span data-ttu-id="08264-198">Para obter mais informações sobre como usar camadas, consulte a [visão geral de camadas](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="08264-198">For more information about using layers, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="08264-199">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08264-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08264-200">Visão geral de pincéis</span><span class="sxs-lookup"><span data-stu-id="08264-200">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="08264-201">Visão geral de camadas</span><span class="sxs-lookup"><span data-stu-id="08264-201">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

 

 