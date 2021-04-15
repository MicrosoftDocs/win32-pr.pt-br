---
title: Desenhar com Direct2D
description: Depois de criar seus recursos gráficos, você estará pronto para desenhar.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f8f3cf82d3ce6f485a7c54700c32c9eb65d054
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454010"
---
# <a name="drawing-with-direct2d"></a><span data-ttu-id="86f9f-103">Desenhar com Direct2D</span><span class="sxs-lookup"><span data-stu-id="86f9f-103">Drawing with Direct2D</span></span>

<span data-ttu-id="86f9f-104">Depois de criar seus recursos gráficos, você estará pronto para desenhar.</span><span class="sxs-lookup"><span data-stu-id="86f9f-104">After you create your graphics resources, you are ready to draw.</span></span>

## <a name="drawing-an-ellipse"></a><span data-ttu-id="86f9f-105">Desenhando uma elipse</span><span class="sxs-lookup"><span data-stu-id="86f9f-105">Drawing an Ellipse</span></span>

<span data-ttu-id="86f9f-106">O programa [Circle](your-first-direct2d-program.md) executa uma lógica de desenho muito simples:</span><span class="sxs-lookup"><span data-stu-id="86f9f-106">The [Circle](your-first-direct2d-program.md) program performs very simple drawing logic:</span></span>

1.  <span data-ttu-id="86f9f-107">Preencha o plano de fundo com uma cor sólida.</span><span class="sxs-lookup"><span data-stu-id="86f9f-107">Fill the background with a solid color.</span></span>
2.  <span data-ttu-id="86f9f-108">Desenhe um círculo preenchido.</span><span class="sxs-lookup"><span data-stu-id="86f9f-108">Draw a filled circle.</span></span>

![uma captura de tela do programa de círculo.](images/graphics08.png)

