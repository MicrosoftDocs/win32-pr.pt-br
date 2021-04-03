---
title: Respondendo a cliques do mouse
description: Respondendo a cliques do mouse
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c37903264ca638aeca1c0b28fb2ea7fa792660
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084533"
---
# <a name="responding-to-mouse-clicks"></a><span data-ttu-id="110f3-103">Respondendo a cliques do mouse</span><span class="sxs-lookup"><span data-stu-id="110f3-103">Responding to Mouse Clicks</span></span>

<span data-ttu-id="110f3-104">Se o usuário clicar em um botão do mouse enquanto o cursor estiver sobre a área do cliente de uma janela, a janela receberá uma das mensagens a seguir.</span><span class="sxs-lookup"><span data-stu-id="110f3-104">If the user clicks a mouse button while the cursor is over the client area of a window, the window receives one of the following messages.</span></span>



| <span data-ttu-id="110f3-105">Mensagem</span><span class="sxs-lookup"><span data-stu-id="110f3-105">Message</span></span>                                        | <span data-ttu-id="110f3-106">Significado</span><span class="sxs-lookup"><span data-stu-id="110f3-106">Meaning</span></span>                   |
|------------------------------------------------|---------------------------|
| [<span data-ttu-id="110f3-107">**LBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="110f3-107">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown) | <span data-ttu-id="110f3-108">Botão esquerdo para baixo</span><span class="sxs-lookup"><span data-stu-id="110f3-108">Left button down</span></span>          |
| [<span data-ttu-id="110f3-109">**LBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="110f3-109">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)     | <span data-ttu-id="110f3-110">Botão esquerdo para cima</span><span class="sxs-lookup"><span data-stu-id="110f3-110">Left button up</span></span>            |
| [<span data-ttu-id="110f3-111">**MBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="110f3-111">**WM\_MBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-mbuttondown) | <span data-ttu-id="110f3-112">Botão do meio para baixo</span><span class="sxs-lookup"><span data-stu-id="110f3-112">Middle button down</span></span>        |
| [<span data-ttu-id="110f3-113">**MBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="110f3-113">**WM\_MBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-mbuttonup)     | <span data-ttu-id="110f3-114">Botão do meio para cima</span><span class="sxs-lookup"><span data-stu-id="110f3-114">Middle button up</span></span>          |
| [<span data-ttu-id="110f3-115">**RBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="110f3-115">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown) | <span data-ttu-id="110f3-116">Botão direito para baixo</span><span class="sxs-lookup"><span data-stu-id="110f3-116">Right button down</span></span>         |
| [<span data-ttu-id="110f3-117">**RBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="110f3-117">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)     | <span data-ttu-id="110f3-118">Botão direito para cima</span><span class="sxs-lookup"><span data-stu-id="110f3-118">Right button up</span></span>           |
| [<span data-ttu-id="110f3-119">**XBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="110f3-119">**WM\_XBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-xbuttondown) | <span data-ttu-id="110f3-120">XBUTTON1 ou XBUTTON2 down</span><span class="sxs-lookup"><span data-stu-id="110f3-120">XBUTTON1 or XBUTTON2 down</span></span> |
| [<span data-ttu-id="110f3-121">**XBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="110f3-121">**WM\_XBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-xbuttonup)     | <span data-ttu-id="110f3-122">XBUTTON1 ou XBUTTON2 up</span><span class="sxs-lookup"><span data-stu-id="110f3-122">XBUTTON1 or XBUTTON2 up</span></span>   |



 

<span data-ttu-id="110f3-123">Lembre-se de que a área do cliente é a parte da janela que exclui o quadro.</span><span class="sxs-lookup"><span data-stu-id="110f3-123">Recall that the client area is the portion of the window that excludes the frame.</span></span> <span data-ttu-id="110f3-124">Para obter mais informações sobre áreas de cliente, consulte [o que é uma janela?](what-is-a-window-.md)</span><span class="sxs-lookup"><span data-stu-id="110f3-124">For more information about client areas, see [What Is a Window?](what-is-a-window-.md)</span></span>

### <a name="mouse-coordinates"></a><span data-ttu-id="110f3-125">Coordenadas do mouse</span><span class="sxs-lookup"><span data-stu-id="110f3-125">Mouse Coordinates</span></span>

