---
title: Visão geral de destinos de renderização
description: Descreve os diferentes tipos de destinos de renderização Direct2D e como usá-los.
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D, destinos de renderização
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917431"
---
# <a name="render-targets-overview"></a><span data-ttu-id="97745-104">Visão geral de destinos de renderização</span><span class="sxs-lookup"><span data-stu-id="97745-104">Render Targets Overview</span></span>

<span data-ttu-id="97745-105">Um destino de renderização é um recurso que herda da interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="97745-105">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="97745-106">Um destino de renderização cria recursos para desenhar e executa operações de desenho reais.</span><span class="sxs-lookup"><span data-stu-id="97745-106">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="97745-107">Este tópico descreve os diferentes tipos de destinos de renderização Direct2D e como usá-los.</span><span class="sxs-lookup"><span data-stu-id="97745-107">This topic describes the different types of Direct2D render targets and how to use them.</span></span>

-   [<span data-ttu-id="97745-108">Destinos de renderização</span><span class="sxs-lookup"><span data-stu-id="97745-108">Render Targets</span></span>](#render-targets-overview)
    -   [<span data-ttu-id="97745-109">Recursos de destino de renderização</span><span class="sxs-lookup"><span data-stu-id="97745-109">Render Target Features</span></span>](#render-target-features)
    -   [<span data-ttu-id="97745-110">Renderizar recursos de destino</span><span class="sxs-lookup"><span data-stu-id="97745-110">Render Target Resources</span></span>](#render-target-resources)
    -   [<span data-ttu-id="97745-111">Comandos de desenho</span><span class="sxs-lookup"><span data-stu-id="97745-111">Drawing Commands</span></span>](#drawing-commands)
    -   [<span data-ttu-id="97745-112">Tratamento de erro</span><span class="sxs-lookup"><span data-stu-id="97745-112">Error Handling</span></span>](#error-handling)
-   [<span data-ttu-id="97745-113">Exemplo: renderizar conteúdo em uma janela</span><span class="sxs-lookup"><span data-stu-id="97745-113">Example: Render Content to a Window</span></span>](#example-render-content-to-a-window)

## <a name="render-targets"></a><span data-ttu-id="97745-114">Destinos de renderização</span><span class="sxs-lookup"><span data-stu-id="97745-114">Render Targets</span></span>

<span data-ttu-id="97745-115">Um destino de renderização é um recurso que herda da interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="97745-115">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="97745-116">Um destino de renderização cria recursos para desenhar e executa operações de desenho reais.</span><span class="sxs-lookup"><span data-stu-id="97745-116">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="97745-117">Há vários tipos de destinos de renderização que podem ser usados para renderizar elementos gráficos das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="97745-117">There are several kinds of render targets that can be used to render graphics in the following ways:</span></span>

-   <span data-ttu-id="97745-118">Os objetos [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) renderizam o conteúdo em uma janela.</span><span class="sxs-lookup"><span data-stu-id="97745-118">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) objects render content to a window.</span></span>
-   <span data-ttu-id="97745-119">Os objetos [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) são renderizados em um contexto de dispositivo GDI.</span><span class="sxs-lookup"><span data-stu-id="97745-119">[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) objects render to a GDI device context.</span></span>
-   <span data-ttu-id="97745-120">Os objetos de destino de renderização de bitmap renderizam conteúdo para um bitmap fora da tela.</span><span class="sxs-lookup"><span data-stu-id="97745-120">Bitmap render target objects render content to an off-screen bitmap.</span></span>
-   <span data-ttu-id="97745-121">Os objetos de destino de renderização DXGI são renderizados em uma superfície DXGI para uso com o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="97745-121">DXGI render target objects render to a DXGI surface for use with Direct3D.</span></span>

<span data-ttu-id="97745-122">Como um destino de renderização é associado a um dispositivo de renderização específico, ele é um recurso dependente de dispositivo e deixa de funcionar se o dispositivo for removido.</span><span class="sxs-lookup"><span data-stu-id="97745-122">Because a render target is associated with a particular rendering device, it is a device-dependent resource and ceases to function if the device is removed.</span></span>

### <a name="render-target-features"></a><span data-ttu-id="97745-123">Recursos de destino de renderização</span><span class="sxs-lookup"><span data-stu-id="97745-123">Render Target Features</span></span>

<span data-ttu-id="97745-124">Você pode especificar se um destino de renderização usa aceleração de hardware e se a exibição remota é renderizada por um computador local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="97745-124">You can specify whether a render target uses hardware acceleration and whether remote display is rendered by a local or a remote computer.</span></span> <span data-ttu-id="97745-125">Os destinos de renderização podem ser configurados para renderização com alias ou AntiAlias.</span><span class="sxs-lookup"><span data-stu-id="97745-125">Render targets can be set up for aliased or antialiased rendering.</span></span> <span data-ttu-id="97745-126">Para a renderização de cenas com um grande número de primitivos, um desenvolvedor também pode renderizar gráficos 2D no modo com alias e usar a suavização de vários exemplos do D3D para obter maior escalabilidade.</span><span class="sxs-lookup"><span data-stu-id="97745-126">For rendering scenes with a large number of primitives, a developer can also render 2-D graphics in aliased mode and use D3D multisample antialiasing to achieve greater scalability.</span></span>

<span data-ttu-id="97745-127">Os destinos de renderização também podem agrupar operações de desenho em camadas representadas pela interface [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) .</span><span class="sxs-lookup"><span data-stu-id="97745-127">Render targets can also group drawing operations into layers represented by the [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) interface.</span></span> <span data-ttu-id="97745-128">As camadas são úteis para coletar operações de desenho a serem compostas ao renderizar um quadro.</span><span class="sxs-lookup"><span data-stu-id="97745-128">Layers are useful for collecting drawing operations to be composited together when rendering a frame.</span></span> <span data-ttu-id="97745-129">Para alguns cenários, isso pode ser uma alternativa útil para renderizar para um destino de renderização de bitmap e, em seguida, reutilizar o conteúdo do bitmap, já que os custos de alocação para a disposição em camadas são menores do que para um [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="97745-129">For some scenarios, this can be a useful alternative to rendering to a bitmap render target, and then reusing the bitmap contents, as allocation costs for layering are lower than for an [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).</span></span>

<span data-ttu-id="97745-130">Os destinos de renderização podem criar novos destinos de renderização que são compatíveis com eles próprios, o que é útil para o processamento fora da tela intermediário enquanto retém as várias propriedades de destino de renderização que foram definidas no original.</span><span class="sxs-lookup"><span data-stu-id="97745-130">Render targets can create new render targets that are compatible with themselves, which is useful for intermediate off-screen rendering while retaining the various render-target properties that were set on the original.</span></span>

<span data-ttu-id="97745-131">Também é possível renderizar usando GDI em um destino de renderização Direct2D chamando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em um destino de renderização para [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), que tem os métodos [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) e [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) que podem ser usados para recuperar um contexto de dispositivo GDI.</span><span class="sxs-lookup"><span data-stu-id="97745-131">It is also possible to render using GDI on a Direct2D render target by calling [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a render target for [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which has [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) and [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) methods on it that can be used to retrieve a GDI device context.</span></span> <span data-ttu-id="97745-132">A renderização por meio de GDI só será possível se o destino de renderização tiver sido criado com o sinalizador de [**\_ uso de \_ destino \_ \_ \_ compatível com GDI do d2d1 render**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) .</span><span class="sxs-lookup"><span data-stu-id="97745-132">Rendering via GDI is possible only if the render target was created with the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag set.</span></span> <span data-ttu-id="97745-133">Isso é útil para aplicativos que são principalmente renderizados com Direct2D, mas têm um modelo de extensibilidade ou outro conteúdo herdado que requer a capacidade de renderizar com o GDI.</span><span class="sxs-lookup"><span data-stu-id="97745-133">This is useful for applications that are primarily rendering with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span> <span data-ttu-id="97745-134">Para obter mais informações, consulte a [visão geral de interoperabilidade Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="97745-134">For more information, see the [Direct2D and GDI Interoperation Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

### <a name="render-target-resources"></a><span data-ttu-id="97745-135">Renderizar recursos de destino</span><span class="sxs-lookup"><span data-stu-id="97745-135">Render Target Resources</span></span>

<span data-ttu-id="97745-136">Como uma fábrica, um destino de renderização pode criar recursos de desenho.</span><span class="sxs-lookup"><span data-stu-id="97745-136">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="97745-137">Todos os recursos criados por um destino de renderização são recursos dependentes do dispositivo (assim como o destino de renderização).</span><span class="sxs-lookup"><span data-stu-id="97745-137">Any resources created by a render target are device-dependent resources (just like the render target).</span></span> <span data-ttu-id="97745-138">Um destino de renderização pode criar os seguintes tipos de recursos:</span><span class="sxs-lookup"><span data-stu-id="97745-138">A render target can create the following types of resources:</span></span>

-   <span data-ttu-id="97745-139">Bitmaps</span><span class="sxs-lookup"><span data-stu-id="97745-139">Bitmaps</span></span>
-   <span data-ttu-id="97745-140">Pincéis</span><span class="sxs-lookup"><span data-stu-id="97745-140">Brushes</span></span>
-   <span data-ttu-id="97745-141">Camadas</span><span class="sxs-lookup"><span data-stu-id="97745-141">Layers</span></span>
-   <span data-ttu-id="97745-142">Malhas</span><span class="sxs-lookup"><span data-stu-id="97745-142">Meshes</span></span>

### <a name="drawing-commands"></a><span data-ttu-id="97745-143">Comandos de desenho</span><span class="sxs-lookup"><span data-stu-id="97745-143">Drawing Commands</span></span>

<span data-ttu-id="97745-144">Para renderizar o conteúdo, use os métodos de desenho de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="97745-144">To render content, you use the render target drawing methods.</span></span> <span data-ttu-id="97745-145">Antes de começar a desenhar, chame o método [**ID2D1RenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) .</span><span class="sxs-lookup"><span data-stu-id="97745-145">Before you begin drawing, you call the [**ID2D1RenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method.</span></span> <span data-ttu-id="97745-146">Depois de terminar o desenho, chame o método [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="97745-146">After you finished drawing, you call the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="97745-147">Entre essas chamadas, você usa os métodos Draw e Fill para renderizar os recursos de desenho.</span><span class="sxs-lookup"><span data-stu-id="97745-147">Between these calls, you use Draw and Fill methods to render drawing resources.</span></span> <span data-ttu-id="97745-148">A maioria dos métodos Draw e Fill pega uma forma (uma primitiva ou uma geometry) e um pincel para preencher ou estruturar a forma.</span><span class="sxs-lookup"><span data-stu-id="97745-148">Most Draw and Fill methods take a shape (either a primitive or a geometry) and a brush for filling or outlining the shape.</span></span>

<span data-ttu-id="97745-149">Os destinos de renderização fornecem métodos para recorte, aplicação de máscaras de opacidade e transformação do espaço de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="97745-149">Render targets provide methods for clipping, applying opacity masks, and transforming the coordinate space.</span></span>

<span data-ttu-id="97745-150">Direct2D usa um sistema de coordenadas à esquerda: valores positivos do eixo x passam para os valores do eixo y direito e positivo para baixo.</span><span class="sxs-lookup"><span data-stu-id="97745-150">Direct2D uses a left-handed coordinate system: positive x-axis values proceed to the right and positive y-axis values proceed downward.</span></span>

### <a name="error-handling"></a><span data-ttu-id="97745-151">Tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="97745-151">Error Handling</span></span>

<span data-ttu-id="97745-152">Processar comandos de desenho de destino não indique se a operação solicitada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="97745-152">Render target drawing commands do not indicate whether the requested operation was successful.</span></span> <span data-ttu-id="97745-153">Para descobrir se há erros de desenho, chame o método de [**liberação**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) de destino render ou o método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) para obter um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="97745-153">To find out whether there are drawing errors, call the render target [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) method or [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method to obtain an **HRESULT**.</span></span>

## <a name="example-render-content-to-a-window"></a><span data-ttu-id="97745-154">Exemplo: renderizar conteúdo em uma janela</span><span class="sxs-lookup"><span data-stu-id="97745-154">Example: Render Content to a Window</span></span>

<span data-ttu-id="97745-155">O exemplo a seguir usa o método [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) para criar um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span><span class="sxs-lookup"><span data-stu-id="97745-155">The following example uses the [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) method to create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



<span data-ttu-id="97745-156">O exemplo a seguir usa o [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) para desenhar texto na janela.</span><span class="sxs-lookup"><span data-stu-id="97745-156">The next example uses the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) to draw text to the window.</span></span>


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



<span data-ttu-id="97745-157">O código foi omitido neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="97745-157">Code has been omitted from this example.</span></span>

 

 