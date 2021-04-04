---
title: Início rápido do Direct2D
description: Resume as etapas necessárias para desenhar com Direct2D e fornece código de exemplo.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D, exemplo de código de retângulo de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa59d7da057a7a9922e270d83937307762b06a40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084570"
---
# <a name="direct2d-quickstart"></a><span data-ttu-id="dc1ff-104">Início rápido do Direct2D</span><span class="sxs-lookup"><span data-stu-id="dc1ff-104">Direct2D QuickStart</span></span>

<span data-ttu-id="dc1ff-105">Direct2D é uma API de modo imediato, de código nativo para a criação de gráficos 2D.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-105">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="dc1ff-106">Este tópico ilustra como usar o Direct2D em um aplicativo Win32 típico para desenhar um **HWND**.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-106">This topic illustrates how to use Direct2D within a typical Win32 application to draw to an **HWND**.</span></span>

> [!Note]  
> <span data-ttu-id="dc1ff-107">Se você quiser criar um aplicativo da Windows Store que usa Direct2D, consulte o tópico [início rápido do Direct2D para Windows 8](direct2d-quickstart-with-device-context.md) .</span><span class="sxs-lookup"><span data-stu-id="dc1ff-107">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="dc1ff-108">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="dc1ff-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="dc1ff-109">Desenhando um retângulo simples</span><span class="sxs-lookup"><span data-stu-id="dc1ff-109">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="dc1ff-110">Etapa 1: incluir o cabeçalho Direct2D</span><span class="sxs-lookup"><span data-stu-id="dc1ff-110">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="dc1ff-111">Etapa 2: criar um ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="dc1ff-111">Step 2: Create an ID2D1Factory</span></span>](#step-2-create-an-id2d1factory)
-   [<span data-ttu-id="dc1ff-112">Etapa 3: criar um ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="dc1ff-112">Step 3: Create an ID2D1HwndRenderTarget</span></span>](#step-3-create-an-id2d1hwndrendertarget)
-   [<span data-ttu-id="dc1ff-113">Etapa 4: criar um pincel</span><span class="sxs-lookup"><span data-stu-id="dc1ff-113">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="dc1ff-114">Etapa 5: desenhar o retângulo</span><span class="sxs-lookup"><span data-stu-id="dc1ff-114">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="dc1ff-115">Etapa 6: liberar recursos</span><span class="sxs-lookup"><span data-stu-id="dc1ff-115">Step 6: Release Resources</span></span>](#step-6-release-resources)
-   [<span data-ttu-id="dc1ff-116">Criar um aplicativo Direct2D simples</span><span class="sxs-lookup"><span data-stu-id="dc1ff-116">Create a Simple Direct2D Application</span></span>](#create-a-simple-direct2d-application)
-   [<span data-ttu-id="dc1ff-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc1ff-117">Related topics</span></span>](#related-topics)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="dc1ff-118">Desenhando um retângulo simples</span><span class="sxs-lookup"><span data-stu-id="dc1ff-118">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="dc1ff-119">Para desenhar um retângulo usando [GDI](/windows/desktop/gdi/windows-gdi), você pode manipular a mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-119">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


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



<span data-ttu-id="dc1ff-120">O código para desenhar o mesmo retângulo com Direct2D é semelhante: ele cria recursos de desenho, descreve uma forma para desenhar, desenha a forma e libera os recursos de desenho.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-120">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="dc1ff-121">As seções a seguir descrevem cada uma dessas etapas em detalhes.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-121">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="dc1ff-122">Etapa 1: incluir o cabeçalho Direct2D</span><span class="sxs-lookup"><span data-stu-id="dc1ff-122">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="dc1ff-123">Além dos cabeçalhos necessários para um aplicativo Win32, inclua o cabeçalho d2d1. h.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-123">In addition to the headers required for a Win32 application, include the d2d1.h header.</span></span>

## <a name="step-2-create-an-id2d1factory"></a><span data-ttu-id="dc1ff-124">Etapa 2: criar um ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="dc1ff-124">Step 2: Create an ID2D1Factory</span></span>

<span data-ttu-id="dc1ff-125">Uma das primeiras coisas que qualquer exemplo de Direct2D faz é criar um [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="dc1ff-125">One of the first things that any Direct2D example does is create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



<span data-ttu-id="dc1ff-126">A interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) é o ponto de partida para usar Direct2D; Use um **ID2D1Factory** para criar recursos do Direct2D.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-126">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface is the starting point for using Direct2D; use an **ID2D1Factory** to create Direct2D resources.</span></span>

<span data-ttu-id="dc1ff-127">Ao criar uma fábrica, você pode especificar se ela é de vários ou de thread único.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-127">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="dc1ff-128">(Para obter mais informações sobre fábricas com vários threads, consulte os comentários na [**página de referência do ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) Este exemplo cria uma fábrica de thread único.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-128">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="dc1ff-129">Em geral, seu aplicativo deve criar a fábrica uma vez e mantê-la para a vida útil do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-129">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1hwndrendertarget"></a><span data-ttu-id="dc1ff-130">Etapa 3: criar um ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="dc1ff-130">Step 3: Create an ID2D1HwndRenderTarget</span></span>

<span data-ttu-id="dc1ff-131">Depois de criar uma fábrica, use-a para criar um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-131">After you create a factory, use it to create a render target.</span></span>


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



<span data-ttu-id="dc1ff-132">Um destino de renderização é um dispositivo que pode executar operações de desenho e criar recursos de desenho dependentes de dispositivo, como pincéis.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-132">A render target is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="dc1ff-133">Tipos diferentes de destinos de renderização renderizam para diferentes dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-133">Different types of render targets render to different devices.</span></span> <span data-ttu-id="dc1ff-134">O exemplo anterior usa um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), que é renderizado para uma parte da tela.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-134">The preceding example uses an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), which renders to a portion of the screen.</span></span>

<span data-ttu-id="dc1ff-135">Quando possível, um destino de renderização usa a GPU para acelerar as operações de renderização e criar recursos de desenho.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-135">When possible, a render target uses the GPU to accelerate rendering operations and create drawing resources.</span></span> <span data-ttu-id="dc1ff-136">Caso contrário, o destino de renderização usa a CPU para processar instruções de renderização e criar recursos.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-136">Otherwise, the render target uses the CPU to process rendering instructions and create resources.</span></span> <span data-ttu-id="dc1ff-137">(Você pode modificar esse comportamento usando os sinalizadores [**de \_ \_ \_ tipo de destino d2d1 render**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) ao criar o destino render.)</span><span class="sxs-lookup"><span data-stu-id="dc1ff-137">(You can modify this behavior by using the [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) flags when you create the render target.)</span></span>

<span data-ttu-id="dc1ff-138">O método [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) usa três parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-138">The [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method takes three parameters.</span></span> <span data-ttu-id="dc1ff-139">O primeiro parâmetro, uma estrutura de [**\_ Propriedades de \_ destino \_ de renderização d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , especifica opções de exibição remotas, se deve forçar o destino de renderização a renderizar para software ou hardware e o DPI.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-139">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) struct, specifies remote display options, whether to force the render target to render to software or hardware, and the DPI.</span></span> <span data-ttu-id="dc1ff-140">O código neste exemplo usa a função auxiliar [**d2d1:: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) para aceitar Propriedades de destino de renderização padrão.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-140">The code in this example uses the [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) helper function to accept default render target properties.</span></span>

<span data-ttu-id="dc1ff-141">O segundo parâmetro, uma estrutura de [**\_ \_ \_ \_ Propriedades de destino de d2d1 HWND**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) , especifica o **HWND** para o qual o conteúdo é renderizado, o tamanho inicial do destino de renderização (em pixels) e suas [**Opções de apresentação**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options).</span><span class="sxs-lookup"><span data-stu-id="dc1ff-141">The second parameter, a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) struct, specifies the **HWND** to which content is rendered, the initial size of the render target (in pixels), and its [**presentation options**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options).</span></span> <span data-ttu-id="dc1ff-142">Este exemplo usa a função auxiliar [**d2d1:: HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) para especificar um HWND e um tamanho inicial.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-142">This example uses the [**D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) helper function to specify an HWND and initial size.</span></span> <span data-ttu-id="dc1ff-143">Ele usa opções de apresentação padrão.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-143">It uses default presentation options.</span></span>

<span data-ttu-id="dc1ff-144">O terceiro parâmetro é o endereço do ponteiro que recebe a referência de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-144">The third parameter is the address of the pointer that receives the render target reference.</span></span>

<span data-ttu-id="dc1ff-145">Quando você cria um destino de renderização e a aceleração de hardware está disponível, você aloca recursos na GPU do computador.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-145">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="dc1ff-146">Ao criar um destino de renderização uma vez e mantê-lo o mais longo possível, você obterá benefícios de desempenho.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-146">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="dc1ff-147">Seu aplicativo deve criar destinos de renderização uma vez e mantê-los durante a vida útil do aplicativo ou até que o erro de [**\_ \_ destino de recriação de D2DERR**](direct2d-error-codes.md) seja recebido.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-147">Your application should create render targets once and hold on to them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="dc1ff-148">Quando receber esse erro, você precisará recriar o destino de renderização (e todos os recursos que ele criou).</span><span class="sxs-lookup"><span data-stu-id="dc1ff-148">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="step-4-create-a-brush"></a><span data-ttu-id="dc1ff-149">Etapa 4: criar um pincel</span><span class="sxs-lookup"><span data-stu-id="dc1ff-149">Step 4: Create a Brush</span></span>

<span data-ttu-id="dc1ff-150">Como uma fábrica, um destino de renderização pode criar recursos de desenho.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-150">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="dc1ff-151">Neste exemplo, o destino de renderização cria um pincel.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-151">In this example, the render target creates a brush.</span></span>


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



<span data-ttu-id="dc1ff-152">Um pincel é um objeto que pinta uma área, como o traço de uma forma ou o preenchimento de uma geometria.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-152">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="dc1ff-153">O pincel neste exemplo pinta uma área com uma cor sólida predefinida, preta.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-153">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="dc1ff-154">O Direct2D também fornece outros tipos de pincéis: pincéis de gradiente para pintar gradientes lineares e radiais e um pincel de bitmap para pintura com bitmaps e padrões.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-154">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, and a bitmap brush for painting with bitmaps and patterns.</span></span>

<span data-ttu-id="dc1ff-155">Algumas APIs de desenho fornecem canetas para desenhar contornos e pincéis para preencher formas.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-155">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="dc1ff-156">Direct2D é diferente: ele não fornece um objeto Pen, mas usa um pincel para desenhar contornos e preencher formas.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-156">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="dc1ff-157">Ao desenhar contornos, use a interface [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) com um pincel para controlar as operações de traçado de caminho.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-157">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface with a brush to control path stroking operations.</span></span>

<span data-ttu-id="dc1ff-158">Um pincel só pode ser usado com o destino de renderização que o criou e com outros destinos de renderização no mesmo domínio de recurso.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-158">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="dc1ff-159">Em geral, você deve criar pincéis uma vez e remantê-las para a vida útil do destino de renderização que as criou.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-159">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="dc1ff-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) é a exceção solitário; Como é relativamente barato criar, você pode criar um **ID2D1SolidColorBrush** toda vez que desenhar um quadro, sem qualquer impacto perceptível no desempenho.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="dc1ff-161">Você também pode usar um único **ID2D1SolidColorBrush** e apenas alterar sua cor toda vez que usá-lo.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-161">You can also use a single **ID2D1SolidColorBrush** and just change its color every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="dc1ff-162">Etapa 5: desenhar o retângulo</span><span class="sxs-lookup"><span data-stu-id="dc1ff-162">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="dc1ff-163">Em seguida, use o destino de renderização para desenhar o retângulo.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-163">Next, use the render target to draw the rectangle.</span></span>


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



<span data-ttu-id="dc1ff-164">O método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) usa dois parâmetros: o retângulo a ser desenhado e o pincel a ser usado para pintar o contorno do retângulo.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-164">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="dc1ff-165">Opcionalmente, você também pode especificar as opções largura do traço, padrão de tracejado, junção de linha e extremidade de fim.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-165">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="dc1ff-166">Você deve chamar o método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir qualquer comando de desenho, e deve chamar o método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) depois de concluir a emissão de comandos de desenho.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-166">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="dc1ff-167">O método **EndDraw** retorna um **HRESULT** que indica se os comandos de desenho foram bem-sucedidos.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-167">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span>

