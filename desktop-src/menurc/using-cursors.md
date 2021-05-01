---
title: Usando cursores
description: Esta seção fornece exemplos de código que mostram como executar tarefas relacionadas a cursores.
ms.assetid: eab7b781-783e-4fc5-868d-6ff773c40a21
keywords:
- recursos, cursores
- cursores, personalizado
- cursores personalizados
- cursor de ampulheta
- cursores, criando
- cursores, ampulheta
- Criando cursores
- destruindo cursores
- exibindo cursores
- confinando cursores
- cursores, destruindo
- cursores, exibindo
- cursores, confinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cf681fd17f3e79e4559e9936be232ae09f8453
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327121"
---
# <a name="using-cursors"></a><span data-ttu-id="eb889-116">Usando cursores</span><span class="sxs-lookup"><span data-stu-id="eb889-116">Using Cursors</span></span>

<span data-ttu-id="eb889-117">Esta seção aborda os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb889-117">This section discusses the following topics.</span></span>

-   [<span data-ttu-id="eb889-118">Criando um cursor</span><span class="sxs-lookup"><span data-stu-id="eb889-118">Creating a Cursor</span></span>](#creating-a-cursor)
-   [<span data-ttu-id="eb889-119">Exibindo um cursor</span><span class="sxs-lookup"><span data-stu-id="eb889-119">Displaying a Cursor</span></span>](#displaying-a-cursor)
-   [<span data-ttu-id="eb889-120">Confinando um cursor</span><span class="sxs-lookup"><span data-stu-id="eb889-120">Confining a Cursor</span></span>](#confining-a-cursor)
-   [<span data-ttu-id="eb889-121">Usando funções de cursor para criar um ratoeira</span><span class="sxs-lookup"><span data-stu-id="eb889-121">Using Cursor Functions to Create a Mousetrap</span></span>](#using-cursor-functions-to-create-a-mousetrap)
-   [<span data-ttu-id="eb889-122">Usando o teclado para mover o cursor</span><span class="sxs-lookup"><span data-stu-id="eb889-122">Using the Keyboard to Move the Cursor</span></span>](#using-the-keyboard-to-move-the-cursor)

## <a name="creating-a-cursor"></a><span data-ttu-id="eb889-123">Criando um cursor</span><span class="sxs-lookup"><span data-stu-id="eb889-123">Creating a Cursor</span></span>

<span data-ttu-id="eb889-124">O exemplo a seguir cria duas alças de cursor: uma para o cursor de ampulheta padrão e outra para um cursor personalizado incluído como um recurso no arquivo de definição de recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eb889-124">The following example creates two cursor handles: one for the standard hourglass cursor and one for a custom cursor included as a resource in the application's resource-definition file.</span></span>


```
HINSTANCE hinst;            // handle to current instance 
HCURSOR hCurs1, hCurs2;     // cursor handles 
 
// Create a standard hourglass cursor. 
 
hCurs1 = LoadCursor(NULL, IDC_WAIT); 
 
// Create a custom cursor based on a resource. 
 
hCurs2 = LoadCursor(hinst, MAKEINTRESOURCE(240)); 
```



<span data-ttu-id="eb889-125">Você deve implementar cursores personalizados como recursos.</span><span class="sxs-lookup"><span data-stu-id="eb889-125">You should implement custom cursors as resources.</span></span> <span data-ttu-id="eb889-126">Em vez de criar os cursores em tempo de execução, use a função [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)ou [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) para evitar a dependência do dispositivo, para simplificar a localização e para permitir que os aplicativos compartilhem designs de cursores.</span><span class="sxs-lookup"><span data-stu-id="eb889-126">Rather than create the cursors at run time, use the [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea), or [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) function to avoid device dependence, to simplify localization, and to enable applications to share cursor designs.</span></span>

<span data-ttu-id="eb889-127">O exemplo a seguir usa a função [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) para criar um cursor personalizado em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="eb889-127">The following example uses the [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) function to create a custom cursor at run time.</span></span> <span data-ttu-id="eb889-128">O exemplo é incluído aqui para ilustrar como o sistema interpreta máscaras de cursor.</span><span class="sxs-lookup"><span data-stu-id="eb889-128">The example is included here to illustrate how the system interprets cursor masks.</span></span>


```
HINSTANCE hinst;            // handle to current instance  
HCURSOR hCurs1, hCurs2;     // cursor handles 
 
HCURSOR hCurs3;             // cursor handle 
 
// Yin-shaped cursor AND mask 
 
BYTE ANDmaskCursor[] = 
{ 
    0xFF, 0xFC, 0x3F, 0xFF,   // line 1 
    0xFF, 0xC0, 0x1F, 0xFF,   // line 2 
    0xFF, 0x00, 0x3F, 0xFF,   // line 3 
    0xFE, 0x00, 0xFF, 0xFF,   // line 4 
 
    0xF7, 0x01, 0xFF, 0xFF,   // line 5 
    0xF0, 0x03, 0xFF, 0xFF,   // line 6 
    0xF0, 0x03, 0xFF, 0xFF,   // line 7 
    0xE0, 0x07, 0xFF, 0xFF,   // line 8 
 
    0xC0, 0x07, 0xFF, 0xFF,   // line 9 
    0xC0, 0x0F, 0xFF, 0xFF,   // line 10 
    0x80, 0x0F, 0xFF, 0xFF,   // line 11 
    0x80, 0x0F, 0xFF, 0xFF,   // line 12 
 
    0x80, 0x07, 0xFF, 0xFF,   // line 13 
    0x00, 0x07, 0xFF, 0xFF,   // line 14 
    0x00, 0x03, 0xFF, 0xFF,   // line 15 
    0x00, 0x00, 0xFF, 0xFF,   // line 16 
 
    0x00, 0x00, 0x7F, 0xFF,   // line 17 
    0x00, 0x00, 0x1F, 0xFF,   // line 18 
    0x00, 0x00, 0x0F, 0xFF,   // line 19 
    0x80, 0x00, 0x0F, 0xFF,   // line 20 
 
    0x80, 0x00, 0x07, 0xFF,   // line 21 
    0x80, 0x00, 0x07, 0xFF,   // line 22 
    0xC0, 0x00, 0x07, 0xFF,   // line 23 
    0xC0, 0x00, 0x0F, 0xFF,   // line 24 
 
    0xE0, 0x00, 0x0F, 0xFF,   // line 25 
    0xF0, 0x00, 0x1F, 0xFF,   // line 26 
    0xF0, 0x00, 0x1F, 0xFF,   // line 27 
    0xF8, 0x00, 0x3F, 0xFF,   // line 28 
 
    0xFE, 0x00, 0x7F, 0xFF,   // line 29 
    0xFF, 0x00, 0xFF, 0xFF,   // line 30 
    0xFF, 0xC3, 0xFF, 0xFF,   // line 31 
    0xFF, 0xFF, 0xFF, 0xFF    // line 32 
};
 
// Yin-shaped cursor XOR mask 
 
BYTE XORmaskCursor[] = 
{ 
    0x00, 0x00, 0x00, 0x00,   // line 1 
    0x00, 0x03, 0xC0, 0x00,   // line 2 
    0x00, 0x3F, 0x00, 0x00,   // line 3 
    0x00, 0xFE, 0x00, 0x00,   // line 4 
 
    0x0E, 0xFC, 0x00, 0x00,   // line 5 
    0x07, 0xF8, 0x00, 0x00,   // line 6 
    0x07, 0xF8, 0x00, 0x00,   // line 7 
    0x0F, 0xF0, 0x00, 0x00,   // line 8 
 
    0x1F, 0xF0, 0x00, 0x00,   // line 9 
    0x1F, 0xE0, 0x00, 0x00,   // line 10 
    0x3F, 0xE0, 0x00, 0x00,   // line 11 
    0x3F, 0xE0, 0x00, 0x00,   // line 12 
 
    0x3F, 0xF0, 0x00, 0x00,   // line 13 
    0x7F, 0xF0, 0x00, 0x00,   // line 14 
    0x7F, 0xF8, 0x00, 0x00,   // line 15 
    0x7F, 0xFC, 0x00, 0x00,   // line 16 
 
    0x7F, 0xFF, 0x00, 0x00,   // line 17 
    0x7F, 0xFF, 0x80, 0x00,   // line 18 
    0x7F, 0xFF, 0xE0, 0x00,   // line 19 
    0x3F, 0xFF, 0xE0, 0x00,   // line 20 
 
    0x3F, 0xC7, 0xF0, 0x00,   // line 21 
    0x3F, 0x83, 0xF0, 0x00,   // line 22 
    0x1F, 0x83, 0xF0, 0x00,   // line 23 
    0x1F, 0x83, 0xE0, 0x00,   // line 24 
 
    0x0F, 0xC7, 0xE0, 0x00,   // line 25 
    0x07, 0xFF, 0xC0, 0x00,   // line 26 
    0x07, 0xFF, 0xC0, 0x00,   // line 27 
    0x01, 0xFF, 0x80, 0x00,   // line 28 
 
    0x00, 0xFF, 0x00, 0x00,   // line 29 
    0x00, 0x3C, 0x00, 0x00,   // line 30 
    0x00, 0x00, 0x00, 0x00,   // line 31 
    0x00, 0x00, 0x00, 0x00    // line 32 
};
 
// Create a custom cursor at run time. 
 
hCurs3 = CreateCursor( hinst,   // app. instance 
             19,                // horizontal position of hot spot 
             2,                 // vertical position of hot spot 
             32,                // cursor width 
             32,                // cursor height 
             ANDmaskCursor,     // AND mask 
             XORmaskCursor );   // XOR mask 
```



<span data-ttu-id="eb889-129">Para criar o cursor, [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) aplica a seguinte tabela da verdade às máscaras **e** e **XOR** .</span><span class="sxs-lookup"><span data-stu-id="eb889-129">To create the cursor, [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) applies the following truth table to the **AND** and **XOR** masks.</span></span>



| <span data-ttu-id="eb889-130">E máscara</span><span class="sxs-lookup"><span data-stu-id="eb889-130">AND mask</span></span> | <span data-ttu-id="eb889-131">Máscara XOR</span><span class="sxs-lookup"><span data-stu-id="eb889-131">XOR mask</span></span> | <span data-ttu-id="eb889-132">Monitor</span><span class="sxs-lookup"><span data-stu-id="eb889-132">Display</span></span>        |
|----------|----------|----------------|
| <span data-ttu-id="eb889-133">0</span><span class="sxs-lookup"><span data-stu-id="eb889-133">0</span></span>        | <span data-ttu-id="eb889-134">0</span><span class="sxs-lookup"><span data-stu-id="eb889-134">0</span></span>        | <span data-ttu-id="eb889-135">Preto</span><span class="sxs-lookup"><span data-stu-id="eb889-135">Black</span></span>          |
| <span data-ttu-id="eb889-136">0</span><span class="sxs-lookup"><span data-stu-id="eb889-136">0</span></span>        | <span data-ttu-id="eb889-137">1</span><span class="sxs-lookup"><span data-stu-id="eb889-137">1</span></span>        | <span data-ttu-id="eb889-138">Branca</span><span class="sxs-lookup"><span data-stu-id="eb889-138">White</span></span>          |
| <span data-ttu-id="eb889-139">1</span><span class="sxs-lookup"><span data-stu-id="eb889-139">1</span></span>        | <span data-ttu-id="eb889-140">0</span><span class="sxs-lookup"><span data-stu-id="eb889-140">0</span></span>        | <span data-ttu-id="eb889-141">Tela</span><span class="sxs-lookup"><span data-stu-id="eb889-141">Screen</span></span>         |
| <span data-ttu-id="eb889-142">1</span><span class="sxs-lookup"><span data-stu-id="eb889-142">1</span></span>        | <span data-ttu-id="eb889-143">1</span><span class="sxs-lookup"><span data-stu-id="eb889-143">1</span></span>        | <span data-ttu-id="eb889-144">Tela reversa</span><span class="sxs-lookup"><span data-stu-id="eb889-144">Reverse screen</span></span> |



 

<span data-ttu-id="eb889-145">Para obter mais informações, consulte [bitmaps](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="eb889-145">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

<span data-ttu-id="eb889-146">Antes de fechar, você deve usar a função [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) para destruir os cursores criados com [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor).</span><span class="sxs-lookup"><span data-stu-id="eb889-146">Before closing, you must use the [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) function to destroy any cursors you created with [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor).</span></span> <span data-ttu-id="eb889-147">Não é necessário destruir cursores criados por outras funções.</span><span class="sxs-lookup"><span data-stu-id="eb889-147">It is not necessary to destroy cursors created by other functions.</span></span>

## <a name="displaying-a-cursor"></a><span data-ttu-id="eb889-148">Exibindo um cursor</span><span class="sxs-lookup"><span data-stu-id="eb889-148">Displaying a Cursor</span></span>

<span data-ttu-id="eb889-149">O sistema exibe automaticamente o cursor de classe (o cursor associado à janela à qual o cursor está apontando).</span><span class="sxs-lookup"><span data-stu-id="eb889-149">The system automatically displays the class cursor (the cursor associated with the window to which the cursor is pointing).</span></span> <span data-ttu-id="eb889-150">Você pode atribuir um cursor de classe ao registrar uma classe de janela.</span><span class="sxs-lookup"><span data-stu-id="eb889-150">You can assign a class cursor while registering a window class.</span></span> <span data-ttu-id="eb889-151">O exemplo a seguir ilustra isso atribuindo um identificador de cursor ao membro **hCursor** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) identificada pelo parâmetro *WC* .</span><span class="sxs-lookup"><span data-stu-id="eb889-151">The following example illustrates this by assigning a cursor handle to the **hCursor** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure identified by the *wc* parameter.</span></span>


```
WNDCLASS  wc; 
 
// Fill the window class structure with parameters that 
// describe the main window. 
 
wc.style = NULL;                        // class style(s) 
wc.lpfnWndProc = (WNDPROC) MainWndProc; // window procedure 
wc.cbClsExtra = 0;           // no per-class extra data 
wc.cbWndExtra = 0;           // no per-window extra data 
wc.hInstance = hinst;        // application that owns the class 
wc.hIcon = LoadIcon(NULL, IDI_APPLICATION);     // class icon 
wc.hCursor = LoadCursor(hinst, MAKEINTRESOURCE(230)); // class cursor 
wc.hbrBackground = GetStockObject(WHITE_BRUSH); // class background 
wc.lpszMenuName =  "GenericMenu";               // class menu 
wc.lpszClassName = "GenericWClass"              // class name 
 
// Register the window class. 
 
return RegisterClass(&wc); 
```



<span data-ttu-id="eb889-152">Quando a classe Window é registrada, o cursor identificado por 230 no arquivo de definição de recurso do aplicativo é o cursor padrão para todas as janelas baseadas na classe.</span><span class="sxs-lookup"><span data-stu-id="eb889-152">When the window class is registered, the cursor identified by 230 in the application's resource-definition file is the default cursor for all windows based on the class.</span></span>

<span data-ttu-id="eb889-153">Seu aplicativo pode alterar o design do cursor usando a função [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) e especificando um identificador de cursor diferente.</span><span class="sxs-lookup"><span data-stu-id="eb889-153">Your application can change the design of the cursor by using the [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) function and specifying a different cursor handle.</span></span> <span data-ttu-id="eb889-154">No entanto, quando o cursor se move, o sistema redesenha o cursor de classe no novo local.</span><span class="sxs-lookup"><span data-stu-id="eb889-154">However, when the cursor moves, the system redraws the class cursor at the new location.</span></span> <span data-ttu-id="eb889-155">Para impedir que o cursor de classe seja redesenhado, você deve processar a mensagem [**\_ SetCursor do WM**](wm-setcursor.md) .</span><span class="sxs-lookup"><span data-stu-id="eb889-155">To prevent the class cursor from being redrawn, you must process the [**WM\_SETCURSOR**](wm-setcursor.md) message.</span></span> <span data-ttu-id="eb889-156">Cada vez que o cursor se move e a entrada do mouse não é capturada, o sistema envia essa mensagem para a janela na qual o cursor está se movendo.</span><span class="sxs-lookup"><span data-stu-id="eb889-156">Each time the cursor moves and mouse input is not captured, the system sends this message to the window in which the cursor is moving.</span></span>

<span data-ttu-id="eb889-157">Você pode especificar cursores diferentes para diferentes condições ao processar o [**WM \_ SetCursor**](wm-setcursor.md).</span><span class="sxs-lookup"><span data-stu-id="eb889-157">You can specify different cursors for different conditions while processing [**WM\_SETCURSOR**](wm-setcursor.md).</span></span> <span data-ttu-id="eb889-158">Por exemplo, o exemplo a seguir mostra como exibir o cursor sempre que o cursor se move sobre o ícone de um aplicativo minimizado.</span><span class="sxs-lookup"><span data-stu-id="eb889-158">For example, the following example shows how to display the cursor whenever the cursor moves over the icon of a minimized application.</span></span>


```
case WM_SETCURSOR: 
 
    // If the window is minimized, draw the hCurs3 cursor. 
    // If the window is not minimized, draw the default 
    // cursor (class cursor). 
 
    if (IsIconic(hwnd)) 
    { 
        SetCursor(hCurs3); 
        break; 
    } 
```



<span data-ttu-id="eb889-159">Quando a janela não é minimizada, o sistema exibe o cursor de classe.</span><span class="sxs-lookup"><span data-stu-id="eb889-159">When the window is not minimized, the system displays the class cursor.</span></span>

<span data-ttu-id="eb889-160">Você pode substituir um cursor de classe usando a função [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) .</span><span class="sxs-lookup"><span data-stu-id="eb889-160">You can replace a class cursor by using the [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) function.</span></span> <span data-ttu-id="eb889-161">Essa função altera as configurações de janela padrão para todas as janelas de uma classe especificada.</span><span class="sxs-lookup"><span data-stu-id="eb889-161">This function changes the default window settings for all windows of a specified class.</span></span> <span data-ttu-id="eb889-162">O exemplo a seguir substitui o cursor de classe existente pelo `hCurs2` cursor.</span><span class="sxs-lookup"><span data-stu-id="eb889-162">The following example replaces the existing class cursor with the `hCurs2` cursor.</span></span>


```
// Change the cursor for window class represented by hwnd. 
 
SetClassLongPtr(hwnd,    // window handle 
    GCLP_HCURSOR,        // change cursor 
    (LONG_PTR) hCurs2);  // new cursor 
```



<span data-ttu-id="eb889-163">Para obter mais informações, consulte [classes de janela](/windows/desktop/winmsg/window-classes) e [entrada do mouse](/windows/desktop/inputdev/mouse-input).</span><span class="sxs-lookup"><span data-stu-id="eb889-163">For more information, see [Window Classes](/windows/desktop/winmsg/window-classes) and [Mouse Input](/windows/desktop/inputdev/mouse-input).</span></span>

## <a name="confining-a-cursor"></a><span data-ttu-id="eb889-164">Confinando um cursor</span><span class="sxs-lookup"><span data-stu-id="eb889-164">Confining a Cursor</span></span>

<span data-ttu-id="eb889-165">O exemplo a seguir ajusta o cursor para a janela do aplicativo e restaura o cursor para sua janela anterior.</span><span class="sxs-lookup"><span data-stu-id="eb889-165">The following example confines the cursor to the application's window and then restores the cursor to its previous window.</span></span> <span data-ttu-id="eb889-166">O exemplo usa a função [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) para registrar a área na qual o cursor pode se mover e a função [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) para confinar e restaurar o cursor.</span><span class="sxs-lookup"><span data-stu-id="eb889-166">The example uses the [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) function to record the area in which the cursor can move and the [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) function to confine and restore the cursor.</span></span>


```
RECT rcClip;           // new area for ClipCursor
RECT rcOldClip;        // previous area for ClipCursor
 
// Record the area in which the cursor can move. 
 
GetClipCursor(&rcOldClip); 
 
// Get the dimensions of the application's window. 
 
GetWindowRect(hwnd, &rcClip); 
 
// Confine the cursor to the application's window. 
 
ClipCursor(&rcClip); 
 
   // 
   // Process input from the confined cursor. 
   // 
 
// Restore the cursor to its previous area. 
 
ClipCursor(&rcOldClip); 
```



<span data-ttu-id="eb889-167">Como há apenas um cursor de cada vez disponível no sistema, um aplicativo que confina o cursor deve restaurar o cursor antes de ceder o controle a outra janela.</span><span class="sxs-lookup"><span data-stu-id="eb889-167">Because there is only one cursor at a time available in the system, an application that confines the cursor must restore the cursor before relinquishing control to another window.</span></span>

## <a name="using-cursor-functions-to-create-a-mousetrap"></a><span data-ttu-id="eb889-168">Usando funções de cursor para criar um ratoeira</span><span class="sxs-lookup"><span data-stu-id="eb889-168">Using Cursor Functions to Create a Mousetrap</span></span>

<span data-ttu-id="eb889-169">O exemplo a seguir usa as funções [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos), [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos), [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) [**, LoadCursor e**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) para criar um ratoeira simples.</span><span class="sxs-lookup"><span data-stu-id="eb889-169">The following example uses the [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos), [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos), [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor), [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), and [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) functions to create a simple mousetrap.</span></span> <span data-ttu-id="eb889-170">Ele também usa as funções cursor e timer para monitorar a posição do cursor a cada 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="eb889-170">It also uses cursor and timer functions to monitor the cursor's position every 10 seconds.</span></span> <span data-ttu-id="eb889-171">Se a posição do cursor não tiver sido alterada nos últimos 10 segundos e a janela principal do aplicativo for minimizada, o aplicativo alterará o cursor e o moverá para o ícone de ratoeira.</span><span class="sxs-lookup"><span data-stu-id="eb889-171">If the cursor position has not changed in the last 10 seconds and the application's main window is minimized, the application changes the cursor and moves it to the mousetrap icon.</span></span>

<span data-ttu-id="eb889-172">Um exemplo de um ratoeira semelhante é incluído em [ícones](icons.md).</span><span class="sxs-lookup"><span data-stu-id="eb889-172">An example for a similar mousetrap is included in [Icons](icons.md).</span></span> <span data-ttu-id="eb889-173">Ele usa as funções [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) e [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) em vez das funções [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) e [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) dependentes de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="eb889-173">It uses the [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) and [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) functions instead of the more device-dependent [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) and [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) functions.</span></span>


```
HICON hIcon1;               // icon handles 
POINT ptOld;                // previous cursor location 
HCURSOR hCurs1;             // cursor handle 
 
 
// The following cursor masks are defined in a code 
// example that appears earlier in this section. 
 
// Yin-shaped cursor AND and XOR masks 
 
BYTE ANDmaskCursor[] = ... 
BYTE XORmaskCursor[] = ... 
 
// Yang-shaped icon AND mask 
 
BYTE ANDmaskIcon[] = {0xFF, 0xFF, 0xFF, 0xFF,  // line 1 
                      0xFF, 0xFF, 0xC3, 0xFF,  // line 2 
                      0xFF, 0xFF, 0x00, 0xFF,  // line 3 
                      0xFF, 0xFE, 0x00, 0x7F,  // line 4 
 
                      0xFF, 0xFC, 0x00, 0x1F,  // line 5 
                      0xFF, 0xF8, 0x00, 0x0F,  // line 6 
                      0xFF, 0xF8, 0x00, 0x0F,  // line 7 
                      0xFF, 0xF0, 0x00, 0x07,  // line 8 
 
                      0xFF, 0xF0, 0x00, 0x03,  // line 9 
                      0xFF, 0xE0, 0x00, 0x03,  // line 10 
                      0xFF, 0xE0, 0x00, 0x01,  // line 11 
                      0xFF, 0xE0, 0x00, 0x01,  // line 12 
 
                      0xFF, 0xF0, 0x00, 0x01,  // line 13 
                      0xFF, 0xF0, 0x00, 0x00,  // line 14 
                      0xFF, 0xF8, 0x00, 0x00,  // line 15 
                      0xFF, 0xFC, 0x00, 0x00,  // line 16 
 
                      0xFF, 0xFF, 0x00, 0x00,  // line 17 
                      0xFF, 0xFF, 0x80, 0x00,  // line 18 
                      0xFF, 0xFF, 0xE0, 0x00,  // line 19 
                      0xFF, 0xFF, 0xE0, 0x01,  // line 20 
 
                      0xFF, 0xFF, 0xF0, 0x01,  // line 21 
                      0xFF, 0xFF, 0xF0, 0x01,  // line 22 
                      0xFF, 0xFF, 0xF0, 0x03,  // line 23 
                      0xFF, 0xFF, 0xE0, 0x03,  // line 24 
 
                      0xFF, 0xFF, 0xE0, 0x07,  // line 25 
                      0xFF, 0xFF, 0xC0, 0x0F,  // line 26 
                      0xFF, 0xFF, 0xC0, 0x0F,  // line 27 
                      0xFF, 0xFF, 0x80, 0x1F,  // line 28 
 
                      0xFF, 0xFF, 0x00, 0x7F,  // line 29 
                      0xFF, 0xFC, 0x00, 0xFF,  // line 30 
                      0xFF, 0xF8, 0x03, 0xFF,  // line 31 
                      0xFF, 0xFC, 0x3F, 0xFF}; // line 32 
 
// Yang-shaped icon XOR mask 
 
BYTE XORmaskIcon[] = {0x00, 0x00, 0x00, 0x00,  // line 1 
                      0x00, 0x00, 0x00, 0x00,  // line 2 
                      0x00, 0x00, 0x00, 0x00,  // line 3 
                      0x00, 0x00, 0x00, 0x00,  // line 4 
 
                      0x00, 0x00, 0x00, 0x00,  // line 5 
                      0x00, 0x00, 0x00, 0x00,  // line 6 
                      0x00, 0x00, 0x00, 0x00,  // line 7 
                      0x00, 0x00, 0x38, 0x00,  // line 8 
 
                      0x00, 0x00, 0x7C, 0x00,  // line 9 
                      0x00, 0x00, 0x7C, 0x00,  // line 10 
                      0x00, 0x00, 0x7C, 0x00,  // line 11  
                      0x00, 0x00, 0x38, 0x00,  // line 12 
 
                      0x00, 0x00, 0x00, 0x00,  // line 13 
                      0x00, 0x00, 0x00, 0x00,  // line 14 
                      0x00, 0x00, 0x00, 0x00,  // line 15 
                      0x00, 0x00, 0x00, 0x00,  // line 16 
 
                      0x00, 0x00, 0x00, 0x00,  // line 17 
                      0x00, 0x00, 0x00, 0x00,  // line 18 
                      0x00, 0x00, 0x00, 0x00,  // line 19 
                      0x00, 0x00, 0x00, 0x00,  // line 20 
 
                      0x00, 0x00, 0x00, 0x00,  // line 21 
                      0x00, 0x00, 0x00, 0x00,  // line 22 
                      0x00, 0x00, 0x00, 0x00,  // line 23 
                      0x00, 0x00, 0x00, 0x00,  // line 24 
 
                      0x00, 0x00, 0x00, 0x00,  // line 25 
                      0x00, 0x00, 0x00, 0x00,  // line 26 
                      0x00, 0x00, 0x00, 0x00,  // line 27 
                      0x00, 0x00, 0x00, 0x00,  // line 28 
 
                      0x00, 0x00, 0x00, 0x00,  // line 29 
                      0x00, 0x00, 0x00, 0x00,  // line 30 
                      0x00, 0x00, 0x00, 0x00,  // line 31 
                      0x00, 0x00, 0x00, 0x00}; // line 32 
 
hIcon1 = CreateIcon(hinst, // handle to app. instance 
             32,           // icon width 
             32,           // icon height 
             1,            // number of XOR planes 
             1,            // number of bits per pixel 
             ANDmaskIcon,  // AND mask 
             XORmaskIcon); // XOR mask 
 
hCurs1 = CreateCursor(hinst, // handle to app. instance
             19,             // horizontal position of hot spot 
             2,              // vertical position of hot spot 
             32,             // cursor width 
             32,             // cursor height 
             ANDmaskCursor,  // AND mask 
             XORmaskCursor); // XOR mask 
 
// Fill in the window class structure. 
 
WNDCLASS  wc; 
 
wc.hIcon = hIcon1;                        // class icon 
wc.hCursor = LoadCursor(NULL, IDC_ARROW); // class cursor 
 
//
// Register the window class and perform 
// other application initialization. 
//
 
// Set a timer for the mousetrap. 
 
GetCursorPos(&ptOld); 
 
SetTimer(hwnd, IDT_CURSOR, 10000, (TIMERPROC) NULL); 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // window handle 
    UINT message,       // type of message 
    UINT wParam,        // additional information 
    LONG lParam)        // additional information 
{ 
 
    HDC hdc;            // handle to device context 
    POINT pt;           // current cursor location 
    RECT rc;            // minimized window location 
 
    switch (message) 
    { 
        //
        // Process other messages. 
        // 
        case WM_TIMER: 
        // If the window is minimized, compare the 
        // current cursor position with the one 10 
        // seconds before. If the cursor position has 
        // not changed, move the cursor to the icon. 
 
            if (IsIconic(hwnd)) 
            { 
                GetCursorPos(&pt); 
 
                if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
                { 
                    GetWindowRect(hwnd, &rc); 
                    SetCursorPos(rc.left + 20, rc.top + 4); 
 
                    // Note that the additional constants 
                    // (20 and 4) are application-specific 
                    // values to align the yin-shaped cursor 
                    // and the yang-shaped icon. 
 
                } 
                else 
                { 
                    ptOld.x = pt.x; 
                    ptOld.y = pt.y; 
                } 
            } 
 
            return 0; 
 
        case WM_SETCURSOR: 
        // If the window is minimized, draw hCurs1. 
        // If the window is not minimized, draw the 
        // default cursor (class cursor). 
 
            if (IsIconic(hwnd)) 
            { 
                SetCursor(hCurs1); 
                break; 
            } 
 
        case WM_DESTROY: 
        // Destroy timer. 
 
            KillTimer(hwnd, IDT_CURSOR); 
 
            PostQuitMessage(0); 
            break; 
    } 
} 
```



## <a name="using-the-keyboard-to-move-the-cursor"></a><span data-ttu-id="eb889-174">Usando o teclado para mover o cursor</span><span class="sxs-lookup"><span data-stu-id="eb889-174">Using the Keyboard to Move the Cursor</span></span>

<span data-ttu-id="eb889-175">Como o sistema não requer um mouse, um aplicativo deve ser capaz de simular ações do mouse com o teclado.</span><span class="sxs-lookup"><span data-stu-id="eb889-175">Because the system does not require a mouse, an application should be able to simulate mouse actions with the keyboard.</span></span> <span data-ttu-id="eb889-176">O exemplo a seguir mostra como conseguir isso usando as funções [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) e [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) e processando a entrada das teclas de direção.</span><span class="sxs-lookup"><span data-stu-id="eb889-176">The following example shows how to achieve this by using the [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) and [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) functions and by processing input from the arrow keys.</span></span>


```
HCURSOR hCurs1, hCurs2;    // cursor handles 
 
POINT pt;                  // cursor location  
RECT rc;                   // client area coordinates 
static int repeat = 1;     // repeat key counter 
 
// 
// Other declarations and initialization. 
// 
 
switch (message) 
{ 
// 
// Process other messages. 
// 
 
    case WM_KEYDOWN: 
 
        if (wParam != VK_LEFT && wParam != VK_RIGHT && 
        wParam != VK_UP && wParam != VK_DOWN) 
        { 
            break; 
        } 
 
        GetCursorPos(&pt); 
 
        // Convert screen coordinates to client coordinates. 
 
        ScreenToClient(hwnd, &pt); 
 
        switch (wParam) 
        { 
        // Move the cursor to reflect which 
        // arrow keys are pressed. 
 
            case VK_LEFT:               // left arrow 
                pt.x -= repeat; 
                break; 
 
            case VK_RIGHT:              // right arrow 
                pt.x += repeat; 
                break; 
 
            case VK_UP:                 // up arrow 
                pt.y -= repeat; 
                break; 
 
            case VK_DOWN:               // down arrow 
                pt.y += repeat; 
                break; 
 
            default: 
                return 0; 
        } 
 
        repeat++;           // Increment repeat count. 
 
        // Keep the cursor in the client area. 
 
        GetClientRect(hwnd, &rc); 
 
        if (pt.x >= rc.right) 
        { 
            pt.x = rc.right - 1; 
        } 
        else 
        { 
            if (pt.x < rc.left) 
            { 
                pt.x = rc.left; 
            } 
        } 
 
        if (pt.y >= rc.bottom) 
            pt.y = rc.bottom - 1; 
        else 
            if (pt.y < rc.top) 
                pt.y = rc.top; 
 
        // Convert client coordinates to screen coordinates. 
 
        ClientToScreen(hwnd, &pt); 
        SetCursorPos(pt.x, pt.y); 
        return 0; 

 
    case WM_KEYUP: 
 
        repeat = 1;            // Clear repeat count. 
        return 0; 
 
} 
```



 

 
