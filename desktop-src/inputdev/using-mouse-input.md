---
title: Usando a entrada do mouse
description: Esta seção aborda as tarefas associadas à entrada do mouse.
ms.assetid: b96d0046-a507-4733-bcf3-fcf757beec7f
keywords:
- entrada do usuário, entrada do mouse
- capturando entrada do usuário, entrada do mouse
- entrada do mouse
- cursores, entrada do mouse
- cursor do mouse
- clique duas vezes em processamento de mensagens
- roda do mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc38105da1fbbe3bee1be9ca280f1f5573dbb41ba4b7b6aa2013d9c600b8ad00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829966"
---
# <a name="using-mouse-input"></a>Usando a entrada do mouse

Esta seção aborda as tarefas associadas à entrada do mouse.

-   [Acompanhando o cursor do mouse](#tracking-the-mouse-cursor)
-   [Desenhando linhas com o mouse](#drawing-lines-with-the-mouse)
-   [Processamento de uma mensagem de clique duplo](#processing-a-double-click-message)
-   [Selecionando uma linha de texto](#selecting-a-line-of-text)
-   [Usando uma roda do mouse em um documento com objetos inseridos](#using-a-mouse-wheel-in-a-document-with-embedded-objects)
-   [Recuperando o número de linhas de rolagem da roda do mouse](#retrieving-the-number-of-mouse-wheel-scroll-lines)

## <a name="tracking-the-mouse-cursor"></a>Acompanhando o cursor do mouse

Os aplicativos geralmente executam tarefas que envolvem o acompanhamento da posição do cursor do mouse. A maioria dos aplicativos de desenho, por exemplo, rastreia a posição do cursor do mouse durante operações de desenho, permitindo que o usuário desenhe na área do cliente de uma janela arrastando o mouse. Os aplicativos de processamento de palavras também acompanham o cursor, permitindo que o usuário selecione uma palavra ou bloco de texto clicando e arrastando o mouse.

O acompanhamento do cursor normalmente envolve o processamento das mensagens [**WM \_ LBUTTONDOWN,**](wm-lbuttondown.md) [**WM \_ MOUSEMOVE**](wm-mousemove.md)e [**WM \_ LBUTTONUP.**](wm-lbuttonup.md) Uma janela determina quando começar a acompanhar o cursor verificando a posição do cursor fornecida no parâmetro *lParam* da mensagem **WM \_ LBUTTONDOWN.** Por exemplo, um aplicativo de processamento de palavras começaria a acompanhar o cursor somente se a mensagem **WM \_ LBUTTONDOWN** ocorresse enquanto o cursor estava em uma linha de texto, mas não se ele tivesse passado do final do documento.

Uma janela rastreia a posição do cursor processando o fluxo de mensagens [**WM \_ MOUSEMOVE**](wm-mousemove.md) postadas na janela conforme o mouse se move. O processamento da **mensagem WM \_ MOUSEMOVE** normalmente envolve uma operação repetitiva de pintura ou desenho na área do cliente. Por exemplo, um aplicativo de desenho pode redesenhar uma linha repetidamente à medida que o mouse se move. Uma janela usa a [**mensagem WM \_ LBUTTONUP**](wm-lbuttonup.md) como um sinal para interromper o acompanhamento do cursor.

Além disso, um aplicativo pode chamar a [**função TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) para que o sistema envie outras mensagens úteis para acompanhar o cursor. O sistema posta a [**mensagem WM \_ MOUSEHOVER**](wm-mousehover.md) quando o cursor passar o mouse sobre a área do cliente por um determinado período de tempo. Ele posta a [**mensagem WM \_ MOUSELEAVE**](wm-mouseleave.md) quando o cursor sai da área do cliente. As [**mensagens WM \_ NCMOUSEHOVER**](wm-ncmousehover.md) e [**WM \_ NCMOUSELEAVE**](wm-ncmouseleave.md) são as mensagens correspondentes para as áreas não dependentes.

## <a name="drawing-lines-with-the-mouse"></a>Desenhando linhas com o mouse

O exemplo nesta seção demonstra como acompanhar o cursor do mouse. Ele contém partes de um procedimento de janela que permite que o usuário desenhe linhas na área do cliente de uma janela arrastando o mouse.

Quando o procedimento de janela recebe uma mensagem [**WM \_ LBUTTONDOWN,**](wm-lbuttondown.md) ele captura o mouse e salva as coordenadas do cursor, usando as coordenadas como o ponto inicial da linha. Ele também usa a [**função ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) para limitar o cursor à área do cliente durante a operação de desenho de linha.

Durante a primeira [**mensagem WM \_ MOUSEMOVE,**](wm-mousemove.md) o procedimento de janela desenha uma linha do ponto inicial para a posição atual do cursor. Durante as **mensagens WM \_ MOUSEMOVE** subsequentes, o procedimento de janela apaga a linha anterior desenhando sobre ela com uma cor de caneta invertida. Em seguida, ele desenha uma nova linha do ponto de partida para a nova posição do cursor.

A [**mensagem WM \_ LBUTTONUP**](wm-lbuttonup.md) sinaliza o final da operação de desenho. O procedimento de janela libera a captura do mouse e libera o mouse da área do cliente.


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                       // handle to device context 
    RECT rcClient;                 // client area rectangle 
    POINT ptClientUL;              // client upper left corner 
    POINT ptClientLR;              // client lower right corner 
    static POINTS ptsBegin;        // beginning point 
    static POINTS ptsEnd;          // new endpoint 
    static POINTS ptsPrevEnd;      // previous endpoint 
    static BOOL fPrevLine = FALSE; // previous line flag 
 
    switch (uMsg) 
    { 
       case WM_LBUTTONDOWN: 
 
            // Capture mouse input. 
 
            SetCapture(hwndMain); 
 
            // Retrieve the screen coordinates of the client area, 
            // and convert them into client coordinates. 
 
            GetClientRect(hwndMain, &rcClient); 
            ptClientUL.x = rcClient.left; 
            ptClientUL.y = rcClient.top; 
 
            // Add one to the right and bottom sides, because the 
            // coordinates retrieved by GetClientRect do not 
            // include the far left and lowermost pixels. 
 
            ptClientLR.x = rcClient.right + 1; 
            ptClientLR.y = rcClient.bottom + 1; 
            ClientToScreen(hwndMain, &ptClientUL); 
            ClientToScreen(hwndMain, &ptClientLR); 
 
            // Copy the client coordinates of the client area 
            // to the rcClient structure. Confine the mouse cursor 
            // to the client area by passing the rcClient structure 
            // to the ClipCursor function. 
 
            SetRect(&rcClient, ptClientUL.x, ptClientUL.y, 
                ptClientLR.x, ptClientLR.y); 
            ClipCursor(&rcClient); 
 
            // Convert the cursor coordinates into a POINTS 
            // structure, which defines the beginning point of the 
            // line drawn during a WM_MOUSEMOVE message. 
 
            ptsBegin = MAKEPOINTS(lParam); 
            return 0; 
 
        case WM_MOUSEMOVE: 
 
            // When moving the mouse, the user must hold down 
            // the left mouse button to draw lines. 
 
            if (wParam & MK_LBUTTON) 
            { 
 
                // Retrieve a device context (DC) for the client area. 
 
                hdc = GetDC(hwndMain); 
 
                // The following function ensures that pixels of 
                // the previously drawn line are set to white and 
                // those of the new line are set to black. 
 
                SetROP2(hdc, R2_NOTXORPEN); 
 
                // If a line was drawn during an earlier WM_MOUSEMOVE 
                // message, draw over it. This erases the line by 
                // setting the color of its pixels to white. 
 
                if (fPrevLine) 
                { 
                    MoveToEx(hdc, ptsBegin.x, ptsBegin.y, 
                        (LPPOINT) NULL); 
                    LineTo(hdc, ptsPrevEnd.x, ptsPrevEnd.y); 
                } 
 
                // Convert the current cursor coordinates to a 
                // POINTS structure, and then draw a new line. 
 
                ptsEnd = MAKEPOINTS(lParam); 
                MoveToEx(hdc, ptsBegin.x, ptsBegin.y, (LPPOINT) NULL); 
                LineTo(hdc, ptsEnd.x, ptsEnd.y); 
 
                // Set the previous line flag, save the ending 
                // point of the new line, and then release the DC. 
 
                fPrevLine = TRUE; 
                ptsPrevEnd = ptsEnd; 
                ReleaseDC(hwndMain, hdc); 
            } 
            break; 
 
        case WM_LBUTTONUP: 
 
            // The user has finished drawing the line. Reset the 
            // previous line flag, release the mouse cursor, and 
            // release the mouse capture. 
 
            fPrevLine = FALSE; 
            ClipCursor(NULL); 
            ReleaseCapture(); 
            return 0; 
 
        case WM_DESTROY: 
            PostQuitMessage(0); 
            break; 
 
        // Process other messages. 
        
```



## <a name="processing-a-double-click-message"></a>Processamento de uma mensagem de clique duplo

Para receber mensagens de clique duplo, uma janela deve pertencer a uma classe de janela que tenha o estilo de classe [**\_ DBLCLKS do CS.**](/windows/desktop/winmsg/about-window-classes) Você definirá esse estilo ao registrar a classe de janela, conforme mostrado no exemplo a seguir.


```
BOOL InitApplication(HINSTANCE hInstance) 
{ 
    WNDCLASS wc; 
 
    wc.style = CS_DBLCLKS | CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hInstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_IBEAM); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName = "MainMenu"; 
    wc.lpszClassName = "MainWClass"; 
 
    return RegisterClass(&wc); 
} 
```



Uma mensagem de clique duplo sempre é precedida por uma mensagem de botão para baixo. Por esse motivo, os aplicativos normalmente usam uma mensagem de clique duplo para estender uma tarefa que começou durante uma mensagem de botão para baixo.

## <a name="selecting-a-line-of-text"></a>Selecionando uma linha de texto

O exemplo nesta seção é retirado de um aplicativo de processamento de palavras simples. Ele inclui código que permite ao usuário definir a posição do aro clicando em qualquer lugar em uma linha de texto e selecionando (realça) uma linha de texto clicando duas vezes em qualquer lugar da linha.


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                     // handle to device context 
    TEXTMETRIC tm;               // font size data 
    int i, j;                    // loop counters 
    int cCR = 0;                 // count of carriage returns 
    char ch;                     // character from input buffer 
    static int nBegLine;         // beginning of selected line 
    static int nCurrentLine = 0; // currently selected line 
    static int nLastLine = 0;    // last text line 
    static int nCaretPosX = 0;   // x-coordinate of caret 
    static int cch = 0;          // number of characters entered 
    static int nCharWidth = 0;   // exact width of a character 
    static char szHilite[128];   // text string to highlight 
    static DWORD dwCharX;        // average width of characters 
    static DWORD dwLineHeight;   // line height 
    static POINTS ptsCursor;     // coordinates of mouse cursor 
    static COLORREF crPrevText;  // previous text color 
    static COLORREF crPrevBk;    // previous background color 
    static PTCHAR pchInputBuf;   // pointer to input buffer 
    static BOOL fTextSelected = FALSE; // text-selection flag 
    size_t * pcch;
    HRESULT hResult;
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Get the metrics of the current font. 
 
            hdc = GetDC(hwndMain); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwndMain, hdc); 
 
            // Save the average character width and height. 
 
            dwCharX = tm.tmAveCharWidth; 
            dwLineHeight = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep( (UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return, and position the 
                    // caret at the beginning of the new line. 
 
                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCurrentLine += 1; 
                    break; 
 
                default:    / displayable character 
 
                    ch = (char) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width, and display the 
                    // character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, 
                        nCurrentLine * dwLineHeight, &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer. 
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the new position exceeds the maximum, 
                    // insert a carriage return and reposition the 
                    // caret at the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwMaxCharX) 
                    { 
                        nCaretPosX = 0; 
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCurrentLine; 
                    } 
 
                    ShowCaret(hwndMain); 
 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            nLastLine = max(nLastLine, nCurrentLine); 
            break; 
 
        // Process other messages. 
 
        case WM_LBUTTONDOWN: 
 
            // If a line of text is currently highlighted, redraw 
            // the text to remove the highlighting. 
 
            if (fTextSelected) 
            { 
                hdc = GetDC(hwndMain); 
                SetTextColor(hdc, crPrevText); 
                SetBkColor(hdc, crPrevBk);
                hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
                if (FAILED(hResult))
                {
                // TODO: write error handler
                } 
                TextOut(hdc, 0, nCurrentLine * dwLineHeight, 
                    szHilite, *pcch); 
                ReleaseDC(hwndMain, hdc); 
                ShowCaret(hwndMain); 
                fTextSelected = FALSE; 
            } 
 
            // Save the current mouse-cursor coordinates. 
 
            ptsCursor = MAKEPOINTS(lParam); 
 
            // Determine which line the cursor is on, and save 
            // the line number. Do not allow line numbers greater 
            // than the number of the last line of text. The 
            // line number is later multiplied by the average height 
            // of the current font. The result is used to set the 
            // y-coordinate of the caret. 
 
            nCurrentLine = min((int)(ptsCursor.y / dwLineHeight), 
                nLastLine); 
 
            // Parse the text input buffer to find the first 
            // character in the selected line of text. Each 
            // line ends with a carriage return, so it is possible 
            // to count the carriage returns to find the selected 
            // line. 
 
            cCR = 0; 
            nBegLine = 0; 
            if (nCurrentLine != 0) 
            { 
                for (i = 0; (i < cch) && 
                        (cCR < nCurrentLine); i++) 
                { 
                    if (pchInputBuf[i] == 0x0D) 
                        ++cCR; 
                } 
                nBegLine = i; 
            } 
 
            // Starting at the beginning of the selected line, 
            // measure  the width of each character, summing the 
            // width with each character measured. Stop when the 
            // sum is greater than the x-coordinate of the cursor. 
            // The sum is used to set the x-coordinate of the caret. 
 
            hdc = GetDC(hwndMain); 
            nCaretPosX = 0; 
            for (i = nBegLine; 
                (pchInputBuf[i] != 0x0D) && (i < cch); i++) 
            { 
                ch = pchInputBuf[i]; 
                GetCharWidth32(hdc, (int) ch, (int) ch, &nCharWidth); 
                if ((nCaretPosX + nCharWidth) > ptsCursor.x) break; 
                else nCaretPosX += nCharWidth; 
            } 
            ReleaseDC(hwndMain, hdc); 
 
            // Set the caret to the user-selected position. 
 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            break; 
 
        case WM_LBUTTONDBLCLK: 
 
            // Copy the selected line of text to a buffer. 
 
            for (i = nBegLine, j = 0; (pchInputBuf[i] != 0x0D) && 
                    (i < cch); i++) 
            {
                szHilite[j++] = pchInputBuf[i]; 
            }
            szHilite[j] = '\0'; 
 
            // Hide the caret, invert the background and foreground 
            // colors, and then redraw the selected line. 
 
            HideCaret(hwndMain); 
            hdc = GetDC(hwndMain); 
            crPrevText = SetTextColor(hdc, RGB(255, 255, 255)); 
            crPrevBk = SetBkColor(hdc, RGB(0, 0, 0));
            hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 0, nCurrentLine * dwLineHeight, szHilite, *pcch); 
            SetTextColor(hdc, crPrevText); 
            SetBkColor(hdc, crPrevBk); 
            ReleaseDC(hwndMain, hdc); 
 
            fTextSelected = TRUE; 
            break; 

            // Process other messages. 

        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="using-a-mouse-wheel-in-a-document-with-embedded-objects"></a>Usando uma roda do mouse em um documento com objetos inseridos

Este exemplo pressupõe um Microsoft Word com vários objetos inseridos:

-   Uma planilha Microsoft Excel dados
-   Um controle de caixa de listagem inserido que rola em resposta à roda
-   Um controle de caixa de texto inserido que não responde à roda

A [mensagem MSH \_ MOUSEWHEEL](about-mouse-input.md) sempre é enviada para a janela principal no Microsoft Word. Isso é verdadeiro mesmo se a planilha inserida estiver ativa. A tabela a seguir explica como a mensagem \_ MSH MOUSEWHEEL é tratada de acordo com o foco.



| O foco está em                | A manipulação é a seguinte                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Documento do Word              | O Word rola a janela do documento.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Planilha Excel inserida | O Word posta a mensagem Excel. Você deve decidir se o aplicativo inserido deve responder à mensagem ou não.                                                                                                                                                                                                                                                                                                                                                            |
| Controle inserido           | É responsabilidade do aplicativo enviar a mensagem para um controle inserido que tem o foco e verificar o código de retorno para ver se o controle o tratou. Se o controle não o tiver controlado, o aplicativo deverá rolar a janela do documento. Por exemplo, se o usuário clicasse em uma caixa de listagem e rolasse a roda, esse controle rolaria em resposta a uma rotação de roda. Se o usuário clicasse em uma caixa de texto e girasse a roda, o documento inteiro rolaria. |



 

Este exemplo a seguir mostra como um aplicativo pode lidar com as mensagens de duas roda.


```
/************************************************
* this code deals with MSH_MOUSEWHEEL
*************************************************/
#include "zmouse.h"

//
// Mouse Wheel rotation stuff, only define if we are
// on a version of the OS that does not support
// WM_MOUSEWHEEL messages.
//
#ifndef WM_MOUSEWHEEL
#define WM_MOUSEWHEEL WM_MOUSELAST+1 
    // Message ID for IntelliMouse wheel
#endif

UINT uMSH_MOUSEWHEEL = 0;   // Value returned from
                            // RegisterWindowMessage()

/**************************************************

INT WINAPI WinMain(
         HINSTANCE hInst, 
         HINSTANCE hPrevInst, 
         LPSTR lpCmdLine, 
         INT nCmdShow)
{
    MSG msg;
    BOOL bRet;

    if (!InitInstance(hInst, nCmdShow))
        return FALSE;

    //
    // The new IntelliMouse uses a Registered message to transmit
    // wheel rotation info. So register for it!
 
    uMSH_MOUSEWHEEL =
     RegisterWindowMessage(MSH_MOUSEWHEEL); 
    if ( !uMSH_MOUSEWHEEL )
    {
        MessageBox(NULL,"
                   RegisterWindowMessag Failed!",
                   "Error",MB_OK);
        return msg.wParam;
    }
    
    while (( bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            if (!TranslateAccelerator(ghwndApp,
                                      ghaccelTable,
                                      &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }

    return msg.wParam;
}

/************************************************
* this code deals with WM_MOUSEWHEEL
*************************************************/
LONG APIENTRY MainWndProc(
    HWND hwnd,
    UINT msg,
    WPARAM wParam,
    LPARAM lParam)
{
    static int nZoom = 0;
    

    switch (msg)
    {
        //
        // Handle Mouse Wheel messages generated
        // by the operating systems that have built-in
        // support for the WM_MOUSEWHEEL message.
        //

        case WM_MOUSEWHEEL:
            ((short) HIWORD(wParam)< 0) ? nZoom-- : nZoom++;

            //
            // Do other wheel stuff...
            //

            break;

        default:
            //
            // uMSH_MOUSEWHEEL is a message registered by
            // the mswheel dll on versions of Windows that
            // do not support the new message in the OS.

            if( msg == uMSH_MOUSEWHEEL )
            {
               ((int)wParam < 0) ? nZoom-- : nZoom++;

                //
                // Do other wheel stuff...
                //
                break;
            }

            return DefWindowProc(hwnd,
                                 msg,
                                 wParam,
                                 lParam);
    }

    return 0L;
}
```



## <a name="retrieving-the-number-of-mouse-wheel-scroll-lines"></a>Recuperando o número de linhas de rolagem da roda do mouse

O código a seguir permite que um aplicativo recupere o número de linhas de rolagem usando a [**função SystemParametersInfo.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)


```
#ifndef SPI_GETWHEELSCROLLLINES
#define SPI_GETWHEELSCROLLLINES   104
#endif

#include "zmouse.h"

/*********************************************************
* FUNCTION: GetNumScrollLines
* Purpose : An OS independent method to retrieve the 
*           number of wheel scroll lines
* Params  : none
* Returns : UINT:  Number of scroll lines where WHEEL_PAGESCROLL 
*           indicates to scroll a page at a time.
*********************************************************/
UINT GetNumScrollLines(void)
{
   HWND hdlMsWheel;
   UINT ucNumLines=3;  // 3 is the default
   OSVERSIONINFO osversion;
   UINT uiMsh_MsgScrollLines;
   

   memset(&osversion, 0, sizeof(osversion));
   osversion.dwOSVersionInfoSize =sizeof(osversion);
   GetVersionEx(&osversion);

   if ((osversion.dwPlatformId == VER_PLATFORM_WIN32_WINDOWS) ||
       ( (osversion.dwPlatformId == VER_PLATFORM_WIN32_NT) && 
         (osversion.dwMajorVersion < 4) )   )
   {
        hdlMsWheel = FindWindow(MSH_WHEELMODULE_CLASS, 
                                MSH_WHEELMODULE_TITLE);
        if (hdlMsWheel)
        {
           uiMsh_MsgScrollLines = RegisterWindowMessage
                                     (MSH_SCROLL_LINES);
           if (uiMsh_MsgScrollLines)
                ucNumLines = (int)SendMessage(hdlMsWheel,
                                    uiMsh_MsgScrollLines, 
                                                       0, 
                                                       0);
        }
   }
   else if ( (osversion.dwPlatformId ==
                         VER_PLATFORM_WIN32_NT) &&
             (osversion.dwMajorVersion >= 4) )
   {
      SystemParametersInfo(SPI_GETWHEELSCROLLLINES,
                                          0,
                                    &ucNumLines, 0);
   }
   return(ucNumLines);
}
```



 

 