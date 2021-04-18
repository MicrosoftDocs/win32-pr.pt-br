---
title: Movimento do mouse
description: Movimento do mouse
ms.assetid: 54366E9B-470A-4155-8A5F-425BAC8AC1A5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14176310882651cdeb2939d0db55368ff133ea11
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "105810479"
---
# <a name="mouse-movement"></a><span data-ttu-id="e3aec-103">Movimento do mouse</span><span class="sxs-lookup"><span data-stu-id="e3aec-103">Mouse Movement</span></span>

<span data-ttu-id="e3aec-104">Quando o mouse se move, o Windows posta uma mensagem [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="e3aec-104">When the mouse moves, Windows posts a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="e3aec-105">Por padrão, o **WM \_ MOUSEMOVE** vai para a janela que contém o cursor.</span><span class="sxs-lookup"><span data-stu-id="e3aec-105">By default, **WM\_MOUSEMOVE** goes to the window that contains the cursor.</span></span> <span data-ttu-id="e3aec-106">Você pode substituir esse comportamento *capturando* o mouse, que é descrito na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="e3aec-106">You can override this behavior by *capturing* the mouse, which is described in the next section.</span></span>

<span data-ttu-id="e3aec-107">A [**mensagem \_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) contém os mesmos parâmetros que as mensagens para cliques do mouse.</span><span class="sxs-lookup"><span data-stu-id="e3aec-107">The [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message contains the same parameters as the messages for mouse clicks.</span></span> <span data-ttu-id="e3aec-108">Os 16 bits mais baixos de *lParam* contêm a coordenada x e os próximos 16 bits contêm a coordenada y.</span><span class="sxs-lookup"><span data-stu-id="e3aec-108">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="e3aec-109">Use as macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para desempacotar as coordenadas do *lParam*.</span><span class="sxs-lookup"><span data-stu-id="e3aec-109">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span> <span data-ttu-id="e3aec-110">O parâmetro *wParam* contém um **ou** mais bits de sinalizadores, indicando o estado dos outros botões do mouse mais as teclas Shift e Ctrl.</span><span class="sxs-lookup"><span data-stu-id="e3aec-110">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span> <span data-ttu-id="e3aec-111">O código a seguir obtém as coordenadas do mouse do *lParam*.</span><span class="sxs-lookup"><span data-stu-id="e3aec-111">The following code gets the mouse coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="e3aec-112">Lembre-se de que essas coordenadas estão em pixels, não em DIPs (pixels independentes de dispositivo).</span><span class="sxs-lookup"><span data-stu-id="e3aec-112">Remember that these coordinates are in pixels, not device-independent pixels (DIPs).</span></span> <span data-ttu-id="e3aec-113">Posteriormente neste tópico, veremos o código que converte entre as duas unidades.</span><span class="sxs-lookup"><span data-stu-id="e3aec-113">Later in this topic, we will look at code that converts between the two units.</span></span>

<span data-ttu-id="e3aec-114">Uma janela também pode receber uma mensagem do [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) se a posição do cursor mudar em relação à janela.</span><span class="sxs-lookup"><span data-stu-id="e3aec-114">A window can also receive a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message if the position of the cursor changes relative to the window.</span></span> <span data-ttu-id="e3aec-115">Por exemplo, se o cursor estiver posicionado sobre uma janela e o usuário ocultar a janela, a janela receberá mensagens do **WM \_ MOUSEMOVE** , mesmo que o mouse não tenha se movido.</span><span class="sxs-lookup"><span data-stu-id="e3aec-115">For example, if the cursor is positioned over a window, and the user hides the window, the window receives **WM\_MOUSEMOVE** messages even if the mouse did not move.</span></span> <span data-ttu-id="e3aec-116">Uma consequência desse comportamento é que as coordenadas do mouse podem não mudar entre as mensagens **\_ MOUSEMOVE do WM** .</span><span class="sxs-lookup"><span data-stu-id="e3aec-116">One consequence of this behavior is that the mouse coordinates might not change between **WM\_MOUSEMOVE** messages.</span></span>

## <a name="capturing-mouse-movement-outside-the-window"></a><span data-ttu-id="e3aec-117">Captura do movimento do mouse fora da janela</span><span class="sxs-lookup"><span data-stu-id="e3aec-117">Capturing Mouse Movement Outside the Window</span></span>

<span data-ttu-id="e3aec-118">Por padrão, uma janela para de receber mensagens do [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) se o mouse passar para a borda da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="e3aec-118">By default, a window stops receiving [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages if the mouse moves past the edge of the client area.</span></span> <span data-ttu-id="e3aec-119">Mas, para algumas operações, talvez seja necessário controlar a posição do mouse além desse ponto.</span><span class="sxs-lookup"><span data-stu-id="e3aec-119">But for some operations, you might need to track the mouse position beyond this point.</span></span> <span data-ttu-id="e3aec-120">Por exemplo, um programa de desenho pode permitir que o usuário arraste o retângulo de seleção para além da borda da janela, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="e3aec-120">For example, a drawing program might enable the user to drag the selection rectangle beyond the edge of the window, as shown in the following diagram.</span></span>

![uma ilustração de captura do mouse.](images/input01.png)

<span data-ttu-id="e3aec-122">Para receber mensagens de movimentação do mouse após a borda da janela, chame a função [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) .</span><span class="sxs-lookup"><span data-stu-id="e3aec-122">To receive mouse-move messages past the edge of the window, call the [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) function.</span></span> <span data-ttu-id="e3aec-123">Depois que essa função for chamada, a janela continuará a receber mensagens do [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) enquanto o usuário mantiver pelo menos um botão do mouse pressionado, mesmo se o mouse se mover para fora da janela.</span><span class="sxs-lookup"><span data-stu-id="e3aec-123">After this function is called, the window will continue to receive [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages for as long as the user holds at least one mouse button down, even if the mouse moves outside the window.</span></span> <span data-ttu-id="e3aec-124">A janela de captura deve ser a janela em primeiro plano e apenas uma janela pode ser a janela de captura por vez.</span><span class="sxs-lookup"><span data-stu-id="e3aec-124">The capture window must be the foreground window, and only one window can be the capture window at a time.</span></span> <span data-ttu-id="e3aec-125">Para liberar a captura do mouse, chame a função [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) .</span><span class="sxs-lookup"><span data-stu-id="e3aec-125">To release mouse capture, call the [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) function.</span></span>

<span data-ttu-id="e3aec-126">Normalmente, você usaria [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) e [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="e3aec-126">You would typically use [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) and [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) in the following way.</span></span>

1.  <span data-ttu-id="e3aec-127">Quando o usuário pressiona o botão esquerdo do mouse, chame [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) para começar a capturar o mouse.</span><span class="sxs-lookup"><span data-stu-id="e3aec-127">When the user presses the left mouse button, call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to start capturing the mouse.</span></span>
2.  <span data-ttu-id="e3aec-128">Responder às mensagens do mouse-mover.</span><span class="sxs-lookup"><span data-stu-id="e3aec-128">Respond to mouse-move messages.</span></span>
3.  <span data-ttu-id="e3aec-129">Quando o usuário libera o botão esquerdo do mouse, chame [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).</span><span class="sxs-lookup"><span data-stu-id="e3aec-129">When the user releases the left mouse button, call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).</span></span>

## <a name="example-drawing-circles"></a><span data-ttu-id="e3aec-130">Exemplo: círculos de desenho</span><span class="sxs-lookup"><span data-stu-id="e3aec-130">Example: Drawing Circles</span></span>

<span data-ttu-id="e3aec-131">Vamos estender o programa de círculo do [módulo 3](module-3---windows-graphics.md) habilitando o usuário a desenhar um círculo com o mouse.</span><span class="sxs-lookup"><span data-stu-id="e3aec-131">Let's extend the Circle program from [Module 3](module-3---windows-graphics.md) by enabling the user to draw a circle with the mouse.</span></span> <span data-ttu-id="e3aec-132">Comece com o programa de [exemplo de círculo Direct2D](direct2d-circle-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="e3aec-132">Start with the [Direct2D Circle Sample](direct2d-circle-sample.md) program.</span></span> <span data-ttu-id="e3aec-133">Modificaremos o código neste exemplo para adicionar desenho simples.</span><span class="sxs-lookup"><span data-stu-id="e3aec-133">We will modify the code in this sample to add simple drawing.</span></span> <span data-ttu-id="e3aec-134">Primeiro, adicione uma nova variável de membro à `MainWindow` classe.</span><span class="sxs-lookup"><span data-stu-id="e3aec-134">First, add a new member variable to the `MainWindow` class.</span></span>


```C++
    D2D1_POINT_2F           ptMouse;
```



<span data-ttu-id="e3aec-135">Essa variável armazena a posição do mouse para baixo enquanto o usuário está arrastando o mouse.</span><span class="sxs-lookup"><span data-stu-id="e3aec-135">This variable stores the mouse-down position while the user is dragging the mouse.</span></span> <span data-ttu-id="e3aec-136">No `MainWindow` Construtor, inicialize as variáveis *Ellipse* e *ptMouse* .</span><span class="sxs-lookup"><span data-stu-id="e3aec-136">In the `MainWindow` constructor, initialize the *ellipse* and *ptMouse* variables.</span></span>


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



<span data-ttu-id="e3aec-137">Remova o corpo do `MainWindow::CalculateLayout` método; ele não é necessário para este exemplo.</span><span class="sxs-lookup"><span data-stu-id="e3aec-137">Remove the body of the `MainWindow::CalculateLayout` method; it's not required for this example.</span></span>


```C++
    void    CalculateLayout() { }
```



<span data-ttu-id="e3aec-138">Em seguida, declare os manipuladores de mensagens para o botão esquerdo inferior, o botão esquerdo para cima e as mensagens de movimentação do mouse.</span><span class="sxs-lookup"><span data-stu-id="e3aec-138">Next, declare message handlers for the left-button down, left-button up, and mouse-move messages.</span></span>


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



<span data-ttu-id="e3aec-139">As coordenadas do mouse são dadas em pixels físicos, mas o Direct2D espera pixels independentes de dispositivo (DIPs).</span><span class="sxs-lookup"><span data-stu-id="e3aec-139">Mouse coordinates are given in physical pixels, but Direct2D expects device-independent pixels (DIPs).</span></span> <span data-ttu-id="e3aec-140">Para tratar as configurações de alto DPI corretamente, você deve converter as coordenadas de pixel em DIPs.</span><span class="sxs-lookup"><span data-stu-id="e3aec-140">To handle high-DPI settings correctly, you must translate the pixel coordinates into DIPs.</span></span> <span data-ttu-id="e3aec-141">Para obter mais discussões sobre DPI, consulte [dpi e Device-Independent pixels](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="e3aec-141">For more discussion about DPI, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span> <span data-ttu-id="e3aec-142">O código a seguir mostra uma classe auxiliar que converte pixels em DIPs.</span><span class="sxs-lookup"><span data-stu-id="e3aec-142">The following code shows a helper class that converts pixels into DIPs.</span></span>


```C++
class DPIScale
{
    static float scaleX;
    static float scaleY;

public:
    static void Initialize(ID2D1Factory *pFactory)
    {
        FLOAT dpiX, dpiY;
        pFactory->GetDesktopDpi(&dpiX, &dpiY);
        scaleX = dpiX/96.0f;
        scaleY = dpiY/96.0f;
    }

    template <typename T>
    static D2D1_POINT_2F PixelsToDips(T x, T y)
    {
        return D2D1::Point2F(static_cast<float>(x) / scaleX, static_cast<float>(y) / scaleY);
    }
};

float DPIScale::scaleX = 1.0f;
float DPIScale::scaleY = 1.0f;
```



<span data-ttu-id="e3aec-143">Chame `DPIScale::Initialize` em seu manipulador de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) , depois de criar o objeto de fábrica Direct2D.</span><span class="sxs-lookup"><span data-stu-id="e3aec-143">Call `DPIScale::Initialize` in your [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) handler, after you create the Direct2D factory object.</span></span>


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        DPIScale::Initialize(pFactory);
        return 0;
```



<span data-ttu-id="e3aec-144">Para obter as coordenadas do mouse em DIPs das mensagens do mouse, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e3aec-144">To get the mouse coordinates in DIPs from the mouse messages, do the following:</span></span>

1.  <span data-ttu-id="e3aec-145">Use as macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para obter as coordenadas de pixel.</span><span class="sxs-lookup"><span data-stu-id="e3aec-145">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to get the pixel coordinates.</span></span> <span data-ttu-id="e3aec-146">Essas macros são definidas em WindowsX. h, portanto, lembre-se de incluir esse cabeçalho em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="e3aec-146">These macros are defined in WindowsX.h, so remember to include that header in your project.</span></span>
2.  <span data-ttu-id="e3aec-147">Chame `DPIScale::PixelsToDipsX` e `DPIScale::PixelsToDipsY` para converter pixels em DIPs.</span><span class="sxs-lookup"><span data-stu-id="e3aec-147">Call `DPIScale::PixelsToDipsX` and `DPIScale::PixelsToDipsY` to convert pixels to DIPs.</span></span>

<span data-ttu-id="e3aec-148">Agora, adicione os manipuladores de mensagens ao seu procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="e3aec-148">Now add the message handlers to your window procedure.</span></span>


```C++
    case WM_LBUTTONDOWN: 
        OnLButtonDown(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;

    case WM_LBUTTONUP: 
        OnLButtonUp();
        return 0;

    case WM_MOUSEMOVE: 
        OnMouseMove(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;
```



<span data-ttu-id="e3aec-149">Por fim, implemente os próprios manipuladores de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e3aec-149">Finally, implement the message handlers themselves.</span></span>

### <a name="left-button-down"></a><span data-ttu-id="e3aec-150">Botão esquerdo para baixo</span><span class="sxs-lookup"><span data-stu-id="e3aec-150">Left Button Down</span></span>

<span data-ttu-id="e3aec-151">Para a mensagem de botão esquerdo para baixo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e3aec-151">For the left-button down message, do the following:</span></span>

1.  <span data-ttu-id="e3aec-152">Chame [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) para começar a capturar o mouse.</span><span class="sxs-lookup"><span data-stu-id="e3aec-152">Call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to begin capturing the mouse.</span></span>
2.  <span data-ttu-id="e3aec-153">Armazene a posição do clique do mouse na variável *ptMouse* .</span><span class="sxs-lookup"><span data-stu-id="e3aec-153">Store the position of the mouse click in the *ptMouse* variable.</span></span> <span data-ttu-id="e3aec-154">Essa posição define o canto superior esquerdo da caixa delimitadora para a elipse.</span><span class="sxs-lookup"><span data-stu-id="e3aec-154">This position defines the upper left corner of the bounding box for the ellipse.</span></span>
3.  <span data-ttu-id="e3aec-155">Redefina a estrutura da elipse.</span><span class="sxs-lookup"><span data-stu-id="e3aec-155">Reset the ellipse structure.</span></span>
4.  <span data-ttu-id="e3aec-156">Chame [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="e3aec-156">Call [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="e3aec-157">Essa função força a janela a ser redesenhada.</span><span class="sxs-lookup"><span data-stu-id="e3aec-157">This function forces the window to be repainted.</span></span>


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a><span data-ttu-id="e3aec-158">Movimentação do mouse</span><span class="sxs-lookup"><span data-stu-id="e3aec-158">Mouse Move</span></span>

<span data-ttu-id="e3aec-159">Para a mensagem mouse-move, verifique se o botão esquerdo do mouse está inoperante.</span><span class="sxs-lookup"><span data-stu-id="e3aec-159">For the mouse-move message, check whether the left mouse button is down.</span></span> <span data-ttu-id="e3aec-160">Se for, recalcule a elipse e repinte a janela.</span><span class="sxs-lookup"><span data-stu-id="e3aec-160">If it is, recalculate the ellipse and repaint the window.</span></span> <span data-ttu-id="e3aec-161">No Direct2D, uma elipse é definida pelo ponto central e raios x e y.</span><span class="sxs-lookup"><span data-stu-id="e3aec-161">In Direct2D, an ellipse is defined by the center point and x- and y-radii.</span></span> <span data-ttu-id="e3aec-162">Desejamos desenhar uma elipse que se ajuste à caixa delimitadora definida pelo ponto do mouse (*ptMouse*) e da posição atual do cursor (*x*, *y*), de modo que um pouco de aritmética seja necessário para localizar a largura, a altura e a posição da elipse.</span><span class="sxs-lookup"><span data-stu-id="e3aec-162">We want to draw an ellipse that fits the bounding box defined by the mouse-down point (*ptMouse*) and the current cursor position (*x*, *y*), so a bit of arithmetic is needed to find the width, height, and position of the ellipse.</span></span>

<span data-ttu-id="e3aec-163">O código a seguir recalcula a elipse e, em seguida, chama [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) para redesenhar a janela.</span><span class="sxs-lookup"><span data-stu-id="e3aec-163">The following code recalculates the ellipse and then calls [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) to repaint the window.</span></span>

![Diagrama que mostra uma elipse com raio x e y.](images/input02.png)


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    if (flags & MK_LBUTTON) 
    { 
        const D2D1_POINT_2F dips = DPIScale::PixelsToDips(pixelX, pixelY);

        const float width = (dips.x - ptMouse.x) / 2;
        const float height = (dips.y - ptMouse.y) / 2;
        const float x1 = ptMouse.x + width;
        const float y1 = ptMouse.y + height;

        ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);

        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



### <a name="left-button-up"></a><span data-ttu-id="e3aec-165">Botão esquerdo para cima</span><span class="sxs-lookup"><span data-stu-id="e3aec-165">Left Button Up</span></span>

<span data-ttu-id="e3aec-166">Para a mensagem de botão esquerdo, basta chamar [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) para liberar a captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="e3aec-166">For the left-button-up message, simply call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) to release the mouse capture.</span></span>


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a><span data-ttu-id="e3aec-167">Avançar</span><span class="sxs-lookup"><span data-stu-id="e3aec-167">Next</span></span>

[<span data-ttu-id="e3aec-168">Outras operações do mouse</span><span class="sxs-lookup"><span data-stu-id="e3aec-168">Other Mouse Operations</span></span>](other-mouse-operations.md)

 

 