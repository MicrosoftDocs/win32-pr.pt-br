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
# <a name="using-carets"></a><span data-ttu-id="c2e16-120">Usando os Cursors</span><span class="sxs-lookup"><span data-stu-id="c2e16-120">Using Carets</span></span>

<span data-ttu-id="c2e16-121">Esta seção tem exemplos de código para as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="c2e16-121">This section has code samples for the following tasks:</span></span>

-   [<span data-ttu-id="c2e16-122">Criando e exibindo um cursor</span><span class="sxs-lookup"><span data-stu-id="c2e16-122">Creating and Displaying a Caret</span></span>](#creating-and-displaying-a-caret)
-   [<span data-ttu-id="c2e16-123">Ocultando um cursor</span><span class="sxs-lookup"><span data-stu-id="c2e16-123">Hiding a Caret</span></span>](#hiding-a-caret)
-   [<span data-ttu-id="c2e16-124">Destruindo um cursor</span><span class="sxs-lookup"><span data-stu-id="c2e16-124">Destroying a Caret</span></span>](#destroying-a-caret)
-   [<span data-ttu-id="c2e16-125">Ajustando o tempo de intermitência</span><span class="sxs-lookup"><span data-stu-id="c2e16-125">Adjusting the Blink Time</span></span>](#adjusting-the-blink-time)
-   [<span data-ttu-id="c2e16-126">Processando entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="c2e16-126">Processing Keyboard Input</span></span>](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a><span data-ttu-id="c2e16-127">Criando e exibindo um cursor</span><span class="sxs-lookup"><span data-stu-id="c2e16-127">Creating and Displaying a Caret</span></span>

<span data-ttu-id="c2e16-128">Após o recebimento do foco do teclado, a janela deve criar e exibir o cursor.</span><span class="sxs-lookup"><span data-stu-id="c2e16-128">Upon receiving the keyboard focus, the window should create and display the caret.</span></span> <span data-ttu-id="c2e16-129">Use a função [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) para criar um cursor na janela especificada.</span><span class="sxs-lookup"><span data-stu-id="c2e16-129">Use the [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) function to create a caret in the given window.</span></span> <span data-ttu-id="c2e16-130">Em seguida, você pode chamar [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) para definir a posição atual do cursor e o [**cuidado**](/windows/desktop/api/Winuser/nf-winuser-showcaret) para tornar o cursor visível.</span><span class="sxs-lookup"><span data-stu-id="c2e16-130">You can then call [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) to set the current position of the caret and [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) to make the caret visible.</span></span>

<span data-ttu-id="c2e16-131">O sistema envia a mensagem do [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) para a janela que recebe o foco do teclado; portanto, um aplicativo deve criar e exibir o cursor durante o processamento dessa mensagem.</span><span class="sxs-lookup"><span data-stu-id="c2e16-131">The system sends the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message to the window receiving keyboard focus; therefore, an application should create and display the caret while processing this message.</span></span>


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



<span data-ttu-id="c2e16-132">Para criar um cursor baseado em um bitmap, você deve especificar um identificador de bitmap ao usar o [**Createcarent**](/windows/desktop/api/Winuser/nf-winuser-createcaret).</span><span class="sxs-lookup"><span data-stu-id="c2e16-132">To create a caret based on a bitmap, you must specify a bitmap handle when using [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret).</span></span> <span data-ttu-id="c2e16-133">Você pode usar um aplicativo de gráficos para criar o bitmap e um compilador de recurso para adicionar o bitmap aos recursos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2e16-133">You can use a graphics application to create the bitmap and a resource compiler to add the bitmap to your application's resources.</span></span> <span data-ttu-id="c2e16-134">Em seguida, seu aplicativo pode usar a função [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) para carregar o identificador de bitmap.</span><span class="sxs-lookup"><span data-stu-id="c2e16-134">Your application can then use the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function to load the bitmap handle.</span></span> <span data-ttu-id="c2e16-135">Por exemplo, você pode substituir a linha **Createcarent** no exemplo anterior pelas linhas a seguir para criar um cursor de bitmap.</span><span class="sxs-lookup"><span data-stu-id="c2e16-135">For example, you could replace the **CreateCaret** line in the preceding example with the following lines to create a bitmap caret.</span></span>


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



<span data-ttu-id="c2e16-136">Como alternativa, você pode usar a função [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) ou [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) para recuperar o identificador do bitmap de cursor.</span><span class="sxs-lookup"><span data-stu-id="c2e16-136">Alternatively, you can use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) or [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) function to retrieve the handle of the caret bitmap.</span></span> <span data-ttu-id="c2e16-137">Para obter mais informações sobre bitmaps, consulte [bitmaps](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="c2e16-137">For more information about bitmaps, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

<span data-ttu-id="c2e16-138">Se o seu aplicativo especificar um identificador de bitmap, o [**Createcareout**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ignorará os parâmetros de largura e altura.</span><span class="sxs-lookup"><span data-stu-id="c2e16-138">If your application specifies a bitmap handle, [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ignores the width and height parameters.</span></span> <span data-ttu-id="c2e16-139">O bitmap define o tamanho do cursor.</span><span class="sxs-lookup"><span data-stu-id="c2e16-139">The bitmap defines the size of the caret.</span></span>

## <a name="hiding-a-caret"></a><span data-ttu-id="c2e16-140">Ocultando um cursor</span><span class="sxs-lookup"><span data-stu-id="c2e16-140">Hiding a Caret</span></span>

<span data-ttu-id="c2e16-141">Sempre que o aplicativo redesenha uma tela durante o processamento de uma mensagem diferente do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint), ele deve tornar o cursor invisível usando a função [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) .</span><span class="sxs-lookup"><span data-stu-id="c2e16-141">Whenever your application redraws a screen while processing a message other than [**WM\_PAINT**](/windows/desktop/gdi/wm-paint), it must make the caret invisible by using the [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) function.</span></span> <span data-ttu-id="c2e16-142">Quando seu aplicativo terminar de desenhar, reexiba o cursor usando a função de [**Iscaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) .</span><span class="sxs-lookup"><span data-stu-id="c2e16-142">When your application is finished drawing, redisplay the caret by using the [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) function.</span></span> <span data-ttu-id="c2e16-143">Se seu aplicativo processa a mensagem do **WM \_ Paint** , não é necessário ocultar e reexibir o cursor, pois essa função faz isso automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c2e16-143">If your application processes the **WM\_PAINT** message, it is not necessary to hide and redisplay the caret, because this function does this automatically.</span></span>

<span data-ttu-id="c2e16-144">O exemplo de código a seguir mostra como fazer com que seu aplicativo oculte o cursor enquanto desenha um caractere na tela e durante o processamento da mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="c2e16-144">The following code sample shows how to have your application hide the caret while drawing a character on the screen and while processing the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>


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



<span data-ttu-id="c2e16-145">Se seu aplicativo chamar a função [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) várias vezes sem chamar o [**cuidado**](/windows/desktop/api/Winuser/nf-winuser-showcaret), o cursor não será exibido até que o aplicativo **também chame o** mesmo número de vezes.</span><span class="sxs-lookup"><span data-stu-id="c2e16-145">If your application calls the [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) function several times without calling [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret), the caret will not be displayed until the application also calls **ShowCaret** the same number of times.</span></span>

## <a name="destroying-a-caret"></a><span data-ttu-id="c2e16-146">Destruindo um cursor</span><span class="sxs-lookup"><span data-stu-id="c2e16-146">Destroying a Caret</span></span>

<span data-ttu-id="c2e16-147">Quando uma janela perde o foco do teclado, o sistema envia a mensagem do [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) para a janela.</span><span class="sxs-lookup"><span data-stu-id="c2e16-147">When a window loses the keyboard focus, the system sends the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message to the window.</span></span> <span data-ttu-id="c2e16-148">Seu aplicativo deve destruir o cursor durante o processamento dessa mensagem usando a função [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) .</span><span class="sxs-lookup"><span data-stu-id="c2e16-148">Your application should destroy the caret while processing this message by using the [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) function.</span></span> <span data-ttu-id="c2e16-149">O código a seguir mostra como destruir um cursor em uma janela que não tem mais o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="c2e16-149">The following code shows how to destroy a caret in a window that no longer has the keyboard focus.</span></span>


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a><span data-ttu-id="c2e16-150">Ajustando o tempo de intermitência</span><span class="sxs-lookup"><span data-stu-id="c2e16-150">Adjusting the Blink Time</span></span>

<span data-ttu-id="c2e16-151">No Windows de 16 bits, um aplicativo baseado no Windows poderia chamar a função [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) para salvar o tempo de intermitência atual e, em seguida, chamar a função [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) para ajustar o tempo de intermitência durante o processamento da mensagem do [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="c2e16-151">In 16-bit Windows, a Windows-based application could call the [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) function to save the current blink time, then call the [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) function to adjust the blink time during its processing of the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="c2e16-152">O aplicativo restauraria o tempo de intermitência salvo para o uso de outros aplicativos chamando **SetCaretBlinkTime** durante o processamento da mensagem do [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="c2e16-152">The application would restore the saved blink time for the use of other applications by calling **SetCaretBlinkTime** during its processing of the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="c2e16-153">No entanto, essa técnica não funciona em ambientes multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="c2e16-153">However, this technique does not work in multithreaded environments.</span></span> <span data-ttu-id="c2e16-154">Especificamente, a desativação de um aplicativo não é sincronizada com a ativação de outro aplicativo, de modo que, se um aplicativo parar, outro aplicativo ainda poderá ser ativado.</span><span class="sxs-lookup"><span data-stu-id="c2e16-154">Specifically, the deactivation of one application is not synchronized with the activation of another application, so that if one application hangs, another application can still be activated.</span></span>

<span data-ttu-id="c2e16-155">Os aplicativos devem respeitar o tempo de intermitência escolhido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c2e16-155">Applications should respect the blink time chosen by the user.</span></span> <span data-ttu-id="c2e16-156">A função [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) só deve ser chamada por um aplicativo que permita ao usuário definir o tempo de intermitência.</span><span class="sxs-lookup"><span data-stu-id="c2e16-156">The [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) function should only be called by an application that allows the user to set the blink time.</span></span>

## <a name="processing-keyboard-input"></a><span data-ttu-id="c2e16-157">Processando entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="c2e16-157">Processing Keyboard Input</span></span>

<span data-ttu-id="c2e16-158">O exemplo a seguir demonstra como usar um cursor em um editor de texto simples.</span><span class="sxs-lookup"><span data-stu-id="c2e16-158">The following example demonstrates how to use a caret in a simple text editor.</span></span> <span data-ttu-id="c2e16-159">O exemplo atualiza a posição do cursor à medida que o usuário digita caracteres imprimíveis e usa várias chaves para percorrer a área do cliente.</span><span class="sxs-lookup"><span data-stu-id="c2e16-159">The example updates the caret position as the user types printable characters and uses various keys to move through the client area.</span></span>


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



 

 