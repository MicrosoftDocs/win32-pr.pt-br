---
title: Visão geral da interoperabilidade do Direct2D e da GDI
description: Descreve como usar o Direct2D e o GDI juntos.
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Interoperação Direct2D, GDI
- Direct2D, interoperabilidade
- interoperabilidade, Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilidade, Graphics Device Interface (GDI)
- Direct3D, interoperabilidade
- Interoperação do Direct3D, Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991d94b4460e9130b3353be38d5f749511434eb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641690"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a><span data-ttu-id="e99cf-111">Visão geral da interoperabilidade do Direct2D e da GDI</span><span class="sxs-lookup"><span data-stu-id="e99cf-111">Direct2D and GDI Interoperability Overview</span></span>

<span data-ttu-id="e99cf-112">Este tópico descreve como usar o Direct2D e o [GDI](/windows/desktop/gdi/windows-gdi) juntos.</span><span class="sxs-lookup"><span data-stu-id="e99cf-112">This topic describes how to use Direct2D and [GDI](/windows/desktop/gdi/windows-gdi) together.</span></span> <span data-ttu-id="e99cf-113">Há duas maneiras de combinar Direct2D com GDI: você pode gravar o conteúdo GDI em um destino de renderização compatível com GDI Direct2D ou pode gravar o conteúdo de Direct2D em um [controlador de domínio de dispositivo GDI (DC)](/windows/desktop/gdi/device-contexts).</span><span class="sxs-lookup"><span data-stu-id="e99cf-113">There are two ways to combine Direct2D with GDI: you can write GDI content to a Direct2D GDI-compatible render target, or you can write Direct2D content to a [GDI Device Context (DC)](/windows/desktop/gdi/device-contexts).</span></span>