<span data-ttu-id="86f9f-110">Como o destino de renderização é uma janela (em oposição a um bitmap ou outra superfície fora da tela), o desenho é feito em resposta às mensagens do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="86f9f-110">Because the render target is a window (as opposed to a bitmap or other offscreen surface), drawing is done in response to [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) messages.</span></span> <span data-ttu-id="86f9f-111">O código a seguir mostra o procedimento de janela para o programa de círculo.</span><span class="sxs-lookup"><span data-stu-id="86f9f-111">The following code shows the window procedure for the Circle program.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_PAINT:
            OnPaint();
            return 0;

         // Other messages not shown...
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```

<span data-ttu-id="86f9f-112">Este é o código que desenha o círculo.</span><span class="sxs-lookup"><span data-stu-id="86f9f-112">Here is the code that draws the circle.</span></span>

```C++
void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="86f9f-113">A interface [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) é usada para todas as operações de desenho.</span><span class="sxs-lookup"><span data-stu-id="86f9f-113">The [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface is used for all drawing operations.</span></span> <span data-ttu-id="86f9f-114">O método do programa `OnPaint` faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="86f9f-114">The program's `OnPaint` method does the following:</span></span>

1.  <span data-ttu-id="86f9f-115">O método [**ID2D1RenderTarget:: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) sinaliza o início do desenho.</span><span class="sxs-lookup"><span data-stu-id="86f9f-115">The [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method signals the start of drawing.</span></span>
2.  <span data-ttu-id="86f9f-116">O método [**ID2D1RenderTarget:: Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) preenche todo o destino de renderização com uma cor sólida.</span><span class="sxs-lookup"><span data-stu-id="86f9f-116">The [**ID2D1RenderTarget::Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) method fills the entire render target with a solid color.</span></span> <span data-ttu-id="86f9f-117">A cor é fornecida como uma [**estrutura \_ \_ F de cor d2d1**](/windows/desktop/Direct2D/d2d1-color-f) .</span><span class="sxs-lookup"><span data-stu-id="86f9f-117">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) structure.</span></span> <span data-ttu-id="86f9f-118">Você pode usar a classe [**d2d1:: colorf**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) para inicializar a estrutura.</span><span class="sxs-lookup"><span data-stu-id="86f9f-118">You can use the [**D2D1::ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) class to initialize the structure.</span></span> <span data-ttu-id="86f9f-119">Para obter mais informações, consulte [usando a cor em Direct2D](using-color-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="86f9f-119">For more information, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>
3.  <span data-ttu-id="86f9f-120">O método [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) desenha uma elipse preenchida, usando o pincel especificado para o preenchimento.</span><span class="sxs-lookup"><span data-stu-id="86f9f-120">The [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws a filled ellipse, using the specified brush for the fill.</span></span> <span data-ttu-id="86f9f-121">Uma elipse é especificada por um ponto central e o raios x e y.</span><span class="sxs-lookup"><span data-stu-id="86f9f-121">An ellipse is specified by a center point and the x- and y-radii.</span></span> <span data-ttu-id="86f9f-122">Se o raios x e y forem os mesmos, o resultado será um círculo.</span><span class="sxs-lookup"><span data-stu-id="86f9f-122">If the x- and y-radii are the same, the result is a circle.</span></span>
4.  <span data-ttu-id="86f9f-123">O método [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) sinaliza a conclusão do desenho para este quadro.</span><span class="sxs-lookup"><span data-stu-id="86f9f-123">The [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method signals the completion of drawing for this frame.</span></span> <span data-ttu-id="86f9f-124">Todas as operações de desenho devem ser colocadas entre as chamadas para [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e **EndDraw**.</span><span class="sxs-lookup"><span data-stu-id="86f9f-124">All drawing operations must be placed between calls to [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw**.</span></span>

<span data-ttu-id="86f9f-125">Todos os métodos [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)e [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) têm um tipo de retorno **void** .</span><span class="sxs-lookup"><span data-stu-id="86f9f-125">The [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear), and [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) methods all have a **void** return type.</span></span> <span data-ttu-id="86f9f-126">Se ocorrer um erro durante a execução de qualquer um desses métodos, o erro será sinalizado pelo valor de retorno do método [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="86f9f-126">If an error occurs during the execution of any of these methods, the error is signaled through the return value of the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="86f9f-127">O `CreateGraphicsResources` método é mostrado no tópico [criando recursos Direct2D](render-targets--devices--and-resources.md).</span><span class="sxs-lookup"><span data-stu-id="86f9f-127">The `CreateGraphicsResources` method is shown in the topic [Creating Direct2D Resources](render-targets--devices--and-resources.md).</span></span> <span data-ttu-id="86f9f-128">Esse método cria o destino de renderização e o pincel de cor sólida.</span><span class="sxs-lookup"><span data-stu-id="86f9f-128">This method creates the render target and the solid-color brush.</span></span>

<span data-ttu-id="86f9f-129">O dispositivo pode armazenar em buffer os comandos de desenho e adiar sua execução até que o [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="86f9f-129">The device might buffer the drawing commands and defer executing them until [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) is called.</span></span> <span data-ttu-id="86f9f-130">Você pode forçar o dispositivo a executar qualquer comando de desenho pendente chamando [**ID2D1RenderTarget:: flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span><span class="sxs-lookup"><span data-stu-id="86f9f-130">You can force the device to execute any pending drawing commands by calling [**ID2D1RenderTarget::Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span> <span data-ttu-id="86f9f-131">No entanto, a liberação pode reduzir o desempenho.</span><span class="sxs-lookup"><span data-stu-id="86f9f-131">Flushing can reduce performance, however.</span></span>

## <a name="handling-device-loss"></a><span data-ttu-id="86f9f-132">Lidando com a perda de dispositivo</span><span class="sxs-lookup"><span data-stu-id="86f9f-132">Handling Device Loss</span></span>

<span data-ttu-id="86f9f-133">Enquanto o programa está em execução, o dispositivo de gráficos que você está usando pode se tornar indisponível.</span><span class="sxs-lookup"><span data-stu-id="86f9f-133">While your program is running, the graphics device that you are using might become unavailable.</span></span> <span data-ttu-id="86f9f-134">Por exemplo, o dispositivo poderá ser perdido se a resolução de vídeo for alterada ou se o usuário remover o adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="86f9f-134">For example, the device can be lost if the display resolution changes, or if the user removes the display adapter.</span></span> <span data-ttu-id="86f9f-135">Se o dispositivo for perdido, o destino de renderização também se tornará inválido, juntamente com todos os recursos dependentes do dispositivo que foram associados ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86f9f-135">If the device is lost, the render target also becomes invalid, along with any device-dependent resources that were associated with the device.</span></span> <span data-ttu-id="86f9f-136">Direct2D sinaliza um dispositivo perdido retornando o código de erro **D2DERR \_ recriar \_ destino** do método [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="86f9f-136">Direct2D signals a lost device by returning the error code **D2DERR\_RECREATE\_TARGET** from the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="86f9f-137">Se você receber esse código de erro, deverá recriar o destino de renderização e todos os recursos dependentes do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86f9f-137">If you receive this error code, you must re-create the render target and all device-dependent resources.</span></span>

<span data-ttu-id="86f9f-138">Para descartar um recurso, basta liberar a interface para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="86f9f-138">To discard a resource, simply release the interface for that resource.</span></span>


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



<span data-ttu-id="86f9f-139">A criação de um recurso pode ser uma operação cara, portanto, não recrie seus recursos para todas as mensagens do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="86f9f-139">Creating a resource can be an expensive operation, so do not recreate your resources for every [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="86f9f-140">Crie um recurso uma vez e armazene o ponteiro do recurso em cache até que o recurso se torne inválido devido à perda do dispositivo ou até que você não precise mais desse recurso.</span><span class="sxs-lookup"><span data-stu-id="86f9f-140">Create a resource once, and cache the resource pointer until the resource becomes invalid due to device loss, or until you no longer need that resource.</span></span>

## <a name="the-direct2d-render-loop"></a><span data-ttu-id="86f9f-141">O loop de renderização Direct2D</span><span class="sxs-lookup"><span data-stu-id="86f9f-141">The Direct2D Render Loop</span></span>

<span data-ttu-id="86f9f-142">Independentemente do que você desenhar, o programa deve executar um loop semelhante ao seguinte.</span><span class="sxs-lookup"><span data-stu-id="86f9f-142">Regardless of what you draw, your program should perform a loop similar to following.</span></span>

1.  <span data-ttu-id="86f9f-143">Crie recursos independentes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86f9f-143">Create device-independent resources.</span></span>
2.  <span data-ttu-id="86f9f-144">Renderizar a cena.</span><span class="sxs-lookup"><span data-stu-id="86f9f-144">Render the scene.</span></span>
    1.  <span data-ttu-id="86f9f-145">Verifique se existe um destino de renderização válido.</span><span class="sxs-lookup"><span data-stu-id="86f9f-145">Check if a valid render target exists.</span></span> <span data-ttu-id="86f9f-146">Caso contrário, crie o destino de renderização e os recursos dependentes do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86f9f-146">If not, create the render target and the device-dependent resources.</span></span>
    2.  <span data-ttu-id="86f9f-147">Chame [**ID2D1RenderTarget:: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).</span><span class="sxs-lookup"><span data-stu-id="86f9f-147">Call [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).</span></span>
    3.  <span data-ttu-id="86f9f-148">Emitir comandos de desenho.</span><span class="sxs-lookup"><span data-stu-id="86f9f-148">Issue drawing commands.</span></span>
    4.  <span data-ttu-id="86f9f-149">Chame [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="86f9f-149">Call [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>
    5.  <span data-ttu-id="86f9f-150">Se [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) retornar **D2DERR \_ recriar \_ destino**, descarte os recursos de destino de renderização e dependentes do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86f9f-150">If [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) returns **D2DERR\_RECREATE\_TARGET**, discard the render target and device-dependent resources.</span></span>
3.  <span data-ttu-id="86f9f-151">Repita a etapa 2 sempre que precisar atualizar ou redesenhar a cena.</span><span class="sxs-lookup"><span data-stu-id="86f9f-151">Repeat step 2 whenever you need to update or redraw the scene.</span></span>

<span data-ttu-id="86f9f-152">Se o destino de renderização for uma janela, a etapa 2 ocorrerá sempre que a janela receber uma mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="86f9f-152">If the render target is a window, step 2 occurs whenever the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="86f9f-153">O loop mostrado aqui lida com a perda do dispositivo descartando os recursos dependentes do dispositivo e recriando-os no início do próximo loop (etapa 2a).</span><span class="sxs-lookup"><span data-stu-id="86f9f-153">The loop shown here handles device loss by discarding the device-dependent resources and re-creating them at the start of the next loop (step 2a).</span></span>

## <a name="next"></a><span data-ttu-id="86f9f-154">Avançar</span><span class="sxs-lookup"><span data-stu-id="86f9f-154">Next</span></span>

[<span data-ttu-id="86f9f-155">DPI e Device-Independent pixels</span><span class="sxs-lookup"><span data-stu-id="86f9f-155">DPI and Device-Independent Pixels</span></span>](dpi-and-device-independent-pixels.md)

 

 