<span data-ttu-id="110f3-126">Em todas essas mensagens, o parâmetro *lParam* contém as coordenadas x e y do ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="110f3-126">In all of these messages, the *lParam* parameter contains the x- and y-coordinates of the mouse pointer.</span></span> <span data-ttu-id="110f3-127">Os 16 bits mais baixos de *lParam* contêm a coordenada x e os próximos 16 bits contêm a coordenada y.</span><span class="sxs-lookup"><span data-stu-id="110f3-127">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="110f3-128">Use as macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para desempacotar as coordenadas do *lParam*.</span><span class="sxs-lookup"><span data-stu-id="110f3-128">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="110f3-129">Essas macros são definidas no arquivo de cabeçalho WindowsX. h.</span><span class="sxs-lookup"><span data-stu-id="110f3-129">These macros are defined in the header file WindowsX.h.</span></span>

<span data-ttu-id="110f3-130">No Windows de 64 bits, *lParam* é um valor de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="110f3-130">On 64-bit Windows, *lParam* is 64-bit value.</span></span> <span data-ttu-id="110f3-131">Os 32 bits superiores de *lParam* não são usados.</span><span class="sxs-lookup"><span data-stu-id="110f3-131">The upper 32 bits of *lParam* are not used.</span></span> <span data-ttu-id="110f3-132">A documentação do MSDN menciona a "palavra de ordem inferior" e "palavra de ordem superior" do *lParam*.</span><span class="sxs-lookup"><span data-stu-id="110f3-132">The MSDN documentation mentions the "low-order word" and "high-order word" of *lParam*.</span></span> <span data-ttu-id="110f3-133">No caso de 64 bits, isso significa as palavras de ordem inferior e superior dos bits inferiores de 32.</span><span class="sxs-lookup"><span data-stu-id="110f3-133">In the 64-bit case, this means the low- and high-order words of the lower 32 bits.</span></span> <span data-ttu-id="110f3-134">As macros extraem os valores certos, portanto, se você usá-las, será seguro.</span><span class="sxs-lookup"><span data-stu-id="110f3-134">The macros extract the right values, so if you use them, you will be safe.</span></span>

