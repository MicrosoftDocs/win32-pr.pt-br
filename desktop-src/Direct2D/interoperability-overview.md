---
title: Visão geral sobre interoperabilidade
description: Resume as diferentes tecnologias que você pode usar com o Direct2D.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Interoperação Direct2D, GDI
- Interoperação Direct2D, GDI+
- Direct2D, interoperabilidade
- Direct2D, DirectWrite interoperation
- interoperabilidade, Direct2D
- interoperabilidade, Direct3D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilidade, Graphics Device Interface (GDI)
- interoperabilidade, GDI+
- Interoperabilidade do DirectWrite
- interoperabilidade, DirectWrite
- Windows Imaging Component (WIC)
- WIC (Windows Imaging Component)
- interoperabilidade, Windows Imaging Component (WIC)
- Direct2D, interoperação de WIC
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6f56c570a837a541bac9467477d4f6009bda019e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366187"
---
# <a name="interoperability-overview"></a><span data-ttu-id="20b9e-119">Visão geral sobre interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="20b9e-119">Interoperability Overview</span></span>

<span data-ttu-id="20b9e-120">Um dos principais recursos do Direct2D's é permitir a interoperabilidade entre Direct2D e outras plataformas de renderização para que os desenvolvedores possam usar os pontos fortes específicos de cada plataforma sem serem forçados a comprometeções escolhendo uma plataforma para todas as necessidades.</span><span class="sxs-lookup"><span data-stu-id="20b9e-120">One of Direct2D's key features is enabling interoperability between Direct2D and other rendering platforms so that developers can use the specific strengths of each platform without being forced into compromises by choosing one platform for all needs.</span></span> <span data-ttu-id="20b9e-121">Este tópico resume as diferentes plataformas com as quais o Direct2D é interoperável.</span><span class="sxs-lookup"><span data-stu-id="20b9e-121">This topic summarizes the different platforms with which Direct2D is interoperable.</span></span> <span data-ttu-id="20b9e-122">Ele contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="20b9e-122">It contains the following sections.</span></span>

