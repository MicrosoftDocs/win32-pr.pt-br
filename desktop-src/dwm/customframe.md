---
title: Quadro de janela personalizado usando DWM
description: Este tópico demonstra como usar as APIs de Gerenciador de Janelas da Área de Trabalho (DWM) para criar quadros de janela personalizados para seu aplicativo.
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), quadros de janela personalizados
- DWM (Gerenciador de Janelas da Área de Trabalho), quadros de janela personalizados
- quadros de janela personalizados
- removendo quadros padrão
- estendendo quadros de cliente
- Gerenciador de Janelas da Área de Trabalho (DWM), estendendo quadros de cliente
- DWM (Gerenciador de Janelas da Área de Trabalho), estendendo quadros de cliente
- Gerenciador de Janelas da Área de Trabalho (DWM), removendo quadros padrão
- DWM (Gerenciador de Janelas da Área de Trabalho), removendo quadros padrão
- Gerenciador de Janelas da Área de Trabalho (DWM), desenho em quadros estendidos
- DWM (Gerenciador de Janelas da Área de Trabalho), desenho em quadros estendidos
- desenho em quadros estendidos
- testes de clique
- Gerenciador de Janelas da Área de Trabalho (DWM), teste de clique
- DWM (Gerenciador de Janelas da Área de Trabalho), teste de clique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a27a9b71dd2dd91cb000a352ef039de2a71cd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008333"
---
# <a name="custom-window-frame-using-dwm"></a>Quadro de janela personalizado usando DWM

Este tópico demonstra como usar as APIs de Gerenciador de Janelas da Área de Trabalho (DWM) para criar quadros de janela personalizados para seu aplicativo.

