---
title: Diversas operações de mouse
description: As seções anteriores discutiram os cliques do mouse e o movimento do mouse. Aqui estão algumas outras operações que podem ser executadas com o mouse.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfba63dce8116d79a557cbbbf8895f17d2a8f1b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294037"
---
# <a name="miscellaneous-mouse-operations"></a><span data-ttu-id="64058-104">Diversas operações de mouse</span><span class="sxs-lookup"><span data-stu-id="64058-104">Miscellaneous Mouse Operations</span></span>

<span data-ttu-id="64058-105">As seções anteriores discutiram os cliques do mouse e o movimento do mouse.</span><span class="sxs-lookup"><span data-stu-id="64058-105">The previous sections have discussed mouse clicks and mouse movement.</span></span> <span data-ttu-id="64058-106">Aqui estão algumas outras operações que podem ser executadas com o mouse.</span><span class="sxs-lookup"><span data-stu-id="64058-106">Here are some other operations that can be performed with the mouse.</span></span>

## <a name="dragging-ui-elements"></a><span data-ttu-id="64058-107">Arrastando elementos da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="64058-107">Dragging UI Elements</span></span>

<span data-ttu-id="64058-108">Se sua interface do usuário der suporte ao arrastar de elementos da interface do usuário, há uma outra função que você deve chamar no manipulador de mensagens do mouse-Down: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect).</span><span class="sxs-lookup"><span data-stu-id="64058-108">If your UI supports dragging of UI elements, there is one other function that you should call in your mouse-down message handler: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect).</span></span> <span data-ttu-id="64058-109">A função **DragDetect** retornará **true** se o usuário iniciar um gesto do mouse que deve ser interpretado como arrastando.</span><span class="sxs-lookup"><span data-stu-id="64058-109">The **DragDetect** function returns **TRUE** if the user initiates a mouse gesture that should be interpreted as dragging.</span></span> <span data-ttu-id="64058-110">O código a seguir mostra como usar essa função.</span><span class="sxs-lookup"><span data-stu-id="64058-110">The following code shows how to use this function.</span></span>


```C++
    case WM_LBUTTONDOWN: 
        {
            POINT pt = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam) };
            if (DragDetect(m_hwnd, pt))
            {
                // Start dragging.
            }
        }
        return 0;
```



<span data-ttu-id="64058-111">Esta é a ideia: quando um programa dá suporte a arrastar e soltar, você não quer que cada clique do mouse seja interpretado como um arrastar.</span><span class="sxs-lookup"><span data-stu-id="64058-111">Here's the idea: When a program supports drag and drop, you don't want every mouse click to be interpreted as a drag.</span></span> <span data-ttu-id="64058-112">Caso contrário, o usuário pode acidentalmente arrastar algo quando ele simplesmente pretendia clicar nele (por exemplo, para selecioná-lo).</span><span class="sxs-lookup"><span data-stu-id="64058-112">Otherwise, the user might accidentally drag something when he or she simply meant to click on it (for example, to select it).</span></span> <span data-ttu-id="64058-113">Mas se um mouse for particularmente confidencial, pode ser difícil manter o mouse perfeitamente ao clicar.</span><span class="sxs-lookup"><span data-stu-id="64058-113">But if a mouse is particularly sensitive, it can be hard to keep the mouse perfectly still while clicking.</span></span> <span data-ttu-id="64058-114">Portanto, o Windows define um limite de arraste de alguns pixels.</span><span class="sxs-lookup"><span data-stu-id="64058-114">Therefore, Windows defines a drag threshold of a few pixels.</span></span> <span data-ttu-id="64058-115">Quando o usuário pressiona o botão do mouse, ele não é considerado um arrastar, a menos que o mouse cruze esse limite.</span><span class="sxs-lookup"><span data-stu-id="64058-115">When the user presses the mouse button, it is not considered a drag unless the mouse crosses this threshold.</span></span> <span data-ttu-id="64058-116">A função [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) testa se esse limite é atingido.</span><span class="sxs-lookup"><span data-stu-id="64058-116">The [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function tests whether this threshold is reached.</span></span> <span data-ttu-id="64058-117">Se a função retornar **true**, você poderá interpretar o clique do mouse como um arrastar.</span><span class="sxs-lookup"><span data-stu-id="64058-117">If the function returns **TRUE**, you can interpret the mouse click as a drag.</span></span> <span data-ttu-id="64058-118">Caso contrário, não faça isso.</span><span class="sxs-lookup"><span data-stu-id="64058-118">Otherwise, do not.</span></span>

> [!Note]  
> <span data-ttu-id="64058-119">Se [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) retornar **false**, o Windows suprimirá a mensagem do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) quando o usuário liberar o botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="64058-119">If [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) returns **FALSE**, Windows suppresses the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message when the user releases the mouse button.</span></span> <span data-ttu-id="64058-120">Portanto, não chame **DragDetect** , a menos que seu programa esteja atualmente em um modo que ofereça suporte a arrastar.</span><span class="sxs-lookup"><span data-stu-id="64058-120">Therefore, do not call **DragDetect** unless your program is currently in a mode that supports dragging.</span></span> <span data-ttu-id="64058-121">(Por exemplo, se um elemento de interface do usuário arrastável já estiver selecionado.) No final deste módulo, veremos um exemplo de código mais longo que usa a função **DragDetect** .</span><span class="sxs-lookup"><span data-stu-id="64058-121">(For example, if a draggable UI element is already selected.) At the end of this module, we will see a longer code example that uses the **DragDetect** function.</span></span>

 