<span data-ttu-id="110f3-135">As coordenadas do mouse são dadas em pixels, não nos DIPs (pixels independentes do dispositivo) e são medidos em relação à área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="110f3-135">Mouse coordinates are given in pixels, not device-independent pixels (DIPs), and are measured relative to the client area of the window.</span></span> <span data-ttu-id="110f3-136">As coordenadas são valores assinados.</span><span class="sxs-lookup"><span data-stu-id="110f3-136">Coordinates are signed values.</span></span> <span data-ttu-id="110f3-137">As posições acima e à esquerda da área do cliente têm coordenadas negativas, o que é importante se você rastrear a posição do mouse fora da janela.</span><span class="sxs-lookup"><span data-stu-id="110f3-137">Positions above and to the left of the client area have negative coordinates, which is important if you track the mouse position outside the window.</span></span> <span data-ttu-id="110f3-138">Veremos como fazer isso em um tópico posterior, [capturando o movimento do mouse fora da janela](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="110f3-138">We will see how to do that in a later topic, [Capturing Mouse Movement Outside the Window](mouse-movement.md).</span></span>

### <a name="additional-flags"></a><span data-ttu-id="110f3-139">Sinalizadores adicionais</span><span class="sxs-lookup"><span data-stu-id="110f3-139">Additional Flags</span></span>

<span data-ttu-id="110f3-140">O parâmetro *wParam* contém um **ou** mais bits de sinalizadores, indicando o estado dos outros botões do mouse mais as teclas Shift e Ctrl.</span><span class="sxs-lookup"><span data-stu-id="110f3-140">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span>



| <span data-ttu-id="110f3-141">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="110f3-141">Flag</span></span>             | <span data-ttu-id="110f3-142">Significado</span><span class="sxs-lookup"><span data-stu-id="110f3-142">Meaning</span></span>                          |
|------------------|----------------------------------|
| <span data-ttu-id="110f3-143">**\_controle MK**</span><span class="sxs-lookup"><span data-stu-id="110f3-143">**MK\_CONTROL**</span></span>  | <span data-ttu-id="110f3-144">A tecla CTRL está inoperante.</span><span class="sxs-lookup"><span data-stu-id="110f3-144">The CTRL key is down.</span></span>            |
| <span data-ttu-id="110f3-145">**\_LBUTTON MK**</span><span class="sxs-lookup"><span data-stu-id="110f3-145">**MK\_LBUTTON**</span></span>  | <span data-ttu-id="110f3-146">O botão esquerdo do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="110f3-146">The left mouse button is down.</span></span>   |
| <span data-ttu-id="110f3-147">**\_MBUTTON MK**</span><span class="sxs-lookup"><span data-stu-id="110f3-147">**MK\_MBUTTON**</span></span>  | <span data-ttu-id="110f3-148">O botão do meio do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="110f3-148">The middle mouse button is down.</span></span> |
| <span data-ttu-id="110f3-149">**\_RBUTTON MK**</span><span class="sxs-lookup"><span data-stu-id="110f3-149">**MK\_RBUTTON**</span></span>  | <span data-ttu-id="110f3-150">O botão direito do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="110f3-150">The right mouse button is down.</span></span>  |
| <span data-ttu-id="110f3-151">**\_turno MK**</span><span class="sxs-lookup"><span data-stu-id="110f3-151">**MK\_SHIFT**</span></span>    | <span data-ttu-id="110f3-152">A tecla SHIFT está inoperante.</span><span class="sxs-lookup"><span data-stu-id="110f3-152">The SHIFT key is down.</span></span>           |
| <span data-ttu-id="110f3-153">**\_XButton1 MK**</span><span class="sxs-lookup"><span data-stu-id="110f3-153">**MK\_XBUTTON1**</span></span> | <span data-ttu-id="110f3-154">O botão XBUTTON1 está inoperante.</span><span class="sxs-lookup"><span data-stu-id="110f3-154">The XBUTTON1 button is down.</span></span>     |
| <span data-ttu-id="110f3-155">**\_XButton2 MK**</span><span class="sxs-lookup"><span data-stu-id="110f3-155">**MK\_XBUTTON2**</span></span> | <span data-ttu-id="110f3-156">O botão XBUTTON2 está inoperante.</span><span class="sxs-lookup"><span data-stu-id="110f3-156">The XBUTTON2 button is down.</span></span>     |



 

<span data-ttu-id="110f3-157">A ausência de um sinalizador significa que o botão ou a chave correspondente não foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="110f3-157">The absence of a flag means the corresponding button or key was not pressed.</span></span> <span data-ttu-id="110f3-158">Por exemplo, para testar se a tecla CTRL está inoperante:</span><span class="sxs-lookup"><span data-stu-id="110f3-158">For example, to test whether the CTRL key is down:</span></span>


```C++
if (wParam & MK_CONTROL) { ...
```



<span data-ttu-id="110f3-159">Se você precisar localizar o estado de outras chaves além de CTRL e SHIFT, use a função [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) , que é descrita em [entrada de teclado](keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="110f3-159">If you need to find the state of other keys besides CTRL and SHIFT, use the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function, which is described in [Keyboard Input](keyboard-input.md).</span></span>

<span data-ttu-id="110f3-160">As mensagens de janela do [**WM \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) e do [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) se aplicam a XBUTTON1 e XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="110f3-160">The [**WM\_XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) and [**WM\_XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) window messages apply to both XBUTTON1 and XBUTTON2.</span></span> <span data-ttu-id="110f3-161">O parâmetro *wParam* indica em qual botão foi clicado.</span><span class="sxs-lookup"><span data-stu-id="110f3-161">The *wParam* parameter indicates which button was clicked.</span></span>


```C++
UINT button = GET_XBUTTON_WPARAM(wParam);  
if (button == XBUTTON1)
{
    // XBUTTON1 was clicked.
}
else if (button == XBUTTON2)
{
    // XBUTTON2 was clicked.
}
```



## <a name="double-clicks"></a><span data-ttu-id="110f3-162">Cliques duplos</span><span class="sxs-lookup"><span data-stu-id="110f3-162">Double Clicks</span></span>

<span data-ttu-id="110f3-163">Uma janela não recebe notificações de clique duplo por padrão.</span><span class="sxs-lookup"><span data-stu-id="110f3-163">A window does not receive double-click notifications by default.</span></span> <span data-ttu-id="110f3-164">Para receber cliques duplos, defina o sinalizador **cs \_ DBLCLKS** na estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ao registrar a classe Window.</span><span class="sxs-lookup"><span data-stu-id="110f3-164">To receive double clicks, set the **CS\_DBLCLKS** flag in the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure when you register the window class.</span></span>


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



<span data-ttu-id="110f3-165">Se você definir o sinalizador **cs \_ DBLCLKS** conforme mostrado, a janela receberá notificações de clique duplo.</span><span class="sxs-lookup"><span data-stu-id="110f3-165">If you set the **CS\_DBLCLKS** flag as shown, the window will receive double-click notifications.</span></span> <span data-ttu-id="110f3-166">Um clique duplo é indicado por uma mensagem de janela com "DBLCLK" no nome.</span><span class="sxs-lookup"><span data-stu-id="110f3-166">A double click is indicated by a window message with "DBLCLK" in the name.</span></span> <span data-ttu-id="110f3-167">Por exemplo, um clique duplo no botão esquerdo do mouse produz a seguinte sequência de mensagens:</span><span class="sxs-lookup"><span data-stu-id="110f3-167">For example, a double click on the left mouse button produces the following sequence of messages:</span></span>

<dl>

[<span data-ttu-id="110f3-168">**LBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="110f3-168">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)  
[<span data-ttu-id="110f3-169">**LBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="110f3-169">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
[<span data-ttu-id="110f3-170">**LBUTTONDBLCLK do WM \_**</span><span class="sxs-lookup"><span data-stu-id="110f3-170">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)  
[<span data-ttu-id="110f3-171">**LBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="110f3-171">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

<span data-ttu-id="110f3-172">Na verdade, a segunda mensagem do [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) que normalmente seria gerada se torna uma mensagem do [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) .</span><span class="sxs-lookup"><span data-stu-id="110f3-172">In effect, the second [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message that would normally be generated becomes a [**WM\_LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) message.</span></span> <span data-ttu-id="110f3-173">As mensagens equivalentes são definidas para os botões direito, meio e XBUTTON.</span><span class="sxs-lookup"><span data-stu-id="110f3-173">Equivalent messages are defined for right, middle, and XBUTTON buttons.</span></span>

<span data-ttu-id="110f3-174">Até que você receba a mensagem de clique duplo, não há como dizer que o primeiro clique do mouse é o início de um clique duplo.</span><span class="sxs-lookup"><span data-stu-id="110f3-174">Until you get the double-click message, there is no way to tell that the first mouse click is the start of a double click.</span></span> <span data-ttu-id="110f3-175">Portanto, uma ação de clique duplo deve continuar em uma ação que começa com o primeiro clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="110f3-175">Therefore, a double-click action should continue an action that begins with the first mouse click.</span></span> <span data-ttu-id="110f3-176">Por exemplo, no Shell do Windows, um único clique seleciona uma pasta, enquanto um clique duplo abre a pasta.</span><span class="sxs-lookup"><span data-stu-id="110f3-176">For example, in the Windows Shell, a single click selects a folder, while a double click opens the folder.</span></span>

## <a name="non-client-mouse-messages"></a><span data-ttu-id="110f3-177">Mensagens de mouse não cliente</span><span class="sxs-lookup"><span data-stu-id="110f3-177">Non-client Mouse Messages</span></span>

<span data-ttu-id="110f3-178">Um conjunto separado de mensagens é definido para eventos de mouse que ocorrem na área não cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="110f3-178">A separate set of messages are defined for mouse events that occur within the non-client area of the window.</span></span> <span data-ttu-id="110f3-179">Essas mensagens têm as letras "NC" no nome.</span><span class="sxs-lookup"><span data-stu-id="110f3-179">These messages have the letters "NC" in the name.</span></span> <span data-ttu-id="110f3-180">Por exemplo, o [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) é o equivalente não-cliente do [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span><span class="sxs-lookup"><span data-stu-id="110f3-180">For example, [**WM\_NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) is the non-client equivalent of [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span></span> <span data-ttu-id="110f3-181">Um aplicativo típico não interceptará essas mensagens, pois a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) lida com essas mensagens corretamente.</span><span class="sxs-lookup"><span data-stu-id="110f3-181">A typical application will not intercept these messages, because the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function handles these messages correctly.</span></span> <span data-ttu-id="110f3-182">No entanto, eles podem ser úteis para determinadas funções avançadas.</span><span class="sxs-lookup"><span data-stu-id="110f3-182">However, they can be useful for certain advanced functions.</span></span> <span data-ttu-id="110f3-183">Por exemplo, você pode usar essas mensagens para implementar o comportamento personalizado na barra de título.</span><span class="sxs-lookup"><span data-stu-id="110f3-183">For example, you could use these messages to implement custom behavior in the title bar.</span></span> <span data-ttu-id="110f3-184">Se você lidar com essas mensagens, geralmente deverá passá-las para **DefWindowProc** posteriormente.</span><span class="sxs-lookup"><span data-stu-id="110f3-184">If you do handle these messages, you should generally pass them to **DefWindowProc** afterward.</span></span> <span data-ttu-id="110f3-185">Caso contrário, seu aplicativo irá interromper a funcionalidade padrão, como arrastar ou minimizar a janela.</span><span class="sxs-lookup"><span data-stu-id="110f3-185">Otherwise, your application will break standard functionality such as dragging or minimizing the window.</span></span>

## <a name="next"></a><span data-ttu-id="110f3-186">Avançar</span><span class="sxs-lookup"><span data-stu-id="110f3-186">Next</span></span>

[<span data-ttu-id="110f3-187">Movimento do mouse</span><span class="sxs-lookup"><span data-stu-id="110f3-187">Mouse Movement</span></span>](mouse-movement.md)

 

 