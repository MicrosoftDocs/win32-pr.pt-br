---
title: Usando entrada de teclado
description: Esta seção aborda as tarefas associadas à entrada do teclado.
ms.assetid: d08e7f12-6595-4234-bfc4-08daad93e4c4
keywords:
- entrada do usuário, entrada de teclado
- capturando entrada do usuário, entrada de teclado
- entrada do teclado
- mensagens de pressionamento de tecla
- mensagens de caracteres
- acento circunflexo, entrada de teclado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1be8753ec6a5f920f09f6e5376b7988a88de0f9a49551492408e84908bb0c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248268"
---
# <a name="using-keyboard-input"></a>Usando entrada de teclado

Uma janela recebe entrada de teclado na forma de mensagens de pressionamento de teclas e de caracteres. O loop de mensagem anexado à janela deve incluir o código para converter as mensagens de pressionamento de tecla nas mensagens de caracteres correspondentes. Se a janela exibir entrada de teclado em sua área de cliente, ela deverá criar e exibir um cursor para indicar a posição em que o próximo caractere será inserido. As seções a seguir descrevem o código envolvido no recebimento, processamento e exibição da entrada do teclado:

-   [Processando mensagens de pressionamento de tecla](#processing-keystroke-messages)
-   [Convertendo mensagens de caracteres](#translating-character-messages)
-   [Processando mensagens de caracteres](#processing-character-messages)
-   [Usando o cursor](#using-the-caret)
-   [Exibindo entrada do teclado](#displaying-keyboard-input)

## <a name="processing-keystroke-messages"></a>Processando mensagens de pressionamento de tecla

O procedimento de janela da janela que tem o foco do teclado recebe mensagens de pressionamento de tecla quando o usuário digita no teclado. As mensagens de pressionamento de tecla são [**WM \_ KEYDOWN**](wm-keydown.md), [**WM \_ KEYUP**](wm-keyup.md), [**WM \_ SYSKEYDOWN**](wm-syskeydown.md)e [**WM \_ SYSKEYUP**](wm-syskeyup.md). Um procedimento de janela típico ignora todas as mensagens de pressionamento de tecla, exceto o **WM \_ KEYDOWN**. O sistema posta a mensagem do **WM \_ KEYDOWN** quando o usuário pressiona uma tecla.

Quando o procedimento de janela recebe a mensagem do [**WM \_ KEYDOWN**](wm-keydown.md) , ele deve examinar o código de chave virtual que acompanha a mensagem para determinar como processar o pressionamento de tecla. O código de chave virtual está no parâmetro *wParam* da mensagem. Normalmente, um aplicativo processa apenas pressionamentos de teclas gerados por chaves que não sejam caracteres, incluindo as teclas de função, as chaves de movimento do cursor e as chaves de finalidade especial, como INS, DEL, HOME e END.

O exemplo a seguir mostra a estrutura de procedimento de janela que um aplicativo típico usa para receber e processar mensagens de pressionamento de tecla.


```
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT: 
                    
                    // Process the LEFT ARROW key. 
                     
                    break; 
 
                case VK_RIGHT: 
                    
                    // Process the RIGHT ARROW key. 
                     
                    break; 
 
                case VK_UP: 
                    
                    // Process the UP ARROW key. 
                     
                    break; 
 
                case VK_DOWN: 
                    
                    // Process the DOWN ARROW key. 
                     
                    break; 
 
                case VK_HOME: 
                    
                    // Process the HOME key. 
                     
                    break; 
 
                case VK_END: 
                    
                    // Process the END key. 
                     
                    break; 
 
                case VK_INSERT: 
                    
                    // Process the INS key. 
                     
                    break; 
 
                case VK_DELETE: 
                    
                    // Process the DEL key. 
                     
                    break; 
 
                case VK_F2: 
                    
                    // Process the F2 key. 
                    
                    break; 
 
                
                // Process other non-character keystrokes. 
                 
                default: 
                    break; 
            } 
```



## <a name="translating-character-messages"></a>Convertendo mensagens de caracteres

Qualquer thread que recebe a entrada de caracteres do usuário deve incluir a função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) em seu loop de mensagem. Essa função examina o código de chave virtual de uma mensagem de pressionamento de tecla e, se o código corresponder a um caractere, colocará uma mensagem de caractere na fila de mensagens. A mensagem de caractere é removida e despachada na próxima iteração do loop de mensagem; o parâmetro *wParam* da mensagem contém o código de caractere.

Em geral, o loop de mensagem de um thread deve usar a função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) para converter todas as mensagens, não apenas as mensagens de chave virtual. Embora **TranslateMessage** não tenha efeito sobre outros tipos de mensagens, ele garante que a entrada do teclado seja traduzida corretamente. O exemplo a seguir mostra como incluir a função **TranslateMessage** em um loop de mensagem de thread típico.


```
MSG msg;
BOOL bRet;

while (( bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0) 
{
    if (bRet == -1);
    {
        // handle the error and possibly exit
    }
    else
    { 
        if (TranslateAccelerator(hwndMain, haccl, &msg) == 0) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



## <a name="processing-character-messages"></a>Processando mensagens de caracteres

Um procedimento de janela recebe uma mensagem de caractere quando a função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) converte um código de chave virtual correspondente a uma chave de caractere. As mensagens de caracteres [**são \_ WM Char**](wm-char.md), [**WM \_ DEADCHAR**](wm-deadchar.md), [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)e [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md). Um procedimento de janela típico ignora todas as mensagens de caracteres, exceto **WM \_ Char**. A função **TranslateMessage** gera uma mensagem do **WM \_ Char** quando o usuário pressiona qualquer uma das seguintes chaves:

-   Qualquer chave de caractere
-   BACKSPACE
-   ENTER (retorno de carro)
-   ESC
-   SHIFT + ENTER (avanço de alimentação)
-   TAB

Quando um procedimento de janela recebe a mensagem do [**WM \_ Char**](wm-char.md) , ele deve examinar o código de caractere que acompanha a mensagem para determinar como processar o caractere. O código de caractere está no parâmetro *wParam* da mensagem.

O exemplo a seguir mostra a estrutura de procedimento de janela que um aplicativo típico usa para receber e processar mensagens de caracteres.


```
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08: 
                    
                    // Process a backspace. 
                     
                    break; 
 
                case 0x0A: 
                    
                    // Process a linefeed. 
                     
                    break; 
 
                case 0x1B: 
                    
                    // Process an escape. 
                    
                    break; 
 
                case 0x09: 
                    
                    // Process a tab. 
                     
                    break; 
 
                case 0x0D: 
                    
                    // Process a carriage return. 
                     
                    break; 
 
                default: 
                    
                    // Process displayable characters. 
                     
                    break; 
            } 
```



## <a name="using-the-caret"></a>Usando o cursor

Uma janela que recebe entrada de teclado normalmente exibe os caracteres que o usuário digita na área do cliente da janela. Uma janela deve usar um cursor para indicar a posição na área do cliente onde o próximo caractere será exibido. A janela também deve criar e exibir o cursor quando receber o foco do teclado e ocultar e destruir o cursor quando ele perder o foco. Uma janela pode executar essas operações no processamento das mensagens do [**WM \_ SETFOCUS**](wm-setfocus.md) e do [**WM \_ KILLFOCUS**](wm-killfocus.md) . Para obter mais informações sobre os Cursors, consulte [Cursors](/windows/desktop/menurc/carets).

## <a name="displaying-keyboard-input"></a>Exibindo entrada do teclado

O exemplo nesta seção mostra como um aplicativo pode receber caracteres do teclado, exibi-los na área do cliente de uma janela e atualizar a posição do cursor com cada caractere digitado. Ele também demonstra como mover o cursor em resposta para a seta para a esquerda, seta para a direita, página inicial e pressionamentos de teclas END e mostra como realçar o texto selecionado em resposta à combinação de teclas SHIFT + seta para a direita.

Durante o processamento da mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) , o procedimento de janela mostrado no exemplo aloca um buffer de 64K para armazenar a entrada do teclado. Ele também recupera as métricas da fonte carregada atualmente, salvando a altura e a largura média dos caracteres na fonte. A altura e a largura são usadas no processamento da mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) para calcular o comprimento da linha e o número máximo de linhas, com base no tamanho da área do cliente.

O procedimento de janela cria e exibe o cursor ao processar a mensagem do [**WM \_ SETFOCUS**](wm-setfocus.md) . Ele oculta e exclui o cursor ao processar a mensagem [**\_ KILLFOCUS do WM**](wm-killfocus.md) .

Ao processar a mensagem do [**WM \_ Char**](wm-char.md) , o procedimento de janela exibe caracteres, armazena-os no buffer de entrada e atualiza a posição do cursor. O procedimento de janela também converte caracteres de tabulação em quatro caracteres de espaço consecutivos. Caracteres de Backspace, avanço de alimentação e escape geram um aviso sonoro, mas não são processados de outra forma.

O procedimento de janela executa os movimentos de cursor esquerdo, direito, final e início ao processar a mensagem [**\_ KEYDOWN do WM**](wm-keydown.md) . Durante o processamento da ação da tecla de seta para a direita, o procedimento de janela verifica o estado da tecla SHIFT e, se estiver inativo, seleciona o caractere à direita do cursor à medida que o cursor é movido.

Observe que o código a seguir é escrito para que possa ser compilado como Unicode ou ANSI. Se o código-fonte definir UNICODE, as cadeias de caracteres serão manipuladas como caractere Unicode; caso contrário, eles serão tratados como caracteres ANSI.


```
#define BUFSIZE 65535 
#define SHIFTED 0x8000 
 
LONG APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                   // handle to device context 
    TEXTMETRIC tm;             // structure for text metrics 
    static DWORD dwCharX;      // average width of characters 
    static DWORD dwCharY;      // height of characters 
    static DWORD dwClientX;    // width of client area 
    static DWORD dwClientY;    // height of client area 
    static DWORD dwLineLen;    // line length 
    static DWORD dwLines;      // text lines in client area 
    static int nCaretPosX = 0; // horizontal position of caret 
    static int nCaretPosY = 0; // vertical position of caret 
    static int nCharWidth = 0; // width of a character 
    static int cch = 0;        // characters in buffer 
    static int nCurChar = 0;   // index of current character 
    static PTCHAR pchInputBuf; // input buffer 
    int i, j;                  // loop counters 
    int cCR = 0;               // count of carriage returns 
    int nCRIndex = 0;          // index of last carriage return 
    int nVirtKey;              // virtual-key code 
    TCHAR szBuf[128];          // temporary buffer 
    TCHAR ch;                  // current character 
    PAINTSTRUCT ps;            // required by BeginPaint 
    RECT rc;                   // output rectangle for DrawText 
    SIZE sz;                   // string dimensions 
    COLORREF crPrevText;       // previous text color 
    COLORREF crPrevBk;         // previous background color
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
            dwCharY = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPTSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
            return 0; 
 
        case WM_SIZE: 
 
            // Save the new width and height of the client area. 
 
            dwClientX = LOWORD(lParam); 
            dwClientY = HIWORD(lParam); 
 
            // Calculate the maximum width of a line and the 
            // maximum number of lines in the client area. 
            
            dwLineLen = dwClientX - dwCharX; 
            dwLines = dwClientY / dwCharY; 
            break; 
 
 
        case WM_SETFOCUS: 
 
            // Create, position, and display the caret when the 
            // window receives the keyboard focus. 
 
            CreateCaret(hwndMain, (HBITMAP) 1, 0, dwCharY); 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            ShowCaret(hwndMain); 
            break; 
 
        case WM_KILLFOCUS: 
 
            // Hide and destroy the caret when the window loses the 
            // keyboard focus. 
 
            HideCaret(hwndMain); 
            DestroyCaret(); 
            break; 
 
        case WM_CHAR:
        // check if current location is close enough to the
        // end of the buffer that a buffer overflow may
        // occur. If so, add null and display contents. 
    if (cch > BUFSIZE-5)
    {
        pchInputBuf[cch] = 0x00;
        SendMessage(hwndMain, WM_PAINT, 0, 0);
    } 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return and position the 
                    // caret at the beginning of the new line.

                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCaretPosY += 1; 
                    break; 
 
                default:    // displayable character 
 
                    ch = (TCHAR) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width and output 
                    // the character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, nCaretPosY * dwCharY, 
                        &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer.
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the position exceeds the maximum, 
                    // insert a carriage return and move the caret 
                    // to the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwLineLen) 
                    { 
                        nCaretPosX = 0;
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCaretPosY; 
                    } 
                    nCurChar = cch; 
                    ShowCaret(hwndMain); 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT:   // LEFT ARROW 
 
                    // The caret can move only to the beginning of 
                    // the current line. 
 
                    if (nCaretPosX > 0) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the left of 
                        // the caret, calculate the character's 
                        // width, then subtract the width from the 
                        // current horizontal position of the caret 
                        // to obtain the new position. 
 
                        ch = pchInputBuf[--nCurChar]; 
                        hdc = GetDC(hwndMain); 
                        GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                        ReleaseDC(hwndMain, hdc); 
                        nCaretPosX = max(nCaretPosX - nCharWidth, 
                            0); 
                        ShowCaret(hwndMain); 
                    } 
                    break; 
 
                case VK_RIGHT:  // RIGHT ARROW 
 
                    // Caret moves to the right or, when a carriage 
                    // return is encountered, to the beginning of 
                    // the next line. 
 
                    if (nCurChar < cch) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the right of 
                        // the caret. If it's a carriage return, 
                        // position the caret at the beginning of 
                        // the next line. 
 
                        ch = pchInputBuf[nCurChar]; 
                        if (ch == 0x0D) 
                        { 
                            nCaretPosX = 0; 
                            nCaretPosY++; 
                        } 
 
                        // If the character isn't a carriage 
                        // return, check to see whether the SHIFT 
                        // key is down. If it is, invert the text 
                        // colors and output the character. 
 
                        else 
                        { 
                            hdc = GetDC(hwndMain); 
                            nVirtKey = GetKeyState(VK_SHIFT); 
                            if (nVirtKey & SHIFTED) 
                            { 
                                crPrevText = SetTextColor(hdc, 
                                    RGB(255, 255, 255)); 
                                crPrevBk = SetBkColor(hdc, 
                                    RGB(0,0,0)); 
                                TextOut(hdc, nCaretPosX, 
                                    nCaretPosY * dwCharY, 
                                    &ch, 1); 
                                SetTextColor(hdc, crPrevText); 
                                SetBkColor(hdc, crPrevBk); 
                            } 
 
                            // Get the width of the character and 
                            // calculate the new horizontal 
                            // position of the caret. 
 
                            GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                            ReleaseDC(hwndMain, hdc); 
                            nCaretPosX = nCaretPosX + nCharWidth; 
                        } 
                        nCurChar++; 
                        ShowCaret(hwndMain); 
                        break; 
                    } 
                    break; 
 
                case VK_UP:     // UP ARROW 
                case VK_DOWN:   // DOWN ARROW 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case VK_HOME:   // HOME 
 
                    // Set the caret's position to the upper left 
                    // corner of the client area. 
 
                    nCaretPosX = nCaretPosY = 0; 
                    nCurChar = 0; 
                    break; 
 
                case VK_END:    // END  
 
                    // Move the caret to the end of the text. 
 
                    for (i=0; i < cch; i++) 
                    { 
                        // Count the carriage returns and save the 
                        // index of the last one. 
 
                        if (pchInputBuf[i] == 0x0D) 
                        { 
                            cCR++; 
                            nCRIndex = i + 1; 
                        } 
                    } 
                    nCaretPosY = cCR; 
 
                    // Copy all text between the last carriage 
                    // return and the end of the keyboard input 
                    // buffer to a temporary buffer. 
 
                    for (i = nCRIndex, j = 0; i < cch; i++, j++) 
                        szBuf[j] = pchInputBuf[i]; 
                    szBuf[j] = TEXT('\0'); 
 
                    // Retrieve the text extent and use it 
                    // to set the horizontal position of the 
                    // caret. 
 
                    hdc = GetDC(hwndMain);
                    hResult = StringCchLength(szBuf, 128, pcch);
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    GetTextExtentPoint32(hdc, szBuf, *pcch, 
                        &sz); 
                    nCaretPosX = sz.cx; 
                    ReleaseDC(hwndMain, hdc); 
                    nCurChar = cch; 
                    break; 
 
                default: 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_PAINT: 
            if (cch == 0)       // nothing in input buffer 
                break; 
 
            hdc = BeginPaint(hwndMain, &ps); 
            HideCaret(hwndMain); 
 
            // Set the clipping rectangle, and then draw the text 
            // into it. 
 
            SetRect(&rc, 0, 0, dwLineLen, dwClientY); 
            DrawText(hdc, pchInputBuf, -1, &rc, DT_LEFT); 
 
            ShowCaret(hwndMain); 
            EndPaint(hwndMain, &ps); 
            break; 
        
        // Process other messages. 
        
        case WM_DESTROY: 
            PostQuitMessage(0); 
 
            // Free the input buffer. 
 
            GlobalFree((HGLOBAL) pchInputBuf); 
            UnregisterHotKey(hwndMain, 0xAAAA); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



 

 