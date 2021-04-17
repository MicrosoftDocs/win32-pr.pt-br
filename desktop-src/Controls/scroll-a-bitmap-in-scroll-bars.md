---
title: Como rolar um bitmap
description: Esta seção descreve as alterações que você pode fazer no procedimento de janela principal de um aplicativo para permitir que o usuário Role um bitmap.
ms.assetid: FA6FEA49-25EB-4C18-AD07-74BD77501906
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a01a93fbb005b75d7cd860bc8545c4e77a80767
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454383"
---
# <a name="how-to-scroll-a-bitmap"></a>Como rolar um bitmap

Esta seção descreve as alterações que você pode fazer no procedimento de janela principal de um aplicativo para permitir que o usuário Role um bitmap.

O exemplo inclui um item de menu que copia o conteúdo da tela para um bitmap e exibe o bitmap na área do cliente. O exemplo também processa as mensagens do [**WM \_ HSCROLL**](wm-hscroll.md) e do [**WM \_ VSCROLL**](wm-vscroll.md) que são geradas pelas barras de rolagem para que o usuário possa rolar o bitmap horizontalmente e verticalmente. Ao contrário do exemplo de texto rolado, o exemplo de bitmap emprega a função [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) para desenhar a parte inválida da área do cliente.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="processing-the-wm_create-message"></a>Processando a \_ mensagem de criação do WM

Quando a mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) é processada, as variáveis que são necessárias para rolagem são inicializadas. Use a função [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) para criar um DC (contexto de dispositivo) compatível, a função [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) para criar um bitmap e a função [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) para selecionar o bitmap para o controlador de domínio. Observe que um controlador de domínio compatível também é conhecido como um controlador de domínio de memória.

As informações específicas do dispositivo sobre o dispositivo de vídeo são recuperadas. Se um controlador de domínio compatível for criado para a tela, como no exemplo, use a função [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) para obter essas informações. As informações incluem o número de bits de cor adjacentes por pixel, o número de planos de cores e a altura e a largura do controlador de domínio.

### <a name="processing-the-wm_size-message"></a>Processando a \_ mensagem de tamanho do WM

O processamento da mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) requer o ajuste do intervalo de rolagem e da posição, de modo que ele reflita as dimensões da área do cliente e o bitmap que será exibido.

A função [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) define os valores mínimo e máximo da posição, o tamanho da página e a posição da rolagem para uma barra de rolagem.

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a>Processando as \_ mensagens do WM HSCROLL e do WM \_ VSCROLL

Quando as mensagens do [**WM \_ HSCROLL**](wm-hscroll.md) e do [**WM \_ VSCROLL**](wm-vscroll.md) são processadas, o código de solicitação da barra de rolagem é examinado e a posição da rolagem é definida como um novo valor que reflete a ação de rolagem do usuário. Se a posição de rolagem estiver dentro do intervalo de rolagem, a janela será rolada para a nova posição usando a função [**ScrollWindow**](/windows/desktop/api/Winuser/nf-winuser-scrollwindow) . Em seguida, a posição da caixa de rolagem é ajustada usando a função [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) .

Depois que uma janela é rolada, parte de sua área do cliente é inválida. Para garantir que a região inválida seja atualizada, use a função [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) para gerar uma mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) . Ao processar a mensagem de **\_ pintura do WM** , um aplicativo deve redesenhar a região inválida na parte inferior da área do cliente. Ao rolar ou redimensionar a área do cliente, o exemplo usa a função [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) para copiar a parte apropriada do bitmap para a parte inválida da área do cliente.

## <a name="example-of-scrolling-a-bitmap"></a>Exemplo de rolagem de um bitmap

O exemplo a seguir permite que o usuário Capture o conteúdo da tela em um bitmap e role o bitmap na área do cliente. O conteúdo da tela é capturado quando o usuário clica com o botão direito do mouse na área do cliente.


