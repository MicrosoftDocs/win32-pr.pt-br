---
title: Renderizar Alvos, Dispositivos e Recursos
description: Renderizar Alvos, Dispositivos e Recursos
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeddd84e12c52e0fd0ae82dab8b5e8741a2e0891
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293991"
---
# <a name="render-targets-devices-and-resources"></a><span data-ttu-id="14364-103">Renderizar Alvos, Dispositivos e Recursos</span><span class="sxs-lookup"><span data-stu-id="14364-103">Render Targets, Devices, and Resources</span></span>

<span data-ttu-id="14364-104">Um *destino de renderização* é simplesmente o local onde o programa será desenhado.</span><span class="sxs-lookup"><span data-stu-id="14364-104">A *render target* is simply the location where your program will draw.</span></span> <span data-ttu-id="14364-105">Normalmente, o destino de renderização é uma janela (especificamente, a área cliente da janela).</span><span class="sxs-lookup"><span data-stu-id="14364-105">Typically, the render target is a window (specifically, the client area of the window).</span></span> <span data-ttu-id="14364-106">Também pode ser um bitmap na memória que não é exibido.</span><span class="sxs-lookup"><span data-stu-id="14364-106">It could also be a bitmap in memory that is not displayed.</span></span> <span data-ttu-id="14364-107">Um destino de renderização é representado pela interface [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="14364-107">A render target is represented by the [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span>

<span data-ttu-id="14364-108">Um *dispositivo* é uma abstração que representa o que realmente desenha os pixels.</span><span class="sxs-lookup"><span data-stu-id="14364-108">A *device* is an abstraction that represents whatever actually draws the pixels.</span></span> <span data-ttu-id="14364-109">Um dispositivo de hardware usa a GPU para um desempenho mais rápido, enquanto que um dispositivo de software usa a CPU.</span><span class="sxs-lookup"><span data-stu-id="14364-109">A hardware device uses the GPU for faster performance, whereas a software device uses the CPU.</span></span> <span data-ttu-id="14364-110">O aplicativo não cria o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14364-110">The application does not create the device.</span></span> <span data-ttu-id="14364-111">Em vez disso, o dispositivo é criado implicitamente quando o aplicativo cria o destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="14364-111">Instead, the device is created implicitly when the application creates the render target.</span></span> <span data-ttu-id="14364-112">Cada destino de renderização é associado a um dispositivo específico, de hardware ou software.</span><span class="sxs-lookup"><span data-stu-id="14364-112">Each render target is associated with a particular device, either hardware or software.</span></span>

![um diagrama que mostra a relação entre um destino de renderização e um dispositivo.](images/graphics09.png)

<span data-ttu-id="14364-114">Um *recurso* é um objeto que o programa usa para desenhar.</span><span class="sxs-lookup"><span data-stu-id="14364-114">A *resource* is an object that the program uses for drawing.</span></span> <span data-ttu-id="14364-115">Aqui estão alguns exemplos de recursos que são definidos em Direct2D:</span><span class="sxs-lookup"><span data-stu-id="14364-115">Here are some examples of resources that are defined in Direct2D:</span></span>

-   <span data-ttu-id="14364-116">**Pincel**.</span><span class="sxs-lookup"><span data-stu-id="14364-116">**Brush**.</span></span> <span data-ttu-id="14364-117">Controla como as linhas e regiões são pintadas.</span><span class="sxs-lookup"><span data-stu-id="14364-117">Controls how lines and regions are painted.</span></span> <span data-ttu-id="14364-118">Os tipos de pincel incluem pincéis de cor sólida e pincéis de gradiente.</span><span class="sxs-lookup"><span data-stu-id="14364-118">Brush types include solid-color brushes and gradient brushes.</span></span>
-   <span data-ttu-id="14364-119">**Estilo do traço**.</span><span class="sxs-lookup"><span data-stu-id="14364-119">**Stroke style**.</span></span> <span data-ttu-id="14364-120">Controla a aparência de uma linha, por exemplo, tracejada ou sólida.</span><span class="sxs-lookup"><span data-stu-id="14364-120">Controls the appearance of a line—for example, dashed or solid.</span></span>
-   <span data-ttu-id="14364-121">**Geometry**.</span><span class="sxs-lookup"><span data-stu-id="14364-121">**Geometry**.</span></span> <span data-ttu-id="14364-122">Representa uma coleção de linhas e curvas.</span><span class="sxs-lookup"><span data-stu-id="14364-122">Represents a collection of lines and curves.</span></span>
-   <span data-ttu-id="14364-123">**Malha**.</span><span class="sxs-lookup"><span data-stu-id="14364-123">**Mesh**.</span></span> <span data-ttu-id="14364-124">Uma forma formada fora dos triângulos.</span><span class="sxs-lookup"><span data-stu-id="14364-124">A shape formed out of triangles.</span></span> <span data-ttu-id="14364-125">Os dados de malha podem ser consumidos diretamente pela GPU, ao contrário dos dados de geometria, que devem ser convertidos antes da renderização.</span><span class="sxs-lookup"><span data-stu-id="14364-125">Mesh data can be consumed directly by the GPU, unlike geometry data, which must be converted before rendering.</span></span>

<span data-ttu-id="14364-126">Os destinos de renderização também são considerados um tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="14364-126">Render targets are also considered a type of resource.</span></span>

<span data-ttu-id="14364-127">Alguns recursos se beneficiam da aceleração de hardware.</span><span class="sxs-lookup"><span data-stu-id="14364-127">Some resources benefit from hardware acceleration.</span></span> <span data-ttu-id="14364-128">Um recurso desse tipo é sempre associado a um dispositivo específico, hardware (GPU) ou software (CPU).</span><span class="sxs-lookup"><span data-stu-id="14364-128">A resource of this type is always associated with a particular device, either hardware (GPU) or software (CPU).</span></span> <span data-ttu-id="14364-129">Esse tipo de recurso é chamado *de dependente de dispositivo*.</span><span class="sxs-lookup"><span data-stu-id="14364-129">This type of resource is called *device-dependent*.</span></span> <span data-ttu-id="14364-130">Pincéis e malhas são exemplos de recursos dependentes do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14364-130">Brushes and meshes are examples of device-dependent resources.</span></span> <span data-ttu-id="14364-131">Se o dispositivo ficar indisponível, o recurso deverá ser recriado para um novo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14364-131">If the device becomes unavailable, the resource must be re-created for a new device.</span></span>

<span data-ttu-id="14364-132">Outros recursos são mantidos na memória da CPU, independentemente de qual dispositivo é usado.</span><span class="sxs-lookup"><span data-stu-id="14364-132">Other resources are kept in CPU memory, regardless of what device is used.</span></span> <span data-ttu-id="14364-133">Esses recursos são *independentes de dispositivo*, pois não estão associados a um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="14364-133">These resources are *device-independent*, because they are not associated with a particular device.</span></span> <span data-ttu-id="14364-134">Não é necessário recriar recursos independentes de dispositivo quando o dispositivo é alterado.</span><span class="sxs-lookup"><span data-stu-id="14364-134">It is not necessary to re-create device-independent resources when the device changes.</span></span> <span data-ttu-id="14364-135">Estilos e geometrias de traço são recursos independentes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14364-135">Stroke styles and geometries are device-independent resources.</span></span>

<span data-ttu-id="14364-136">A documentação do MSDN para cada recurso informa se o recurso é dependente de dispositivo ou independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14364-136">The MSDN documentation for each resource states whether the resource is device-dependent or device-independent.</span></span> <span data-ttu-id="14364-137">Cada tipo de recurso é representado por uma interface que deriva de [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource).</span><span class="sxs-lookup"><span data-stu-id="14364-137">Every resource type is represented by an interface that derives from [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource).</span></span> <span data-ttu-id="14364-138">Por exemplo, os pincéis são representados pela interface [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) .</span><span class="sxs-lookup"><span data-stu-id="14364-138">For example, brushes are represented by the [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) interface.</span></span>

## <a name="the-direct2d-factory-object"></a><span data-ttu-id="14364-139">O objeto de fábrica Direct2D</span><span class="sxs-lookup"><span data-stu-id="14364-139">The Direct2D Factory Object</span></span>

<span data-ttu-id="14364-140">A primeira etapa ao usar Direct2D é criar uma instância do objeto de fábrica Direct2D.</span><span class="sxs-lookup"><span data-stu-id="14364-140">The first step when using Direct2D is to create an instance of the Direct2D factory object.</span></span> <span data-ttu-id="14364-141">Na programação de computador, uma *fábrica* é um objeto que cria outros objetos.</span><span class="sxs-lookup"><span data-stu-id="14364-141">In computer programming, a *factory* is an object that creates other objects.</span></span> <span data-ttu-id="14364-142">A fábrica Direct2D cria os seguintes tipos de objetos:</span><span class="sxs-lookup"><span data-stu-id="14364-142">The Direct2D factory creates the following types of objects:</span></span>

-   <span data-ttu-id="14364-143">Processar destinos.</span><span class="sxs-lookup"><span data-stu-id="14364-143">Render targets.</span></span>
-   <span data-ttu-id="14364-144">Recursos independentes de dispositivo, como estilos de traço e geometrias.</span><span class="sxs-lookup"><span data-stu-id="14364-144">Device-independent resources, such as stroke styles and geometries.</span></span>

<span data-ttu-id="14364-145">Recursos dependentes do dispositivo, como pincéis e bitmaps, são criados pelo objeto de destino render.</span><span class="sxs-lookup"><span data-stu-id="14364-145">Device-dependent resources, such as brushes and bitmaps, are created by the render target object.</span></span>

![um diagrama que mostra a fábrica Direct2D.](images/graphics10.png)

<span data-ttu-id="14364-147">Para criar o objeto de fábrica Direct2D, chame a função [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .</span><span class="sxs-lookup"><span data-stu-id="14364-147">To create the Direct2D factory object, call the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



<span data-ttu-id="14364-148">O primeiro parâmetro é um sinalizador que especifica as opções de criação.</span><span class="sxs-lookup"><span data-stu-id="14364-148">The first parameter is a flag that specifies creation options.</span></span> <span data-ttu-id="14364-149">O sinalizador de **\_ \_ \_ \_ thread único do tipo de fábrica d2d1** significa que você não chamará Direct2D de vários threads.</span><span class="sxs-lookup"><span data-stu-id="14364-149">The **D2D1\_FACTORY\_TYPE\_SINGLE\_THREADED** flag means that you will not call Direct2D from multiple threads.</span></span> <span data-ttu-id="14364-150">Para dar suporte a chamadas de vários threads, especifique o **tipo de fábrica d2d1 com \_ \_ \_ vários \_ threads**.</span><span class="sxs-lookup"><span data-stu-id="14364-150">To support calls from multiple threads, specify **D2D1\_FACTORY\_TYPE\_MULTI\_THREADED**.</span></span> <span data-ttu-id="14364-151">Se o seu programa usar um único thread para chamar o Direct2D, a opção de thread único será mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="14364-151">If your program uses a single thread to call into Direct2D, the single-threaded option is more efficient.</span></span>

<span data-ttu-id="14364-152">O segundo parâmetro para a função [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) recebe um ponteiro para a interface [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) .</span><span class="sxs-lookup"><span data-stu-id="14364-152">The second parameter to the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function receives a pointer to the [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) interface.</span></span>

<span data-ttu-id="14364-153">Você deve criar o objeto de fábrica Direct2D antes da primeira mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="14364-153">You should create the Direct2D factory object before the first [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="14364-154">O manipulador de [**\_ criação**](/windows/desktop/winmsg/wm-create) de mensagem do WM é um bom local para criar a fábrica:</span><span class="sxs-lookup"><span data-stu-id="14364-154">The [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message handler is a good place to create the factory:</span></span>


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a><span data-ttu-id="14364-155">Criando recursos do Direct2D</span><span class="sxs-lookup"><span data-stu-id="14364-155">Creating Direct2D Resources</span></span>

<span data-ttu-id="14364-156">O programa Circle usa os seguintes recursos dependentes do dispositivo:</span><span class="sxs-lookup"><span data-stu-id="14364-156">The Circle program uses the following device-dependent resources:</span></span>

-   <span data-ttu-id="14364-157">Um destino de renderização associado à janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14364-157">A render target that is associated with the application window.</span></span>
-   <span data-ttu-id="14364-158">Um pincel de cor sólida para pintar o círculo.</span><span class="sxs-lookup"><span data-stu-id="14364-158">A solid-color brush to paint the circle.</span></span>

<span data-ttu-id="14364-159">Cada um desses recursos é representado por uma interface COM:</span><span class="sxs-lookup"><span data-stu-id="14364-159">Each of these resources is represented by a COM interface:</span></span>

-   <span data-ttu-id="14364-160">A interface [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) representa o destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="14364-160">The [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) interface represents the render target.</span></span>
-   <span data-ttu-id="14364-161">A interface [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) representa o pincel.</span><span class="sxs-lookup"><span data-stu-id="14364-161">The [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interface represents the brush.</span></span>

<span data-ttu-id="14364-162">O programa Circle armazena ponteiros para essas interfaces como variáveis de membro da `MainWindow` classe:</span><span class="sxs-lookup"><span data-stu-id="14364-162">The Circle program stores pointers to these interfaces as member variables of the `MainWindow` class:</span></span>


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



<span data-ttu-id="14364-163">O código a seguir cria esses dois recursos.</span><span class="sxs-lookup"><span data-stu-id="14364-163">The following code creates these two resources.</span></span>


```C++
HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}
```



<span data-ttu-id="14364-164">Para criar um destino de renderização para uma janela, chame o método [**ID2D1Factory:: CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) na fábrica Direct2D.</span><span class="sxs-lookup"><span data-stu-id="14364-164">To create a render target for a window, call the [**ID2D1Factory::CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method on the Direct2D factory.</span></span>

-   <span data-ttu-id="14364-165">O primeiro parâmetro especifica opções que são comuns a qualquer tipo de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="14364-165">The first parameter specifies options that are common to any type of render target.</span></span> <span data-ttu-id="14364-166">Aqui, passamos as opções padrão chamando a função auxiliar [**d2d1:: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).</span><span class="sxs-lookup"><span data-stu-id="14364-166">Here, we pass in default options by calling the helper function [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).</span></span>
-   <span data-ttu-id="14364-167">O segundo parâmetro especifica o identificador para a janela mais o tamanho do destino de renderização, em pixels.</span><span class="sxs-lookup"><span data-stu-id="14364-167">The second parameter specifies the handle to the window plus the size of the render target, in pixels.</span></span>
-   <span data-ttu-id="14364-168">O terceiro parâmetro recebe um ponteiro [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="14364-168">The third parameter receives an [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) pointer.</span></span>

<span data-ttu-id="14364-169">Para criar o pincel de cor sólida, chame o método [**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) no destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="14364-169">To create the solid-color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method on the render target.</span></span> <span data-ttu-id="14364-170">A cor é fornecida como um [**valor \_ \_ F de cor d2d1**](/windows/desktop/Direct2D/d2d1-color-f) .</span><span class="sxs-lookup"><span data-stu-id="14364-170">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) value.</span></span> <span data-ttu-id="14364-171">Para obter mais informações sobre cores em Direct2D, consulte [usando a cor em Direct2D](using-color-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="14364-171">For more information about colors in Direct2D, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>

<span data-ttu-id="14364-172">Além disso, observe que, se o destino de renderização já existir, o `CreateGraphicsResources` método retornará **S \_ OK** sem fazer nada.</span><span class="sxs-lookup"><span data-stu-id="14364-172">Also, notice that if the render target already exists, the `CreateGraphicsResources` method returns **S\_OK** without doing anything.</span></span> <span data-ttu-id="14364-173">O motivo para esse design ficará claro no próximo tópico.</span><span class="sxs-lookup"><span data-stu-id="14364-173">The reason for this design will become clear in the next topic.</span></span>

## <a name="next"></a><span data-ttu-id="14364-174">Avançar</span><span class="sxs-lookup"><span data-stu-id="14364-174">Next</span></span>

[<span data-ttu-id="14364-175">Desenhar com Direct2D</span><span class="sxs-lookup"><span data-stu-id="14364-175">Drawing with Direct2D</span></span>](drawing-with-direct2d.md)

 

 