## <a name="step-6-release-resources"></a><span data-ttu-id="dc1ff-168">Etapa 6: liberar recursos</span><span class="sxs-lookup"><span data-stu-id="dc1ff-168">Step 6: Release Resources</span></span>

<span data-ttu-id="dc1ff-169">Quando não houver mais quadros para desenhar, ou quando você receber o erro [**de \_ \_ destino de recriação de D2DERR**](direct2d-error-codes.md) , libere o destino de renderização e todos os dispositivos que ele criou.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-169">When there are no more frames to draw, or when you receive the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error, release the render target and any devices it created.</span></span>


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



<span data-ttu-id="dc1ff-170">Quando o aplicativo terminar de usar os recursos do Direct2D (como quando está prestes a sair), libere a fábrica do Direct2D.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-170">When your application has finished using Direct2D resources (such as when it is about to exit), release the Direct2D factory.</span></span>


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a><span data-ttu-id="dc1ff-171">Criar um aplicativo Direct2D simples</span><span class="sxs-lookup"><span data-stu-id="dc1ff-171">Create a Simple Direct2D Application</span></span>

<span data-ttu-id="dc1ff-172">O código neste tópico mostra os elementos básicos de um aplicativo Direct2D.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-172">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="dc1ff-173">Para resumir, o tópico omite a estrutura do aplicativo e o código de tratamento de erros que é característica de um aplicativo bem escrito.</span><span class="sxs-lookup"><span data-stu-id="dc1ff-173">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span> <span data-ttu-id="dc1ff-174">Para obter um passo a passo mais detalhado que mostra o código completo para criar um aplicativo Direct2D simples e demonstra as melhores práticas de design, consulte [criando um aplicativo Direct2D simples](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="dc1ff-174">For a more detailed walk-through that shows the complete code for creating a simple Direct2D application and demonstrates best design practices, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc1ff-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc1ff-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc1ff-176">Criando um aplicativo Direct2D simples</span><span class="sxs-lookup"><span data-stu-id="dc1ff-176">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> </dl>

 

 