## <a name="confining-the-cursor"></a><span data-ttu-id="64058-122">Confinando o cursor</span><span class="sxs-lookup"><span data-stu-id="64058-122">Confining the Cursor</span></span>

<span data-ttu-id="64058-123">Às vezes, talvez você queira restringir o cursor para a área do cliente ou uma parte da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="64058-123">Sometimes you might want to restrict the cursor to the client area or a portion of the client area.</span></span> <span data-ttu-id="64058-124">A função [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) restringe a movimentação do cursor para um retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="64058-124">The [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) function restricts the movement of the cursor to a specified rectangle.</span></span> <span data-ttu-id="64058-125">Esse retângulo é fornecido em coordenadas de tela, em vez de coordenadas de cliente, portanto, o ponto (0, 0) significa o canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="64058-125">This rectangle is given in screen coordinates, rather than client coordinates, so the point (0, 0) means the upper left corner of the screen.</span></span> <span data-ttu-id="64058-126">Para converter as coordenadas do cliente em coordenadas da tela, chame a função [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).</span><span class="sxs-lookup"><span data-stu-id="64058-126">To translate client coordinates into screen coordinates, call the function [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).</span></span>

<span data-ttu-id="64058-127">O código a seguir confina o cursor para a área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="64058-127">The following code confines the cursor to the client area of the window.</span></span>


```C++
    // Get the window client area.
    RECT rc;
    GetClientRect(m_hwnd, &rc);

    // Convert the client area to screen coordinates.
    POINT pt = { rc.left, rc.top };
    POINT pt2 = { rc.right, rc.bottom };
    ClientToScreen(m_hwnd, &pt);
    ClientToScreen(m_hwnd, &pt2);
    SetRect(&rc, pt.x, pt.y, pt2.x, pt2.y);

    // Confine the cursor.
    ClipCursor(&rc);
```



