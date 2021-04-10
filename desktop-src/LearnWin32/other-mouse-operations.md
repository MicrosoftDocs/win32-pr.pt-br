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
# <a name="miscellaneous-mouse-operations"></a>Diversas operações de mouse

As seções anteriores discutiram os cliques do mouse e o movimento do mouse. Aqui estão algumas outras operações que podem ser executadas com o mouse.

## <a name="dragging-ui-elements"></a>Arrastando elementos da interface do usuário

Se sua interface do usuário der suporte ao arrastar de elementos da interface do usuário, há uma outra função que você deve chamar no manipulador de mensagens do mouse-Down: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect). A função **DragDetect** retornará **true** se o usuário iniciar um gesto do mouse que deve ser interpretado como arrastando. O código a seguir mostra como usar essa função.


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



Esta é a ideia: quando um programa dá suporte a arrastar e soltar, você não quer que cada clique do mouse seja interpretado como um arrastar. Caso contrário, o usuário pode acidentalmente arrastar algo quando ele simplesmente pretendia clicar nele (por exemplo, para selecioná-lo). Mas se um mouse for particularmente confidencial, pode ser difícil manter o mouse perfeitamente ao clicar. Portanto, o Windows define um limite de arraste de alguns pixels. Quando o usuário pressiona o botão do mouse, ele não é considerado um arrastar, a menos que o mouse cruze esse limite. A função [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) testa se esse limite é atingido. Se a função retornar **true**, você poderá interpretar o clique do mouse como um arrastar. Caso contrário, não faça isso.

> [!Note]  
> Se [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) retornar **false**, o Windows suprimirá a mensagem do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) quando o usuário liberar o botão do mouse. Portanto, não chame **DragDetect** , a menos que seu programa esteja atualmente em um modo que ofereça suporte a arrastar. (Por exemplo, se um elemento de interface do usuário arrastável já estiver selecionado.) No final deste módulo, veremos um exemplo de código mais longo que usa a função **DragDetect** .

 

## <a name="confining-the-cursor"></a>Confinando o cursor

Às vezes, talvez você queira restringir o cursor para a área do cliente ou uma parte da área do cliente. A função [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) restringe a movimentação do cursor para um retângulo especificado. Esse retângulo é fornecido em coordenadas de tela, em vez de coordenadas de cliente, portanto, o ponto (0, 0) significa o canto superior esquerdo da tela. Para converter as coordenadas do cliente em coordenadas da tela, chame a função [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).

O código a seguir confina o cursor para a área do cliente da janela.


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



[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) usa uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) , mas [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) usa uma estrutura de [**pontos**](/previous-versions//dd162805(v=vs.85)) . Um retângulo é definido por seus pontos superior esquerdo e inferior direito. Você pode confinar o cursor para qualquer área retangular, incluindo áreas fora da janela, mas o confinamento do cursor para a área do cliente é uma maneira típica de usar a função. O confinamento do cursor para uma região totalmente fora de sua janela seria incomum e os usuários provavelmente a perceberam como um bug.

Para remover a restrição, chame [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) com o valor **NULL**.


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a>Eventos de rastreamento do mouse: focalizar e sair

Duas outras mensagens do mouse são desabilitadas por padrão, mas podem ser úteis para alguns aplicativos:

-   [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): o cursor foi focalizado na área do cliente por um período de tempo fixo.
-   [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): o cursor saiu da área do cliente.

Para habilitar essas mensagens, chame a função [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) .


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



A estrutura [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) contém os parâmetros para a função. O membro **dwFlags** da estrutura contém sinalizadores de bits que especificam em quais mensagens de rastreamento você está interessado. Você pode optar por obter o [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) e o [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), como mostrado aqui ou apenas um dos dois. O membro **dwHoverTime** especifica por quanto tempo o mouse precisa ser focalizado antes que o sistema gere uma mensagem de foco. Esse valor é fornecido em milissegundos. O **\_ padrão de foco** constante significa usar o padrão do sistema.

Depois que você receber uma das mensagens solicitadas, a função [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) será redefinida. Você deve chamá-lo novamente para obter outra mensagem de rastreamento. No entanto, você deve aguardar até a próxima mensagem de movimentação do mouse antes de chamar **TrackMouseEvent** novamente. Caso contrário, sua janela poderá ser inundada com mensagens de rastreamento. Por exemplo, se o mouse estiver focalizando, o sistema continuaria a gerar um fluxo de mensagens do [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) , enquanto o mouse é estático. Na verdade, você não quer outra mensagem do **WM \_ MOUSEHOVER** até que o mouse se mova para outro ponto e focalize novamente.

Aqui está uma pequena classe auxiliar que você pode usar para gerenciar eventos de controle de mouse.


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



O exemplo a seguir mostra como usar essa classe em seu procedimento de janela.


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



Os eventos de rastreamento do mouse exigem processamento adicional pelo sistema, portanto, deixe-os desabilitados se você não precisar deles.

Para fins de integridade, aqui está uma função que consulta o sistema para o tempo limite de foco padrão.


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



## <a name="mouse-wheel"></a>Botão de rolagem do mouse

A função a seguir verifica se uma roda do mouse está presente.


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



Se o usuário girar a roda do mouse, a janela com foco receberá uma mensagem do [**WM \_ MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) . O parâmetro *wParam* dessa mensagem contém um valor inteiro chamado *Delta* que mede a distância em que a roda foi girada. O Delta usa unidades arbitrárias, nas quais 120 unidades são definidas como a rotação necessária para executar uma "ação". É claro que a definição de uma ação depende do seu programa. Por exemplo, se a roda do mouse for usada para rolar o texto, cada 120 unidades de rotação rolarão uma linha de texto.

O sinal do Delta indica a direção da rotação:

-   Positivo: gire para frente, para longe do usuário.
-   Negativo: girar para trás, para o usuário.

O valor do Delta é colocado em *wParam* junto com alguns sinalizadores adicionais. Use a macro do [**\_ wParam do \_ Delta \_ da roda Get**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) para obter o valor do Delta.


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Se a roda do mouse tiver uma resolução alta, o valor absoluto do Delta poderá ser menor que 120. Nesse caso, se fizer sentido para que a ação ocorra em incrementos menores, você poderá fazer isso. Por exemplo, o texto pode rolar por incrementos de menos de uma linha. Caso contrário, acumule o Delta total até que a roda gire o suficiente para executar a ação. Armazene o Delta não utilizado em uma variável e, quando as unidades 120 se acumulam (positivas ou negativas), execute a ação.

## <a name="next"></a>Avançar

[Entrada de teclado](keyboard-input.md)

 

 