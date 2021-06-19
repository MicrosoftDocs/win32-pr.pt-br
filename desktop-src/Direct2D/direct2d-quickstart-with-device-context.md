---
title: Guia de início rápido do Direct2D para Windows 8
description: Resume as etapas necessárias para desenhar com o Direct2D para Windows 8 e fornece código de exemplo. Direct2D é uma API de código nativo para criar gráficos 2D.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D, exemplo de código de retângulo de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43442e57ed0949bdf39fc05ce1a69fded42b4b3d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406139"
---
# <a name="direct2d-quickstart-for-windows-8"></a><span data-ttu-id="7ffeb-105">Guia de início rápido do Direct2D para Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ffeb-105">Direct2D Quickstart for Windows 8</span></span>

<span data-ttu-id="7ffeb-106">Direct2D é uma API de modo imediato, de código nativo para a criação de gráficos 2D.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-106">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="7ffeb-107">Este tópico ilustra como usar o Direct2D para desenhar para um [**Windows:: UI:: Core:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="7ffeb-107">This topic illustrates how to use Direct2D to draw to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

<span data-ttu-id="7ffeb-108">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="7ffeb-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="7ffeb-109">Desenhando um retângulo simples</span><span class="sxs-lookup"><span data-stu-id="7ffeb-109">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="7ffeb-110">Etapa 1: incluir o cabeçalho Direct2D</span><span class="sxs-lookup"><span data-stu-id="7ffeb-110">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="7ffeb-111">Etapa 2: criar um ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="7ffeb-111">Step 2: Create an ID2D1Factory1</span></span>](#step-2-create-an-id2d1factory1)
-   [<span data-ttu-id="7ffeb-112">Etapa 3: criar um ID2D1Device e um ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="7ffeb-112">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [<span data-ttu-id="7ffeb-113">Etapa 4: criar um pincel</span><span class="sxs-lookup"><span data-stu-id="7ffeb-113">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="7ffeb-114">Etapa 5: desenhar o retângulo</span><span class="sxs-lookup"><span data-stu-id="7ffeb-114">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="7ffeb-115">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="7ffeb-115">Example code</span></span>](#example-code)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="7ffeb-116">Desenhando um retângulo simples</span><span class="sxs-lookup"><span data-stu-id="7ffeb-116">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="7ffeb-117">Para desenhar um retângulo usando [GDI](/windows/desktop/gdi/windows-gdi), você pode manipular a mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-117">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



<span data-ttu-id="7ffeb-118">O código para desenhar o mesmo retângulo com Direct2D é semelhante: ele cria recursos de desenho, descreve uma forma para desenhar, desenha a forma e libera os recursos de desenho.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-118">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="7ffeb-119">As seções a seguir descrevem cada uma dessas etapas em detalhes.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-119">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="7ffeb-120">Etapa 1: incluir o cabeçalho Direct2D</span><span class="sxs-lookup"><span data-stu-id="7ffeb-120">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="7ffeb-121">Além dos cabeçalhos necessários para o aplicativo, inclua os cabeçalhos d2d1. h e d2d1 \_ 1. h.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-121">In addition to the headers required for the application, include the d2d1.h and d2d1\_1.h headers.</span></span>

## <a name="step-2-create-an-id2d1factory1"></a><span data-ttu-id="7ffeb-122">Etapa 2: criar um ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="7ffeb-122">Step 2: Create an ID2D1Factory1</span></span>

<span data-ttu-id="7ffeb-123">Uma das primeiras coisas que qualquer exemplo de Direct2D faz é criar um [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span><span class="sxs-lookup"><span data-stu-id="7ffeb-123">One of the first things that any Direct2D example does is create an [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span></span>


```C++
DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );
```



<span data-ttu-id="7ffeb-124">A interface [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) é o ponto de partida para usar Direct2D; Use um **ID2D1Factory1** para criar recursos do Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-124">The [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface is the starting point for using Direct2D; use an **ID2D1Factory1** to create Direct2D resources.</span></span>

<span data-ttu-id="7ffeb-125">Ao criar uma fábrica, você pode especificar se ela é de vários ou de thread único.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-125">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="7ffeb-126">(Para obter mais informações sobre fábricas com vários threads, consulte os comentários na [**página de referência do ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) Este exemplo cria uma fábrica de thread único.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-126">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="7ffeb-127">Em geral, seu aplicativo deve criar a fábrica uma vez e mantê-la para a vida útil do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-127">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a><span data-ttu-id="7ffeb-128">Etapa 3: criar um ID2D1Device e um ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="7ffeb-128">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>

<span data-ttu-id="7ffeb-129">Depois de criar uma fábrica, use-a para criar um dispositivo Direct2D e, em seguida, use o dispositivo para criar um contexto de dispositivo Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-129">After you create a factory, use it to create a Direct2D device and then use the device to create a Direct2D device context.</span></span> <span data-ttu-id="7ffeb-130">Para criar esses objetos Direct2D, você deve ter um [**dispositivo Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , um [**dispositivo dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)e uma [**cadeia de permuta dxgi**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span><span class="sxs-lookup"><span data-stu-id="7ffeb-130">In order to create these Direct2D objects, you must have a [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , a [**DXGI device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice), and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="7ffeb-131">Confira [dispositivos e contextos de dispositivo](devices-and-device-contexts.md) para obter informações sobre como criar os pré-requisitos necessários.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-131">See [Devices and Device Contexts](devices-and-device-contexts.md) for info on creating the necessary prerequisites.</span></span>


```C++

    // Obtain the underlying DXGI device of the Direct3D11.1 device.
    DX::ThrowIfFailed(
        m_d3dDevice.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // And get its corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



<span data-ttu-id="7ffeb-132">Um contexto de dispositivo é um dispositivo que pode executar operações de desenho e criar recursos de desenho dependentes de dispositivo, como pincéis.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-132">A device context is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="7ffeb-133">Você também usa o contexto do dispositivo para vincular um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a uma superfície DXGI para usar como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-133">You also use the device context to link a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) to a DXGI surface to use as a render target.</span></span> <span data-ttu-id="7ffeb-134">O contexto do dispositivo pode ser renderizado para diferentes tipos de destinos.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-134">The device context can render to different types of targets.</span></span>

<span data-ttu-id="7ffeb-135">O código aqui declara as propriedades de bitmap que vincula a uma cadeia de permuta DXGI que é renderizada para um [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="7ffeb-135">The code here declares the properties for bitmap that links to a DXGI swap chain that renders to a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span> <span data-ttu-id="7ffeb-136">O método [**ID2D1DeviceContext:: CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) Obtém uma superfície de Direct2D da superfície DXGI.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-136">The [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method gets a Direct2D surface from the DXGI surface.</span></span> <span data-ttu-id="7ffeb-137">Isso faz com que tudo que seja processado para o [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) de destino seja renderizado para a superfície da cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-137">This makes it so anything rendered to the target [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is rendered to the surface of the swap chain.</span></span>

<span data-ttu-id="7ffeb-138">Quando você tiver a superfície Direct2D, use o método [**ID2D1DeviceContext:: SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) para defini-lo como o destino de renderização ativo.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-138">Once you have the Direct2D surface, use the [**ID2D1DeviceContext::SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) method to set it as the active render target.</span></span>


```C++
    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it will be directly rendered to the 
    // swapchain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // So now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



## <a name="step-4-create-a-brush"></a><span data-ttu-id="7ffeb-139">Etapa 4: criar um pincel</span><span class="sxs-lookup"><span data-stu-id="7ffeb-139">Step 4: Create a Brush</span></span>

<span data-ttu-id="7ffeb-140">Como uma fábrica, um contexto de dispositivo pode criar recursos de desenho.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-140">Like a factory, a device context can create drawing resources.</span></span> <span data-ttu-id="7ffeb-141">Neste exemplo, o contexto do dispositivo cria um pincel.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-141">In this example, the device context creates a brush.</span></span>


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



<span data-ttu-id="7ffeb-142">Um pincel é um objeto que pinta uma área, como o traço de uma forma ou o preenchimento de uma geometria.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-142">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="7ffeb-143">O pincel neste exemplo pinta uma área com uma cor sólida predefinida, preta.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-143">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="7ffeb-144">O Direct2D também fornece outros tipos de pincéis: pincéis de gradiente para pintura de gradientes lineares e radiais, um [**pincel de bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para pintura com bitmaps e padrões e, a partir do Windows 8, um [**pincel de imagem**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) para pintar com uma imagem renderizada.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-144">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, a [**bitmap brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) for painting with bitmaps and patterns, and starting in Windows 8, an [**image brush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) for painting with a rendered image.</span></span>

<span data-ttu-id="7ffeb-145">Algumas APIs de desenho fornecem canetas para desenhar contornos e pincéis para preencher formas.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-145">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="7ffeb-146">Direct2D é diferente: ele não fornece um objeto Pen, mas usa um pincel para desenhar contornos e preencher formas.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-146">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="7ffeb-147">Ao desenhar contornos, use a interface [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) ou a partir do Windows 8, a interface [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) , com um pincel para controlar as operações de traçado de caminho.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-147">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface, or starting in Windows 8 the [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) interface, with a brush to control path stroking operations.</span></span>

<span data-ttu-id="7ffeb-148">Um pincel só pode ser usado com o destino de renderização que o criou e com outros destinos de renderização no mesmo domínio de recurso.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-148">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="7ffeb-149">Em geral, você deve criar pincéis uma vez e remantê-las para a vida útil do destino de renderização que as criou.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-149">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="7ffeb-150">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) é a exceção solitário; Como é relativamente barato criar, você pode criar um **ID2D1SolidColorBrush** toda vez que desenhar um quadro, sem qualquer impacto perceptível no desempenho.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-150">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="7ffeb-151">Você também pode usar um único **ID2D1SolidColorBrush** e apenas alterar sua cor ou opacidade sempre que usá-lo.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-151">You can also use a single **ID2D1SolidColorBrush** and just change its color or opacity every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="7ffeb-152">Etapa 5: desenhar o retângulo</span><span class="sxs-lookup"><span data-stu-id="7ffeb-152">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="7ffeb-153">Em seguida, use o contexto do dispositivo para desenhar o retângulo.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-153">Next, use the device context to draw the rectangle.</span></span>


```C++
 
m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



<span data-ttu-id="7ffeb-154">O método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) usa dois parâmetros: o retângulo a ser desenhado e o pincel a ser usado para pintar o contorno do retângulo.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-154">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="7ffeb-155">Opcionalmente, você também pode especificar as opções largura do traço, padrão de tracejado, junção de linha e extremidade de fim.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-155">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="7ffeb-156">Você deve chamar o método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir qualquer comando de desenho, e deve chamar o método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) depois de concluir a emissão de comandos de desenho.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-156">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="7ffeb-157">O método **EndDraw** retorna um **HRESULT** que indica se os comandos de desenho foram bem-sucedidos.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-157">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span> <span data-ttu-id="7ffeb-158">Se não for bem-sucedida, a função auxiliar ThrowIfFailed gerará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-158">If it is not successful, the ThrowIfFailed helper function will throw an exception.</span></span>

<span data-ttu-id="7ffeb-159">O método [**IDXGISwapChain::P reenviado**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) troca a superfície do buffer pela superfície na tela para exibir o resultado.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-159">The [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method swaps the buffer surface with the on screen surface to display the result.</span></span>

## <a name="example-code"></a><span data-ttu-id="7ffeb-160">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="7ffeb-160">Example code</span></span>

<span data-ttu-id="7ffeb-161">O código neste tópico mostra os elementos básicos de um aplicativo Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-161">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="7ffeb-162">Para resumir, o tópico omite a estrutura do aplicativo e o código de tratamento de erros que é característica de um aplicativo bem escrito.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-162">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span>

 

 