-   [Introdução](#introduction)
-   [Estendendo o quadro do cliente](#extending-the-client-frame)
-   [Removendo o quadro padrão](#removing-the-standard-frame)
-   [Desenho na janela do quadro estendido](#drawing-in-the-extended-frame-window)
-   [Habilitando o teste de clique para o quadro personalizado](#enabling-hit-testing-for-the-custom-frame)
-   [Apêndice A: procedimento de janela de exemplo](#appendix-a-sample-window-procedure)
-   [Apêndice B: pintando o título da legenda](#appendix-b-painting-the-caption-title)
-   [Apêndice C: função HitTestNCA](#appendix-c-hittestnca-function)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

No Windows Vista e posterior, a aparência das áreas que não são de cliente das janelas de aplicativos (a barra de título, o ícone, a borda da janela e os botões de legenda) é controlada pelo DWM. Usando as APIs DWM, você pode alterar a maneira como o DWM renderiza o quadro de uma janela.

Um recurso das APIs do DWM é a capacidade de estender o quadro do aplicativo para a área do cliente. Isso permite que você integre um elemento de interface do usuário do cliente — como uma barra de ferramentas — ao quadro, dando à interface do usuário um lugar mais proeminente na interface do usuário do aplicativo. Por exemplo, o Windows Internet Explorer 7 no Windows Vista integra a barra de navegação no quadro da janela, estendendo a parte superior do quadro, conforme mostrado na captura de tela a seguir.

![barra de navegação integrada ao quadro da janela.](images/ie7-extendedborder-boxed.png)

A capacidade de estender o quadro da janela também permite que você crie quadros personalizados mantendo a aparência da janela. Por exemplo, Microsoft Office o Word 2007 desenha o botão do Office e a barra de ferramentas de acesso rápido dentro do quadro personalizado, fornecendo os botões de legenda padrão de minimizar, maximizar e fechar, conforme mostrado na captura de tela a seguir.

![botão do Office e barra de ferramentas de acesso rápido no Word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a>Estendendo o quadro do cliente

A funcionalidade para estender o quadro para a área do cliente é exposta pela função [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) . Para estender o quadro, passe o identificador da janela de destino junto com os valores de margem inserida para **DwmExtendFrameIntoClientArea**. Os valores de margem interna determinam a distância para estender o quadro nos quatro lados da janela.

O código a seguir demonstra o uso de [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) para estender o quadro.


```
// Handle the window activation.
if (message == WM_ACTIVATE)
{
    // Extend the frame into the client area.
    MARGINS margins;

    margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
    margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
    margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
    margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

    hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

    if (!SUCCEEDED(hr))
    {
        // Handle the error.
    }

    fCallDWP = true;
    lRet = 0;
}
```



Observe que a extensão de quadro é feita na mensagem de [**\_ ativação do WM**](/windows/desktop/inputdev/wm-activate) em vez da mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) . Isso garante que a extensão de quadro seja manipulada corretamente quando a janela estiver em seu tamanho padrão e quando for maximizada.

A imagem a seguir mostra um quadro de janela padrão (à esquerda) e o mesmo quadro de janela estendido (à direita). O quadro é estendido usando o exemplo de código anterior e a tela de fundo padrão Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) (janela de cores \_ + 1).

![captura de tela de um padrão (à esquerda) e quadro estendido (à direita) com plano de fundo branco](images/white-sidebyside.png)

A diferença visual entre essas duas janelas é muito sutil. A única diferença entre os dois é que a borda da linha preta fina da região do cliente na janela à esquerda está ausente na janela à direita. O motivo para essa falta de borda é que ela é incorporada ao quadro estendido, mas o restante da área do cliente não é. Para que os quadros estendidos fiquem visíveis, as regiões subjacentes a cada um dos lados do quadro estendido devem ter dados de pixel com um valor alfa de 0. A borda preta em torno da região do cliente tem dados de pixel em que todos os valores de cor (vermelho, verde, azul e alfa) são definidos como 0. O restante do plano de fundo não tem o valor alfa definido como 0, portanto, o restante do quadro estendido não está visível.

A maneira mais fácil de garantir que os quadros estendidos fiquem visíveis é pintar toda a região do cliente em preto. Para fazer isso, inicialize o membro *hbrBackground* da sua estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ou [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) para o identificador do pincel preto de estoque \_ . A imagem a seguir mostra o mesmo quadro padrão (à esquerda) e o quadro estendido (à direita) mostrado anteriormente. Dessa vez, no entanto, *hbrBackground* é definido como o \_ identificador de pincel preto obtido da função [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) .

![captura de tela de um padrão (à esquerda) e quadro estendido (à direita) com plano de fundo preto](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a>Removendo o quadro padrão

Depois de estender o quadro do aplicativo e tornar-o visível, você pode remover o quadro padrão. A remoção do quadro padrão permite que você controle a largura de cada lado do quadro em vez de simplesmente estender o quadro padrão.

Para remover o quadro de janela padrão, você deve manipular a mensagem do [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) , especificamente quando seu valor *wParam* é **true** e o valor de retorno é 0. Ao fazer isso, seu aplicativo usa a região da janela inteira como a área do cliente, removendo o quadro padrão.

Os resultados da manipulação da mensagem do [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) não são visíveis até que a região do cliente precise ser redimensionada. Até esse momento, a exibição inicial da janela é exibida com o quadro padrão e as bordas estendidas. Para resolver isso, você deve redimensionar a janela ou executar uma ação que inicia uma mensagem do **WM \_ NCCALCSIZE** no momento da criação da janela. Isso pode ser feito usando a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para mover sua janela e redimensioná-la. O código a seguir demonstra uma chamada para **SetWindowPos** que força uma mensagem **\_ NCCALCSIZE do WM** a ser enviada usando os atributos de retângulo da janela atual e o \_ sinalizador framechanged do SWP.


```
// Handle window creation.
if (message == WM_CREATE)
{
    RECT rcClient;
    GetWindowRect(hWnd, &rcClient);

    // Inform the application of the frame change.
    SetWindowPos(hWnd, 
                 NULL, 
                 rcClient.left, rcClient.top,
                 RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                 SWP_FRAMECHANGED);

    fCallDWP = true;
    lRet = 0;
}
```



A imagem a seguir mostra o quadro padrão (à esquerda) e o quadro recentemente estendido sem o quadro padrão (direita).

![captura de tela de um quadro padrão (à esquerda) e quadro personalizado (à direita)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a>Desenho na janela do quadro estendido

Ao remover o quadro padrão, você perde o desenho automático do ícone e do título do aplicativo. Para adicioná-los de volta ao seu aplicativo, você mesmo deve desenhá-los. Para fazer isso, primeiro examine a alteração que ocorreu na sua área de cliente.

Com a remoção do quadro padrão, sua área de cliente agora consiste em toda a janela, incluindo o quadro estendido. Isso inclui a região onde os botões de legenda são desenhados. Na seguinte comparação lado a lado, a área do cliente para o quadro padrão e o quadro estendido personalizado é realçado em vermelho. A área do cliente para a janela de quadro padrão (esquerda) é a região preta. Na janela do quadro estendido (à direita), a área do cliente é a janela inteira.

![captura de tela de áreas de cliente em vermelho realçadas em quadro padrão e personalizado](images/clientarea-sidebyside.png)

Como a janela inteira é a área do cliente, você pode simplesmente desenhar o que deseja no quadro estendido. Para adicionar um título ao seu aplicativo, basta desenhar o texto na região apropriada. A imagem a seguir mostra o texto com tema desenhado no quadro de legenda personalizada. O título é desenhado usando a função [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) . Para exibir o código que pinta o título, consulte [o apêndice B: pintando o título da legenda](#appendix-b-painting-the-caption-title).

![captura de tela de um quadro personalizado com título](images/custom-caption-title.png)

> [!Note]  
> Ao desenhar em seu quadro personalizado, tenha cuidado ao colocar os controles da interface do usuário. Como a janela inteira é sua região de cliente, você deve ajustar o posicionamento do controle de interface do usuário para cada largura de quadro se não quiser que eles apareçam no quadro estendido ou no mesmo.

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a>Habilitando o teste de clique para o quadro personalizado

Um efeito colateral de remover o quadro padrão é a perda do comportamento padrão de redimensionamento e movimentação. Para que seu aplicativo eMule corretamente o comportamento de janela padrão, você precisará implementar a lógica para lidar com o teste de clique de botão de legenda e o redimensionamento/movimentação de quadros.

Para teste de clique de botão de legenda, o DWM fornece a função [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) . Para testar corretamente os botões de legenda em cenários de quadro personalizados, as mensagens devem primeiro ser passadas para **DwmDefWindowProc** para manipulação. **DwmDefWindowProc** retornará **true** se uma mensagem for manipulada e **false** se não for. Se a mensagem não for tratada pelo **DwmDefWindowProc**, seu aplicativo deverá lidar com a própria mensagem ou passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Para redimensionamento e movimentação de quadros, seu aplicativo deve fornecer a lógica de teste de cliques e manipular mensagens de teste de clique de quadro. As mensagens de teste de quadro de quadros são enviadas para você por meio da mensagem do [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) , mesmo que seu aplicativo crie um quadro personalizado sem o quadro padrão. O código a seguir demonstra como tratar a mensagem do **WM \_ NCHITTEST** quando o [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) não a trata. Para ver o código da função chamada `HitTestNCA` , consulte o [Apêndice C: HitTestNCA function](#appendix-c-hittestnca-function).


```
// Handle hit testing in the NCA if not handled by DwmDefWindowProc.
if ((message == WM_NCHITTEST) && (lRet == 0))
{
    lRet = HitTestNCA(hWnd, wParam, lParam);

    if (lRet != HTNOWHERE)
    {
        fCallDWP = false;
    }
}
```



## <a name="appendix-a-sample-window-procedure"></a>Apêndice A: procedimento de janela de exemplo

O exemplo de código a seguir demonstra um procedimento de janela e suas funções de trabalho de suporte usadas para criar um aplicativo de quadro personalizado.


```
//
//  Main WinProc.
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    bool fCallDWP = true;
    BOOL fDwmEnabled = FALSE;
    LRESULT lRet = 0;
    HRESULT hr = S_OK;

    // Winproc worker for custom frame issues.
    hr = DwmIsCompositionEnabled(&fDwmEnabled);
    if (SUCCEEDED(hr))
    {
        lRet = CustomCaptionProc(hWnd, message, wParam, lParam, &fCallDWP);
    }

    // Winproc worker for the rest of the application.
    if (fCallDWP)
    {
        lRet = AppWinProc(hWnd, message, wParam, lParam);
    }
    return lRet;
}

//
// Message handler for handling the custom caption messages.
//
LRESULT CustomCaptionProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam, bool* pfCallDWP)
{
    LRESULT lRet = 0;
    HRESULT hr = S_OK;
    bool fCallDWP = true; // Pass on to DefWindowProc?

    fCallDWP = !DwmDefWindowProc(hWnd, message, wParam, lParam, &lRet);

    // Handle window creation.
    if (message == WM_CREATE)
    {
        RECT rcClient;
        GetWindowRect(hWnd, &rcClient);

        // Inform application of the frame change.
        SetWindowPos(hWnd, 
                     NULL, 
                     rcClient.left, rcClient.top,
                     RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                     SWP_FRAMECHANGED);

        fCallDWP = true;
        lRet = 0;
    }

    // Handle window activation.
    if (message == WM_ACTIVATE)
    {
        // Extend the frame into the client area.
        MARGINS margins;

        margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
        margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
        margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
        margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

        hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

        if (!SUCCEEDED(hr))
        {
            // Handle error.
        }

        fCallDWP = true;
        lRet = 0;
    }

    if (message == WM_PAINT)
    {
        HDC hdc;
        {
            PAINTSTRUCT ps;
            hdc = BeginPaint(hWnd, &ps);
            PaintCustomCaption(hWnd, hdc);
            EndPaint(hWnd, &ps);
        }

        fCallDWP = true;
        lRet = 0;
    }

    // Handle the non-client size message.
    if ((message == WM_NCCALCSIZE) && (wParam == TRUE))
    {
        // Calculate new NCCALCSIZE_PARAMS based on custom NCA inset.
        NCCALCSIZE_PARAMS *pncsp = reinterpret_cast<NCCALCSIZE_PARAMS*>(lParam);

        pncsp->rgrc[0].left   = pncsp->rgrc[0].left   + 0;
        pncsp->rgrc[0].top    = pncsp->rgrc[0].top    + 0;
        pncsp->rgrc[0].right  = pncsp->rgrc[0].right  - 0;
        pncsp->rgrc[0].bottom = pncsp->rgrc[0].bottom - 0;

        lRet = 0;
        
        // No need to pass the message on to the DefWindowProc.
        fCallDWP = false;
    }

    // Handle hit testing in the NCA if not handled by DwmDefWindowProc.
    if ((message == WM_NCHITTEST) && (lRet == 0))
    {
        lRet = HitTestNCA(hWnd, wParam, lParam);

        if (lRet != HTNOWHERE)
        {
            fCallDWP = false;
        }
    }

    *pfCallDWP = fCallDWP;

    return lRet;
}

//
// Message handler for the application.
//
LRESULT AppWinProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    HRESULT hr; 
    LRESULT result = 0;

    switch (message)
    {
        case WM_CREATE:
            {}
            break;
        case WM_COMMAND:
            wmId    = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            // Parse the menu selections:
            switch (wmId)
            {
                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }
            break;
        case WM_PAINT:
            {
                hdc = BeginPaint(hWnd, &ps);
                PaintCustomCaption(hWnd, hdc);
                
                // Add any drawing code here...
    
                EndPaint(hWnd, &ps);
            }
            break;
        case WM_DESTROY:
            PostQuitMessage(0);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



## <a name="appendix-b-painting-the-caption-title"></a>Apêndice B: pintando o título da legenda

O código a seguir demonstra como pintar um título de legenda no quadro estendido. Essa função deve ser chamada de dentro das chamadas [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) .


```
// Paint the title on the custom frame.
void PaintCustomCaption(HWND hWnd, HDC hdc)
{
    RECT rcClient;
    GetClientRect(hWnd, &rcClient);

    HTHEME hTheme = OpenThemeData(NULL, L"CompositedWindow::Window");
    if (hTheme)
    {
        HDC hdcPaint = CreateCompatibleDC(hdc);
        if (hdcPaint)
        {
            int cx = RECTWIDTH(rcClient);
            int cy = RECTHEIGHT(rcClient);

            // Define the BITMAPINFO structure used to draw text.
            // Note that biHeight is negative. This is done because
            // DrawThemeTextEx() needs the bitmap to be in top-to-bottom
            // order.
            BITMAPINFO dib = { 0 };
            dib.bmiHeader.biSize            = sizeof(BITMAPINFOHEADER);
            dib.bmiHeader.biWidth           = cx;
            dib.bmiHeader.biHeight          = -cy;
            dib.bmiHeader.biPlanes          = 1;
            dib.bmiHeader.biBitCount        = BIT_COUNT;
            dib.bmiHeader.biCompression     = BI_RGB;

            HBITMAP hbm = CreateDIBSection(hdc, &dib, DIB_RGB_COLORS, NULL, NULL, 0);
            if (hbm)
            {
                HBITMAP hbmOld = (HBITMAP)SelectObject(hdcPaint, hbm);

                // Setup the theme drawing options.
                DTTOPTS DttOpts = {sizeof(DTTOPTS)};
                DttOpts.dwFlags = DTT_COMPOSITED | DTT_GLOWSIZE;
                DttOpts.iGlowSize = 15;

                // Select a font.
                LOGFONT lgFont;
                HFONT hFontOld = NULL;
                if (SUCCEEDED(GetThemeSysFont(hTheme, TMT_CAPTIONFONT, &lgFont)))
                {
                    HFONT hFont = CreateFontIndirect(&lgFont);
                    hFontOld = (HFONT) SelectObject(hdcPaint, hFont);
                }

                // Draw the title.
                RECT rcPaint = rcClient;
                rcPaint.top += 8;
                rcPaint.right -= 125;
                rcPaint.left += 8;
                rcPaint.bottom = 50;
                DrawThemeTextEx(hTheme, 
                                hdcPaint, 
                                0, 0, 
                                szTitle, 
                                -1, 
                                DT_LEFT | DT_WORD_ELLIPSIS, 
                                &rcPaint, 
                                &DttOpts);

                // Blit text to the frame.
                BitBlt(hdc, 0, 0, cx, cy, hdcPaint, 0, 0, SRCCOPY);

                SelectObject(hdcPaint, hbmOld);
                if (hFontOld)
                {
                    SelectObject(hdcPaint, hFontOld);
                }
                DeleteObject(hbm);
            }
            DeleteDC(hdcPaint);
        }
        CloseThemeData(hTheme);
    }
}
```



## <a name="appendix-c-hittestnca-function"></a>Apêndice C: função HitTestNCA

O código a seguir mostra a `HitTestNCA` função usada [para habilitar o teste de clique para o quadro personalizado](#enabling-hit-testing-for-the-custom-frame). Essa função manipula a lógica de teste de cliques para o [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) quando o [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) não manipula a mensagem.


```
// Hit test the frame for resizing and moving.
LRESULT HitTestNCA(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    // Get the point coordinates for the hit test.
    POINT ptMouse = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam)};

    // Get the window rectangle.
    RECT rcWindow;
    GetWindowRect(hWnd, &rcWindow);

    // Get the frame rectangle, adjusted for the style without a caption.
    RECT rcFrame = { 0 };
    AdjustWindowRectEx(&rcFrame, WS_OVERLAPPEDWINDOW & ~WS_CAPTION, FALSE, NULL);

    // Determine if the hit test is for resizing. Default middle (1,1).
    USHORT uRow = 1;
    USHORT uCol = 1;
    bool fOnResizeBorder = false;

    // Determine if the point is at the top or bottom of the window.
    if (ptMouse.y >= rcWindow.top && ptMouse.y < rcWindow.top + TOPEXTENDWIDTH)
    {
        fOnResizeBorder = (ptMouse.y < (rcWindow.top - rcFrame.top));
        uRow = 0;
    }
    else if (ptMouse.y < rcWindow.bottom && ptMouse.y >= rcWindow.bottom - BOTTOMEXTENDWIDTH)
    {
        uRow = 2;
    }

    // Determine if the point is at the left or right of the window.
    if (ptMouse.x >= rcWindow.left && ptMouse.x < rcWindow.left + LEFTEXTENDWIDTH)
    {
        uCol = 0; // left side
    }
    else if (ptMouse.x < rcWindow.right && ptMouse.x >= rcWindow.right - RIGHTEXTENDWIDTH)
    {
        uCol = 2; // right side
    }

    // Hit test (HTTOPLEFT, ... HTBOTTOMRIGHT)
    LRESULT hitTests[3][3] = 
    {
        { HTTOPLEFT,    fOnResizeBorder ? HTTOP : HTCAPTION,    HTTOPRIGHT },
        { HTLEFT,       HTNOWHERE,     HTRIGHT },
        { HTBOTTOMLEFT, HTBOTTOM, HTBOTTOMRIGHT },
    };

    return hitTests[uRow][uCol];
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do Gerenciador de Janelas da Área de Trabalho](dwm-overview.md)
</dt> </dl>

 

 