```C++
LRESULT CALLBACK MyBitmapWindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    HDC hdc; 
    PAINTSTRUCT ps; 
    SCROLLINFO si; 
 
    // These variables are required by BitBlt. 
    static HDC hdcWin;           // window DC 
    static HDC hdcScreen;        // DC for entire screen 
    static HDC hdcScreenCompat;  // memory DC for screen 
    static HBITMAP hbmpCompat;   // bitmap handle to old DC 
    static BITMAP bmp;           // bitmap data structure 
    static BOOL fBlt;            // TRUE if BitBlt occurred 
    static BOOL fScroll;         // TRUE if scrolling occurred 
    static BOOL fSize;           // TRUE if fBlt & WM_SIZE 
 
    // These variables are required for horizontal scrolling. 
    static int xMinScroll;       // minimum horizontal scroll value 
    static int xCurrentScroll;   // current horizontal scroll value 
    static int xMaxScroll;       // maximum horizontal scroll value 
 
    // These variables are required for vertical scrolling. 
    static int yMinScroll;       // minimum vertical scroll value 
    static int yCurrentScroll;   // current vertical scroll value 
    static int yMaxScroll;       // maximum vertical scroll value 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create a normal DC and a memory DC for the entire 
            // screen. The normal DC provides a snapshot of the 
            // screen contents. The memory DC keeps a copy of this 
            // snapshot in the associated bitmap. 
            hdcScreen = CreateDC(L"DISPLAY", (PCTSTR) NULL, 
                (PCTSTR) NULL, (CONST DEVMODE *) NULL); 
            hdcScreenCompat = CreateCompatibleDC(hdcScreen); 
 
            // Retrieve the metrics for the bitmap associated with the 
            // regular device context. 
            bmp.bmBitsPixel = 
                (BYTE) GetDeviceCaps(hdcScreen, BITSPIXEL); 
            bmp.bmPlanes = (BYTE) GetDeviceCaps(hdcScreen, PLANES); 
            bmp.bmWidth = GetDeviceCaps(hdcScreen, HORZRES); 
            bmp.bmHeight = GetDeviceCaps(hdcScreen, VERTRES); 
 
            // The width must be byte-aligned. 
            bmp.bmWidthBytes = ((bmp.bmWidth + 15) &~15)/8; 
 
            // Create a bitmap for the compatible DC. 
            hbmpCompat = CreateBitmap(bmp.bmWidth, bmp.bmHeight, 
                bmp.bmPlanes, bmp.bmBitsPixel, (CONST VOID *) NULL); 
 
            // Select the bitmap for the compatible DC. 
            SelectObject(hdcScreenCompat, hbmpCompat); 
 
            // Initialize the flags. 
            fBlt = FALSE; 
            fScroll = FALSE; 
            fSize = FALSE; 
 
            // Initialize the horizontal scrolling variables. 
            xMinScroll = 0; 
            xCurrentScroll = 0; 
            xMaxScroll = 0; 
 
            // Initialize the vertical scrolling variables. 
            yMinScroll = 0; 
            yCurrentScroll = 0; 
            yMaxScroll = 0; 
 
            break; 
 
        case WM_SIZE: 
        { 
            int xNewSize; 
            int yNewSize; 
 
            xNewSize = LOWORD(lParam); 
            yNewSize = HIWORD(lParam); 
 
            if (fBlt) 
                fSize = TRUE; 
     
            // The horizontal scrolling range is defined by 
            // (bitmap_width) - (client_width). The current horizontal 
            // scroll value remains within the horizontal scrolling range. 
            xMaxScroll = max(bmp.bmWidth-xNewSize, 0); 
            xCurrentScroll = min(xCurrentScroll, xMaxScroll); 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_RANGE | SIF_PAGE | SIF_POS; 
            si.nMin   = xMinScroll; 
            si.nMax   = bmp.bmWidth; 
            si.nPage  = xNewSize; 
            si.nPos   = xCurrentScroll; 
            SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
            // The vertical scrolling range is defined by 
            // (bitmap_height) - (client_height). The current vertical 
            // scroll value remains within the vertical scrolling range. 
            yMaxScroll = max(bmp.bmHeight - yNewSize, 0); 
            yCurrentScroll = min(yCurrentScroll, yMaxScroll); 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_RANGE | SIF_PAGE | SIF_POS; 
            si.nMin   = yMinScroll; 
            si.nMax   = bmp.bmHeight; 
            si.nPage  = yNewSize; 
            si.nPos   = yCurrentScroll; 
            SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 

            break; 
        } 
 
        case WM_PAINT: 
        { 
            PRECT prect; 
 
            hdc = BeginPaint(hwnd, &ps); 
 
            // If the window has been resized and the user has 
            // captured the screen, use the following call to 
            // BitBlt to paint the window's client area. 
            if (fSize) 
            { 
                BitBlt(ps.hdc, 
                    0, 0, 
                    bmp.bmWidth, bmp.bmHeight, 
                    hdcScreenCompat, 
                    xCurrentScroll, yCurrentScroll, 
                    SRCCOPY); 
 
                fSize = FALSE; 
            } 
 
            // If scrolling has occurred, use the following call to 
            // BitBlt to paint the invalid rectangle. 
            // 
            // The coordinates of this rectangle are specified in the 
            // RECT structure to which prect points. 
            // 
            // Note that it is necessary to increment the seventh 
            // argument (prect->left) by xCurrentScroll and the 
            // eighth argument (prect->top) by yCurrentScroll in 
            // order to map the correct pixels from the source bitmap. 
             if (fScroll) 
            { 
                prect = &ps.rcPaint; 
 
                BitBlt(ps.hdc, 
                    prect->left, prect->top, 
                    (prect->right - prect->left), 
                    (prect->bottom - prect->top), 
                    hdcScreenCompat, 
                    prect->left + xCurrentScroll, 
                    prect->top + yCurrentScroll, 
                    SRCCOPY); 
 
                fScroll = FALSE; 
            } 
 
            EndPaint(hwnd, &ps); 

            break; 
        } 

        case WM_HSCROLL: 
        { 
            int xDelta;     // xDelta = new_pos - current_pos  
            int xNewPos;    // new position 
            int yDelta = 0; 
 
            switch (LOWORD(wParam)) 
            { 
                // User clicked the scroll bar shaft left of the scroll box. 
                case SB_PAGEUP: 
                    xNewPos = xCurrentScroll - 50; 
                    break; 
 
                // User clicked the scroll bar shaft right of the scroll box. 
                case SB_PAGEDOWN: 
                    xNewPos = xCurrentScroll + 50; 
                    break; 
 
                // User clicked the left arrow. 
                case SB_LINEUP: 
                    xNewPos = xCurrentScroll - 5; 
                    break; 
 
                // User clicked the right arrow. 
                case SB_LINEDOWN: 
                    xNewPos = xCurrentScroll + 5; 
                    break; 
 
                // User dragged the scroll box. 
                case SB_THUMBPOSITION: 
                    xNewPos = HIWORD(wParam); 
                    break; 
 
                default: 
                    xNewPos = xCurrentScroll; 
            } 
 
            // New position must be between 0 and the screen width. 
            xNewPos = max(0, xNewPos); 
            xNewPos = min(xMaxScroll, xNewPos); 
 
            // If the current position does not change, do not scroll.
            if (xNewPos == xCurrentScroll) 
                break; 
 
            // Set the scroll flag to TRUE. 
            fScroll = TRUE; 
 
            // Determine the amount scrolled (in pixels). 
            xDelta = xNewPos - xCurrentScroll; 
 
            // Reset the current scroll position. 
            xCurrentScroll = xNewPos; 
 
            // Scroll the window. (The system repaints most of the 
            // client area when ScrollWindowEx is called; however, it is 
            // necessary to call UpdateWindow in order to repaint the 
            // rectangle of pixels that were invalidated.) 
            ScrollWindowEx(hwnd, -xDelta, -yDelta, (CONST RECT *) NULL, 
                (CONST RECT *) NULL, (HRGN) NULL, (PRECT) NULL, 
                SW_INVALIDATE); 
            UpdateWindow(hwnd); 
 
            // Reset the scroll bar. 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_POS; 
            si.nPos   = xCurrentScroll; 
            SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
            break; 
        } 
        
        case WM_VSCROLL: 
        { 
            int xDelta = 0; 
            int yDelta;     // yDelta = new_pos - current_pos 
            int yNewPos;    // new position 
 
            switch (LOWORD(wParam)) 
            { 
                // User clicked the scroll bar shaft above the scroll box. 
                case SB_PAGEUP: 
                    yNewPos = yCurrentScroll - 50; 
                    break; 
 
                // User clicked the scroll bar shaft below the scroll box. 
                case SB_PAGEDOWN: 
                    yNewPos = yCurrentScroll + 50; 
                    break; 
 
                // User clicked the top arrow. 
                case SB_LINEUP: 
                    yNewPos = yCurrentScroll - 5; 
                    break; 
 
                // User clicked the bottom arrow. 
                case SB_LINEDOWN: 
                    yNewPos = yCurrentScroll + 5; 
                    break; 
 
                // User dragged the scroll box. 
                case SB_THUMBPOSITION: 
                    yNewPos = HIWORD(wParam); 
                    break; 
 
                default: 
                    yNewPos = yCurrentScroll; 
            } 
 
            // New position must be between 0 and the screen height. 
            yNewPos = max(0, yNewPos); 
            yNewPos = min(yMaxScroll, yNewPos); 
 
            // If the current position does not change, do not scroll.
            if (yNewPos == yCurrentScroll) 
                break; 
 
            // Set the scroll flag to TRUE. 
            fScroll = TRUE; 
 
            // Determine the amount scrolled (in pixels). 
            yDelta = yNewPos - yCurrentScroll; 
 
            // Reset the current scroll position. 
            yCurrentScroll = yNewPos; 
 
            // Scroll the window. (The system repaints most of the 
            // client area when ScrollWindowEx is called; however, it is 
            // necessary to call UpdateWindow in order to repaint the 
            // rectangle of pixels that were invalidated.) 
            ScrollWindowEx(hwnd, -xDelta, -yDelta, (CONST RECT *) NULL, 
                (CONST RECT *) NULL, (HRGN) NULL, (PRECT) NULL, 
                SW_INVALIDATE); 
            UpdateWindow(hwnd); 
 
            // Reset the scroll bar. 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_POS; 
            si.nPos   = yCurrentScroll; 
            SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 

            break; 
        } 

        case WM_RBUTTONDOWN:
        {
            // Get the compatible DC of the client area. 
            hdcWin = GetDC(hwnd); 

            // Fill the client area to remove any existing contents. 
            RECT rect;
            GetClientRect(hwnd, &rect);
            FillRect(hdcWin, &rect, (HBRUSH)(COLOR_WINDOW+1));
 
            // Copy the contents of the current screen 
            // into the compatible DC. 
            BitBlt(hdcScreenCompat, 0, 0, bmp.bmWidth, 
                bmp.bmHeight, hdcScreen, 0, 0, SRCCOPY); 
 
            // Copy the compatible DC to the client area.
            BitBlt(hdcWin, 0, 0, bmp.bmWidth, bmp.bmHeight, 
                hdcScreenCompat, 0, 0, SRCCOPY); 
 
            ReleaseDC(hwnd, hdcWin); 
            fBlt = TRUE; 
            break; 
        }

        case WM_DESTROY :
            PostQuitMessage (0);
            return 0;
    }
    return DefWindowProc (hwnd, uMsg, wParam, lParam);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando barras de rolagem](using-scroll-bars.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 