<span data-ttu-id="64058-128">[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) usa uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) , mas [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) usa uma estrutura de [**pontos**](/previous-versions//dd162805(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="64058-128">[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) takes a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure, but [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) takes a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="64058-129">Um retângulo é definido por seus pontos superior esquerdo e inferior direito.</span><span class="sxs-lookup"><span data-stu-id="64058-129">A rectangle is defined by its top-left and bottom-right points.</span></span> <span data-ttu-id="64058-130">Você pode confinar o cursor para qualquer área retangular, incluindo áreas fora da janela, mas o confinamento do cursor para a área do cliente é uma maneira típica de usar a função.</span><span class="sxs-lookup"><span data-stu-id="64058-130">You can confine the cursor to any rectangular area, including areas outside the window, but confining the cursor to the client area is a typical way to use the function.</span></span> <span data-ttu-id="64058-131">O confinamento do cursor para uma região totalmente fora de sua janela seria incomum e os usuários provavelmente a perceberam como um bug.</span><span class="sxs-lookup"><span data-stu-id="64058-131">Confining the cursor to a region entirely outside your window would be unusual, and users would probably perceive it as a bug.</span></span>

<span data-ttu-id="64058-132">Para remover a restrição, chame [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) com o valor **NULL**.</span><span class="sxs-lookup"><span data-stu-id="64058-132">To remove the restriction, call [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) with the value **NULL**.</span></span>


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a><span data-ttu-id="64058-133">Eventos de rastreamento do mouse: focalizar e sair</span><span class="sxs-lookup"><span data-stu-id="64058-133">Mouse Tracking Events: Hover and Leave</span></span>

<span data-ttu-id="64058-134">Duas outras mensagens do mouse são desabilitadas por padrão, mas podem ser úteis para alguns aplicativos:</span><span class="sxs-lookup"><span data-stu-id="64058-134">Two other mouse messages are disabled by default, but may be useful for some applications:</span></span>

-   <span data-ttu-id="64058-135">[**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): o cursor foi focalizado na área do cliente por um período de tempo fixo.</span><span class="sxs-lookup"><span data-stu-id="64058-135">[**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): The cursor has hovered over the client area for a fixed period of time.</span></span>
-   <span data-ttu-id="64058-136">[**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): o cursor saiu da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="64058-136">[**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): The cursor has left the client area.</span></span>

<span data-ttu-id="64058-137">Para habilitar essas mensagens, chame a função [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) .</span><span class="sxs-lookup"><span data-stu-id="64058-137">To enable these messages, call the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function.</span></span>


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



<span data-ttu-id="64058-138">A estrutura [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) contém os parâmetros para a função.</span><span class="sxs-lookup"><span data-stu-id="64058-138">The [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) structure contains the parameters for the function.</span></span> <span data-ttu-id="64058-139">O membro **dwFlags** da estrutura contém sinalizadores de bits que especificam em quais mensagens de rastreamento você está interessado.</span><span class="sxs-lookup"><span data-stu-id="64058-139">The **dwFlags** member of the structure contains bit flags that specify which tracking messages you are interested in.</span></span> <span data-ttu-id="64058-140">Você pode optar por obter o [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) e o [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), como mostrado aqui ou apenas um dos dois.</span><span class="sxs-lookup"><span data-stu-id="64058-140">You can choose to get both [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) and [**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), as shown here, or just one of the two.</span></span> <span data-ttu-id="64058-141">O membro **dwHoverTime** especifica por quanto tempo o mouse precisa ser focalizado antes que o sistema gere uma mensagem de foco.</span><span class="sxs-lookup"><span data-stu-id="64058-141">The **dwHoverTime** member specifies how long the mouse needs to hover before the system generates a hover message.</span></span> <span data-ttu-id="64058-142">Esse valor é fornecido em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="64058-142">This value is given in milliseconds.</span></span> <span data-ttu-id="64058-143">O **\_ padrão de foco** constante significa usar o padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="64058-143">The constant **HOVER\_DEFAULT** means to use the system default.</span></span>

<span data-ttu-id="64058-144">Depois que você receber uma das mensagens solicitadas, a função [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) será redefinida.</span><span class="sxs-lookup"><span data-stu-id="64058-144">After you get one of the messages that you requested, the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function resets.</span></span> <span data-ttu-id="64058-145">Você deve chamá-lo novamente para obter outra mensagem de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="64058-145">You must call it again to get another tracking message.</span></span> <span data-ttu-id="64058-146">No entanto, você deve aguardar até a próxima mensagem de movimentação do mouse antes de chamar **TrackMouseEvent** novamente.</span><span class="sxs-lookup"><span data-stu-id="64058-146">However, you should wait until the next mouse-move message before calling **TrackMouseEvent** again.</span></span> <span data-ttu-id="64058-147">Caso contrário, sua janela poderá ser inundada com mensagens de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="64058-147">Otherwise, your window might be flooded with tracking messages.</span></span> <span data-ttu-id="64058-148">Por exemplo, se o mouse estiver focalizando, o sistema continuaria a gerar um fluxo de mensagens do [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) , enquanto o mouse é estático.</span><span class="sxs-lookup"><span data-stu-id="64058-148">For example, if the mouse is hovering, the system would continue to generate a stream of [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) messages while the mouse is stationary.</span></span> <span data-ttu-id="64058-149">Na verdade, você não quer outra mensagem do **WM \_ MOUSEHOVER** até que o mouse se mova para outro ponto e focalize novamente.</span><span class="sxs-lookup"><span data-stu-id="64058-149">You don't actually want another **WM\_MOUSEHOVER** message until the mouse moves to another spot and hovers again.</span></span>

<span data-ttu-id="64058-150">Aqui está uma pequena classe auxiliar que você pode usar para gerenciar eventos de controle de mouse.</span><span class="sxs-lookup"><span data-stu-id="64058-150">Here is a small helper class that you can use to manage mouse-tracking events.</span></span>


```C++
class MouseTrackEvents
{
    bool m_bMouseTracking;

public:
    MouseTrackEvents() : m_bMouseTracking(false)
    {
    }
    
    void OnMouseMove(HWND hwnd)
    {
        if (!m_bMouseTracking)
        {
            // Enable mouse tracking.
            TRACKMOUSEEVENT tme;
            tme.cbSize = sizeof(tme);
            tme.hwndTrack = hwnd;
            tme.dwFlags = TME_HOVER | TME_LEAVE;
            tme.dwHoverTime = HOVER_DEFAULT;
            TrackMouseEvent(&tme);
            m_bMouseTracking = true;
        }
    }
    void Reset(HWND hwnd)
    {
        m_bMouseTracking = false;
    }
};
```



<span data-ttu-id="64058-151">O exemplo a seguir mostra como usar essa classe em seu procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="64058-151">The next example shows how to use this class in your window procedure.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_MOUSEMOVE:
        mouseTrack.OnMouseMove(m_hwnd);  // Start tracking.

        // TODO: Handle the mouse-move message.

        return 0;

    case WM_MOUSELEAVE:

        // TODO: Handle the mouse-leave message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    case WM_MOUSEHOVER:

        // TODO: Handle the mouse-hover message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="64058-152">Os eventos de rastreamento do mouse exigem processamento adicional pelo sistema, portanto, deixe-os desabilitados se você não precisar deles.</span><span class="sxs-lookup"><span data-stu-id="64058-152">Mouse tracking events require additional processing by the system, so leave them disabled if you do not need them.</span></span>

<span data-ttu-id="64058-153">Para fins de integridade, aqui está uma função que consulta o sistema para o tempo limite de foco padrão.</span><span class="sxs-lookup"><span data-stu-id="64058-153">For completeness, here is a function that queries the system for the default hover timeout.</span></span>


```C++
UINT GetMouseHoverTime()
{
    UINT msec; 
    if (SystemParametersInfo(SPI_GETMOUSEHOVERTIME, 0, &msec, 0))
    {   
        return msec;
    }
    else
    {
        return 0;
    }
}
```



## <a name="mouse-wheel"></a><span data-ttu-id="64058-154">Botão de rolagem do mouse</span><span class="sxs-lookup"><span data-stu-id="64058-154">Mouse Wheel</span></span>

<span data-ttu-id="64058-155">A função a seguir verifica se uma roda do mouse está presente.</span><span class="sxs-lookup"><span data-stu-id="64058-155">The following function checks if a mouse wheel is present.</span></span>


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



<span data-ttu-id="64058-156">Se o usuário girar a roda do mouse, a janela com foco receberá uma mensagem do [**WM \_ MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) .</span><span class="sxs-lookup"><span data-stu-id="64058-156">If the user rotates the mouse wheel, the window with focus receives a [**WM\_MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) message.</span></span> <span data-ttu-id="64058-157">O parâmetro *wParam* dessa mensagem contém um valor inteiro chamado *Delta* que mede a distância em que a roda foi girada.</span><span class="sxs-lookup"><span data-stu-id="64058-157">The *wParam* parameter of this message contains an integer value called the *delta* that measures how far the wheel was rotated.</span></span> <span data-ttu-id="64058-158">O Delta usa unidades arbitrárias, nas quais 120 unidades são definidas como a rotação necessária para executar uma "ação".</span><span class="sxs-lookup"><span data-stu-id="64058-158">The delta uses arbitrary units, where 120 units is defined as the rotation needed to perform one "action."</span></span> <span data-ttu-id="64058-159">É claro que a definição de uma ação depende do seu programa.</span><span class="sxs-lookup"><span data-stu-id="64058-159">Of course, the definition of an action depends on your program.</span></span> <span data-ttu-id="64058-160">Por exemplo, se a roda do mouse for usada para rolar o texto, cada 120 unidades de rotação rolarão uma linha de texto.</span><span class="sxs-lookup"><span data-stu-id="64058-160">For example, if the mouse wheel is used to scroll text, each 120 units of rotation would scroll one line of text.</span></span>

<span data-ttu-id="64058-161">O sinal do Delta indica a direção da rotação:</span><span class="sxs-lookup"><span data-stu-id="64058-161">The sign of the delta indicates the direction of rotation:</span></span>

-   <span data-ttu-id="64058-162">Positivo: gire para frente, para longe do usuário.</span><span class="sxs-lookup"><span data-stu-id="64058-162">Positive: Rotate forward, away from the user.</span></span>
-   <span data-ttu-id="64058-163">Negativo: girar para trás, para o usuário.</span><span class="sxs-lookup"><span data-stu-id="64058-163">Negative: Rotate backward, toward the user.</span></span>

<span data-ttu-id="64058-164">O valor do Delta é colocado em *wParam* junto com alguns sinalizadores adicionais.</span><span class="sxs-lookup"><span data-stu-id="64058-164">The value of the delta is placed in *wParam* along with some additional flags.</span></span> <span data-ttu-id="64058-165">Use a macro do [**\_ wParam do \_ Delta \_ da roda Get**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) para obter o valor do Delta.</span><span class="sxs-lookup"><span data-stu-id="64058-165">Use the [**GET\_WHEEL\_DELTA\_WPARAM**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) macro to get the value of the delta.</span></span>


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="64058-166">Se a roda do mouse tiver uma resolução alta, o valor absoluto do Delta poderá ser menor que 120.</span><span class="sxs-lookup"><span data-stu-id="64058-166">If the mouse wheel has a high resolution, the absolute value of the delta might be less than 120.</span></span> <span data-ttu-id="64058-167">Nesse caso, se fizer sentido para que a ação ocorra em incrementos menores, você poderá fazer isso.</span><span class="sxs-lookup"><span data-stu-id="64058-167">In that case, if it makes sense for the action to occur in smaller increments, you can do so.</span></span> <span data-ttu-id="64058-168">Por exemplo, o texto pode rolar por incrementos de menos de uma linha.</span><span class="sxs-lookup"><span data-stu-id="64058-168">For example, text could scroll by increments of less than one line.</span></span> <span data-ttu-id="64058-169">Caso contrário, acumule o Delta total até que a roda gire o suficiente para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="64058-169">Otherwise, accumulate the total delta until the wheel rotates enough to perform the action.</span></span> <span data-ttu-id="64058-170">Armazene o Delta não utilizado em uma variável e, quando as unidades 120 se acumulam (positivas ou negativas), execute a ação.</span><span class="sxs-lookup"><span data-stu-id="64058-170">Store the unused delta in a variable, and when 120 units accumulate (either positive or negative), perform the action.</span></span>

## <a name="next"></a><span data-ttu-id="64058-171">Avançar</span><span class="sxs-lookup"><span data-stu-id="64058-171">Next</span></span>

[<span data-ttu-id="64058-172">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="64058-172">Keyboard Input</span></span>](keyboard-input.md)

 

 