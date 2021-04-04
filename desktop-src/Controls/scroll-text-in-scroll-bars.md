---
title: Como rolar o texto
description: Esta seção descreve as alterações que você pode fazer no procedimento de janela principal de um aplicativo para permitir que um usuário Role o texto.
ms.assetid: ACB4FF34-38EF-4F3D-9395-D48D58A72C0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ef9a2eea9490beac7b6ff5048b70de61eb635f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103823994"
---
# <a name="how-to-scroll-text"></a>Como rolar o texto

Esta seção descreve as alterações que você pode fazer no procedimento de janela principal de um aplicativo para permitir que um usuário Role o texto. O exemplo nesta seção cria e exibe uma matriz de cadeias de caracteres de texto e processa mensagens de barra de rolagem do [**WM \_ HSCROLL**](wm-hscroll.md) e do [**WM \_ VSCROLL**](wm-vscroll.md) para que o usuário possa rolar o texto vertical e horizontalmente.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="processing-the-wm_create-message"></a>Processando a \_ mensagem de criação do WM

As unidades de rolagem normalmente são definidas durante o processamento da mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) . É conveniente basear as unidades de rolagem nas dimensões da fonte associada ao contexto do dispositivo (DC) da janela. Para recuperar as dimensões de fonte de um controlador de domínio específico, use a função [**GetTextMetrics**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) .

No exemplo nesta seção, uma unidade de rolagem vertical é equivalente à altura de uma célula de caractere, além de uma entrelinha externa. Uma unidade de rolagem horizontal é equivalente à largura média de uma célula de caractere. As posições de rolagem horizontal, portanto, não correspondem aos caracteres reais, a menos que a fonte da tela tenha largura fixa.

### <a name="processing-the-wm_size-message"></a>Processando a \_ mensagem de tamanho do WM

Ao processar a mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) , é conveniente ajustar o intervalo de rolagem e a posição de rolagem para refletir as dimensões da área do cliente, bem como o número de linhas de texto que serão exibidas.

A função [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) define os valores mínimo e máximo da posição, o tamanho da página e a posição da rolagem para uma barra de rolagem.

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a>Processando as \_ mensagens do WM HSCROLL e do WM \_ VSCROLL

A barra de rolagem envia mensagens do [**WM \_ HSCROLL**](wm-hscroll.md) e do [**WM \_ VSCROLL**](wm-vscroll.md) para o procedimento de janela sempre que o usuário clica na barra de rolagem ou arrasta a caixa de rolagem. As palavras de ordem inferior do **WM \_ VSCROLL** e do **WM \_ HSCROLL** contêm um código de solicitação que indica a direção e a magnitude da ação de rolagem.

Quando as mensagens do [**WM \_ HSCROLL**](wm-hscroll.md) e do [**WM \_ VSCROLL**](wm-vscroll.md) são processadas, o código de solicitação da barra de rolagem é examinado e o incremento de rolagem é calculado. Depois que o incremento é aplicado à posição de rolagem atual, a janela é rolada para a nova posição usando a função [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) e a posição da caixa de rolagem é ajustada usando a função [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) .

Depois que uma janela é rolada, parte de sua área do cliente é inválida. Para garantir que a região inválida seja atualizada, a função [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) é usada para gerar uma mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) .

### <a name="processing-the-wm_paint-message"></a>Processando a \_ mensagem de pintura do WM

Ao processar a mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) , é conveniente desenhar as linhas de texto que você deseja que apareçam na parte inválida da janela. O exemplo a seguir usa a posição de rolagem atual e as dimensões da região inválida para determinar o intervalo de linhas dentro da região inválida para exibi-las.

## <a name="example-of-scrolling-text"></a>Exemplo de texto de rolagem

O exemplo a seguir é um procedimento de janela para uma janela que exibe texto em sua área de cliente. O exemplo demonstra como rolar o texto em resposta à entrada das barras de rolagem horizontal e vertical.


