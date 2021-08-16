---
title: Operações diversas do mouse
description: As seções anteriores discutiram os cliques do mouse e o movimento do mouse. Aqui estão algumas outras operações que podem ser executadas com o mouse.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31877ab5a71819fa896fd1253e7391f9ed748dffff636ab9d3e8591669b7fae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387962"
---
# <a name="miscellaneous-mouse-operations"></a>Operações diversas do mouse

As seções anteriores discutiram os cliques do mouse e o movimento do mouse. Aqui estão algumas outras operações que podem ser executadas com o mouse.

## <a name="dragging-ui-elements"></a>Arrastando elementos da interface do usuário

Se a interface do usuário dá suporte ao arrastar de elementos da interface do usuário, há outra função que você deve chamar no manipulador de mensagens do mouse para baixo: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect). A **função DragDetect** retornará **TRUE se** o usuário iniciar um gesto do mouse que deve ser interpretado como arrastar. O código a seguir mostra como usar essa função.


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



Esta é a ideia: quando um programa dá suporte a arrastar e soltar, você não deseja que cada clique do mouse seja interpretado como um arrastar. Caso contrário, o usuário poderá arrastar acidentalmente algo quando simplesmente quiser clicar nele (por exemplo, para selecioná-lo). Mas se um mouse for particularmente sensível, poderá ser difícil manter o mouse perfeitamente parado ao clicar. Portanto, Windows define um limite de arrastar de alguns pixels. Quando o usuário pressiona o botão do mouse, ele não é considerado um arrastar, a menos que o mouse cruze esse limite. A [**função DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) testa se esse limite é atingido. Se a função retornar **TRUE,** você poderá interpretar o clique do mouse como um arrastar. Caso contrário, não faça isso.

> [!Note]  
> Se [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) retornar **FALSE,** Windows suprime a mensagem [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) quando o usuário libera o botão do mouse. Portanto, não chame **DragDetect,** a menos que seu programa esteja atualmente em um modo que dá suporte a arrastar. (Por exemplo, se um elemento de interface do usuário que pode ser arrastada já estiver selecionado.) No final deste módulo, veremos um exemplo de código mais longo que usa a **função DragDetect.**

 

## <a name="confining-the-cursor"></a>Como limitar o cursor

Às vezes, talvez você queira restringir o cursor à área do cliente ou a uma parte da área do cliente. A [**função ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) restringe o movimento do cursor a um retângulo especificado. Esse retângulo é dado em coordenadas de tela, em vez de coordenadas de cliente, portanto, o ponto (0, 0) significa o canto superior esquerdo da tela. Para converter as coordenadas do cliente em coordenadas de tela, chame a [**função ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).

O código a seguir limita o cursor à área do cliente da janela.


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



[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) assume uma [**estrutura RECT,**](/previous-versions//dd162897(v=vs.85)) mas [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) assume uma [**estrutura POINT.**](/previous-versions//dd162805(v=vs.85)) Um retângulo é definido por seus pontos superior esquerdo e inferior direito. Você pode limitar o cursor a qualquer área retangular, incluindo áreas fora da janela, mas limitar o cursor à área do cliente é uma maneira típica de usar a função. Limitar o cursor a uma região totalmente fora da janela seria incomum e os usuários provavelmente perceberiam isso como um bug.

Para remover a restrição, chame [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) com o valor **NULL.**


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a>Eventos de acompanhamento do mouse: passar o mouse e sair

Duas outras mensagens do mouse são desabilitadas por padrão, mas podem ser úteis para alguns aplicativos:

-   [**WM \_ MOUSEHOVER:**](/windows/desktop/inputdev/wm-mousehover)o cursor passou sobre a área do cliente por um período fixo.
-   [**WM \_ MOUSELEAVE:**](/windows/desktop/inputdev/wm-mouseleave)o cursor saiu da área do cliente.

Para habilitar essas mensagens, chame a [**função TrackMouseEvent.**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent)


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



A [**estrutura TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) contém os parâmetros para a função. O **membro dwFlags** da estrutura contém sinalizadores de bits que especificam em quais mensagens de acompanhamento você está interessado. Você pode optar por obter [**o WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) e [**o WM \_ MOUSELEAVE,**](/windows/desktop/inputdev/wm-mouseleave)conforme mostrado aqui, ou apenas um dos dois. O **membro dwHoverTime** especifica por quanto tempo o mouse precisa passar o mouse antes que o sistema gere uma mensagem de foco. Esse valor é dado em milissegundos. A constante **HOVER \_ DEFAULT** significa usar o padrão do sistema.

Depois de obter uma das mensagens solicitadas, a [**função TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) é redefinida. Você deve chamá-lo novamente para obter outra mensagem de acompanhamento. No entanto, você deve aguardar até a próxima mensagem de movimentação do mouse antes de chamar **TrackMouseEvent** novamente. Caso contrário, sua janela poderá ser inundada com mensagens de acompanhamento. Por exemplo, se o mouse estiver passeando, o sistema continuará a gerar um fluxo de mensagens [**\_ WM MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) enquanto o mouse está parado. Na verdade, você não deseja outra mensagem **WM \_ MOUSEHOVER** até que o mouse se mova para outro ponto e passe o mouse novamente.

Aqui está uma pequena classe auxiliar que você pode usar para gerenciar eventos de acompanhamento do mouse.


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



Eventos de acompanhamento do mouse exigem processamento adicional pelo sistema, portanto, deixe-os desabilitados se você não precisar deles.

Para concluir, aqui está uma função que consulta o sistema quanto ao tempo de foco padrão.


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

A função a seguir verifica se há uma roda do mouse.


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



Se o usuário girar a roda do mouse, a janela com foco receberá uma mensagem [**WM \_ MOUSEWHEEL.**](/windows/desktop/inputdev/wm-mousewheel) O *parâmetro wParam* dessa mensagem contém um valor inteiro chamado *delta* que mede até que ponto a roda foi girada. O delta usa unidades arbitrárias, em que 120 unidades são definidas como a rotação necessária para executar uma "ação". É claro que a definição de uma ação depende do programa. Por exemplo, se a roda do mouse for usada para rolar o texto, cada 120 unidades de rotação rolará uma linha de texto.

O sinal do delta indica a direção da rotação:

-   Positivo: gire para frente, longe do usuário.
-   Negativo: gire para trás, em direção ao usuário.

O valor do delta é colocado em *wParam* junto com alguns sinalizadores adicionais. Use a [**macro \_ \_ \_ WPARAM GET WHEEL DELTA**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) para obter o valor do delta.


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Se a roda do mouse tiver uma alta resolução, o valor absoluto do delta poderá ser menor que 120. Nesse caso, se fizer sentido que a ação ocorra em incrementos menores, você poderá fazer isso. Por exemplo, o texto pode rolar por incrementos de menos de uma linha. Caso contrário, acumuque o delta total até que a roda gire o suficiente para executar a ação. Armazene o delta nãoutilado em uma variável e, quando 120 unidades se acumularem (positivas ou negativas), execute a ação.

## <a name="next"></a>Avançar

[Entrada do teclado](keyboard-input.md)

 

 