<span data-ttu-id="e99cf-114">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="e99cf-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e99cf-115">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e99cf-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="e99cf-116">Desenhar conteúdo de Direct2D para um contexto de dispositivo GDI</span><span class="sxs-lookup"><span data-stu-id="e99cf-116">Draw Direct2D Content to a GDI Device Context</span></span>](#draw-direct2d-content-to-a-gdi-device-context)
-   [<span data-ttu-id="e99cf-117">ID2D1DCRenderTargets, transformações GDI e compilações de idiomas da direita para a esquerda do Windows</span><span class="sxs-lookup"><span data-stu-id="e99cf-117">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [<span data-ttu-id="e99cf-118">Desenhar conteúdo GDI para um Direct2D GDI-Compatible destino de renderização</span><span class="sxs-lookup"><span data-stu-id="e99cf-118">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [<span data-ttu-id="e99cf-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e99cf-119">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="e99cf-120">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e99cf-120">Prerequisites</span></span>

<span data-ttu-id="e99cf-121">Esta visão geral pressupõe que você esteja familiarizado com as operações básicas de desenho Direct2D.</span><span class="sxs-lookup"><span data-stu-id="e99cf-121">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="e99cf-122">Para obter um tutorial, consulte o guia de [início rápido do Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="e99cf-122">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="e99cf-123">Ele também pressupõe que você esteja familiarizado com as operações de desenho do GDI.</span><span class="sxs-lookup"><span data-stu-id="e99cf-123">It also assumes that you are familiar with GDI drawing operations.</span></span>

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a><span data-ttu-id="e99cf-124">Desenhar conteúdo de Direct2D para um contexto de dispositivo GDI</span><span class="sxs-lookup"><span data-stu-id="e99cf-124">Draw Direct2D Content to a GDI Device Context</span></span>

<span data-ttu-id="e99cf-125">Para desenhar o conteúdo do Direct2D em um controlador de domínio GDI, use um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span><span class="sxs-lookup"><span data-stu-id="e99cf-125">To draw Direct2D content to a GDI DC, you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span> <span data-ttu-id="e99cf-126">Para criar um destino de renderização de DC, use o método [**ID2D1Factory:: CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="e99cf-126">To create a DC render target, you use the [**ID2D1Factory::CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) method.</span></span> <span data-ttu-id="e99cf-127">Esse método usa dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e99cf-127">This method takes two parameters.</span></span>

<span data-ttu-id="e99cf-128">O primeiro parâmetro, uma estrutura de [**\_ Propriedades de \_ destino \_ de renderização d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , especifica a RENDERIZAÇÃO, comunicação remota, DPI, formato de pixel e informações de uso.</span><span class="sxs-lookup"><span data-stu-id="e99cf-128">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) structure, specifies rendering, remoting, DPI, pixel format, and usage information.</span></span> <span data-ttu-id="e99cf-129">Para habilitar o destino de renderização do controlador de domínio para trabalhar com o GDI, defina o formato DXGI para o [ \_ formato dxgi \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) e o modo alfa para [**d2d1 modo alfa, \_ \_ \_ premultiplicado**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) ou **d2d1 \_ \_ modo alfa \_ ignore**.</span><span class="sxs-lookup"><span data-stu-id="e99cf-129">To enable the DC render target to work with GDI, set the DXGI format to [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) and the alpha mode to [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="e99cf-130">O segundo parâmetro é o endereço do ponteiro que recebe a referência de destino de renderização de DC.</span><span class="sxs-lookup"><span data-stu-id="e99cf-130">The second parameter is the address of the pointer that receive the DC render target reference.</span></span>

<span data-ttu-id="e99cf-131">O código a seguir cria um destino de renderização de DC.</span><span class="sxs-lookup"><span data-stu-id="e99cf-131">The following code creates a DC render target.</span></span>


```C++
// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory->CreateDCRenderTarget(&props, &m_pDCRT);
```



<span data-ttu-id="e99cf-132">No código anterior, *m \_ pD2DFactory* é um ponteiro para um [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)e *m \_ pDCRT* é um ponteiro para um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span><span class="sxs-lookup"><span data-stu-id="e99cf-132">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pDCRT* is a pointer to an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span>

<span data-ttu-id="e99cf-133">Antes de poder renderizar com o destino de renderização do DC, você deve usar seu método [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) para associá-lo a um controlador de domínio GDI.</span><span class="sxs-lookup"><span data-stu-id="e99cf-133">Before you can render with the DC render target, you must use its [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method to associate it with a GDI DC.</span></span> <span data-ttu-id="e99cf-134">Você faz isso sempre que usar um controlador de domínio diferente ou o tamanho da área que deseja desenhar para alterações.</span><span class="sxs-lookup"><span data-stu-id="e99cf-134">You do this each time you use a different DC, or the size of the area you want to draw to changes.</span></span>

<span data-ttu-id="e99cf-135">O método [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) usa dois parâmetros, *HDC* e *pSubRect*.</span><span class="sxs-lookup"><span data-stu-id="e99cf-135">The [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method takes two parameters, *hDC* and *pSubRect*.</span></span> <span data-ttu-id="e99cf-136">O parâmetro *HDC* fornece um identificador para o contexto do dispositivo que recebe a saída do destino render.</span><span class="sxs-lookup"><span data-stu-id="e99cf-136">The *hDC* parameter provides a handle to the device context that receives the output of the render target.</span></span> <span data-ttu-id="e99cf-137">O parâmetro *pSubRect* é um retângulo que descreve a parte do contexto do dispositivo para o qual o conteúdo é renderizado.</span><span class="sxs-lookup"><span data-stu-id="e99cf-137">The *pSubRect* parameter is a rectangle that describes the portion of the device context to which content is rendered.</span></span> <span data-ttu-id="e99cf-138">O destino de renderização do DC atualiza seu tamanho para corresponder à área de contexto do dispositivo descrita por *pSubRect*, caso ele mude de tamanho.</span><span class="sxs-lookup"><span data-stu-id="e99cf-138">The DC render target updates its size to match the device context area described by *pSubRect*, should it change size.</span></span>

<span data-ttu-id="e99cf-139">O código a seguir associa um controlador de domínio a um destino de renderização de DC.</span><span class="sxs-lookup"><span data-stu-id="e99cf-139">The following code binds a DC to a DC render target.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{


// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e99cf-140">C++</span><span class="sxs-lookup"><span data-stu-id="e99cf-140">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="e99cf-141">Depois de associar o destino de renderização de DC a um DC, você pode usá-lo para desenhar.</span><span class="sxs-lookup"><span data-stu-id="e99cf-141">After you associate the DC render target with a DC, you can use it to draw.</span></span> <span data-ttu-id="e99cf-142">O código a seguir desenha o conteúdo Direct2D e GDI usando um DC.</span><span class="sxs-lookup"><span data-stu-id="e99cf-142">The following code draws Direct2D and GDI content using a DC.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

    HRESULT hr;
    RECT rc;

    // Get the dimensions of the client drawing area.
    GetClientRect(m_hwnd, &rc);

    //
    // Draw the pie chart with Direct2D.
    //

    // Create the DC render target.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Bind the DC to the DC render target.
        hr = m_pDCRT->BindDC(ps.hdc, &rc);

        m_pDCRT->BeginDraw();

        m_pDCRT->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pDCRT->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pDCRT->DrawEllipse(
            D2D1::Ellipse(
                D2D1::Point2F(150.0f, 150.0f),
                100.0f,
                100.0f),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.15425f),
                (150.0f - 100.0f * 0.988f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.525f),
                (150.0f + 100.0f * 0.8509f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f - 100.0f * 0.988f),
                (150.0f - 100.0f * 0.15425f)),
            m_pBlackBrush,
            3.0
            );

        hr = m_pDCRT->EndDraw();
        if (SUCCEEDED(hr))
        {
            //
            // Draw the pie chart with GDI.
            //

            // Save the original object.
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(ps.hdc, blackPen);

            Ellipse(ps.hdc, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);


            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(ps.hdc, pntArray1, 2);
            Polyline(ps.hdc, pntArray2, 2);
            Polyline(ps.hdc, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(ps.hdc, original);
        }
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



<span data-ttu-id="e99cf-143">Esse código produz saídas conforme mostrado na ilustração a seguir (os textos explicativos foram adicionados para realçar a diferença entre a renderização Direct2D e GDI).</span><span class="sxs-lookup"><span data-stu-id="e99cf-143">This code produces outputs as shown in the following illustration (callouts have been added to highlight the difference between Direct2D and GDI rendering.)</span></span>

![ilustração de dois gráficos circulares renderizados com Direct2D e GDI](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a><span data-ttu-id="e99cf-145">ID2D1DCRenderTargets, transformações GDI e compilações de idiomas da direita para a esquerda do Windows</span><span class="sxs-lookup"><span data-stu-id="e99cf-145">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>

<span data-ttu-id="e99cf-146">Quando você usa um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), ele processa o conteúdo de Direct2D para um bitmap interno e, em seguida, renderiza o bitmap para o controlador de domínio com GDI.</span><span class="sxs-lookup"><span data-stu-id="e99cf-146">When you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), it renders Direct2D content to an internal bitmap, and then renders the bitmap to the DC with GDI.</span></span>

<span data-ttu-id="e99cf-147">É possível que o GDI aplique uma transformação GDI (por meio do método [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) ) ou outro efeito ao mesmo DC usado pelo destino de renderização; nesse caso, a GDI transforma o bitmap produzido por Direct2D.</span><span class="sxs-lookup"><span data-stu-id="e99cf-147">It's possible for GDI to apply a GDI transform (through the [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) method) or other effect to the same DC used by the render target, in which case GDI transforms the bitmap produced by Direct2D.</span></span> <span data-ttu-id="e99cf-148">Usar uma transformação GDI para transformar o conteúdo Direct2D tem o potencial de degradar a qualidade visual da saída, pois você está transformando um bitmap para o qual o posicionamento de anti-aliasing e subpixel já foi calculado.</span><span class="sxs-lookup"><span data-stu-id="e99cf-148">Using a GDI transform to transform the Direct2D content has the potential to degrade the visual quality of the output, because you're transforming a bitmap for which antialiasing and subpixel positioning have already been calculated.</span></span>

<span data-ttu-id="e99cf-149">Por exemplo, suponha que você use o destino de renderização para desenhar uma cena que contém geometria e texto com suavização de alias.</span><span class="sxs-lookup"><span data-stu-id="e99cf-149">For example, suppose you use the render target to draw a scene that contains antialiased geometries and text.</span></span> <span data-ttu-id="e99cf-150">Se você usar uma transformação GDI para aplicar uma transformação de escala ao controlador de domínio e dimensionar a cena para que ela seja 10 vezes maior, você verá as bordas denteadas e de pixelização.</span><span class="sxs-lookup"><span data-stu-id="e99cf-150">If you use a GDI transform to apply a scale transform to the DC and scale the scene so that it's 10 times larger, you'll see pixelization and jagged edges.</span></span> <span data-ttu-id="e99cf-151">(Se, no entanto, você aplicou uma transformação semelhante usando Direct2D, a qualidade visual da cena não seria degradada.)</span><span class="sxs-lookup"><span data-stu-id="e99cf-151">(If, however, you applied a similar transform using Direct2D, the visual quality of the scene would not be degraded.)</span></span>

<span data-ttu-id="e99cf-152">Em alguns casos, pode não ser óbvio que a GDI está executando processamento adicional que pode prejudicar a qualidade do conteúdo do Direct2D.</span><span class="sxs-lookup"><span data-stu-id="e99cf-152">In some cases, it might not be obvious that GDI is performing additional processing that might degrade the quality of the Direct2D content.</span></span> <span data-ttu-id="e99cf-153">Por exemplo, em uma compilação da direita para a esquerda (RTL) do Windows, o conteúdo renderizado por um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) pode ser horizontalmente invertido quando o GDI o copia para seu destino.</span><span class="sxs-lookup"><span data-stu-id="e99cf-153">For example, on a right-to-left (RTL) build of Windows, content rendered by an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) might be horizontally inverted when GDI copies it to its destination.</span></span> <span data-ttu-id="e99cf-154">Se o conteúdo é realmente invertido depende das configurações atuais do controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="e99cf-154">Whether the content is actually inverted depends on the current settings of the DC.</span></span>

<span data-ttu-id="e99cf-155">Dependendo do tipo de conteúdo que está sendo renderizado, talvez você queira impedir a inversão.</span><span class="sxs-lookup"><span data-stu-id="e99cf-155">Depending on the type of content being rendered, you might want to prevent the inversion.</span></span> <span data-ttu-id="e99cf-156">Se o conteúdo de Direct2D incluir texto ClearType, essa inversão diminuirá a qualidade do texto.</span><span class="sxs-lookup"><span data-stu-id="e99cf-156">If the Direct2D content includes ClearType text, this inversion will degrade the quality of the text.</span></span>

<span data-ttu-id="e99cf-157">Você pode controlar o comportamento de renderização RTL usando a função GDI [**SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) .</span><span class="sxs-lookup"><span data-stu-id="e99cf-157">You can control RTL rendering behavior by using the [**SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) GDI function.</span></span> <span data-ttu-id="e99cf-158">Para evitar o espelhamento, chame a função GDI **SetLayout** e especifique **\_ BITMAPORIENTATIONPRESERVED de layout** como o único valor para o segundo parâmetro (não o combine com **\_ DPE de layout**), conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="e99cf-158">To prevent the mirroring, call the **SetLayout** GDI function and specify **LAYOUT\_BITMAPORIENTATIONPRESERVED** as the only value for the second parameter (do not combine it with **LAYOUT\_RTL**), as shown in the following example:</span></span>


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a><span data-ttu-id="e99cf-159">Desenhar conteúdo GDI para um Direct2D GDI-Compatible destino de renderização</span><span class="sxs-lookup"><span data-stu-id="e99cf-159">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>

<span data-ttu-id="e99cf-160">A seção anterior descreve como gravar o conteúdo do Direct2D em um controlador de domínio GDI.</span><span class="sxs-lookup"><span data-stu-id="e99cf-160">The previous section describes how to write Direct2D content to a GDI DC.</span></span> <span data-ttu-id="e99cf-161">Você também pode gravar conteúdo GDI em um destino de renderização compatível com GDI Direct2D.</span><span class="sxs-lookup"><span data-stu-id="e99cf-161">You can also write GDI content to a Direct2D GDI-compatible render target.</span></span> <span data-ttu-id="e99cf-162">Essa abordagem é útil para aplicativos que principalmente renderizam com Direct2D, mas têm um modelo de extensibilidade ou outro conteúdo herdado que requer a capacidade de renderizar com o GDI.</span><span class="sxs-lookup"><span data-stu-id="e99cf-162">This approach is useful for applications that primarily render with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span>

<span data-ttu-id="e99cf-163">Para renderizar o conteúdo GDI para um destino de renderização compatível com GDI Direct2D, use um [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), que fornece acesso a um contexto de dispositivo que pode aceitar chamadas de desenho do GDI.</span><span class="sxs-lookup"><span data-stu-id="e99cf-163">To render GDI content to a Direct2D GDI-compatible render target, use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which provides access to a device context that can accept GDI draw calls.</span></span> <span data-ttu-id="e99cf-164">Ao contrário de outras interfaces, um objeto **ID2D1GdiInteropRenderTarget** não é criado diretamente.</span><span class="sxs-lookup"><span data-stu-id="e99cf-164">Unlike other interfaces, an **ID2D1GdiInteropRenderTarget** object is not created directly.</span></span> <span data-ttu-id="e99cf-165">Em vez disso, use o método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de uma instância de destino de renderização existente.</span><span class="sxs-lookup"><span data-stu-id="e99cf-165">Instead, use the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of an existing render target instance.</span></span> <span data-ttu-id="e99cf-166">O código a seguir mostra como fazer isso:</span><span class="sxs-lookup"><span data-stu-id="e99cf-166">The following code shows how to do this:</span></span>


```C++
        D2D1_RENDER_TARGET_PROPERTIES rtProps = D2D1::RenderTargetProperties();
        rtProps.usage =  D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE;

        // Create a GDI compatible Hwnd render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            rtProps,
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );


        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->QueryInterface(__uuidof(ID2D1GdiInteropRenderTarget), (void**)&m_pGDIRT); 
        }
```



<span data-ttu-id="e99cf-167">No código anterior, *m \_ pD2DFactory* é um ponteiro para um [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)e *m \_ pGDIRT* é um ponteiro para um [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).</span><span class="sxs-lookup"><span data-stu-id="e99cf-167">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pGDIRT* is a pointer to an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).</span></span>

<span data-ttu-id="e99cf-168">Observe que o sinalizador compatível com o [**uso de destino do d2d1 \_ \_ \_ \_ \_ render**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) é especificado ao criar o destino de renderização compatível com GDI do HWND.</span><span class="sxs-lookup"><span data-stu-id="e99cf-168">Notice that the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag is specified when creating the Hwnd GDI-compatible render target.</span></span> <span data-ttu-id="e99cf-169">Se um formato de pixel for necessário, use o [ \_ formato dxgi \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e99cf-169">If a pixel format is required, use [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="e99cf-170">Se um modo alfa for necessário, use o modo [**\_ alfa d2d1 \_ \_ bimultiplicado**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) ou o **\_ modo alfa d2d1 \_ \_ ignore**.</span><span class="sxs-lookup"><span data-stu-id="e99cf-170">If an alpha mode is required, use [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="e99cf-171">Observe que o método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sempre tem sucesso.</span><span class="sxs-lookup"><span data-stu-id="e99cf-171">Note that the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method always succeeds.</span></span> <span data-ttu-id="e99cf-172">Para testar se os métodos da interface [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) funcionarão para um determinado destino de renderização, crie uma [**d2d1 de \_ \_ \_ Propriedades de destino de renderização**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) que especifica a compatibilidade GDI e o formato de pixel apropriado e, em seguida, chame o método [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) de destino de renderização para ver se o destino de renderização é compatível com GDI.</span><span class="sxs-lookup"><span data-stu-id="e99cf-172">To test whether the [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) interface's methods will work for a given render target, create a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) that specifies GDI compatibility and the appropriate pixel format, and then call the render target's [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) method to see whether the render target is GDI-compatible.</span></span>

<span data-ttu-id="e99cf-173">O exemplo a seguir mostra como desenhar um gráfico de pizza (conteúdo GDI) para o destino de renderização compatível com GDI do HWND.</span><span class="sxs-lookup"><span data-stu-id="e99cf-173">The following example shows how to draw a pie chart (GDI content) to the Hwnd GDI-compatible render target.</span></span>


```C++
        HDC hDC = NULL;
        hr = m_pGDIRT->GetDC(D2D1_DC_INITIALIZE_MODE_COPY, &hDC);

        if (SUCCEEDED(hr))
        {
            // Draw the pie chart to the GDI render target associated with the Hwnd render target.
            HGDIOBJ original = NULL;
            original = SelectObject(
                hDC,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(hDC, blackPen);

            Ellipse(hDC, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);

            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(hDC, pntArray1, 2);
            Polyline(hDC, pntArray2, 2);
            Polyline(hDC, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(hDC, original);

            m_pGDIRT->ReleaseDC(NULL);
        }

```



<span data-ttu-id="e99cf-174">O código gera gráficos, conforme mostrado na ilustração a seguir com textos explicativos para destacar a diferença de qualidade de renderização.</span><span class="sxs-lookup"><span data-stu-id="e99cf-174">The code outputs charts as shown in the following illustration with callouts to highlight the rendering quality difference.</span></span> <span data-ttu-id="e99cf-175">O gráfico de pizza à direita (conteúdo GDI) reduziu a qualidade de renderização do que o gráfico de pizza à esquerda (conteúdo de Direct2D).</span><span class="sxs-lookup"><span data-stu-id="e99cf-175">The right pie chart (GDI content) has lower rendering quality than the left pie chart (Direct2D content).</span></span> <span data-ttu-id="e99cf-176">Isso ocorre porque o Direct2D é capaz de renderizar com anti-aliasing</span><span class="sxs-lookup"><span data-stu-id="e99cf-176">This is because Direct2D is capable of rendering with antialiasing</span></span>

![ilustração de dois gráficos circulares renderizados em um destino de renderização compatível com GDI do Direct2D](images/gdicontentind2d.png)

## <a name="related-topics"></a><span data-ttu-id="e99cf-178">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e99cf-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e99cf-179">**ID2D1Factory::CreateDCRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="e99cf-179">**ID2D1Factory::CreateDCRenderTarget**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[<span data-ttu-id="e99cf-180">**ID2D1DCRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="e99cf-180">**ID2D1DCRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[<span data-ttu-id="e99cf-181">**ID2D1GdiInteropRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="e99cf-181">**ID2D1GdiInteropRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[<span data-ttu-id="e99cf-182">**\_Propriedades de \_ destino de renderização d2d1 \_**</span><span class="sxs-lookup"><span data-stu-id="e99cf-182">**D2D1\_RENDER\_TARGET\_PROPERTIES**</span></span>](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[<span data-ttu-id="e99cf-183">Contextos de dispositivo GDI</span><span class="sxs-lookup"><span data-stu-id="e99cf-183">GDI Device Contexts</span></span>](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[<span data-ttu-id="e99cf-184">SDK DO GDI</span><span class="sxs-lookup"><span data-stu-id="e99cf-184">GDI SDK</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 