```C++
#include "strsafe.h"

LRESULT CALLBACK MyTextWindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
HDC hdc; 
PAINTSTRUCT ps; 
TEXTMETRIC tm; 
SCROLLINFO si; 
 
// These variables are required to display text. 
static int xClient;     // width of client area 
static int yClient;     // height of client area 
static int xClientMax;  // maximum width of client area 
 
static int xChar;       // horizontal scrolling unit 
static int yChar;       // vertical scrolling unit 
static int xUpper;      // average width of uppercase letters 
 
static int xPos;        // current horizontal scrolling position 
static int yPos;        // current vertical scrolling position 
 
int i;                  // loop counter 
int x, y;               // horizontal and vertical coordinates
 
int FirstLine;          // first line in the invalidated area 
int LastLine;           // last line in the invalidated area 
HRESULT hr;
size_t abcLength;        // length of an abc[] item 

// Create an array of lines to display. 
#define LINES 28 
static TCHAR *abc[] = { 
       TEXT("anteater"),  TEXT("bear"),      TEXT("cougar"), 
       TEXT("dingo"),     TEXT("elephant"),  TEXT("falcon"), 
       TEXT("gazelle"),   TEXT("hyena"),     TEXT("iguana"), 
       TEXT("jackal"),    TEXT("kangaroo"),  TEXT("llama"), 
       TEXT("moose"),     TEXT("newt"),      TEXT("octopus"), 
       TEXT("penguin"),   TEXT("quail"),     TEXT("rat"), 
       TEXT("squid"),     TEXT("tortoise"),  TEXT("urus"), 
       TEXT("vole"),      TEXT("walrus"),    TEXT("xylophone"), 
       TEXT("yak"),       TEXT("zebra"),
       TEXT("This line contains words, but no character. Go figure."),
       TEXT("")
     }; 
 
switch (uMsg) 
{ 
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hwnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hwnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0; 
 
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
        return 0; 
    case WM_HSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;

        // Save the position for comparison later on.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;
        switch (LOWORD (wParam))
        {
        // User clicked the left arrow.
        case SB_LINELEFT: 
            si.nPos -= 1;
            break;
              
        // User clicked the right arrow.
        case SB_LINERIGHT: 
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft left of the scroll box.
        case SB_PAGELEFT:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft right of the scroll box.
        case SB_PAGERIGHT:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK: 
            si.nPos = si.nTrackPos;
            break;
              
        default :
            break;
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_HORZ, &si, TRUE);
        GetScrollInfo (hwnd, SB_HORZ, &si);
         
        // If the position has changed, scroll the window.
        if (si.nPos != xPos)
        {
            ScrollWindow(hwnd, xChar * (xPos - si.nPos), 0, NULL, NULL);
        }

        return 0;
         
    case WM_VSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hwnd, SB_VERT, &si);

        // Save the position for comparison later on.
        yPos = si.nPos;
        switch (LOWORD (wParam))
        {

        // User clicked the HOME keyboard key.
        case SB_TOP:
            si.nPos = si.nMin;
            break;
              
        // User clicked the END keyboard key.
        case SB_BOTTOM:
            si.nPos = si.nMax;
            break;
              
        // User clicked the top arrow.
        case SB_LINEUP:
            si.nPos -= 1;
            break;
              
        // User clicked the bottom arrow.
        case SB_LINEDOWN:
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft above the scroll box.
        case SB_PAGEUP:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft below the scroll box.
        case SB_PAGEDOWN:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK:
            si.nPos = si.nTrackPos;
            break;
              
        default:
            break; 
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_VERT, &si, TRUE);
        GetScrollInfo (hwnd, SB_VERT, &si);

        // If the position has changed, scroll window and update it.
        if (si.nPos != yPos)
        {                    
            ScrollWindow(hwnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
            UpdateWindow (hwnd);
        }

        return 0;
         
    case WM_PAINT :
        // Prepare the window for painting.
        hdc = BeginPaint (hwnd, &ps);

        // Get vertical scroll bar position.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_POS;
        GetScrollInfo (hwnd, SB_VERT, &si);
        yPos = si.nPos;

        // Get horizontal scroll bar position.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;

        // Find painting limits.
        FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
        LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
        for (i = FirstLine; i <= LastLine; i++)
        {
            x = xChar * (1 - xPos);
            y = yChar * (i - yPos);
              
            // Note that "55" in the following depends on the 
            // maximum size of an abc[] item. Also, you must include
            // strsafe.h to use the StringCchLength function.
            hr = StringCchLength(abc[i], 55, &abcLength);
            if ((FAILED(hr))|(abcLength == NULL))
            {
                //
                // TODO: write error handler
                //
            }

            // Write a line of text to the client area.
            TextOut(hdc, x, y, abc[i], abcLength); 
        }

        // Indicate that painting is finished.
        EndPaint (hwnd, &ps);
        return 0;
         
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

 

 