---
title: Usando pontos de cuidado
description: Esta seção fornece exemplos de código que mostram como executar tarefas relacionadas a carets.
ms.assetid: 82b0a84c-49a9-4d9d-b4c8-7c4511d863eb
keywords:
- recursos, pontos de cuidado
- carets, criando
- carets, exibindo
- carets, destruidor
- carets, ocultando
- carets, tempos de piscar
- linhas piscando
- blocos piscando
- bitmaps piscando
- criando pontos de cuidado
- exibindo a caretas
- ocultando a caretas
- destruir os pontos de cuidado
- tempos de piscar
- entrada do usuário, entrada do teclado
- capturando entrada do usuário, entrada de teclado
- entrada do teclado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c930931df8ce401fbed8cc9af16db3cb52de08ebe9cf539109b426497318d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472642"
---
# <a name="using-carets"></a>Usando pontos de cuidado

Esta seção tem exemplos de código para as seguintes tarefas:

-   [Criando e exibindo um a caret](#creating-and-displaying-a-caret)
-   [Ocultando um caret](#hiding-a-caret)
-   [Destruir um caret](#destroying-a-caret)
-   [Ajustando a hora de piscar](#adjusting-the-blink-time)
-   [Processamento da entrada do teclado](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a>Criando e exibindo um a caret

Ao receber o foco do teclado, a janela deve criar e exibir o a tecla caret. Use a [**função CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) para criar um aro na janela determinada. Em seguida, você [**pode chamar SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) para definir a posição atual do aro e [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) para tornar o sinal de aro visível.

O sistema envia a [**mensagem WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) para a janela que recebe o foco do teclado; portanto, um aplicativo deve criar e exibir o acento de acento ao processar essa mensagem.


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



Para criar um acento com base em um bitmap, você deve especificar um alça de bitmap ao usar [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret). Você pode usar um aplicativo gráfico para criar o bitmap e um compilador de recursos para adicionar o bitmap aos recursos do aplicativo. Em seguida, seu aplicativo pode usar [**a função LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) para carregar o alça de bitmap. Por exemplo, você pode substituir a **linha CreateCaret** no exemplo anterior pelas linhas a seguir para criar um bitmap caret.


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



Como alternativa, você pode usar a [**função CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) ou [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) para recuperar o handle do bitmap de adição. Para obter mais informações sobre bitmaps, consulte [Bitmaps](/windows/desktop/gdi/bitmaps).

Se o aplicativo especificar um alça de bitmap, [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ignorará os parâmetros de largura e altura. O bitmap define o tamanho do caret.

## <a name="hiding-a-caret"></a>Ocultando um caret

Sempre que o aplicativo redesenhar uma tela durante o processamento de uma mensagem diferente de [**WM \_ PAINT,**](/windows/desktop/gdi/wm-paint)ele deverá tornar o aro invisível usando a [**função HideCaret.**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) Quando o aplicativo terminar de desenhar, replay o aro usando a [**função ShowCaret.**](/windows/desktop/api/Winuser/nf-winuser-showcaret) Se seu aplicativo processa **a mensagem WM \_ PAINT,** não é necessário ocultar e repetir o aparato, pois essa função faz isso automaticamente.

O exemplo de código a seguir mostra como fazer com que seu aplicativo o oculta enquanto desenha um caractere na tela e durante o processamento da mensagem [**WM \_ CHAR.**](/windows/desktop/inputdev/wm-char)


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



Se o aplicativo chamar a [**função HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) várias vezes sem chamar [**ShowCaret,**](/windows/desktop/api/Winuser/nf-winuser-showcaret)o aro não será exibido até que o aplicativo também chamar **ShowCaret** o mesmo número de vezes.

## <a name="destroying-a-caret"></a>Destruir um caret

Quando uma janela perde o foco do teclado, o sistema envia a [**mensagem WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) para a janela. Seu aplicativo deve destruir o aro ao processar essa mensagem usando a [**função DestroyCaret.**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) O código a seguir mostra como destruir um a careta em uma janela que não tem mais o foco do teclado.


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a>Ajustando a hora de piscar

No Windows de 16 bits, um aplicativo baseado em Windows pode chamar a função [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) para salvar a hora de piscar atual e, em seguida, chamar a função [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) para ajustar o tempo de piscar durante o processamento da mensagem [**WM \_ SETFOCUS.**](/windows/desktop/inputdev/wm-setfocus) O aplicativo restauraria o tempo de piscar salvo para o uso de outros aplicativos chamando **SetCaretBlinkTime** durante o processamento da mensagem [**WM \_ KILLFOCUS.**](/windows/desktop/inputdev/wm-killfocus) No entanto, essa técnica não funciona em ambientes multithread. Especificamente, a desativação de um aplicativo não é sincronizada com a ativação de outro aplicativo, para que, se um aplicativo trava, outro aplicativo ainda possa ser ativado.

Os aplicativos devem respeitar o tempo de piscar escolhido pelo usuário. A [**função SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) só deve ser chamada por um aplicativo que permite ao usuário definir a hora de piscar.

## <a name="processing-keyboard-input"></a>Processamento da entrada do teclado

O exemplo a seguir demonstra como usar um a caret em um editor de texto simples. O exemplo atualiza a posição do cursor à medida que o usuário digita caracteres imprimíveis e usa várias chaves para mover-se pela área do cliente.


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



 

 