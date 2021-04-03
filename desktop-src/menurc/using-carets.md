---
title: Usando os Cursors
description: Esta seção fornece exemplos de código que mostram como executar tarefas relacionadas a interpolações.
ms.assetid: 82b0a84c-49a9-4d9d-b4c8-7c4511d863eb
keywords:
- recursos, Cursors
- Cursors, criando
- Cursors, exibindo
- Cursors, destruindo
- acento circunflexo, ocultando
- interpolações, tempos de intermitência
- linhas piscando
- blocos piscando
- bitmaps piscando
- Criando acento circunflexo
- exibindo acento circunflexo
- ocultando acento circunflexo
- destruindo os interpoladores
- horários de intermitência
- entrada do usuário, entrada de teclado
- capturando entrada do usuário, entrada de teclado
- entrada do teclado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6450a3169588b3072d1fee271f4890a7cdeafd2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007440"
---
# <a name="using-carets"></a>Usando os Cursors

Esta seção tem exemplos de código para as seguintes tarefas:

-   [Criando e exibindo um cursor](#creating-and-displaying-a-caret)
-   [Ocultando um cursor](#hiding-a-caret)
-   [Destruindo um cursor](#destroying-a-caret)
-   [Ajustando o tempo de intermitência](#adjusting-the-blink-time)
-   [Processando entrada de teclado](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a>Criando e exibindo um cursor

Após o recebimento do foco do teclado, a janela deve criar e exibir o cursor. Use a função [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) para criar um cursor na janela especificada. Em seguida, você pode chamar [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) para definir a posição atual do cursor e o [**cuidado**](/windows/desktop/api/Winuser/nf-winuser-showcaret) para tornar o cursor visível.

O sistema envia a mensagem do [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) para a janela que recebe o foco do teclado; portanto, um aplicativo deve criar e exibir o cursor durante o processamento dessa mensagem.


```
HWND hwnd,       // window handle 
int x;           // horizontal coordinate of cursor 
int y;           // vertical coordinate of cursor 
int nWidth;      // width of cursor 
int nHeight;     // height of cursor 
char *lpszChar;  // pointer to character 
 
    case WM_SETFOCUS: 
 
    // Create a solid black caret. 
        CreateCaret(hwnd, (HBITMAP) NULL, nWidth, nHeight); 
 
    // Adjust the caret position, in client coordinates. 
        SetCaretPos(x, y); 
 
    // Display the caret. 
        ShowCaret(hwnd); 
 
        break; 
```



Para criar um cursor baseado em um bitmap, você deve especificar um identificador de bitmap ao usar o [**Createcarent**](/windows/desktop/api/Winuser/nf-winuser-createcaret). Você pode usar um aplicativo de gráficos para criar o bitmap e um compilador de recurso para adicionar o bitmap aos recursos do aplicativo. Em seguida, seu aplicativo pode usar a função [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) para carregar o identificador de bitmap. Por exemplo, você pode substituir a linha **Createcarent** no exemplo anterior pelas linhas a seguir para criar um cursor de bitmap.


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



Como alternativa, você pode usar a função [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) ou [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) para recuperar o identificador do bitmap de cursor. Para obter mais informações sobre bitmaps, consulte [bitmaps](/windows/desktop/gdi/bitmaps).

Se o seu aplicativo especificar um identificador de bitmap, o [**Createcareout**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ignorará os parâmetros de largura e altura. O bitmap define o tamanho do cursor.

## <a name="hiding-a-caret"></a>Ocultando um cursor

Sempre que o aplicativo redesenha uma tela durante o processamento de uma mensagem diferente do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint), ele deve tornar o cursor invisível usando a função [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) . Quando seu aplicativo terminar de desenhar, reexiba o cursor usando a função de [**Iscaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) . Se seu aplicativo processa a mensagem do **WM \_ Paint** , não é necessário ocultar e reexibir o cursor, pois essa função faz isso automaticamente.

O exemplo de código a seguir mostra como fazer com que seu aplicativo oculte o cursor enquanto desenha um caractere na tela e durante o processamento da mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) .


```
HWND hwnd,   // window handle 
HDC hdc;     // device context 
 
    case WM_CHAR: 
        switch (wParam) 
        { 
            case 0x08: 
             
             // Process a backspace. 
             
                break; 
 
            case 0x09: 
             
             // Process a tab.  
             
                break; 
 
            case 0x0D: 
             
             // Process a carriage return. 
             
                break; 
 
            case 0x1B: 
             
             // Process an escape. 
             
                break; 
 
            case 0x0A: 
             
             // Process a linefeed. 
             
                break; 
 
            default: 
                // Hide the caret. 
                HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                hdc = GetDC(hwnd); 
                SelectObject(hdc, 
                    GetStockObject(SYSTEM_FIXED_FONT)); 
 
                TextOut(hdc, x, y, lpszChar, 1); 
 
                ReleaseDC(hwnd, hdc); 
 
                // Display the caret. 
 
                ShowCaret(hwnd); 
 
        } 
```



Se seu aplicativo chamar a função [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) várias vezes sem chamar o [**cuidado**](/windows/desktop/api/Winuser/nf-winuser-showcaret), o cursor não será exibido até que o aplicativo **também chame o** mesmo número de vezes.

## <a name="destroying-a-caret"></a>Destruindo um cursor

Quando uma janela perde o foco do teclado, o sistema envia a mensagem do [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) para a janela. Seu aplicativo deve destruir o cursor durante o processamento dessa mensagem usando a função [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) . O código a seguir mostra como destruir um cursor em uma janela que não tem mais o foco do teclado.


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a>Ajustando o tempo de intermitência

No Windows de 16 bits, um aplicativo baseado no Windows poderia chamar a função [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) para salvar o tempo de intermitência atual e, em seguida, chamar a função [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) para ajustar o tempo de intermitência durante o processamento da mensagem do [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) . O aplicativo restauraria o tempo de intermitência salvo para o uso de outros aplicativos chamando **SetCaretBlinkTime** durante o processamento da mensagem do [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) . No entanto, essa técnica não funciona em ambientes multi-threaded. Especificamente, a desativação de um aplicativo não é sincronizada com a ativação de outro aplicativo, de modo que, se um aplicativo parar, outro aplicativo ainda poderá ser ativado.

Os aplicativos devem respeitar o tempo de intermitência escolhido pelo usuário. A função [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) só deve ser chamada por um aplicativo que permita ao usuário definir o tempo de intermitência.

## <a name="processing-keyboard-input"></a>Processando entrada de teclado

O exemplo a seguir demonstra como usar um cursor em um editor de texto simples. O exemplo atualiza a posição do cursor à medida que o usuário digita caracteres imprimíveis e usa várias chaves para percorrer a área do cliente.


```
#define TEXTMATRIX(x, y) *(pTextMatrix + (y * nWindowCharsX) + x) 
// Global variables.
HINSTANCE hinst;                  // current instance 
HBITMAP hCaret;                   // caret bitmap 
HDC hdc;                          // device context  
PAINTSTRUCT ps;                   // client area paint info 
static char *pTextMatrix = NULL;  // points to text matrix 
static int  nCharX,               // width of char. in logical units 
            nCharY,               // height of char. in logical units 
            nWindowX,             // width of client area 
            nWindowY,             // height of client area 
            nWindowCharsX,        // width of client area 
            nWindowCharsY,        // height of client area 
            nCaretPosX,           // x-position of caret 
            nCaretPosY;           // y-position of caret 
static UINT uOldBlink;            // previous blink rate 
int x, y;                         // coordinates for text matrix 
TEXTMETRIC tm;                    // font information 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,            // window handle 
    UINT message,         // type of message 
    UINT wParam,          // additional information 
    LONG lParam)          // additional information 
{ 
 
    switch (message) 
    { 
        case WM_CREATE: 
        // Select a fixed-width system font, and get its text metrics.
 
            hdc = GetDC(hwnd); 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwnd, hdc); 
 
        // Save the avg. width and height of characters. 
 
            nCharX = tm.tmAveCharWidth; 
            nCharY = tm.tmHeight; 
 
            return 0; 
 
        case WM_SIZE: 
        // Determine the width of the client area, in pixels 
        // and in number of characters. 
 
            nWindowX = LOWORD(lParam); 
            nWindowCharsX = max(1, nWindowX/nCharX); 
 
            // Determine the height of the client area, in 
            // pixels and in number of characters. 
 
            nWindowY = HIWORD(lParam); 
            nWindowCharsY = max(1, nWindowY/nCharY); 
 
            // Clear the buffer that holds the text input. 
 
            if (pTextMatrix != NULL) 
                free(pTextMatrix); 
 
            // If there is enough memory, allocate space for the 
            // text input buffer. 
 
            pTextMatrix = malloc(nWindowCharsX * nWindowCharsY); 
 
            if (pTextMatrix == NULL) 
                ErrorHandler("Not enough memory."); 
            else 
                for (y = 0; y < nWindowCharsY; y++) 
                    for (x = 0; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, y) = ' '; 
 
            // Move the caret to the origin. 
 
            SetCaretPos(0, 0); 
 
            return 0; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_HOME:       // Home 
                    nCaretPosX = 0; 
                    break; 
 
                case VK_END:        // End 
                    nCaretPosX = nWindowCharsX - 1; 
                    break; 
 
                case VK_PRIOR:      // Page Up 
                    nCaretPosY = 0; 
                    break; 
 
                case VK_NEXT:       // Page Down 
                    nCaretPosY = nWindowCharsY -1; 
                    break; 
 
                case VK_LEFT:       // Left arrow 
                    nCaretPosX = max(nCaretPosX - 1, 0); 
                    break; 
 
                case VK_RIGHT:      // Right arrow 
                    nCaretPosX = min(nCaretPosX + 1, 
                        nWindowCharsX - 1); 
                    break; 
 
                case VK_UP:         // Up arrow 
                    nCaretPosY = max(nCaretPosY - 1, 0); 
                    break; 
 
                case VK_DOWN:       // Down arrow 
                    nCaretPosY = min(nCaretPosY + 1, 
                        nWindowCharsY - 1); 
                    break; 
 
                case VK_DELETE:     // Delete 
 
                // Move all the characters that followed the 
                // deleted character (on the same line) one 
                // space back (to the left) in the matrix. 
 
                    for (x = nCaretPosX; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, nCaretPosY) = 
                            TEXTMATRIX(x + 1, nCaretPosY); 
 
                    // Replace the last character on the 
                    // line with a space. 
 
                    TEXTMATRIX(nWindowCharsX - 1, 
                        nCaretPosY) = ' '; 
 
                    // The application will draw outside the 
                    // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                    // Redraw the line, adjusted for the 
                    // deleted character. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 
                        nWindowCharsX - nCaretPosX); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // virtual-key processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:          // Backspace 
                // Move the caret back one space, and then 
                // process this like the DEL key. 
 
                    if (nCaretPosX > 0) 
                    { 
                        nCaretPosX--; 
                        SendMessage(hwnd, WM_KEYDOWN, 
                            VK_DELETE, 1L); 
                    } 
                    break; 
 
                case 0x09:          // Tab 
                // Tab stops exist every four spaces, so add 
                // spaces until the user hits the next tab. 
 
                    do 
                    { 
                        SendMessage(hwnd, WM_CHAR, ' ', 1L); 
                    } while (nCaretPosX % 4 != 0); 
                    break; 
 
                case 0x0D:          // Carriage return 
                // Go to the beginning of the next line. 
                // The bottom line wraps around to the top. 
 
                    nCaretPosX = 0; 
 
                    if (++nCaretPosY == nWindowCharsY) 
                        nCaretPosY = 0; 
                    break; 
 
                case 0x1B:        // Escape 
                case 0x0A:        // Linefeed 
                    MessageBeep((UINT) -1); 
                    break; 
 
                default: 
                // Add the character to the text buffer. 
 
                    TEXTMATRIX(nCaretPosX, nCaretPosY) = 
                        (char) wParam; 
 
                // The application will draw outside the 
                // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 1); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    // Prepare to wrap around if you reached the 
                    // end of the line. 
 
                    if (++nCaretPosX == nWindowCharsX) 
                    { 
                        nCaretPosX = 0; 
                        if (++nCaretPosY == nWindowCharsY) 
                            nCaretPosY = 0; 
                    } 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // character processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_PAINT: 
        // Draw all the characters in the buffer, line by line. 
 
            hdc = BeginPaint(hwnd, &ps); 
 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
 
            for (y = 0; y < nWindowCharsY; y++) 
                TextOut(hdc, 0, y * nCharY, &TEXTMATRIX(0, y), 
                    nWindowCharsX); 
 
            EndPaint(hwnd, &ps); 
 
        case WM_SETFOCUS: 
        // The window has the input focus. Load the 
        // application-defined caret resource. 
 
            hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
            // Create the caret. 
 
            CreateCaret(hwnd, hCaret, 0, 0); 
 
            // Adjust the caret position. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            // Display the caret. 
 
            ShowCaret(hwnd); 
 
            break; 
 
        case WM_KILLFOCUS: 
        // The window is losing the input focus, 
        // so destroy the caret. 
 
            DestroyCaret(); 
 
            break; 
 
        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
    } 
 
    return NULL; 
} 
```



 

 