-   [<span data-ttu-id="20b9e-123">Interoperabilidade GDI</span><span class="sxs-lookup"><span data-stu-id="20b9e-123">GDI Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="20b9e-124">Interoperabilidade de GDI+</span><span class="sxs-lookup"><span data-stu-id="20b9e-124">GDI+ Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="20b9e-125">Interoperabilidade do Direct3D</span><span class="sxs-lookup"><span data-stu-id="20b9e-125">Direct3D Interoperability</span></span>](#direct3d-interoperability)
-   [<span data-ttu-id="20b9e-126">Interoperabilidade do DirectWrite</span><span class="sxs-lookup"><span data-stu-id="20b9e-126">DirectWrite Interoperability</span></span>](#directwrite-interoperability)
-   [<span data-ttu-id="20b9e-127">Interoperabilidade do Windows Imaging Component (WIC)</span><span class="sxs-lookup"><span data-stu-id="20b9e-127">Windows Imaging Component (WIC) Interoperability</span></span>](#windows-imaging-component-wic-interoperability)
-   [<span data-ttu-id="20b9e-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="20b9e-128">Related topics</span></span>](#related-topics)

<span data-ttu-id="20b9e-129">O diagrama a seguir resume as diferentes plataformas com as quais o Direct2D é interoperável e lista alguns métodos e interfaces que fornecem interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="20b9e-129">The following diagram summarizes the different platforms with which Direct2D is interoperable and lists some methods and interfaces that provide interoperability.</span></span>

![diagrama de plataformas com as quais o Direct2D interopera, incluindo Direct3D 10,1, DirectWrite, WIC, GDI+ e GDI](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a><span data-ttu-id="20b9e-131">Interoperabilidade GDI</span><span class="sxs-lookup"><span data-stu-id="20b9e-131">GDI Interoperability</span></span>

<span data-ttu-id="20b9e-132">O Direct2D habilita a interoperabilidade bidirecional com GDI.</span><span class="sxs-lookup"><span data-stu-id="20b9e-132">Direct2D enables two-way interoperability with GDI.</span></span> <span data-ttu-id="20b9e-133">Você pode usar um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para gravar o conteúdo do Direct2D em um DC ( [contexto de dispositivo](/windows/desktop/gdi/device-contexts) GDI) ou pode usar o [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) para obter uma representação de DC de um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="20b9e-133">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to a GDI [device context](/windows/desktop/gdi/device-contexts) (DC), or you can use [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to obtain a DC representation of a render target.</span></span>

<span data-ttu-id="20b9e-134">Para obter mais informações e exemplos, consulte a [visão geral de interoperabilidade Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="20b9e-134">For more information and examples, see the [Direct2D and GDI Interoperability Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="20b9e-135">Interoperabilidade de GDI+</span><span class="sxs-lookup"><span data-stu-id="20b9e-135">GDI+ Interoperability</span></span>

<span data-ttu-id="20b9e-136">Você pode usar o GDI+ com Direct2D da mesma maneira que o GDI.</span><span class="sxs-lookup"><span data-stu-id="20b9e-136">You can use GDI+ with Direct2D in the same manner as GDI.</span></span> <span data-ttu-id="20b9e-137">Você pode usar um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para gravar o conteúdo do Direct2D no mesmo controlador de domínio que o seu conteúdo GDI+.</span><span class="sxs-lookup"><span data-stu-id="20b9e-137">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to the same DC as your GDI+ content.</span></span> <span data-ttu-id="20b9e-138">Essa abordagem permite que você comece a adicionar conteúdo Direct2D a aplicativos que são renderizados principalmente usando o GDI+.</span><span class="sxs-lookup"><span data-stu-id="20b9e-138">This approach enables you to start adding Direct2D content to applications that primarily render by using GDI+.</span></span>

<span data-ttu-id="20b9e-139">Você também pode usar um [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) para fornecer acesso a um controlador de domínio GDI que grava usando Direct2D e, em seguida, usar o método [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) para criar um objeto.</span><span class="sxs-lookup"><span data-stu-id="20b9e-139">You can also use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to provide access to a GDI DC that writes by using Direct2D, and then use the [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) method to create a object.</span></span> <span data-ttu-id="20b9e-140">Essa abordagem é útil para aplicativos que são renderizados principalmente com Direct2D, mas têm um modelo de extensibilidade ou outro conteúdo herdado que requer a capacidade de renderizar com o GDI+.</span><span class="sxs-lookup"><span data-stu-id="20b9e-140">This approach is useful for applications that primarily render with Direct2D, but have an extensibility model or other legacy content that requires the ability to render with GDI+.</span></span>

## <a name="direct3d-interoperability"></a><span data-ttu-id="20b9e-141">Interoperabilidade do Direct3D</span><span class="sxs-lookup"><span data-stu-id="20b9e-141">Direct3D Interoperability</span></span>

<span data-ttu-id="20b9e-142">Direct2D pode usar um destino de renderização de superfície DXGI (criado pelo método [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ) para gravar em um [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface).</span><span class="sxs-lookup"><span data-stu-id="20b9e-142">Direct2D can use a DXGI surface render target (created by the [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method) to write to an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface).</span></span> <span data-ttu-id="20b9e-143">Essa ação permite que você adicione planos de fundo e interfaces 2D a cenas 3D e use o conteúdo Direct2D como uma textura para um modelo 3D.</span><span class="sxs-lookup"><span data-stu-id="20b9e-143">This action enables you to add 2-D backgrounds and interfaces to 3-D scenes and use Direct2D content as a texture for a 3-D model.</span></span> <span data-ttu-id="20b9e-144">Direct2D também pode pegar um [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) e usar o método [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para criar uma representação de bitmap.</span><span class="sxs-lookup"><span data-stu-id="20b9e-144">Direct2D can also take an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) and use the [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) method to create a bitmap representation.</span></span>

<span data-ttu-id="20b9e-145">Para obter mais informações e exemplos, consulte a [visão geral de interoperabilidade do Direct2D e do Direct3D](direct2d-and-direct3d-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="20b9e-145">For more information and examples, see the [Direct2D and Direct3D Interoperability Overview](direct2d-and-direct3d-interoperation-overview.md).</span></span>

## <a name="directwrite-interoperability"></a><span data-ttu-id="20b9e-146">Interoperabilidade do DirectWrite</span><span class="sxs-lookup"><span data-stu-id="20b9e-146">DirectWrite Interoperability</span></span>

<span data-ttu-id="20b9e-147">O Direct2D está totalmente integrado ao DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="20b9e-147">Direct2D is tightly integrated with DirectWrite.</span></span> <span data-ttu-id="20b9e-148">O Direct2D facilita a renderização do conteúdo do DirectWrite fornecendo os métodos [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)e [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="20b9e-148">Direct2D makes it easy to render DirectWrite content by providing the [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), and [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) methods.</span></span>

## <a name="windows-imaging-component-wic-interoperability"></a><span data-ttu-id="20b9e-149">Interoperabilidade do Windows Imaging Component (WIC)</span><span class="sxs-lookup"><span data-stu-id="20b9e-149">Windows Imaging Component (WIC) Interoperability</span></span>

<span data-ttu-id="20b9e-150">O Direct2D fornece os métodos [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)e [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) para manipular bitmaps de WIC.</span><span class="sxs-lookup"><span data-stu-id="20b9e-150">Direct2D provides the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap), and [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) methods for manipulating WIC bitmaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20b9e-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="20b9e-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20b9e-152">Visão geral da interoperabilidade do Direct2D e da GDI</span><span class="sxs-lookup"><span data-stu-id="20b9e-152">Direct2D and GDI Interoperability Overview</span></span>](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[<span data-ttu-id="20b9e-153">Visão geral de interoperabilidade entre Direct2D e Direct3D</span><span class="sxs-lookup"><span data-stu-id="20b9e-153">Direct2D and Direct3D Interoperability Overview</span></span>](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 