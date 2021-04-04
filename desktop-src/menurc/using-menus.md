---
title: Uso de Menus
description: Esta seção fornece exemplos de código para tarefas relacionadas a menus.
ms.assetid: b1391e37-a146-46ec-a329-aa57cfcfd351
keywords:
- recursos, menus
- menus, criando
- menu-recursos de modelo
- recursos, menu-modelo
- menu estendido – formato de modelo
- formato de modelo de menu antigo
- carregando menu – recursos de modelo
- menus, classe
- menus, atalho
- Criando menus
- menus de classe
- menus de atalho
- bitmaps de item de menu
- menus, proprietário desenhado
- menus desenhados pelo proprietário
- bitmaps de marca de seleção personalizados
- menus, caixas de seleção
- menus, fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d216b5fe5e6c25a98b5bdf3abe9d55b4bb0b34f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640962"
---
# <a name="using-menus"></a><span data-ttu-id="04192-121">Uso de Menus</span><span class="sxs-lookup"><span data-stu-id="04192-121">Using Menus</span></span>

<span data-ttu-id="04192-122">Esta seção descreve as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="04192-122">This section describes the following tasks:</span></span>

-   [<span data-ttu-id="04192-123">Usando um recurso Menu-Template</span><span class="sxs-lookup"><span data-stu-id="04192-123">Using a Menu-Template Resource</span></span>](#using-a-menu-template-resource)
    -   [<span data-ttu-id="04192-124">Formato de Menu-Template estendido</span><span class="sxs-lookup"><span data-stu-id="04192-124">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
    -   [<span data-ttu-id="04192-125">Antigo formato de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="04192-125">Old Menu-Template Format</span></span>](#old-menu-template-format)
    -   [<span data-ttu-id="04192-126">Carregando um recurso de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="04192-126">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
    -   [<span data-ttu-id="04192-127">Criando um menu de classe</span><span class="sxs-lookup"><span data-stu-id="04192-127">Creating a Class Menu</span></span>](#creating-a-class-menu)
-   [<span data-ttu-id="04192-128">Criando um menu de atalho</span><span class="sxs-lookup"><span data-stu-id="04192-128">Creating a Shortcut Menu</span></span>](#creating-a-shortcut-menu)
    -   [<span data-ttu-id="04192-129">Processando a \_ mensagem CONTEXTMENU do WM</span><span class="sxs-lookup"><span data-stu-id="04192-129">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
    -   [<span data-ttu-id="04192-130">Criando um menu de Font-Attributes de atalho</span><span class="sxs-lookup"><span data-stu-id="04192-130">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
    -   [<span data-ttu-id="04192-131">Exibindo um menu de atalho</span><span class="sxs-lookup"><span data-stu-id="04192-131">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)
-   [<span data-ttu-id="04192-132">Usando Menu-Item bitmaps</span><span class="sxs-lookup"><span data-stu-id="04192-132">Using Menu-Item Bitmaps</span></span>](#using-menu-item-bitmaps)
    -   [<span data-ttu-id="04192-133">Configurando o sinalizador de tipo de bitmap</span><span class="sxs-lookup"><span data-stu-id="04192-133">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
    -   [<span data-ttu-id="04192-134">Criando o bitmap</span><span class="sxs-lookup"><span data-stu-id="04192-134">Creating the Bitmap</span></span>](#creating-the-bitmap)
    -   [<span data-ttu-id="04192-135">Adicionando linhas e grafos a um menu</span><span class="sxs-lookup"><span data-stu-id="04192-135">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
    -   [<span data-ttu-id="04192-136">Exemplo de bitmaps de Menu-Item</span><span class="sxs-lookup"><span data-stu-id="04192-136">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)
-   [<span data-ttu-id="04192-137">Criando Owner-Drawn itens de menu</span><span class="sxs-lookup"><span data-stu-id="04192-137">Creating Owner-Drawn Menu Items</span></span>](#creating-owner-drawn-menu-items)
    -   [<span data-ttu-id="04192-138">Definindo o sinalizador de Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="04192-138">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
    -   [<span data-ttu-id="04192-139">Menus desenhados pelo proprietário e a mensagem do WM \_ MEASUREITEM</span><span class="sxs-lookup"><span data-stu-id="04192-139">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="04192-140">Menus desenhados pelo proprietário e a mensagem do WM \_ DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="04192-140">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="04192-141">Menus desenhados pelo proprietário e a mensagem do WM \_ MENUCHAR</span><span class="sxs-lookup"><span data-stu-id="04192-141">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
    -   [<span data-ttu-id="04192-142">Definindo fontes para Menu-Item cadeias de caracteres de texto</span><span class="sxs-lookup"><span data-stu-id="04192-142">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
    -   [<span data-ttu-id="04192-143">Exemplo de itens de menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="04192-143">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)
-   [<span data-ttu-id="04192-144">Usando bitmaps de marca de seleção personalizados</span><span class="sxs-lookup"><span data-stu-id="04192-144">Using Custom Check Mark Bitmaps</span></span>](#using-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="04192-145">Criando bitmaps de marca de seleção personalizados</span><span class="sxs-lookup"><span data-stu-id="04192-145">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="04192-146">Associando bitmaps a um item de menu</span><span class="sxs-lookup"><span data-stu-id="04192-146">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
    -   [<span data-ttu-id="04192-147">Definindo o atributo de marca de seleção</span><span class="sxs-lookup"><span data-stu-id="04192-147">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
    -   [<span data-ttu-id="04192-148">Simulando caixas de seleção em um menu</span><span class="sxs-lookup"><span data-stu-id="04192-148">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
    -   [<span data-ttu-id="04192-149">Exemplo de como usar bitmaps de marca de seleção personalizados</span><span class="sxs-lookup"><span data-stu-id="04192-149">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a><span data-ttu-id="04192-150">Usando um recurso Menu-Template</span><span class="sxs-lookup"><span data-stu-id="04192-150">Using a Menu-Template Resource</span></span>

<span data-ttu-id="04192-151">Normalmente, você inclui um menu em um aplicativo Criando um recurso de modelo de menu e, em seguida, carregando o menu em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="04192-151">You typically include a menu in an application by creating a menu-template resource and then loading the menu at run time.</span></span> <span data-ttu-id="04192-152">Esta seção descreve o formato de um modelo de menu e explica como carregar um recurso de modelo de menu e usá-lo em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-152">This section describes the format of a menu template, and explains how to load a menu-template resource and use it in your application.</span></span> <span data-ttu-id="04192-153">Para obter informações sobre como criar um recurso de modelo de menu, consulte a documentação incluída com suas ferramentas de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="04192-153">For information about creating a menu-template resource, see the documentation included with your development tools.</span></span>

-   [<span data-ttu-id="04192-154">Formato de Menu-Template estendido</span><span class="sxs-lookup"><span data-stu-id="04192-154">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
-   [<span data-ttu-id="04192-155">Antigo formato de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="04192-155">Old Menu-Template Format</span></span>](#old-menu-template-format)
-   [<span data-ttu-id="04192-156">Carregando um recurso de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="04192-156">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
-   [<span data-ttu-id="04192-157">Criando um menu de classe</span><span class="sxs-lookup"><span data-stu-id="04192-157">Creating a Class Menu</span></span>](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a><span data-ttu-id="04192-158">Formato de Menu-Template estendido</span><span class="sxs-lookup"><span data-stu-id="04192-158">Extended Menu-Template Format</span></span>

<span data-ttu-id="04192-159">O formato de modelo de menu estendido dá suporte à funcionalidade de menu adicional.</span><span class="sxs-lookup"><span data-stu-id="04192-159">The extended menu-template format supports additional menu functionality.</span></span> <span data-ttu-id="04192-160">Como os recursos de modelo de menu padrão, os recursos de modelo de menu estendido têm o tipo de recurso de **\_ menu RT** .</span><span class="sxs-lookup"><span data-stu-id="04192-160">Like standard menu-template resources, extended menu-template resources have the **RT\_MENU** resource type.</span></span> <span data-ttu-id="04192-161">O sistema distingue os dois formatos de recurso pelo número de versão, que é o primeiro membro do cabeçalho de recurso.</span><span class="sxs-lookup"><span data-stu-id="04192-161">The system distinguishes the two resource formats by the version number, which is the first member of the resource header.</span></span>

<span data-ttu-id="04192-162">Um modelo de menu estendido consiste em uma estrutura de [**\_ \_ cabeçalho de modelo MENUEX**](menuex-template-header.md) seguida por uma ou mais estruturas de definição de item de [**\_ \_ item de modelo MENUEX**](menuex-template-item.md) .</span><span class="sxs-lookup"><span data-stu-id="04192-162">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one more [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) item definition structures.</span></span>

### <a name="old-menu-template-format"></a><span data-ttu-id="04192-163">Antigo formato de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="04192-163">Old Menu-Template Format</span></span>

<span data-ttu-id="04192-164">Um modelo de menu antigo (Microsoft Windows NT 3,51 e anterior) define um menu, mas não oferece suporte à nova funcionalidade de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-164">An old menu template (Microsoft Windows NT 3.51 and earlier) defines a menu, but does not support the new menu functionality.</span></span> <span data-ttu-id="04192-165">Um recurso de modelo de menu antigo tem o tipo de recurso de **\_ menu RT** .</span><span class="sxs-lookup"><span data-stu-id="04192-165">An old menu-template resource has the **RT\_MENU** resource type.</span></span>

<span data-ttu-id="04192-166">Um modelo de menu antigo consiste em uma estrutura [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) seguida por uma ou mais estruturas [**MenuItemTemplate**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) .</span><span class="sxs-lookup"><span data-stu-id="04192-166">An old menu template consists of a [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) structure followed by one or more [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) structures.</span></span>

### <a name="loading-a-menu-template-resource"></a><span data-ttu-id="04192-167">Carregando um recurso de Menu-Template</span><span class="sxs-lookup"><span data-stu-id="04192-167">Loading a Menu-Template Resource</span></span>

<span data-ttu-id="04192-168">Para carregar um recurso de modelo de menu, use a função [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) , especificando um identificador para o módulo que contém o recurso e o identificador do modelo de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-168">To load a menu-template resource, use the [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) function, specifying a handle to the module that contains the resource and the menu template's identifier.</span></span> <span data-ttu-id="04192-169">A função **LoadMenu** retorna um identificador de menu que você pode usar para atribuir o menu a uma janela.</span><span class="sxs-lookup"><span data-stu-id="04192-169">The **LoadMenu** function returns a menu handle that you can use to assign the menu to a window.</span></span> <span data-ttu-id="04192-170">Essa janela torna-se a janela do proprietário do menu, recebendo todas as mensagens geradas pelo menu.</span><span class="sxs-lookup"><span data-stu-id="04192-170">This window becomes the menu's owner window, receiving all the messages generated by the menu.</span></span>

<span data-ttu-id="04192-171">Para criar um menu a partir de um modelo de menu que já está na memória, use a função [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="04192-171">To create a menu from a menu template that is already in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span> <span data-ttu-id="04192-172">Isso será útil se o aplicativo gerar modelos de menu dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="04192-172">This is useful if your application generates menu templates dynamically.</span></span>

<span data-ttu-id="04192-173">Para atribuir um menu a uma janela, use a função [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) ou especifique o identificador do menu no parâmetro *HMenu* da função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ao criar uma janela.</span><span class="sxs-lookup"><span data-stu-id="04192-173">To assign a menu to a window, use the [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) function or specify the menu's handle in the *hMenu* parameter of the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function when creating a window.</span></span> <span data-ttu-id="04192-174">Outra maneira de atribuir um menu a uma janela é especificar um modelo de menu ao registrar uma classe de janela; o modelo identifica o menu especificado como o menu de classe para essa classe de janela.</span><span class="sxs-lookup"><span data-stu-id="04192-174">Another way you can assign a menu to a window is to specify a menu template when you register a window class; the template identifies the specified menu as the class menu for that window class.</span></span>

<span data-ttu-id="04192-175">Para que o sistema atribua automaticamente um menu específico a uma janela, especifique o modelo do menu ao registrar a classe da janela.</span><span class="sxs-lookup"><span data-stu-id="04192-175">To have the system automatically assign a specific menu to a window, specify the menu's template when you register the window's class.</span></span> <span data-ttu-id="04192-176">O modelo identifica o menu especificado como o menu de classe para essa classe de janela.</span><span class="sxs-lookup"><span data-stu-id="04192-176">The template identifies the specified menu as the class menu for that window class.</span></span> <span data-ttu-id="04192-177">Em seguida, quando você cria uma janela da classe especificada, o sistema atribui automaticamente o menu especificado à janela.</span><span class="sxs-lookup"><span data-stu-id="04192-177">Then, when you create a window of the specified class, the system automatically assigns the specified menu to the window.</span></span>

<span data-ttu-id="04192-178">Você não pode atribuir um menu a uma janela que seja uma janela filho.</span><span class="sxs-lookup"><span data-stu-id="04192-178">You cannot assign a menu to a window that is a child window.</span></span>

<span data-ttu-id="04192-179">Para criar um menu de classe, inclua o identificador do recurso de modelo de menu como o membro **lpszMenuName** de uma estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) e, em seguida, passe um ponteiro para a estrutura para a função [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) .</span><span class="sxs-lookup"><span data-stu-id="04192-179">To create a class menu, include the identifier of the menu-template resource as the **lpszMenuName** member of a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure and then pass a pointer to the structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span>

### <a name="creating-a-class-menu"></a><span data-ttu-id="04192-180">Criando um menu de classe</span><span class="sxs-lookup"><span data-stu-id="04192-180">Creating a Class Menu</span></span>

<span data-ttu-id="04192-181">O exemplo a seguir mostra como criar um menu de classe para um aplicativo, criar uma janela que usa o menu de classe e processar comandos de menu no procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="04192-181">The following example shows how to create a class menu for an application, create a window that uses the class menu, and process menu commands in the window procedure.</span></span>

<span data-ttu-id="04192-182">A seguir está a parte relevante do arquivo de cabeçalho do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="04192-182">Following is the relevant portion of the application's header file:</span></span>


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



<span data-ttu-id="04192-183">A seguir estão as partes relevantes do próprio aplicativo:</span><span class="sxs-lookup"><span data-stu-id="04192-183">Following are the relevant portions of the application itself:</span></span>


```
HINSTANCE hinst; 
 
int APIENTRY WinMain(HINSTANCE hinstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg = { };  // message 
    WNDCLASS wc;    // windowclass data 
    HWND hwnd;      // handle to the main window 
 
    // Create the window class for the main window. Specify 
    // the identifier of the menu-template resource as the 
    // lpszMenuName member of the WNDCLASS structure to create 
    // the class menu. 
 
    wc.style = 0; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  MAKEINTRESOURCE(IDM_MYMENURESOURCE); 
    wc.lpszClassName = "MainWClass"; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    hinst = hinstance; 
 
    // Create the main window. Set the hmenu parameter to NULL so 
    // that the system uses the class menu for the window. 
 
    hwnd = CreateWindow("MainWClass", "Sample Application", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, hinstance, 
        NULL); 
 
    if (hwnd == NULL) 
        return FALSE; 
 
    // Make the window visible and send a WM_PAINT message to the 
    // window procedure. 
 
    ShowWindow(hwnd, nCmdShow); 
    UpdateWindow(hwnd); 
 
    // Start the main message loop. 
 
    while (GetMessage(&msg, NULL, 0, 0)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
    return msg.wParam; 
        UNREFERENCED_PARAMETER(hPrevInstance); 
} 
 
 
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    switch (uMsg) 
    { 
        // Process other window messages. 
 
        case WM_COMMAND: 
 
            // Test for the identifier of a command item. 
 
            switch(LOWORD(wParam)) 
            { 
                case IDM_FI_OPEN: 
                    DoFileOpen();   // application-defined 
                    break; 
 
                case IDM_FI_CLOSE: 
                    DoFileClose();  // application-defined 
                    break; 
                // Process other menu commands. 
 
                default: 
                    break; 
 
            } 
            return 0; 
 
        // Process other window messages. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="creating-a-shortcut-menu"></a><span data-ttu-id="04192-184">Criando um menu de atalho</span><span class="sxs-lookup"><span data-stu-id="04192-184">Creating a Shortcut Menu</span></span>

<span data-ttu-id="04192-185">Para usar um menu de atalho em um aplicativo, passe seu identificador para a função [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="04192-185">To use a shortcut menu in an application, pass its handle to the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="04192-186">Um aplicativo normalmente chama **TrackPopupMenuEx** em um procedimento de janela em resposta a uma mensagem gerada pelo usuário, como o [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) ou o [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown).</span><span class="sxs-lookup"><span data-stu-id="04192-186">An application typically calls **TrackPopupMenuEx** in a window procedure in response to a user-generated message, such as [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown).</span></span>

<span data-ttu-id="04192-187">Além do identificador do menu pop-up, o [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) exige que você especifique um identificador para a janela do proprietário, a posição do menu de atalho (nas coordenadas da tela) e o botão do mouse que o usuário pode usar para escolher um item.</span><span class="sxs-lookup"><span data-stu-id="04192-187">In addition to the pop-up menu handle, [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) requires that you specify a handle to the owner window, the position of the shortcut menu (in screen coordinates), and the mouse button that the user can use to choose an item.</span></span>

<span data-ttu-id="04192-188">A função [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) mais antiga ainda tem suporte, mas novos aplicativos devem usar a função [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="04192-188">The older [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function is still supported, but new applications should use the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="04192-189">A função **TrackPopupMenuEx** requer os mesmos parâmetros que **TrackPopupMenu**, mas também permite que você especifique uma parte da tela que o menu não deve obscurecer.</span><span class="sxs-lookup"><span data-stu-id="04192-189">The **TrackPopupMenuEx** function requires the same parameters as **TrackPopupMenu**, but also lets you specify a portion of the screen that the menu should not obscure.</span></span> <span data-ttu-id="04192-190">Normalmente, um aplicativo chama essas funções em um procedimento de janela ao processar a mensagem [**\_ CONTEXTMENU do WM**](wm-contextmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="04192-190">An application typically calls these functions in a window procedure when processing the [**WM\_CONTEXTMENU**](wm-contextmenu.md) message.</span></span>

<span data-ttu-id="04192-191">Você pode especificar a posição de um menu de atalho fornecendo coordenadas x e y juntamente com o sinalizador **TPM \_ CENTERALIGN**, **TPM \_ LEFTALIGN** ou **TPM \_ RIGHTALIGN** .</span><span class="sxs-lookup"><span data-stu-id="04192-191">You can specify the position of a shortcut menu by providing x- and y-coordinates along with the **TPM\_CENTERALIGN**, **TPM\_LEFTALIGN**, or **TPM\_RIGHTALIGN** flag.</span></span> <span data-ttu-id="04192-192">O sinalizador especifica a posição do menu de atalho em relação às coordenadas x e y.</span><span class="sxs-lookup"><span data-stu-id="04192-192">The flag specifies the position of the shortcut menu relative to the x- and y-coordinates.</span></span>

<span data-ttu-id="04192-193">Você deve permitir que o usuário escolha um item em um menu de atalho usando o mesmo botão do mouse usado para exibir o menu.</span><span class="sxs-lookup"><span data-stu-id="04192-193">You should permit the user to choose an item from a shortcut menu by using the same mouse button used to display the menu.</span></span> <span data-ttu-id="04192-194">Para fazer isso, especifique o sinalizador **TPM \_ LEFTBUTTON** ou **TPM \_ RIGHTBUTTON** para indicar qual botão do mouse o usuário pode usar para escolher um item de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-194">To do this, specify either **TPM\_LEFTBUTTON** or **TPM\_RIGHTBUTTON** flag to indicate which mouse button the user can use to choose a menu item.</span></span>

-   [<span data-ttu-id="04192-195">Processando a \_ mensagem CONTEXTMENU do WM</span><span class="sxs-lookup"><span data-stu-id="04192-195">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
-   [<span data-ttu-id="04192-196">Criando um menu de Font-Attributes de atalho</span><span class="sxs-lookup"><span data-stu-id="04192-196">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
-   [<span data-ttu-id="04192-197">Exibindo um menu de atalho</span><span class="sxs-lookup"><span data-stu-id="04192-197">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a><span data-ttu-id="04192-198">Processando a \_ mensagem CONTEXTMENU do WM</span><span class="sxs-lookup"><span data-stu-id="04192-198">Processing the WM\_CONTEXTMENU Message</span></span>

<span data-ttu-id="04192-199">A mensagem de [**\_ CONTEXTMENU do WM**](wm-contextmenu.md) é gerada quando um procedimento de janela do aplicativo passa a mensagem do [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) ou do [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="04192-199">The [**WM\_CONTEXTMENU**](wm-contextmenu.md) message is generated when an application's window procedure passes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="04192-200">O aplicativo pode processar essa mensagem para exibir um menu de atalho apropriado para uma parte específica de sua tela.</span><span class="sxs-lookup"><span data-stu-id="04192-200">The application can process this message to display a shortcut menu appropriate to a specific portion of its screen.</span></span> <span data-ttu-id="04192-201">Se o aplicativo não exibir um menu de atalho, ele deverá passar a mensagem para **DefWindowProc** para manipulação padrão.</span><span class="sxs-lookup"><span data-stu-id="04192-201">If the application does not display a shortcut menu, it should pass the message to **DefWindowProc** for default handling.</span></span>

<span data-ttu-id="04192-202">A seguir, um exemplo de processamento de mensagem [**\_ CONTEXTMENU do WM**](wm-contextmenu.md) como ele pode aparecer no procedimento de janela de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-202">Following is an example of [**WM\_CONTEXTMENU**](wm-contextmenu.md) message processing as it might appear in an application's window procedure.</span></span> <span data-ttu-id="04192-203">As palavras de ordem inferior e de ordem superior do parâmetro *lParam* especificam as coordenadas de tela do mouse quando o botão direito do mouse é liberado (Observe que essas coordenadas podem ter valores negativos em sistemas com vários monitores).</span><span class="sxs-lookup"><span data-stu-id="04192-203">The low-order and high-order words of the *lParam* parameter specify the screen coordinates of the mouse when the right mouse button is released (note that these coordinates can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="04192-204">A função **oncontextmenu** definida pelo aplicativo retornará **true** se exibir um menu de contexto ou **false** se não tiver.</span><span class="sxs-lookup"><span data-stu-id="04192-204">The application-defined **OnContextMenu** function returns **TRUE** if it displays a context menu, or **FALSE** if it does not.</span></span>


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



<span data-ttu-id="04192-205">A função oncontextmenu definida pelo aplicativo a seguir exibirá um menu de atalho se a posição do mouse especificada estiver dentro da área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="04192-205">The following application-defined OnContextMenu function displays a shortcut menu if the specified mouse position is within the window's client area.</span></span> <span data-ttu-id="04192-206">Uma função mais sofisticada pode exibir um dos vários menus diferentes, dependendo de qual parte da área do cliente é especificada.</span><span class="sxs-lookup"><span data-stu-id="04192-206">A more sophisticated function might display one of several different menus, depending on which portion of the client area is specified.</span></span> <span data-ttu-id="04192-207">Para realmente exibir o menu de atalho, este exemplo chama uma função definida pelo aplicativo chamada DisplayContextMenu.</span><span class="sxs-lookup"><span data-stu-id="04192-207">To actually display the shortcut menu, this example calls an application-defined function called DisplayContextMenu.</span></span> <span data-ttu-id="04192-208">Para obter uma descrição dessa função, consulte [exibindo um menu de atalho](#displaying-a-shortcut-menu).</span><span class="sxs-lookup"><span data-stu-id="04192-208">For a description of this function, see [Displaying a Shortcut Menu](#displaying-a-shortcut-menu).</span></span>


```
BOOL WINAPI OnContextMenu(HWND hwnd, int x, int y) 
{ 
    RECT rc;                    // client area of window 
    POINT pt = { x, y };        // location of mouse click 
 
    // Get the bounding rectangle of the client area. 
 
    GetClientRect(hwnd, &rc); 
 
    // Convert the mouse position to client coordinates. 
 
    ScreenToClient(hwnd, &pt); 
 
    // If the position is in the client area, display a  
    // shortcut menu. 
 
    if (PtInRect(&rc, pt)) 
    { 
        ClientToScreen(hwnd, &pt); 
        DisplayContextMenu(hwnd, pt); 
        return TRUE; 
    } 
 
    // Return FALSE if no menu is displayed. 
 
    return FALSE; 
} 
```



### <a name="creating-a-shortcut-font-attributes-menu"></a><span data-ttu-id="04192-209">Criando um menu de Font-Attributes de atalho</span><span class="sxs-lookup"><span data-stu-id="04192-209">Creating a Shortcut Font-Attributes Menu</span></span>

<span data-ttu-id="04192-210">O exemplo nesta seção contém partes do código de um aplicativo que cria e exibe um menu de atalho que permite ao usuário definir fontes e atributos de fonte.</span><span class="sxs-lookup"><span data-stu-id="04192-210">The example in this section contains portions of code from an application that creates and displays a shortcut menu that enables the user to set fonts and font attributes.</span></span> <span data-ttu-id="04192-211">O aplicativo exibe o menu na área do cliente de sua janela principal sempre que o usuário clica no botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="04192-211">The application displays the menu in the client area of its main window whenever the user clicks the left mouse button.</span></span>

<span data-ttu-id="04192-212">Aqui está o modelo de menu para o menu de atalho que é fornecido no arquivo de definição de recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-212">Here is the menu template for the shortcut menu that is provided in the application's resource-definition file.</span></span>


```
PopupMenu MENU 
BEGIN 
  POPUP "Dummy Popup" 
    BEGIN 
      POPUP "Fonts" 
        BEGIN 
          MENUITEM "Courier",     IDM_FONT_COURIER 
          MENUITEM "Times Roman", IDM_FONT_TMSRMN 
          MENUITEM "Swiss",       IDM_FONT_SWISS 
          MENUITEM "Helvetica",   IDM_FONT_HELV 
          MENUITEM "Old English", IDM_FONT_OLDENG 
        END 
      POPUP "Sizes" 
        BEGIN 
          MENUITEM "7",  IDM_SIZE_7 
          MENUITEM "8",  IDM_SIZE_8 
          MENUITEM "9",  IDM_SIZE_9 
          MENUITEM "10", IDM_SIZE_10 
          MENUITEM "11", IDM_SIZE_11 
          MENUITEM "12", IDM_SIZE_12 
          MENUITEM "14", IDM_SIZE_14 
        END 
      POPUP "Styles" 
        BEGIN 
          MENUITEM "Bold",        IDM_STYLE_BOLD 
          MENUITEM "Italic",      IDM_STYLE_ITALIC 
          MENUITEM "Strike Out",  IDM_STYLE_SO 
          MENUITEM "Superscript", IDM_STYLE_SUPER 
          MENUITEM "Subscript",   IDM_STYLE_SUB 
        END 
    END 
 
END 
```



<span data-ttu-id="04192-213">O exemplo a seguir fornece o procedimento de janela e as funções de suporte usadas para criar e exibir o menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="04192-213">The following example gives the window procedure and supporting functions used to create and display the shortcut menu.</span></span>


```
LRESULT APIENTRY MenuWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rc;    // client area             
    POINT pt;   // location of mouse click  
 
    switch (uMsg) 
    { 
        case WM_LBUTTONDOWN: 
 
            // Get the bounding rectangle of the client area. 
 
            GetClientRect(hwnd, (LPRECT) &rc); 
 
            // Get the client coordinates for the mouse click.  
 
            pt.x = GET_X_LPARAM(lParam); 
            pt.y = GET_Y_LPARAM(lParam); 
 
            // If the mouse click took place inside the client 
            // area, execute the application-defined function 
            // that displays the shortcut menu. 
 
            if (PtInRect((LPRECT) &rc, pt)) 
                HandlePopupMenu(hwnd, pt); 
            break; 
        // Process other window messages.  
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
 
VOID APIENTRY HandlePopupMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // menu template          
    HMENU hmenuTrackPopup;  // shortcut menu   
 
    //  Load the menu template containing the shortcut menu from the 
    //  application's resources. 
 
    hmenu = LoadMenu(hinst, "PopupMenu"); 
    if (hmenu == NULL) 
        return; 
 
    // Get the first shortcut menu in the menu template. This is the 
    // menu that TrackPopupMenu displays. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // TrackPopup uses screen coordinates, so convert the 
    // coordinates of the mouse click to screen coordinates. 
 
    ClientToScreen(hwnd, (LPPOINT) &pt); 
 
    // Draw and track the shortcut menu.  
 
    TrackPopupMenu(hmenuTrackPopup, TPM_LEFTALIGN | TPM_LEFTBUTTON, 
        pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



### <a name="displaying-a-shortcut-menu"></a><span data-ttu-id="04192-214">Exibindo um menu de atalho</span><span class="sxs-lookup"><span data-stu-id="04192-214">Displaying a Shortcut Menu</span></span>

<span data-ttu-id="04192-215">A função mostrada no exemplo a seguir exibe um menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="04192-215">The function shown in the following example displays a shortcut menu.</span></span>

<span data-ttu-id="04192-216">O aplicativo inclui um recurso de menu identificado pela cadeia de caracteres "ShortcutExample".</span><span class="sxs-lookup"><span data-stu-id="04192-216">The application includes a menu resource identified by the string "ShortcutExample."</span></span> <span data-ttu-id="04192-217">A barra de menus simplesmente contém um nome de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-217">The menu bar simply contains a menu name.</span></span> <span data-ttu-id="04192-218">O aplicativo usa a função [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) para exibir o menu associado a esse item de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-218">The application uses the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function to display the menu associated with this menu item.</span></span> <span data-ttu-id="04192-219">(A própria barra de menus não é exibida porque **TrackPopupMenu** requer um identificador para um menu, submenu ou menu de atalho.)</span><span class="sxs-lookup"><span data-stu-id="04192-219">(The menu bar itself is not displayed because **TrackPopupMenu** requires a handle to a menu, submenu, or shortcut menu.)</span></span>


```
VOID APIENTRY DisplayContextMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // top-level menu 
    HMENU hmenuTrackPopup;  // shortcut menu 
 
    // Load the menu resource. 
 
    if ((hmenu = LoadMenu(hinst, "ShortcutExample")) == NULL) 
        return; 
 
    // TrackPopupMenu cannot display the menu bar so get 
    // a handle to the first shortcut menu. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // Display the shortcut menu. Track the right mouse 
    // button. 
 
    TrackPopupMenu(hmenuTrackPopup, 
            TPM_LEFTALIGN | TPM_RIGHTBUTTON, 
            pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



## <a name="using-menu-item-bitmaps"></a><span data-ttu-id="04192-220">Usando Menu-Item bitmaps</span><span class="sxs-lookup"><span data-stu-id="04192-220">Using Menu-Item Bitmaps</span></span>

<span data-ttu-id="04192-221">O sistema pode usar um bitmap em vez de uma cadeia de texto para exibir um item de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-221">The system can use a bitmap instead of a text string to display a menu item.</span></span> <span data-ttu-id="04192-222">Para usar um bitmap, você deve definir o sinalizador de **\_ bitmap MIIM** para o item de menu e especificar um identificador para o bitmap que o sistema deve exibir para o item de menu no membro **hbmpItem** da estrutura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="04192-222">To use a bitmap, you must set the **MIIM\_BITMAP** flag for the menu item and specify a handle to the bitmap that the system should display for the menu item in the **hbmpItem** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="04192-223">Esta seção descreve como usar bitmaps para itens de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-223">This section describes how to use bitmaps for menu items.</span></span>

-   [<span data-ttu-id="04192-224">Configurando o sinalizador de tipo de bitmap</span><span class="sxs-lookup"><span data-stu-id="04192-224">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
-   [<span data-ttu-id="04192-225">Criando o bitmap</span><span class="sxs-lookup"><span data-stu-id="04192-225">Creating the Bitmap</span></span>](#creating-the-bitmap)
-   [<span data-ttu-id="04192-226">Adicionando linhas e grafos a um menu</span><span class="sxs-lookup"><span data-stu-id="04192-226">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
-   [<span data-ttu-id="04192-227">Exemplo de bitmaps de Menu-Item</span><span class="sxs-lookup"><span data-stu-id="04192-227">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a><span data-ttu-id="04192-228">Configurando o sinalizador de tipo de bitmap</span><span class="sxs-lookup"><span data-stu-id="04192-228">Setting the Bitmap Type Flag</span></span>

<span data-ttu-id="04192-229">O **sinalizador \_ bitmap MIIM** ou **\_ MF** mostra o sistema para usar um bitmap em vez de uma cadeia de texto para exibir um item de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-229">The **MIIM\_BITMAP** or **MF\_BITMAP** flag tells the system to use a bitmap rather than a text string to display a menu item.</span></span> <span data-ttu-id="04192-230">Um **\_ bitmap MIIM** de um item de menu ou um sinalizador de **\_ bitmap MF** deve ser definido em tempo de execução; você não pode defini-lo no arquivo de definição de recurso.</span><span class="sxs-lookup"><span data-stu-id="04192-230">A menu item's **MIIM\_BITMAP** or **MF\_BITMAP** flag must be set at run time; you cannot set it in the resource-definition file.</span></span>

<span data-ttu-id="04192-231">Para novos aplicativos, você pode usar a função [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) ou [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) para definir o sinalizador de tipo de **\_ bitmap MIIM** .</span><span class="sxs-lookup"><span data-stu-id="04192-231">For new applications, you can use the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) or [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) function to set the **MIIM\_BITMAP** type flag.</span></span> <span data-ttu-id="04192-232">Para alterar um item de menu de um item de texto para um item de bitmap, use **SetMenuItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="04192-232">To change a menu item from a text item to a bitmap item, use **SetMenuItemInfo**.</span></span> <span data-ttu-id="04192-233">Para adicionar um novo item de bitmap a um menu, use a função **InsertMenuItem** .</span><span class="sxs-lookup"><span data-stu-id="04192-233">To add a new bitmap item to a menu, use the **InsertMenuItem** function.</span></span>

<span data-ttu-id="04192-234">Os aplicativos escritos para versões anteriores do sistema podem continuar a usar as funções [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)ou [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) para definir o sinalizador **de \_ bitmap MF** .</span><span class="sxs-lookup"><span data-stu-id="04192-234">Applications written for earlier versions of the system can continue to use the [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to set the **MF\_BITMAP** flag.</span></span> <span data-ttu-id="04192-235">Para alterar um item de menu de um item de cadeia de texto para um item de bitmap, use **ModifyMenu**.</span><span class="sxs-lookup"><span data-stu-id="04192-235">To change a menu item from a text string item to a bitmap item, use **ModifyMenu**.</span></span> <span data-ttu-id="04192-236">Para adicionar um novo item de bitmap a um menu, use o sinalizador de **\_ bitmap MF** com a função **InsertMenu** ou **AppendMenu** .</span><span class="sxs-lookup"><span data-stu-id="04192-236">To add a new bitmap item to a menu, use the **MF\_BITMAP** flag with the **InsertMenu** or **AppendMenu** function.</span></span>

### <a name="creating-the-bitmap"></a><span data-ttu-id="04192-237">Criando o bitmap</span><span class="sxs-lookup"><span data-stu-id="04192-237">Creating the Bitmap</span></span>

<span data-ttu-id="04192-238">Quando você define o **sinalizador \_ bitmap MIIM** ou tipo de **\_ bitmap MF** para um item de menu, também deve especificar um identificador para o bitmap que o sistema deve exibir para o item de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-238">When you set the **MIIM\_BITMAP** or **MF\_BITMAP** type flag for a menu item, you must also specify a handle to the bitmap that the system should display for the menu item.</span></span> <span data-ttu-id="04192-239">Você pode fornecer o bitmap como um recurso de bitmap ou criar o bitmap em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="04192-239">You can provide the bitmap as a bitmap resource or create the bitmap at run time.</span></span> <span data-ttu-id="04192-240">Se você usar um recurso de bitmap, poderá usar a função [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) para carregar o bitmap e obter seu identificador.</span><span class="sxs-lookup"><span data-stu-id="04192-240">If you use a bitmap resource, you can use the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function to load the bitmap and obtain its handle.</span></span>

<span data-ttu-id="04192-241">Para criar o bitmap em tempo de execução, use as funções do Windows Graphics Device Interface (GDI).</span><span class="sxs-lookup"><span data-stu-id="04192-241">To create the bitmap at run time, use Windows Graphics Device Interface (GDI) functions.</span></span> <span data-ttu-id="04192-242">O GDI fornece várias maneiras de criar um bitmap em tempo de execução, mas os desenvolvedores normalmente usam o seguinte método:</span><span class="sxs-lookup"><span data-stu-id="04192-242">GDI provides several ways to create a bitmap at run time, but developers typically use the following method:</span></span>

1.  <span data-ttu-id="04192-243">Use a função [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) para criar um contexto de dispositivo compatível com o contexto do dispositivo usado pela janela principal do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-243">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the device context used by the application's main window.</span></span>
2.  <span data-ttu-id="04192-244">Use a função [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) para criar um bitmap compatível com a janela principal do aplicativo ou use a função [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) para criar um bitmap monocromático.</span><span class="sxs-lookup"><span data-stu-id="04192-244">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window or use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>
3.  <span data-ttu-id="04192-245">Use a função [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) para selecionar o bitmap no contexto do dispositivo compatível.</span><span class="sxs-lookup"><span data-stu-id="04192-245">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="04192-246">Use funções de desenho GDI, como [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) e [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), para desenhar uma imagem no bitmap.</span><span class="sxs-lookup"><span data-stu-id="04192-246">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap.</span></span>

<span data-ttu-id="04192-247">Para obter mais informações, consulte [bitmaps](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="04192-247">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="adding-lines-and-graphs-to-a-menu"></a><span data-ttu-id="04192-248">Adicionando linhas e grafos a um menu</span><span class="sxs-lookup"><span data-stu-id="04192-248">Adding Lines and Graphs to a Menu</span></span>

<span data-ttu-id="04192-249">O exemplo de código a seguir mostra como criar um menu que contém bitmaps de item de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-249">The following code sample shows how to create a menu that contains menu-item bitmaps.</span></span> <span data-ttu-id="04192-250">Ele cria dois menus.</span><span class="sxs-lookup"><span data-stu-id="04192-250">It creates two menus.</span></span> <span data-ttu-id="04192-251">O primeiro é um menu de gráfico que contém três bitmaps de item de menu: um gráfico de pizza, um gráfico de linhas e um gráfico de barras.</span><span class="sxs-lookup"><span data-stu-id="04192-251">The first is a Chart menu that contains three menu-item bitmaps: a pie chart, a line chart, and a bar chart.</span></span> <span data-ttu-id="04192-252">O exemplo demonstra como carregar esses bitmaps do arquivo de recursos do aplicativo e, em seguida, usar as funções [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) e [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) para criar os itens de menu e menu.</span><span class="sxs-lookup"><span data-stu-id="04192-252">The example demonstrates how to load these bitmaps from the application's resource file, and then use the [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) and [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to create the menu and menu items.</span></span>

<span data-ttu-id="04192-253">O segundo menu é um menu de linhas.</span><span class="sxs-lookup"><span data-stu-id="04192-253">The second menu is a Lines menu.</span></span> <span data-ttu-id="04192-254">Ele contém bitmaps que mostram os estilos de linha fornecidos pela caneta predefinida no sistema.</span><span class="sxs-lookup"><span data-stu-id="04192-254">It contains bitmaps showing the line styles provided by the predefined pen in the system.</span></span> <span data-ttu-id="04192-255">Os bitmaps de estilo de linha são criados em tempo de execução usando funções GDI.</span><span class="sxs-lookup"><span data-stu-id="04192-255">The line-style bitmaps are created at run time by using GDI functions.</span></span>

<span data-ttu-id="04192-256">Aqui estão as definições dos recursos de bitmap no arquivo de definição de recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-256">Here are the definitions of the bitmap resources in the application's resource-definition file.</span></span>


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



<span data-ttu-id="04192-257">Aqui estão as partes relevantes do arquivo de cabeçalho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-257">Here are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers 
 
#define IDM_SOLID       PS_SOLID 
#define IDM_DASH        PS_DASH 
#define IDM_DASHDOT     PS_DASHDOT 
#define IDM_DASHDOTDOT  PS_DASHDOTDOT 
 
#define IDM_PIE  1 
#define IDM_LINE 2 
#define IDM_BAR  3 
 
// Line-type flags  
 
#define SOLID       0 
#define DOT         1 
#define DASH        2 
#define DASHDOT     3 
#define DASHDOTDOT  4 
 
// Count of pens  
 
#define CPENS 5 
 
// Chart-type flags  
 
#define PIE  1 
#define LINE 2 
#define BAR  3 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
VOID MakeChartMenu(HWND); 
VOID MakeLineMenu(HWND, HPEN, HBITMAP); 
```



<span data-ttu-id="04192-258">O exemplo a seguir mostra como os menus e bitmaps de item de menu são criados em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-258">The following example shows how menus and menu-item bitmaps are created in an application.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HPEN hpen[CPENS]; 
    static HBITMAP hbmp[CPENS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create the Chart and Line menus.  
 
            MakeChartMenu(hwnd); 
            MakeLineMenu(hwnd, hpen, hbmp); 
            return 0; 
 
        // Process other window messages. 
 
        case WM_DESTROY: 
 
            for (i = 0; i < CPENS; i++) 
            { 
                DeleteObject(hbmp[i]); 
                DeleteObject(hpen[i]); 
            } 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
VOID MakeChartMenu(HWND hwnd) 
{ 
    HBITMAP hbmpPie;    // handle to pie chart bitmap   
    HBITMAP hbmpLine;   // handle to line chart bitmap  
    HBITMAP hbmpBar;    // handle to bar chart bitmap   
    HMENU hmenuMain;    // handle to main menu          
    HMENU hmenuChart;   // handle to Chart menu  
 
    // Load the pie, line, and bar chart bitmaps from the 
    // resource-definition file. 
 
    hbmpPie = LoadBitmap(hinst, MAKEINTRESOURCE(PIE)); 
    hbmpLine = LoadBitmap(hinst, MAKEINTRESOURCE(LINE)); 
    hbmpBar = LoadBitmap(hinst, MAKEINTRESOURCE(BAR)); 
 
    // Create the Chart menu and add it to the menu bar. 
    // Append the Pie, Line, and Bar menu items to the Chart 
    // menu. 
 
    hmenuMain = GetMenu(hwnd); 
    hmenuChart = CreatePopupMenu(); 
    AppendMenu(hmenuMain, MF_STRING | MF_POPUP, (UINT) hmenuChart, 
        "Chart"); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_PIE, (LPCTSTR) hbmpPie); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_LINE, 
        (LPCTSTR) hbmpLine); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_BAR, (LPCTSTR) hbmpBar); 
 
    return; 
} 
 
VOID MakeLineMenu(HWND hwnd, HPEN phpen, HBITMAP phbmp) 
{ 
    HMENU hmenuLines;       // handle to Lines menu      
    HMENU hmenu;            // handle to main menu              
    COLORREF crMenuClr;     // menu-item background color       
    HBRUSH hbrBackground;   // handle to background brush       
    HBRUSH hbrOld;          // handle to previous brush         
    WORD wLineX;            // width of line bitmaps            
    WORD wLineY;            // height of line bitmaps           
    HDC hdcMain;            // handle to main window's DC       
    HDC hdcLines;           // handle to compatible DC          
    HBITMAP hbmpOld;        // handle to previous bitmap        
    int i;                  // loop counter                     
 
    // Create the Lines menu. Add it to the menu bar.  
 
    hmenu = GetMenu(hwnd); 
    hmenuLines = CreatePopupMenu(); 
    AppendMenu(hmenu, MF_STRING | MF_POPUP, 
        (UINT) hmenuLines, "&Lines"); 
 
    // Create a brush for the menu-item background color.  
 
    crMenuClr = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crMenuClr); 
 
    // Create a compatible device context for the line bitmaps, 
    // and then select the background brush into it. 
 
    hdcMain = GetDC(hwnd); 
    hdcLines = CreateCompatibleDC(hdcMain); 
    hbrOld = SelectObject(hdcLines, hbrBackground); 
 
    // Get the dimensions of the check-mark bitmap. The width of 
    // the line bitmaps will be five times the width of the 
    // check-mark bitmap. 
 
    wLineX = GetSystemMetrics(SM_CXMENUCHECK) * (WORD) 5; 
    wLineY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    // Create the bitmaps and select them, one at a time, into the 
    // compatible device context. Initialize each bitmap by 
    // filling it with the menu-item background color. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        phbmp[i] = CreateCompatibleBitmap(hdcMain, wLineX, wLineY); 
        if (i == 0) 
            hbmpOld = SelectObject(hdcLines, phbmp[i]); 
        else 
            SelectObject(hdcLines, phbmp[i]); 
        ExtFloodFill(hdcLines, 0, 0, crMenuClr, FLOODFILLBORDER); 
    } 
 
    // Create the pens.  
 
    phpen[0] = CreatePen(PS_SOLID, 1, RGB(0, 0, 0)); 
    phpen[1] = CreatePen(PS_DOT, 1, RGB(0, 0, 0)); 
    phpen[2] = CreatePen(PS_DASH, 1, RGB(0, 0, 0)); 
    phpen[3] = CreatePen(PS_DASHDOT, 1, RGB(0, 0, 0)); 
    phpen[4] = CreatePen(PS_DASHDOTDOT, 1, RGB(0, 0, 0)); 
 
    // Select a pen and a bitmap into the compatible device 
    // context, draw a line into the bitmap, and then append 
    // the bitmap as an item in the Lines menu. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        SelectObject(hdcLines, phbmp[i]); 
        SelectObject(hdcLines, phpen[i]); 
        MoveToEx(hdcLines, 0, wLineY / 2, NULL); 
        LineTo(hdcLines, wLineX, wLineY / 2); 
        AppendMenu(hmenuLines, MF_BITMAP, i + 1, 
            (LPCTSTR) phbmp[i]); 
    } 
 
    // Release the main window's device context and destroy the 
    // compatible device context. Also, destroy the background 
    // brush. 
 
    ReleaseDC(hwnd, hdcMain); 
    SelectObject(hdcLines, hbrOld); 
    DeleteObject(hbrBackground); 
    SelectObject(hdcLines, hbmpOld); 
    DeleteDC(hdcLines); 
 
    return; 
} 
```



### <a name="example-of-menu-item-bitmaps"></a><span data-ttu-id="04192-259">Exemplo de bitmaps de Menu-Item</span><span class="sxs-lookup"><span data-stu-id="04192-259">Example of Menu-Item Bitmaps</span></span>

<span data-ttu-id="04192-260">O exemplo neste tópico cria dois menus, cada um contendo vários itens de menu de bitmap.</span><span class="sxs-lookup"><span data-stu-id="04192-260">The example in this topic creates two menus, each containing several bitmap menu items.</span></span> <span data-ttu-id="04192-261">Para cada menu, o aplicativo adiciona um nome de menu correspondente à barra de menus da janela principal.</span><span class="sxs-lookup"><span data-stu-id="04192-261">For each menu, the application adds a corresponding menu name to the main window's menu bar.</span></span>

<span data-ttu-id="04192-262">O primeiro menu contém itens de menu mostrando cada um dos três tipos de gráfico: pizza, linha e barra.</span><span class="sxs-lookup"><span data-stu-id="04192-262">The first menu contains menu items showing each of three chart types: pie, line, and bar.</span></span> <span data-ttu-id="04192-263">Os bitmaps desses itens de menu são definidos como recursos e carregados usando a função [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) .</span><span class="sxs-lookup"><span data-stu-id="04192-263">The bitmaps for these menu items are defined as resources and are loaded by using the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function.</span></span> <span data-ttu-id="04192-264">Associado a esse menu há um nome de menu "gráfico" na barra de menus.</span><span class="sxs-lookup"><span data-stu-id="04192-264">Associated with this menu is a "Chart" menu name on the menu bar.</span></span>

<span data-ttu-id="04192-265">O segundo menu contém itens de menu mostrando cada um dos cinco estilos de linha usados com a função [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) : **PS \_ Solid**, **PS \_ Dash**, **PS \_ dot**, **PS \_ travessão ponto** e **PS \_ travessão ponto ponto**.</span><span class="sxs-lookup"><span data-stu-id="04192-265">The second menu contains menu items showing each of the five line styles used with the [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) function: **PS\_SOLID**, **PS\_DASH**, **PS\_DOT**, **PS\_DASHDOT**, and **PS\_DASHDOTDOT**.</span></span> <span data-ttu-id="04192-266">O aplicativo cria os bitmaps para esses itens de menu em tempo de execução usando funções de desenho GDI.</span><span class="sxs-lookup"><span data-stu-id="04192-266">The application creates the bitmaps for these menu items at run time using GDI drawing functions.</span></span> <span data-ttu-id="04192-267">Associado a esse menu há um nome de menu de **linhas** na barra de menus.</span><span class="sxs-lookup"><span data-stu-id="04192-267">Associated with this menu is a **Lines** menu name on the menu bar.</span></span>

<span data-ttu-id="04192-268">Definido no procedimento de janela do aplicativo são duas matrizes estáticas de identificadores de bitmap.</span><span class="sxs-lookup"><span data-stu-id="04192-268">Defined in the application's window procedure are two static arrays of bitmap handles.</span></span> <span data-ttu-id="04192-269">Uma matriz contém os identificadores dos três bitmaps usados para o menu de **gráfico** .</span><span class="sxs-lookup"><span data-stu-id="04192-269">One array contains the handles of the three bitmaps used for the **Chart** menu.</span></span> <span data-ttu-id="04192-270">O outro contém os identificadores dos cinco bitmaps usados para o menu **linhas** .</span><span class="sxs-lookup"><span data-stu-id="04192-270">The other contains the handles of the five bitmaps used for the **Lines** menu.</span></span> <span data-ttu-id="04192-271">Ao processar a mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) , o procedimento de janela carrega os bitmaps de gráfico, cria os bitmaps de linha e, em seguida, adiciona os itens de menu correspondentes.</span><span class="sxs-lookup"><span data-stu-id="04192-271">When processing the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, the window procedure loads the chart bitmaps, creates the line bitmaps, and then adds the corresponding menu items.</span></span> <span data-ttu-id="04192-272">Ao processar a mensagem de [**\_ destruição do WM**](/windows/desktop/winmsg/wm-destroy) , o procedimento de janela exclui todos os bitmaps.</span><span class="sxs-lookup"><span data-stu-id="04192-272">When processing the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the window procedure deletes all of the bitmaps.</span></span>

<span data-ttu-id="04192-273">A seguir estão as partes relevantes do arquivo de cabeçalho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-273">Following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers 
 
#define IDM_PIE         1 
#define IDM_LINE        2 
#define IDM_BAR         3 
 
#define IDM_SOLID       4 
#define IDM_DASH        5 
#define IDM_DASHDOT     6 
#define IDM_DASHDOTDOT  7 
 
// Number of items on the Chart and Lines menus 
 
#define C_LINES         5 
#define C_CHARTS        3 
 
// Bitmap resource identifiers 
 
#define IDB_PIE         1 
#define IDB_LINE        2 
#define IDB_BAR         3 
 
// Dimensions of the line bitmaps 
 
#define CX_LINEBMP      40 
#define CY_LINEBMP      10 
```



<span data-ttu-id="04192-274">A seguir estão as partes relevantes do procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="04192-274">Following are the relevant portions of the window procedure.</span></span> <span data-ttu-id="04192-275">O procedimento de janela executa a maior parte de sua inicialização chamando as funções LoadChartBitmaps, CreateLineBitmaps e AddBitmapMenu definidas pelo aplicativo, descritas posteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="04192-275">The window procedure performs most of its initialization by calling the application-defined LoadChartBitmaps, CreateLineBitmaps, and AddBitmapMenu functions, described later in this topic.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    static HBITMAP aHbmLines[C_LINES]; 
    static HBITMAP aHbmChart[C_CHARTS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
             // Call application-defined functions to load the 
             // bitmaps for the Chart menu and create those for 
             // the Lines menu. 
 
            LoadChartBitmaps(aHbmChart); 
            CreateLineBitmaps(aHbmLines); 
 
             // Call an application-defined function to create 
             // menus containing the bitmap menu items. The function 
             // also adds a menu name to the window's menu bar. 
 
            AddBitmapMenu( 
                    hwnd,      // menu bar's owner window 
                    "&Chart",  // text of menu name on menu bar 
                    IDM_PIE,   // ID of first item on menu 
                    aHbmChart, // array of bitmap handles 
                    C_CHARTS   // number of items on menu 
                    ); 
            AddBitmapMenu(hwnd, "&Lines", IDM_SOLID, 
                    aHbmLines, C_LINES); 
            break; 
 
        case WM_DESTROY: 
            for (i = 0; i < C_LINES; i++) 
                DeleteObject(aHbmLines[i]); 
            for (i = 0; i < C_CHARTS; i++) 
                DeleteObject(aHbmChart[i]); 
            PostQuitMessage(0); 
            break; 
 
        // Process additional messages here. 
 
        default: 
            return (DefWindowProc(hwnd, uMsg, wParam, lParam)); 
    } 
    return 0; 
} 
```



<span data-ttu-id="04192-276">A função LoadChartBitmaps definida pelo aplicativo carrega os recursos de bitmap para o menu do gráfico chamando a função [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) , da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="04192-276">The application-defined LoadChartBitmaps function loads the bitmap resources for the chart menu by calling the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, as follows.</span></span>


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



<span data-ttu-id="04192-277">A função CreateLineBitmaps definida pelo aplicativo cria os bitmaps para o menu linhas usando funções de desenho GDI.</span><span class="sxs-lookup"><span data-stu-id="04192-277">The application-defined CreateLineBitmaps function creates the bitmaps for the Lines menu by using GDI drawing functions.</span></span> <span data-ttu-id="04192-278">A função cria um DC (contexto de dispositivo de memória) com as mesmas propriedades que o DC da janela da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="04192-278">The function creates a memory device context (DC) with the same properties as the desktop window's DC.</span></span> <span data-ttu-id="04192-279">Para cada estilo de linha, a função cria um bitmap, seleciona-o no controlador de domínio de memória e o desenha.</span><span class="sxs-lookup"><span data-stu-id="04192-279">For each line style, the function creates a bitmap, selects it into the memory DC, and draws in it.</span></span>


```
VOID WINAPI CreateLineBitmaps(HBITMAP *paHbm) 
{ 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
    COLORREF clrMenu = GetSysColor(COLOR_MENU); 
    HBRUSH hbrOld; 
    HPEN hpenOld; 
    HBITMAP hbmOld; 
    int fnDrawMode; 
    int i; 
 
     // Create a brush using the menu background color, 
     // and select it into the memory DC. 
 
    hbrOld = SelectObject(hdcMem, CreateSolidBrush(clrMenu)); 
 
     // Create the bitmaps. Select each one into the memory 
     // DC that was created and draw in it. 
 
    for (i = 0; i < C_LINES; i++) 
    { 
        // Create the bitmap and select it into the DC. 
 
        paHbm[i] = CreateCompatibleBitmap(hdcDesktop, 
                CX_LINEBMP, CY_LINEBMP); 
        hbmOld = SelectObject(hdcMem, paHbm[i]); 
 
        // Fill the background using the brush. 
 
        PatBlt(hdcMem, 0, 0, CX_LINEBMP, CY_LINEBMP, PATCOPY); 
 
        // Create the pen and select it into the DC. 
 
        hpenOld = SelectObject(hdcMem, 
                CreatePen(PS_SOLID + i, 1, RGB(0, 0, 0))); 
 
         // Draw the line. To preserve the background color where 
         // the pen is white, use the R2_MASKPEN drawing mode. 
 
        fnDrawMode = SetROP2(hdcMem, R2_MASKPEN); 
        MoveToEx(hdcMem, 0, CY_LINEBMP / 2, NULL); 
        LineTo(hdcMem, CX_LINEBMP, CY_LINEBMP / 2); 
        SetROP2(hdcMem, fnDrawMode); 
 
        // Delete the pen, and select the old pen and bitmap. 
 
        DeleteObject(SelectObject(hdcMem, hpenOld)); 
        SelectObject(hdcMem, hbmOld); 
    } 
 
    // Delete the brush and select the original brush. 
 
    DeleteObject(SelectObject(hdcMem, hbrOld)); 
 
    // Delete the memory DC and release the desktop DC. 
 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
} 
```



<span data-ttu-id="04192-280">A função AddBitmapMenu definida pelo aplicativo cria um menu e adiciona o número especificado de itens de menu de bitmap a ele.</span><span class="sxs-lookup"><span data-stu-id="04192-280">The application-defined AddBitmapMenu function creates a menu and adds the specified number of bitmap menu items to it.</span></span> <span data-ttu-id="04192-281">Em seguida, ele adiciona um nome de menu correspondente à barra de menus da janela especificada.</span><span class="sxs-lookup"><span data-stu-id="04192-281">Then it adds a corresponding menu name to the specified window's menu bar.</span></span>


```
VOID WINAPI AddBitmapMenu( 
        HWND hwnd,          // window that owned the menu bar 
        LPSTR lpszText,     // text of menu name on menu bar 
        UINT uID,           // ID of first bitmap menu item 
        HBITMAP *paHbm,     // bitmaps for the menu items 
        int cItems)         // number bitmap menu items 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup = CreatePopupMenu(); 
    MENUITEMINFO mii; 
    int i; 
 
    // Add the bitmap menu items to the menu. 
 
    for (i = 0; i < cItems; i++) 
    { 
        mii.fMask = MIIM_ID | MIIM_BITMAP | MIIM_DATA; 
        mii.wID = uID + i; 
        mii.hbmpItem = &paHbm[i]; 
        InsertMenuItem(hmenuPopup, i, TRUE, &mii); 
    } 
 
    // Add a menu name to the menu bar. 
 
    mii.fMask = MIIM_STRING | MIIM_DATA | MIIM_SUBMENU; 
    mii.fType = MFT_STRING; 
    mii.hSubMenu = hmenuPopup; 
    mii.dwTypeData = lpszText; 
    InsertMenuItem(hmenuBar, 
        GetMenuItemCount(hmenuBar), TRUE, &mii); 
} 
```



## <a name="creating-owner-drawn-menu-items"></a><span data-ttu-id="04192-282">Criando Owner-Drawn itens de menu</span><span class="sxs-lookup"><span data-stu-id="04192-282">Creating Owner-Drawn Menu Items</span></span>

<span data-ttu-id="04192-283">Se você precisar de controle total sobre a aparência de um item de menu, poderá usar um item de menu desenhado pelo proprietário em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-283">If you need complete control over the appearance of a menu item, you can use an owner-drawn menu item in your application.</span></span> <span data-ttu-id="04192-284">Esta seção descreve as etapas envolvidas na criação e uso de um item de menu desenhado pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="04192-284">This section describes the steps involved in creating and using an owner-drawn menu item.</span></span>

-   [<span data-ttu-id="04192-285">Definindo o sinalizador de Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="04192-285">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
-   [<span data-ttu-id="04192-286">Menus desenhados pelo proprietário e a mensagem do WM \_ MEASUREITEM</span><span class="sxs-lookup"><span data-stu-id="04192-286">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
-   [<span data-ttu-id="04192-287">Menus desenhados pelo proprietário e a mensagem do WM \_ DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="04192-287">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
-   [<span data-ttu-id="04192-288">Menus desenhados pelo proprietário e a mensagem do WM \_ MENUCHAR</span><span class="sxs-lookup"><span data-stu-id="04192-288">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
-   [<span data-ttu-id="04192-289">Definindo fontes para Menu-Item cadeias de caracteres de texto</span><span class="sxs-lookup"><span data-stu-id="04192-289">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
-   [<span data-ttu-id="04192-290">Exemplo de itens de menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="04192-290">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a><span data-ttu-id="04192-291">Definindo o sinalizador de Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="04192-291">Setting the Owner-Drawn Flag</span></span>

<span data-ttu-id="04192-292">Você não pode definir um item de menu desenhado pelo proprietário no arquivo de definição de recurso de seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-292">You cannot define an owner-drawn menu item in your application's resource-definition file.</span></span> <span data-ttu-id="04192-293">Em vez disso, você deve criar um novo item de menu ou modificar um existente usando o sinalizador de menu **MFT \_ OWNERDRAW** .</span><span class="sxs-lookup"><span data-stu-id="04192-293">Instead, you must create a new menu item or modify an existing one by using the **MFT\_OWNERDRAW** menu flag.</span></span>

<span data-ttu-id="04192-294">Você pode usar a função [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) ou [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) para especificar um item de menu desenhado pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="04192-294">You can use the [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) or [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function to specify an owner-drawn menu item.</span></span> <span data-ttu-id="04192-295">Use **InsertMenuItem** para inserir um novo item de menu na posição especificada em uma barra de menus ou em um menu.</span><span class="sxs-lookup"><span data-stu-id="04192-295">Use **InsertMenuItem** to insert a new menu item at the specified position in a menu bar or menu.</span></span> <span data-ttu-id="04192-296">Use **SetMenuItemInfo** para alterar o conteúdo de um menu.</span><span class="sxs-lookup"><span data-stu-id="04192-296">Use **SetMenuItemInfo** to change the contents of a menu.</span></span>

<span data-ttu-id="04192-297">Ao chamar essas duas funções, você deve especificar um ponteiro para uma estrutura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , que especifica as propriedades do novo item de menu ou as propriedades que você deseja alterar para um item de menu existente.</span><span class="sxs-lookup"><span data-stu-id="04192-297">When calling these two functions, you must specify a pointer to a [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, which specifies the properties of the new menu item or the properties you want to change for an existing menu item.</span></span> <span data-ttu-id="04192-298">Para transformar um item em um item desenhado pelo proprietário, especifique o valor de **\_ ftype MIIM** para o membro **fMask** e o valor de **\_ OWNERDRAW de MFT** para o membro **ftype** .</span><span class="sxs-lookup"><span data-stu-id="04192-298">To make an item an owner-drawn item, specify the **MIIM\_FTYPE** value for the **fMask** member and the **MFT\_OWNERDRAW** value for the **fType** member.</span></span>

<span data-ttu-id="04192-299">Ao definir os membros apropriados da estrutura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , você pode associar um valor definido pelo aplicativo, que é chamado de **dados de item**, com cada item de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-299">By setting the appropriate members of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, you can associate an application-defined value, which is called **item data**, with each menu item.</span></span> <span data-ttu-id="04192-300">Para fazer isso, especifique o valor de **\_ dados MIIM** para o membro **fMask** e o valor definido pelo aplicativo para o membro **dwItemData** .</span><span class="sxs-lookup"><span data-stu-id="04192-300">To do so, specify the **MIIM\_DATA** value for the **fMask** member and the application-defined value for the **dwItemData** member.</span></span>

<span data-ttu-id="04192-301">Você pode usar dados de item com qualquer tipo de item de menu, mas é particularmente útil para itens desenhados pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="04192-301">You can use item data with any type of menu item, but it is particularly useful for owner-drawn items.</span></span> <span data-ttu-id="04192-302">Por exemplo, suponha que uma estrutura contenha informações usadas para desenhar um item de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-302">For example, suppose a structure contains information used to draw a menu item.</span></span> <span data-ttu-id="04192-303">Um aplicativo pode usar os dados do item para um item de menu para armazenar um ponteiro para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="04192-303">An application might use the item data for a menu item to store a pointer to the structure.</span></span> <span data-ttu-id="04192-304">Os dados do item são enviados para a janela do proprietário do menu com as mensagens do [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) e do [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) .</span><span class="sxs-lookup"><span data-stu-id="04192-304">The item data is sent to the menu's owner window with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages.</span></span> <span data-ttu-id="04192-305">Para recuperar os dados do item para um menu a qualquer momento, use a função [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="04192-305">To retrieve the item data for a menu at any time, use the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function.</span></span>

<span data-ttu-id="04192-306">Os aplicativos escritos para versões anteriores do sistema podem continuar a chamar [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)ou [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) para atribuir o sinalizador **MF \_ OWNERDRAW** a um item de menu desenhado pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="04192-306">Applications written for earlier versions of the system can continue to call [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) to assign the **MF\_OWNERDRAW** flag to an owner-drawn menu item.</span></span>

<span data-ttu-id="04192-307">Ao chamar qualquer uma dessas três funções, você pode passar um valor como o parâmetro *lpNewItem* .</span><span class="sxs-lookup"><span data-stu-id="04192-307">When you call any of these three functions, you can pass a value as the *lpNewItem* parameter.</span></span> <span data-ttu-id="04192-308">Esse valor pode representar qualquer informação que seja significativa para seu aplicativo e que estará disponível para seu aplicativo quando o item for exibido.</span><span class="sxs-lookup"><span data-stu-id="04192-308">This value can represent any information that is meaningful to your application, and that will be available to your application when the item is to be displayed.</span></span> <span data-ttu-id="04192-309">Por exemplo, o valor pode conter um ponteiro para uma estrutura; a estrutura, por sua vez, pode conter uma cadeia de texto e um identificador para a fonte lógica que seu aplicativo usará para desenhar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="04192-309">For example, the value could contain a pointer to a structure; the structure, in turn, might contain a text string and a handle to the logical font your application will use to draw the string.</span></span>

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a><span data-ttu-id="04192-310">Owner-Drawn menus e a mensagem do WM \_ MEASUREITEM</span><span class="sxs-lookup"><span data-stu-id="04192-310">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>

<span data-ttu-id="04192-311">Antes que o sistema exiba um item de menu desenhado pelo proprietário pela primeira vez, ele envia a mensagem do [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) para o procedimento de janela da janela que possui o menu do item.</span><span class="sxs-lookup"><span data-stu-id="04192-311">Before the system displays an owner-drawn menu item for the first time, it sends the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message to the window procedure of the window that owns the item's menu.</span></span> <span data-ttu-id="04192-312">Essa mensagem contém um ponteiro para uma estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que identifica o item e contém os dados do item que um aplicativo pode ter atribuído a ele.</span><span class="sxs-lookup"><span data-stu-id="04192-312">This message contains a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the item and contains the item data that an application may have assigned to it.</span></span> <span data-ttu-id="04192-313">O procedimento de janela deve preencher os membros de **ItemHeight** e **dowidth** da estrutura antes de retornar do processamento da mensagem.</span><span class="sxs-lookup"><span data-stu-id="04192-313">The window procedure must fill the **itemWidth** and **itemHeight** members of the structure before returning from processing the message.</span></span> <span data-ttu-id="04192-314">O sistema usa as informações nesses membros ao criar o retângulo delimitador no qual um aplicativo desenha o item de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-314">The system uses the information in these members when creating the bounding rectangle in which an application draws the menu item.</span></span> <span data-ttu-id="04192-315">Ele também usa as informações para detectar quando o usuário escolhe o item.</span><span class="sxs-lookup"><span data-stu-id="04192-315">It also uses the information to detect when the user chooses the item.</span></span>

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a><span data-ttu-id="04192-316">Owner-Drawn menus e a mensagem do WM \_ DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="04192-316">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>

<span data-ttu-id="04192-317">Sempre que o item deve ser desenhado (por exemplo, quando é exibido pela primeira vez ou quando o usuário o seleciona), o sistema envia a mensagem do [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) para o procedimento de janela da janela do proprietário do menu.</span><span class="sxs-lookup"><span data-stu-id="04192-317">Whenever the item must be drawn (for example, when it is first displayed or when the user selects it), the system sends the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message to the window procedure of the menu's owner window.</span></span> <span data-ttu-id="04192-318">Essa mensagem contém um ponteiro para uma estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , que contém informações sobre o item, incluindo os dados do item que um aplicativo pode ter atribuído a ele.</span><span class="sxs-lookup"><span data-stu-id="04192-318">This message contains a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure, which contains information about the item, including the item data that an application may have assigned to it.</span></span> <span data-ttu-id="04192-319">Além disso, **DRAWITEMSTRUCT** contém sinalizadores que indicam o estado do item (como se ele está esmaecido ou selecionado), bem como um retângulo delimitador e um contexto de dispositivo que o aplicativo usa para desenhar o item.</span><span class="sxs-lookup"><span data-stu-id="04192-319">In addition, **DRAWITEMSTRUCT** contains flags that indicate the state of the item (such as whether it is grayed or selected) as well as a bounding rectangle and a device context that the application uses to draw the item.</span></span>

<span data-ttu-id="04192-320">Um aplicativo deve fazer o seguinte durante o processamento da mensagem do [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) :</span><span class="sxs-lookup"><span data-stu-id="04192-320">An application must do the following while processing the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message:</span></span>

-   <span data-ttu-id="04192-321">Determine o tipo de desenho necessário.</span><span class="sxs-lookup"><span data-stu-id="04192-321">Determine the type of drawing that is necessary.</span></span> <span data-ttu-id="04192-322">Para fazer isso, verifique o membro de **ação** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="04192-322">To do so, check the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span>
-   <span data-ttu-id="04192-323">Desenhe o item de menu adequadamente, usando o retângulo delimitador e o contexto do dispositivo obtido na estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="04192-323">Draw the menu item appropriately, using the bounding rectangle and device context obtained from the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="04192-324">O aplicativo deve ser desenhado somente dentro do retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="04192-324">The application must draw only within the bounding rectangle.</span></span> <span data-ttu-id="04192-325">Por motivos de desempenho, o sistema não corta partes da imagem que são desenhadas fora do retângulo.</span><span class="sxs-lookup"><span data-stu-id="04192-325">For performance reasons, the system does not clip portions of the image that are drawn outside the rectangle.</span></span>
-   <span data-ttu-id="04192-326">Restaurar todos os objetos GDI selecionados para o contexto do dispositivo do item de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-326">Restore all GDI objects selected for the menu item's device context.</span></span>

<span data-ttu-id="04192-327">Se o usuário selecionar o item de menu, o sistema definirá o membro de **ação** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) como o valor de **\_ seleção de Oda** e definirá o valor de **ODS \_ selecionado** no membro **ItemState** .</span><span class="sxs-lookup"><span data-stu-id="04192-327">If the user selects the menu item, the system sets the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure to the **ODA\_SELECT** value and sets the **ODS\_SELECTED** value in the **itemState** member.</span></span> <span data-ttu-id="04192-328">Esta é a indicação de um aplicativo para redesenhar o item de menu para indicar que ele está selecionado.</span><span class="sxs-lookup"><span data-stu-id="04192-328">This is an application's cue to redraw the menu item to indicate that it is selected.</span></span>

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a><span data-ttu-id="04192-329">Owner-Drawn menus e a mensagem do WM \_ MENUCHAR</span><span class="sxs-lookup"><span data-stu-id="04192-329">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>

<span data-ttu-id="04192-330">Menus diferentes de menus desenhados pelo proprietário podem especificar um mnemônico de menu inserindo um sublinhado ao lado de um caractere na cadeia de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-330">Menus other than owner-drawn menus can specify a menu mnemonic by inserting an underscore next to a character in the menu string.</span></span> <span data-ttu-id="04192-331">Isso permite que o usuário selecione o menu pressionando ALT e pressionando o caractere de menu mnemônico.</span><span class="sxs-lookup"><span data-stu-id="04192-331">This allows the user to select the menu by pressing ALT and pressing the menu mnemonic character.</span></span> <span data-ttu-id="04192-332">No entanto, nos menus desenhados pelo proprietário, você não pode especificar um mnemônico de menu dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="04192-332">In owner-drawn menus, however, you cannot specify a menu mnemonic in this manner.</span></span> <span data-ttu-id="04192-333">Em vez disso, seu aplicativo deve processar a mensagem [**\_ MENUCHAR do WM**](wm-menuchar.md) para fornecer menus desenhados pelo proprietário com mnemônicos de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-333">Instead, your application must process the [**WM\_MENUCHAR**](wm-menuchar.md) message to provide owner-drawn menus with menu mnemonics.</span></span>

<span data-ttu-id="04192-334">A mensagem do [**WM \_ MENUCHAR**](wm-menuchar.md) é enviada quando o usuário digita um mnemônico do menu que não corresponde a nenhum dos mnemônicos predefinidos do menu atual.</span><span class="sxs-lookup"><span data-stu-id="04192-334">The [**WM\_MENUCHAR**](wm-menuchar.md) message is sent when the user types a menu mnemonic that does not match any of the predefined mnemonics of the current menu.</span></span> <span data-ttu-id="04192-335">O valor contido em *wParam* especifica o caractere ASCII que corresponde à chave que o usuário pressionou com a tecla Alt.</span><span class="sxs-lookup"><span data-stu-id="04192-335">The value contained in *wParam* specifies the ASCII character that corresponds to the key the user pressed with the ALT key.</span></span> <span data-ttu-id="04192-336">A palavra de ordem inferior de *wParam* especifica o tipo do menu selecionado e pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="04192-336">The low-order word of *wParam* specifies the type of the selected menu and can be one of the following values:</span></span>

-   <span data-ttu-id="04192-337">**MF \_ POPUP** se o menu atual for um submenu.</span><span class="sxs-lookup"><span data-stu-id="04192-337">**MF\_POPUP** if the current menu is a submenu.</span></span>
-   <span data-ttu-id="04192-338">**MF \_ SYSMENU** se o menu for o menu do sistema.</span><span class="sxs-lookup"><span data-stu-id="04192-338">**MF\_SYSMENU** if the menu is the system menu.</span></span>

<span data-ttu-id="04192-339">A palavra de ordem superior de *wParam* contém o identificador de menu para o menu atual.</span><span class="sxs-lookup"><span data-stu-id="04192-339">The high-order word of *wParam* contains the menu handle to the current menu.</span></span> <span data-ttu-id="04192-340">A janela com os menus desenhados pelo proprietário pode processar o [**WM \_ MENUCHAR**](wm-menuchar.md) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="04192-340">The window with the owner-drawn menus can process [**WM\_MENUCHAR**](wm-menuchar.md) as follows:</span></span>


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



<span data-ttu-id="04192-341">Os dois na palavra de ordem superior do valor de retorno informam ao sistema que a palavra de ordem inferior do valor de retorno contém o índice de base zero do item de menu a ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="04192-341">The two in the high-order word of the return value informs the system that the low-order word of the return value contains the zero-based index of the menu item to be selected.</span></span>

<span data-ttu-id="04192-342">As constantes a seguir correspondem aos possíveis valores de retorno da mensagem do [**WM \_ MENUCHAR**](wm-menuchar.md) .</span><span class="sxs-lookup"><span data-stu-id="04192-342">The following constants correspond to the possible return values from the [**WM\_MENUCHAR**](wm-menuchar.md) message.</span></span>



| <span data-ttu-id="04192-343">Constante</span><span class="sxs-lookup"><span data-stu-id="04192-343">Constant</span></span>         | <span data-ttu-id="04192-344">Valor</span><span class="sxs-lookup"><span data-stu-id="04192-344">Value</span></span> | <span data-ttu-id="04192-345">Significado</span><span class="sxs-lookup"><span data-stu-id="04192-345">Meaning</span></span>                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04192-346">**\_ignorar MNC**</span><span class="sxs-lookup"><span data-stu-id="04192-346">**MNC\_IGNORE**</span></span>  | <span data-ttu-id="04192-347">0</span><span class="sxs-lookup"><span data-stu-id="04192-347">0</span></span>     | <span data-ttu-id="04192-348">O sistema deve descartar o caractere que o usuário pressionou e criar um bipe curto no alto-falante do sistema.</span><span class="sxs-lookup"><span data-stu-id="04192-348">The system should discard the character the user pressed and create a short beep on the system speaker.</span></span>                                                       |
| <span data-ttu-id="04192-349">**MNC \_ fechar**</span><span class="sxs-lookup"><span data-stu-id="04192-349">**MNC\_CLOSE**</span></span>   | <span data-ttu-id="04192-350">1</span><span class="sxs-lookup"><span data-stu-id="04192-350">1</span></span>     | <span data-ttu-id="04192-351">O sistema deve fechar o menu ativo.</span><span class="sxs-lookup"><span data-stu-id="04192-351">The system should close the active menu.</span></span>                                                                                                                      |
| <span data-ttu-id="04192-352">**MNC \_ executar**</span><span class="sxs-lookup"><span data-stu-id="04192-352">**MNC\_EXECUTE**</span></span> | <span data-ttu-id="04192-353">2</span><span class="sxs-lookup"><span data-stu-id="04192-353">2</span></span>     | <span data-ttu-id="04192-354">O sistema deve escolher o item especificado na palavra de ordem inferior do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="04192-354">The system should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="04192-355">A janela do proprietário recebe uma mensagem de [**\_ comando do WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="04192-355">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span> |
| <span data-ttu-id="04192-356">**MNC \_ selecionar**</span><span class="sxs-lookup"><span data-stu-id="04192-356">**MNC\_SELECT**</span></span>  | <span data-ttu-id="04192-357">3</span><span class="sxs-lookup"><span data-stu-id="04192-357">3</span></span>     | <span data-ttu-id="04192-358">O sistema deve selecionar o item especificado na palavra de ordem inferior do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="04192-358">The system should select the item specified in the low-order word of the return value.</span></span>                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a><span data-ttu-id="04192-359">Definindo fontes para Menu-Item cadeias de caracteres de texto</span><span class="sxs-lookup"><span data-stu-id="04192-359">Setting Fonts for Menu-Item Text Strings</span></span>

<span data-ttu-id="04192-360">Este tópico contém um exemplo de um aplicativo que usa itens de menu de desenho proprietário em um menu.</span><span class="sxs-lookup"><span data-stu-id="04192-360">This topic contains an example from an application that uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="04192-361">O menu contém itens que definem os atributos da fonte atual e os itens são exibidos usando o atributo de fonte apropriado.</span><span class="sxs-lookup"><span data-stu-id="04192-361">The menu contains items that set the attributes of the current font, and the items are displayed using the appropriate font attribute.</span></span>

<span data-ttu-id="04192-362">Veja como o menu é definido no arquivo de definição de recurso.</span><span class="sxs-lookup"><span data-stu-id="04192-362">Here is how the menu is defined in the resource-definition file.</span></span> <span data-ttu-id="04192-363">Observe que as cadeias de caracteres dos itens de menu regular, negrito, itálico e sublinhado são atribuídas em tempo de execução, portanto, suas cadeias de caracteres estão vazias no arquivo de definição de recurso.</span><span class="sxs-lookup"><span data-stu-id="04192-363">Note that the strings for the Regular, Bold, Italic, and Underline menu items are assigned at run time, so their strings are empty in the resource-definition file.</span></span>


```
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "",    IDM_REGULAR 
        MENUITEM SEPARATOR 
        MENUITEM    "",    IDM_BOLD 
        MENUITEM    "",    IDM_ITALIC 
        MENUITEM    "",    IDM_ULINE 
    END 
END 
```



<span data-ttu-id="04192-364">O procedimento de janela do aplicativo processa as mensagens envolvidas no uso de itens de menu extraídos pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="04192-364">The application's window procedure processes the messages involved in using owner-drawn menu items.</span></span> <span data-ttu-id="04192-365">O aplicativo usa a mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="04192-365">The application uses the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to do the following:</span></span>

-   <span data-ttu-id="04192-366">Defina o sinalizador **MF \_ OWNERDRAW** para os itens de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-366">Set the **MF\_OWNERDRAW** flag for the menu items.</span></span>
-   <span data-ttu-id="04192-367">Defina as cadeias de caracteres de texto para os itens de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-367">Set the text strings for the menu items.</span></span>
-   <span data-ttu-id="04192-368">Obter identificadores das fontes usadas para desenhar os itens.</span><span class="sxs-lookup"><span data-stu-id="04192-368">Obtain handles of the fonts used to draw the items.</span></span>
-   <span data-ttu-id="04192-369">Obter os valores de cor de plano de fundo e texto para itens de menu selecionados.</span><span class="sxs-lookup"><span data-stu-id="04192-369">Obtain the text and background color values for selected menu items.</span></span>

<span data-ttu-id="04192-370">As cadeias de caracteres de texto e os identificadores de fonte são armazenados em uma matriz de estruturas MYITEM definidas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-370">The text strings and font handles are stored in an array of application-defined MYITEM structures.</span></span> <span data-ttu-id="04192-371">A função GetAFont definida pelo aplicativo cria uma fonte que corresponde ao atributo de fonte especificado e retorna um identificador para a fonte.</span><span class="sxs-lookup"><span data-stu-id="04192-371">The application-defined GetAFont function creates a font that corresponds to the specified font attribute and returns a handle to the font.</span></span> <span data-ttu-id="04192-372">Os identificadores são destruídos durante o processamento da mensagem do [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="04192-372">The handles are destroyed during the processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span>

<span data-ttu-id="04192-373">Durante o processamento da mensagem do [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) , o exemplo obtém a largura e a altura de uma cadeia de caracteres de item de menu e copia esses valores na estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="04192-373">During the processing of the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message, the example gets the width and height of a menu-item string and copies these values into the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure.</span></span> <span data-ttu-id="04192-374">O sistema usa os valores de largura e altura para calcular o tamanho do menu.</span><span class="sxs-lookup"><span data-stu-id="04192-374">The system uses the width and height values to calculate the size of the menu.</span></span>

<span data-ttu-id="04192-375">Durante o processamento da mensagem do [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) , a cadeia de caracteres do item de menu é desenhada com a sala à esquerda ao lado da cadeia de caracteres do bitmap de marca de seleção.</span><span class="sxs-lookup"><span data-stu-id="04192-375">During the processing of the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message, the menu item's string is drawn with room left next to the string for the check-mark bitmap.</span></span> <span data-ttu-id="04192-376">Se o usuário selecionar o item, o texto selecionado e as cores de plano de fundo serão usadas para desenhar o item.</span><span class="sxs-lookup"><span data-stu-id="04192-376">If the user selects the item, the selected text and background colors are used to draw the item.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    typedef struct _MYITEM 
    { 
        HFONT hfont; 
        LPSTR psz; 
    } MYITEM;             // structure for item font and string  
 
    MYITEM *pmyitem;      // pointer to item's font and string        
    static MYITEM myitem[CITEMS];   // array of MYITEMS               
    static HMENU hmenu;             // handle to main menu            
    static COLORREF crSelText;  // text color of selected item        
    static COLORREF crSelBkgnd; // background color of selected item  
    COLORREF crText;            // text color of unselected item      
    COLORREF crBkgnd;           // background color unselected item   
    LPMEASUREITEMSTRUCT lpmis;  // pointer to item of data             
    LPDRAWITEMSTRUCT lpdis;     // pointer to item drawing data        
    HDC hdc;                    // handle to screen DC                
    SIZE size;                  // menu-item text extents             
    WORD wCheckX;               // check-mark width                   
    int nTextX;                 // width of menu item                 
    int nTextY;                 // height of menu item                
    int i;                      // loop counter                       
    HFONT hfontOld;             // handle to old font                 
    BOOL fSelected = FALSE;     // menu-item selection flag
    size_t * pcch;
    HRESULT hResult;           
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Modify the Regular, Bold, Italic, and Underline 
            // menu items to make them owner-drawn items. Associate 
            // a MYITEM structure with each item to contain the 
            // string for and font handle to each item. 
 
            hmenu = GetMenu(hwnd); 
            ModifyMenu(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED | MF_OWNERDRAW, IDM_REGULAR, 
                (LPTSTR) &myitem[REGULAR]); 
            ModifyMenu(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_BOLD, (LPTSTR) &myitem[BOLD]); 
            ModifyMenu(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ITALIC, 
                (LPTSTR) &myitem[ITALIC]); 
            ModifyMenu(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ULINE, (LPTSTR) &myitem[ULINE]); 
 
            // Retrieve each item's font handle and copy it into 
            // the hfont member of each item's MYITEM structure. 
            // Also, copy each item's string into the structures. 
 
            myitem[REGULAR].hfont = GetAFont(REGULAR); 
            myitem[REGULAR].psz = "Regular"; 
            myitem[BOLD].hfont = GetAFont(BOLD); 
            myitem[BOLD].psz = "Bold"; 
            myitem[ITALIC].hfont = GetAFont(ITALIC); 
            myitem[ITALIC].psz = "Italic"; 
            myitem[ULINE].hfont = GetAFont(ULINE); 
            myitem[ULINE].psz = "Underline"; 
 
            // Retrieve the text and background colors of the 
            // selected menu text. 
 
            crSelText = GetSysColor(COLOR_HIGHLIGHTTEXT); 
            crSelBkgnd = GetSysColor(COLOR_HIGHLIGHT); 
 
            return 0; 
 
        case WM_MEASUREITEM: 
 
            // Retrieve a device context for the main window.  
 
            hdc = GetDC(hwnd); 
 
            // Retrieve pointers to the menu item's 
            // MEASUREITEMSTRUCT structure and MYITEM structure. 
 
            lpmis = (LPMEASUREITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpmis->itemData; 
 
            // Select the font associated with the item into 
            // the main window's device context. 
 
            hfontOld = SelectObject(hdc, pmyitem->hfont); 
 
            // Retrieve the width and height of the item's string, 
            // and then copy the width and height into the 
            // MEASUREITEMSTRUCT structure's itemWidth and 
            // itemHeight members.
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            GetTextExtentPoint32(hdc, pmyitem->psz, 
                *pcch, &size); 
            lpmis->itemWidth = size.cx; 
            lpmis->itemHeight = size.cy; 
 
            // Select the old font back into the device context, 
            // and then release the device context. 
 
            SelectObject(hdc, hfontOld); 
            ReleaseDC(hwnd, hdc); 
 
            return TRUE; 
 
            break; 
 
        case WM_DRAWITEM: 
 
            // Get pointers to the menu item's DRAWITEMSTRUCT 
            // structure and MYITEM structure. 
 
            lpdis = (LPDRAWITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpdis->itemData; 
 
            // If the user has selected the item, use the selected 
            // text and background colors to display the item. 
 
            if (lpdis->itemState & ODS_SELECTED) 
            { 
                crText = SetTextColor(lpdis->hDC, crSelText); 
                crBkgnd = SetBkColor(lpdis->hDC, crSelBkgnd); 
                fSelected = TRUE; 
            } 
 
            // Remember to leave space in the menu item for the 
            // check-mark bitmap. Retrieve the width of the bitmap 
            // and add it to the width of the menu item. 
 
            wCheckX = GetSystemMetrics(SM_CXMENUCHECK); 
            nTextX = wCheckX + lpdis->rcItem.left; 
            nTextY = lpdis->rcItem.top; 
 
            // Select the font associated with the item into the 
            // item's device context, and then draw the string. 
 
            hfontOld = SelectObject(lpdis->hDC, pmyitem->hfont);
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            ExtTextOut(lpdis->hDC, nTextX, nTextY, ETO_OPAQUE, 
                &lpdis->rcItem, pmyitem->psz, 
                *pcch, NULL); 
 
            // Select the previous font back into the device 
            // context. 
 
            SelectObject(lpdis->hDC, hfontOld); 
 
            // Return the text and background colors to their 
            // normal state (not selected). 
 
            if (fSelected) 
            { 
                SetTextColor(lpdis->hDC, crText); 
                SetBkColor(lpdis->hDC, crBkgnd); 
            } 
 
            return TRUE; 
 
        // Process other messages.  
 
        case WM_DESTROY: 
 
            // Destroy the menu items' font handles.  
 
            for (i = 0; i < CITEMS; i++) 
                DeleteObject(myitem[i].hfont); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HFONT GetAFont(int fnFont) 
{ 
    static LOGFONT lf;  // structure for font information  
 
    // Get a handle to the ANSI fixed-pitch font, and copy 
    // information about the font to a LOGFONT structure. 
 
    GetObject(GetStockObject(ANSI_FIXED_FONT), sizeof(LOGFONT), 
        &lf); 
 
    // Set the font attributes, as appropriate.  
 
    if (fnFont == BOLD) 
        lf.lfWeight = FW_BOLD; 
    else 
        lf.lfWeight = FW_NORMAL; 
 
    lf.lfItalic = (fnFont == ITALIC); 
    lf.lfItalic = (fnFont == ULINE); 
 
    // Create the font, and then return its handle.  
 
    return CreateFont(lf.lfHeight, lf.lfWidth, 
        lf.lfEscapement, lf.lfOrientation, lf.lfWeight, 
        lf.lfItalic, lf.lfUnderline, lf.lfStrikeOut, lf.lfCharSet, 
        lf.lfOutPrecision, lf.lfClipPrecision, lf.lfQuality, 
        lf.lfPitchAndFamily, lf.lfFaceName); 
} 
```



### <a name="example-of-owner-drawn-menu-items"></a><span data-ttu-id="04192-377">Exemplo de itens de menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="04192-377">Example of Owner-Drawn Menu Items</span></span>

<span data-ttu-id="04192-378">O exemplo neste tópico usa itens de menu de desenho proprietário em um menu.</span><span class="sxs-lookup"><span data-stu-id="04192-378">The example in this topic uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="04192-379">Os itens de menu selecionam atributos de fonte específicos e o aplicativo exibe cada item de menu usando uma fonte que tem o atributo correspondente.</span><span class="sxs-lookup"><span data-stu-id="04192-379">The menu items select specific font attributes, and the application displays each menu item using a font that has the corresponding attribute.</span></span> <span data-ttu-id="04192-380">Por exemplo, o item de menu **itálico** é exibido em uma fonte em itálico.</span><span class="sxs-lookup"><span data-stu-id="04192-380">For example, the **Italic** menu item is displayed in an italic font.</span></span> <span data-ttu-id="04192-381">O nome do menu de **caracteres** na barra de menus abre o menu.</span><span class="sxs-lookup"><span data-stu-id="04192-381">The **Character** menu name on the menu bar opens the menu.</span></span>

<span data-ttu-id="04192-382">A barra de menus e o menu suspenso são definidos inicialmente por um recurso de modelo de menu estendido.</span><span class="sxs-lookup"><span data-stu-id="04192-382">The menu bar and drop-down menu are defined initially by an extended menu-template resource.</span></span> <span data-ttu-id="04192-383">Como um modelo de menu não pode especificar itens desenhados pelo proprietário, o menu inicialmente contém quatro itens de menu de texto com as seguintes cadeias de caracteres: "regular", "negrito", "itálico" e "sublinhado".</span><span class="sxs-lookup"><span data-stu-id="04192-383">Because a menu template cannot specify owner-drawn items, the menu initially contains four text menu items with the following strings: "Regular," "Bold," "Italic," and "Underline."</span></span> <span data-ttu-id="04192-384">O procedimento de janela do aplicativo altera essas mensagens para itens desenhados pelo proprietário ao processar a mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="04192-384">The application's window procedure changes these to owner-drawn items when it processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="04192-385">Quando recebe a mensagem **de \_ criação do WM** , o procedimento de janela chama a função OnCreate definida pelo aplicativo, que executa as seguintes etapas para cada item de menu:</span><span class="sxs-lookup"><span data-stu-id="04192-385">When it receives the **WM\_CREATE** message, the window procedure calls the application-defined OnCreate function, which performs the following steps for each menu item:</span></span>

-   <span data-ttu-id="04192-386">Aloca uma estrutura MYITEM definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-386">Allocates an application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="04192-387">Obtém o texto do item de menu e o salva na estrutura MYITEM definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-387">Gets the text of the menu item and saves it in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="04192-388">Cria a fonte usada para exibir o item de menu e salva seu identificador na estrutura MYITEM definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-388">Creates the font used to display the menu item and saves its handle in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="04192-389">Altera o tipo de item de menu para **MFT \_ OWNERDRAW** e salva um ponteiro para a estrutura MYITEM definida pelo aplicativo como dados de item.</span><span class="sxs-lookup"><span data-stu-id="04192-389">Changes the menu item type to **MFT\_OWNERDRAW** and saves a pointer to the application-defined MYITEM structure as item data.</span></span>

<span data-ttu-id="04192-390">Como um ponteiro para cada estrutura MYITEM definida pelo aplicativo é salvo como dados do item, ele é passado para o procedimento de janela em conjunto com as mensagens do [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) e do [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) para o item de menu correspondente.</span><span class="sxs-lookup"><span data-stu-id="04192-390">Because a pointer to each application-defined MYITEM structure is saved as item data, it is passed to the window procedure in conjunction with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages for the corresponding menu item.</span></span> <span data-ttu-id="04192-391">O ponteiro está contido no membro de todos os **dados** das estruturas [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) e [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="04192-391">The pointer is contained in the **itemData** member of both the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) and [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structures.</span></span>

<span data-ttu-id="04192-392">Uma mensagem do [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) é enviada para cada item de menu desenhado pelo proprietário na primeira vez que é exibido.</span><span class="sxs-lookup"><span data-stu-id="04192-392">A [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message is sent for each owner-drawn menu item the first time it is displayed.</span></span> <span data-ttu-id="04192-393">O aplicativo processa essa mensagem selecionando a fonte do item de menu em um contexto de dispositivo e, em seguida, determinando o espaço necessário para exibir o texto do item de menu nessa fonte.</span><span class="sxs-lookup"><span data-stu-id="04192-393">The application processes this message by selecting the font for the menu item into a device context and then determining the space required to display the menu item text in that font.</span></span> <span data-ttu-id="04192-394">O texto do item de fonte e de menu são ambos especificados pela estrutura do item de menu `MYITEM` (a estrutura definida pelo aplicativo).</span><span class="sxs-lookup"><span data-stu-id="04192-394">The font and menu item text are both specified by the menu item's `MYITEM` structure (the structure defined by the application).</span></span> <span data-ttu-id="04192-395">O aplicativo determina o tamanho do texto usando a função [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) .</span><span class="sxs-lookup"><span data-stu-id="04192-395">The application determines the size of the text by using the [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) function.</span></span>

<span data-ttu-id="04192-396">O procedimento de janela processa a mensagem do [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) exibindo o texto do item de menu na fonte apropriada.</span><span class="sxs-lookup"><span data-stu-id="04192-396">The window procedure processes the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message by displaying the menu item text in the appropriate font.</span></span> <span data-ttu-id="04192-397">O texto do item de fonte e de menu são ambos especificados pela estrutura do item de menu `MYITEM` .</span><span class="sxs-lookup"><span data-stu-id="04192-397">The font and menu item text are both specified by the menu item's `MYITEM` structure.</span></span> <span data-ttu-id="04192-398">O aplicativo seleciona as cores de texto e de plano de fundo apropriadas ao estado do item de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-398">The application selects text and background colors appropriate to the menu item's state.</span></span>

<span data-ttu-id="04192-399">O procedimento de janela processa a mensagem de [**\_ destruição do WM**](/windows/desktop/winmsg/wm-destroy) para destruir fontes e liberar memória.</span><span class="sxs-lookup"><span data-stu-id="04192-399">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message to destroy fonts and free memory.</span></span> <span data-ttu-id="04192-400">O aplicativo exclui a fonte e libera a estrutura MYITEM definida pelo aplicativo para cada item de menu.</span><span class="sxs-lookup"><span data-stu-id="04192-400">The application deletes the font and frees the application-defined MYITEM structure for each menu item.</span></span>

<span data-ttu-id="04192-401">A seguir estão as partes relevantes do arquivo de cabeçalho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-401">The following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_REGULAR   11 
#define IDM_BOLD      12 
#define IDM_ITALIC    13 
#define IDM_UNDERLINE 14 
 
// Structure associated with menu items 
 
typedef struct tagMYITEM 
{ 
    HFONT hfont; 
    int   cchItemText; 
    char  szItemText[1]; 
} MYITEM; 
 
#define CCH_MAXITEMTEXT 256 
 
```



<span data-ttu-id="04192-402">A seguir estão as partes relevantes do procedimento de janela do aplicativo e suas funções associadas.</span><span class="sxs-lookup"><span data-stu-id="04192-402">The following are the relevant portions of the application's window procedure and its associated functions.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_MEASUREITEM: 
            OnMeasureItem(hwnd, (LPMEASUREITEMSTRUCT) lParam); 
            return TRUE; 
 
        case WM_DRAWITEM: 
            OnDrawItem(hwnd, (LPDRAWITEMSTRUCT) lParam); 
            return TRUE; 
 
        // Additional message processing goes here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Modify each menu item. Assume that the IDs IDM_REGULAR 
    // through IDM_UNDERLINE are consecutive numbers. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
         // Allocate an item structure, leaving space for a 
         // string of up to CCH_MAXITEMTEXT characters. 
 
        pMyItem = (MYITEM *) LocalAlloc(LMEM_FIXED, 
                sizeof(MYITEM) + CCH_MAXITEMTEXT); 
 
        // Save the item text in the item structure. 
 
        mii.fMask = MIIM_STRING; 
        mii.dwTypeData = pMyItem->szItemText; 
        mii.cch = CCH_MAXITEMTEXT; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem->cchItemText = mii.cch; 
 
        // Reallocate the structure to the minimum required size. 
 
        pMyItem = (MYITEM *) LocalReAlloc(pMyItem, 
                sizeof(MYITEM) + mii.cch, LMEM_MOVEABLE); 
 
        // Create the font used to draw the item. 
 
        pMyItem->hfont = CreateMenuItemFont(uID); 
 
        // Change the item to an owner-drawn item, and save 
        // the address of the item structure as item data. 
 
        mii.fMask = MIIM_FTYPE | MIIM_DATA; 
        mii.fType = MFT_OWNERDRAW; 
        mii.dwItemData = (ULONG_PTR) pMyItem; 
        SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
    } 
    return TRUE; 
} 
 
HFONT CreateMenuItemFont(UINT uID) 
{ 
    LOGFONT lf;
    HRESULT hr; 
 
    ZeroMemory(&lf, sizeof(lf)); 
    lf.lfHeight = 20; 
    hr = StringCchCopy(lf.lfFaceName, 32, "Times New Roman");
    if (FAILED(hr))
    {
    // TODO: writer error handler
    } 
 
    switch (uID) 
    { 
        case IDM_BOLD: 
            lf.lfWeight = FW_HEAVY; 
            break; 
 
        case IDM_ITALIC: 
            lf.lfItalic = TRUE; 
            break; 
 
        case IDM_UNDERLINE: 
            lf.lfUnderline = TRUE; 
            break; 
    } 
    return CreateFontIndirect(&lf); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get  
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Free resources associated with each menu item. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
        // Get the item data. 
 
        mii.fMask = MIIM_DATA; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem = (MYITEM *) mii.dwItemData; 
 
        // Destroy the font and free the item structure. 
 
        DeleteObject(pMyItem->hfont); 
        LocalFree(pMyItem); 
    } 
} 
 
VOID WINAPI OnMeasureItem(HWND hwnd, LPMEASUREITEMSTRUCT lpmis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpmis->itemData; 
    HDC hdc = GetDC(hwnd); 
    HFONT hfntOld = (HFONT)SelectObject(hdc, pMyItem->hfont); 
    SIZE size; 
 
    GetTextExtentPoint32(hdc, pMyItem->szItemText, 
            pMyItem->cchItemText, &size); 
 
    lpmis->itemWidth = size.cx; 
    lpmis->itemHeight = size.cy; 
 
    SelectObject(hdc, hfntOld); 
    ReleaseDC(hwnd, hdc); 
} 
 
VOID WINAPI OnDrawItem(HWND hwnd, LPDRAWITEMSTRUCT lpdis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpdis->itemData; 
    COLORREF clrPrevText, clrPrevBkgnd; 
    HFONT hfntPrev; 
    int x, y; 
 
    // Set the appropriate foreground and background colors. 
 
    if (lpdis->itemState & ODS_SELECTED) 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHTTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHT)); 
    } 
    else 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_MENUTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_MENU)); 
    } 
 
    // Determine where to draw and leave space for a check mark. 
 
    x = lpdis->rcItem.left; 
    y = lpdis->rcItem.top; 
    x += GetSystemMetrics(SM_CXMENUCHECK); 
 
    // Select the font and draw the text. 
 
    hfntPrev = (HFONT)SelectObject(lpdis->hDC, pMyItem->hfont); 
    ExtTextOut(lpdis->hDC, x, y, ETO_OPAQUE, 
            &lpdis->rcItem, pMyItem->szItemText, 
            pMyItem->cchItemText, NULL); 
 
    // Restore the original font and colors. 
 
    SelectObject(lpdis->hDC, hfntPrev); 
    SetTextColor(lpdis->hDC, clrPrevText); 
    SetBkColor(lpdis->hDC, clrPrevBkgnd); 
} 
```



## <a name="using-custom-check-mark-bitmaps"></a><span data-ttu-id="04192-403">Usando bitmaps de marca de seleção personalizados</span><span class="sxs-lookup"><span data-stu-id="04192-403">Using Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="04192-404">O sistema fornece um bitmap de marca de seleção padrão para exibição ao lado de um item de menu selecionado.</span><span class="sxs-lookup"><span data-stu-id="04192-404">The system provides a default check-mark bitmap for displaying next to a menu item that is selected.</span></span> <span data-ttu-id="04192-405">Você pode personalizar um item de menu individual fornecendo um par de bitmaps para substituir o bitmap de marca de seleção padrão.</span><span class="sxs-lookup"><span data-stu-id="04192-405">You can customize an individual menu item by providing a pair of bitmaps to replace the default check-mark bitmap.</span></span> <span data-ttu-id="04192-406">O sistema exibe um bitmap quando o item é selecionado e o outro quando está claro.</span><span class="sxs-lookup"><span data-stu-id="04192-406">The system displays one bitmap when the item is selected and the other when it is clear.</span></span> <span data-ttu-id="04192-407">Esta seção descreve as etapas envolvidas na criação e no uso de bitmaps de marca de seleção personalizados.</span><span class="sxs-lookup"><span data-stu-id="04192-407">This section describes the steps involved in creating and using custom check-mark bitmaps.</span></span>

-   [<span data-ttu-id="04192-408">Criando bitmaps de marca de seleção personalizados</span><span class="sxs-lookup"><span data-stu-id="04192-408">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
-   [<span data-ttu-id="04192-409">Associando bitmaps a um item de menu</span><span class="sxs-lookup"><span data-stu-id="04192-409">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
-   [<span data-ttu-id="04192-410">Definindo o atributo de marca de seleção</span><span class="sxs-lookup"><span data-stu-id="04192-410">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
-   [<span data-ttu-id="04192-411">Simulando caixas de seleção em um menu</span><span class="sxs-lookup"><span data-stu-id="04192-411">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
-   [<span data-ttu-id="04192-412">Exemplo de como usar bitmaps de marca de seleção personalizados</span><span class="sxs-lookup"><span data-stu-id="04192-412">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a><span data-ttu-id="04192-413">Criando bitmaps de marca de seleção personalizados</span><span class="sxs-lookup"><span data-stu-id="04192-413">Creating Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="04192-414">Um bitmap de marca de seleção personalizado deve ter o mesmo tamanho que o bitmap de marca de seleção padrão.</span><span class="sxs-lookup"><span data-stu-id="04192-414">A custom check-mark bitmap must be the same size as the default check-mark bitmap.</span></span> <span data-ttu-id="04192-415">Você pode recuperar o tamanho da marca de seleção padrão do bitmap chamando a função [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="04192-415">You can retrieve the default check-mark size of the bitmap by calling the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="04192-416">A palavra de ordem inferior do valor de retorno da função especifica a largura; a palavra de ordem superior especifica a altura.</span><span class="sxs-lookup"><span data-stu-id="04192-416">The low-order word of this function's return value specifies the width; the high-order word specifies the height.</span></span>

<span data-ttu-id="04192-417">Você pode usar recursos de bitmap para fornecer bitmaps de marca de seleção.</span><span class="sxs-lookup"><span data-stu-id="04192-417">You can use bitmap resources to provide check-mark bitmaps.</span></span> <span data-ttu-id="04192-418">No entanto, como o tamanho de bitmap necessário varia dependendo do tipo de exibição, talvez seja necessário redimensionar o bitmap em tempo de execução usando a função [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) .</span><span class="sxs-lookup"><span data-stu-id="04192-418">However, because the required bitmap size varies depending on the display type, you may need to resize the bitmap at run time by using the [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) function.</span></span> <span data-ttu-id="04192-419">Dependendo do bitmap, a distorção causada pelo dimensionamento pode produzir resultados inaceitáveis.</span><span class="sxs-lookup"><span data-stu-id="04192-419">Depending on the bitmap, the distortion caused by sizing could produce unacceptable results.</span></span>

<span data-ttu-id="04192-420">Em vez de usar um recurso de bitmap, você pode criar um bitmap em tempo de execução usando funções GDI.</span><span class="sxs-lookup"><span data-stu-id="04192-420">Instead of using a bitmap resource, you can create a bitmap at run time by using GDI functions.</span></span>

<span data-ttu-id="04192-421">**Para criar um bitmap em tempo de execução**</span><span class="sxs-lookup"><span data-stu-id="04192-421">**To create a bitmap at run time**</span></span>

1.  <span data-ttu-id="04192-422">Use a função [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) para criar um contexto de dispositivo compatível com aquele usado pela janela principal do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-422">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the one used by the application's main window.</span></span>

    <span data-ttu-id="04192-423">O parâmetro *HDC* da função pode especificar **NULL** ou o valor de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="04192-423">The function's *hdc* parameter can specify either **NULL** or the return value from the function.</span></span> <span data-ttu-id="04192-424">[**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) retorna um identificador para o contexto do dispositivo compatível.</span><span class="sxs-lookup"><span data-stu-id="04192-424">[**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) returns a handle to the compatible device context.</span></span>

2.  <span data-ttu-id="04192-425">Use a função [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) para criar um bitmap compatível com a janela principal do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-425">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window.</span></span>

    <span data-ttu-id="04192-426">Os parâmetros *nWidth* e *nHeight* da função definem o tamanho do bitmap; Eles devem especificar as informações de largura e altura retornadas pela função [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="04192-426">This function's *nWidth* and *nHeight* parameters set the size of the bitmap; they should specify the width and height information returned by the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span>

    > [!Note]  
    > <span data-ttu-id="04192-427">Você também pode usar a função [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) para criar um bitmap monocromático.</span><span class="sxs-lookup"><span data-stu-id="04192-427">You can also use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>

     

3.  <span data-ttu-id="04192-428">Use a função [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) para selecionar o bitmap no contexto do dispositivo compatível.</span><span class="sxs-lookup"><span data-stu-id="04192-428">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="04192-429">Use funções de desenho GDI, como [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) e [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), para desenhar uma imagem no bitmap ou usar funções como [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) e [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) para copiar uma imagem no bitmap.</span><span class="sxs-lookup"><span data-stu-id="04192-429">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap, or use functions such as [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) and [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) to copy an image into the bitmap.</span></span>

<span data-ttu-id="04192-430">Para obter mais informações, consulte [bitmaps](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="04192-430">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="associating-bitmaps-with-a-menu-item"></a><span data-ttu-id="04192-431">Associando bitmaps a um item de menu</span><span class="sxs-lookup"><span data-stu-id="04192-431">Associating Bitmaps with a Menu Item</span></span>

<span data-ttu-id="04192-432">Você associa um par de bitmaps de marca de seleção a um item de menu passando os identificadores dos bitmaps para a função [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) .</span><span class="sxs-lookup"><span data-stu-id="04192-432">You associate a pair of check-mark bitmaps with a menu item by passing the handles of the bitmaps to the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span> <span data-ttu-id="04192-433">O parâmetro *hBitmapUnchecked* identifica o bitmap limpo e o parâmetro *hBitmapChecked* identifica o bitmap selecionado.</span><span class="sxs-lookup"><span data-stu-id="04192-433">The *hBitmapUnchecked* parameter identifies the clear bitmap, and the *hBitmapChecked* parameter identifies the selected bitmap.</span></span> <span data-ttu-id="04192-434">Se você quiser remover uma ou ambas as marcas de seleção de um item de menu, poderá definir o parâmetro *hBitmapUnchecked* ou *hBitmapChecked* , ou ambos, como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="04192-434">If you want to remove one or both check marks from a menu item, you can set the *hBitmapUnchecked* or *hBitmapChecked* parameter, or both, to **NULL**.</span></span>

### <a name="setting-the-check-mark-attribute"></a><span data-ttu-id="04192-435">Definindo o atributo de marca de seleção</span><span class="sxs-lookup"><span data-stu-id="04192-435">Setting the Check-mark Attribute</span></span>

<span data-ttu-id="04192-436">A função [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) define o atributo de marca de seleção de um item de menu como selecionado ou desmarcado.</span><span class="sxs-lookup"><span data-stu-id="04192-436">The [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) function sets a menu item's check-mark attribute to either selected or cleared.</span></span> <span data-ttu-id="04192-437">Você pode especificar o **valor \_ selecionado MF** para definir o atributo de marca de seleção como selecionado e o valor de **MF \_ desmarcado** para defini-lo como Clear.</span><span class="sxs-lookup"><span data-stu-id="04192-437">You can specify the **MF\_CHECKED** value to set the check-mark attribute to selected and the **MF\_UNCHECKED** value to set it to clear.</span></span>

<span data-ttu-id="04192-438">Você também pode definir o estado de verificação de um item de menu usando a função [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="04192-438">You can also set the check state of a menu item by using the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="04192-439">Às vezes, um grupo de itens de menu representa um conjunto de opções mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="04192-439">Sometimes a group of menu items represents a set of mutually exclusive options.</span></span> <span data-ttu-id="04192-440">Usando a função [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) , você pode verificar um item de menu enquanto remove simultaneamente a marca de seleção de todos os outros itens de menu no grupo.</span><span class="sxs-lookup"><span data-stu-id="04192-440">By using the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function, you can check one menu item while simultaneously removing the check mark from all other menu items in the group.</span></span>

### <a name="simulating-check-boxes-in-a-menu"></a><span data-ttu-id="04192-441">Simulando caixas de seleção em um menu</span><span class="sxs-lookup"><span data-stu-id="04192-441">Simulating Check Boxes in a Menu</span></span>

<span data-ttu-id="04192-442">Este tópico contém um exemplo que mostra como simular caixas de seleção em um menu.</span><span class="sxs-lookup"><span data-stu-id="04192-442">This topic contains an example that shows how to simulate check boxes in a menu.</span></span> <span data-ttu-id="04192-443">O exemplo contém um menu de caracteres cujos itens permitem que o usuário defina os atributos negrito, itálico e sublinhado da fonte atual.</span><span class="sxs-lookup"><span data-stu-id="04192-443">The example contains a Character menu whose items allow the user to set the bold, italic, and underline attributes of the current font.</span></span> <span data-ttu-id="04192-444">Quando um atributo de fonte está em vigor, uma marca de seleção é exibida na caixa de seleção ao lado do item de menu correspondente; caso contrário, uma caixa de seleção vazia será exibida ao lado do item.</span><span class="sxs-lookup"><span data-stu-id="04192-444">When a font attribute is in effect, a check mark is displayed in the check box next to the corresponding menu item; otherwise, an empty check box is displayed next to the item.</span></span>

<span data-ttu-id="04192-445">O exemplo substitui o bitmap de marca de seleção padrão por dois bitmaps: um bitmap com uma caixa de seleção selecionada e o bitmap com uma caixa vazia.</span><span class="sxs-lookup"><span data-stu-id="04192-445">The example replaces the default check-mark bitmap with two bitmaps: a bitmap with a selected check box and the bitmap with an empty box.</span></span> <span data-ttu-id="04192-446">O bitmap da caixa de seleção selecionada é exibido ao lado do item de menu negrito, itálico ou sublinhado quando o atributo de marca de seleção do item é definido como **MF \_ marcado**.</span><span class="sxs-lookup"><span data-stu-id="04192-446">The selected check box bitmap is displayed next to the Bold, Italic, or Underline menu item when the item's check-mark attribute is set to **MF\_CHECKED**.</span></span> <span data-ttu-id="04192-447">O bitmap da caixa de seleção limpar ou vazio é exibido quando o atributo de marca de seleção é definido como **MF \_ desmarcado**.</span><span class="sxs-lookup"><span data-stu-id="04192-447">The clear or empty check box bitmap is displayed when the check-mark attribute is set to **MF\_UNCHECKED**.</span></span>

<span data-ttu-id="04192-448">O sistema fornece um bitmap predefinido que contém as imagens usadas para caixas de seleção e botões de opção.</span><span class="sxs-lookup"><span data-stu-id="04192-448">The system provides a predefined bitmap that contains the images used for check boxes and radio buttons.</span></span> <span data-ttu-id="04192-449">O exemplo isola as caixas de seleção selecionadas e vazias, as copia para dois bitmaps separados e, em seguida, as usa como os bitmaps selecionados e limpos para itens no menu de **caracteres** .</span><span class="sxs-lookup"><span data-stu-id="04192-449">The example isolates the selected and empty check boxes, copies them to two separate bitmaps, and then uses them as the selected and cleared bitmaps for items in the **Character** menu.</span></span>

<span data-ttu-id="04192-450">Para recuperar um identificador para o bitmap da caixa de seleção definido pelo sistema, o exemplo chama a função [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) , especificando **NULL** como o parâmetro *HINSTANCE* e as **caixas de \_ seleção OBM** como o parâmetro *lpBitmapName* .</span><span class="sxs-lookup"><span data-stu-id="04192-450">To retrieve a handle to the system-defined check box bitmap, the example calls the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, specifying **NULL** as the *hInstance* parameter and **OBM\_CHECKBOXES** as the *lpBitmapName* parameter.</span></span> <span data-ttu-id="04192-451">Como as imagens no bitmap têm o mesmo tamanho, o exemplo pode isolá-las dividindo a largura e a altura do bitmap pelo número de imagens em suas linhas e colunas.</span><span class="sxs-lookup"><span data-stu-id="04192-451">Because the images in the bitmap are all the same size, the example can isolate them by dividing the bitmap width and height by the number of images in its rows and columns.</span></span>

<span data-ttu-id="04192-452">A seguinte parte de um arquivo de definição de recurso mostra como os itens de menu no menu de **caracteres** são definidos.</span><span class="sxs-lookup"><span data-stu-id="04192-452">The following portion of a resource-definition file shows how the menu items in the **Character** menu are defined.</span></span> <span data-ttu-id="04192-453">Observe que, inicialmente, nenhum atributo de fonte está em vigor, portanto, os atributos de marca de seleção para o item **regular** são definidos como selecionado e, por padrão, o atributo de marca de seleção dos itens restantes é definido como Clear.</span><span class="sxs-lookup"><span data-stu-id="04192-453">Note that no font attributes are in effect initially, so the check-mark attribute for the **Regular** item is set to selected and, by default, the check-mark attribute of the remaining items is set to clear.</span></span>


```
#include "men3.h" 
 
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "&Regular",     IDM_REGULAR, CHECKED 
        MENUITEM SEPARATOR 
        MENUITEM    "&Bold",        IDM_BOLD 
        MENUITEM    "&Italic",      IDM_ITALIC 
        MENUITEM    "&Underline",   IDM_ULINE 
    END 
END
```



<span data-ttu-id="04192-454">Aqui estão os conteúdos relevantes do arquivo de cabeçalho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-454">Here are the relevant contents of the application's header file.</span></span>


```
// Menu-item identifiers  
 
#define IDM_REGULAR 0x1 
#define IDM_BOLD    0x2 
#define IDM_ITALIC  0x4 
#define IDM_ULINE   0x8 
 
// Check-mark flags  
 
#define CHECK   1 
#define UNCHECK 2 
 
// Font-attribute mask  
 
#define ATTRIBMASK 0xe 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
HBITMAP GetMyCheckBitmaps(UINT); 
BYTE CheckOrUncheckMenuItem(BYTE, HMENU); 
```



<span data-ttu-id="04192-455">O exemplo a seguir mostra as partes do procedimento de janela que criam os bitmaps de marca de seleção; definir o atributo de marca de seleção dos itens de menu **negrito**, **itálico** e **sublinhado** ; e destrua os bitmaps de marca de seleção.</span><span class="sxs-lookup"><span data-stu-id="04192-455">The following example shows the portions of the window procedure that create the check-mark bitmaps; set the check-mark attribute of the **Bold**, **Italic**, and **Underline** menu items; and destroy check-mark bitmaps.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HBITMAP hbmpCheck;   // handle to checked bitmap    
    static HBITMAP hbmpUncheck; // handle to unchecked bitmap  
    static HMENU hmenu;         // handle to main menu         
    BYTE fbFontAttrib;          // font-attribute flags        
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Call the application-defined GetMyCheckBitmaps 
            // function to get the predefined checked and 
            // unchecked check box bitmaps. 
 
            hbmpCheck = GetMyCheckBitmaps(CHECK); 
            hbmpUncheck = GetMyCheckBitmaps(UNCHECK); 
 
            // Set the checked and unchecked bitmaps for the menu 
            // items. 
 
            hmenu = GetMenu(hwndMain); 
            SetMenuItemBitmaps(hmenu, IDM_BOLD, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ITALIC, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ULINE, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the menu commands.  
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // CheckOrUncheckMenuItem is an application- 
                    // defined function that sets the menu item 
                    // checkmarks and returns the user-selected 
                    // font attributes. 
 
                    fbFontAttrib = CheckOrUncheckMenuItem( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // Set the font attributes.  
 
                    return 0; 
 
                // Process other command messages.  
 
                default: 
                    break; 
            } 
 
            break; 
 
        // Process other window messages.  
 
        case WM_DESTROY: 
 
            // Destroy the checked and unchecked bitmaps.  
 
            DeleteObject(hbmpCheck); 
            DeleteObject(hbmpUncheck); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HBITMAP GetMyCheckBitmaps(UINT fuCheck) 
{ 
    COLORREF crBackground;  // background color                  
    HBRUSH hbrBackground;   // background brush                  
    HBRUSH hbrTargetOld;    // original background brush         
    HDC hdcSource;          // source device context             
    HDC hdcTarget;          // target device context             
    HBITMAP hbmpCheckboxes; // handle to check-box bitmap        
    BITMAP bmCheckbox;      // structure for bitmap data         
    HBITMAP hbmpSourceOld;  // handle to original source bitmap  
    HBITMAP hbmpTargetOld;  // handle to original target bitmap  
    HBITMAP hbmpCheck;      // handle to check-mark bitmap       
    RECT rc;                // rectangle for check-box bitmap    
    WORD wBitmapX;          // width of check-mark bitmap        
    WORD wBitmapY;          // height of check-mark bitmap       
 
    // Get the menu background color and create a solid brush 
    // with that color. 
 
    crBackground = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crBackground); 
 
    // Create memory device contexts for the source and 
    // destination bitmaps. 
 
    hdcSource = CreateCompatibleDC((HDC) NULL); 
    hdcTarget = CreateCompatibleDC(hdcSource); 
 
    // Get the size of the system default check-mark bitmap and 
    // create a compatible bitmap of the same size. 
 
    wBitmapX = GetSystemMetrics(SM_CXMENUCHECK); 
    wBitmapY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    hbmpCheck = CreateCompatibleBitmap(hdcSource, wBitmapX, 
        wBitmapY); 
 
    // Select the background brush and bitmap into the target DC. 
 
    hbrTargetOld = SelectObject(hdcTarget, hbrBackground); 
    hbmpTargetOld = SelectObject(hdcTarget, hbmpCheck); 
 
    // Use the selected brush to initialize the background color 
    // of the bitmap in the target device context. 
 
    PatBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, PATCOPY); 
 
    // Load the predefined check box bitmaps and select it 
    // into the source DC. 
 
    hbmpCheckboxes = LoadBitmap((HINSTANCE) NULL, 
        (LPTSTR) OBM_CHECKBOXES); 
 
    hbmpSourceOld = SelectObject(hdcSource, hbmpCheckboxes); 
 
    // Fill a BITMAP structure with information about the 
    // check box bitmaps, and then find the upper-left corner of 
    // the unchecked check box or the checked check box. 
 
    GetObject(hbmpCheckboxes, sizeof(BITMAP), &bmCheckbox); 
 
    if (fuCheck == UNCHECK) 
    { 
        rc.left = 0; 
        rc.right = (bmCheckbox.bmWidth / 4); 
    } 
    else 
    { 
        rc.left = (bmCheckbox.bmWidth / 4); 
        rc.right = (bmCheckbox.bmWidth / 4) * 2; 
    } 
 
    rc.top = 0; 
    rc.bottom = (bmCheckbox.bmHeight / 3); 
 
    // Copy the appropriate bitmap into the target DC. If the 
    // check-box bitmap is larger than the default check-mark 
    // bitmap, use StretchBlt to make it fit; otherwise, just 
    // copy it. 
 
    if (((rc.right - rc.left) > (int) wBitmapX) || 
            ((rc.bottom - rc.top) > (int) wBitmapY)) 
    {
        StretchBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, 
            hdcSource, rc.left, rc.top, rc.right - rc.left, 
            rc.bottom - rc.top, SRCCOPY); 
    }
 
    else 
    {
        BitBlt(hdcTarget, 0, 0, rc.right - rc.left, 
            rc.bottom - rc.top, 
            hdcSource, rc.left, rc.top, SRCCOPY); 
    }
 
    // Select the old source and destination bitmaps into the 
    // source and destination DCs, and then delete the DCs and 
    // the background brush. 
 
    SelectObject(hdcSource, hbmpSourceOld); 
    SelectObject(hdcTarget, hbrTargetOld); 
    hbmpCheck = SelectObject(hdcTarget, hbmpTargetOld); 
 
    DeleteObject(hbrBackground); 
    DeleteObject(hdcSource); 
    DeleteObject(hdcTarget); 
 
    // Return a handle to the new check-mark bitmap.  
 
    return hbmpCheck; 
} 
 
 
BYTE CheckOrUncheckMenuItem(BYTE bMenuItemID, HMENU hmenu) 
{ 
    DWORD fdwMenu; 
    static BYTE fbAttributes; 
 
    switch (bMenuItemID) 
    { 
        case IDM_REGULAR: 
 
            // Whenever the Regular menu item is selected, add a 
            // check mark to it and then remove checkmarks from 
            // any font-attribute menu items. 
 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
            } 
            fbAttributes = IDM_REGULAR; 
            return fbAttributes; 
 
        case IDM_BOLD: 
        case IDM_ITALIC: 
        case IDM_ULINE: 
 
            // Toggle the check mark for the selected menu item and 
            // set the font attribute flags appropriately. 
 
            fdwMenu = GetMenuState(hmenu, (UINT) bMenuItemID, 
                MF_BYCOMMAND); 
            if (!(fdwMenu & MF_CHECKED)) 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes |= bMenuItemID; 
            }
            else 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes ^= bMenuItemID; 
            } 
 
            // If any font attributes are currently selected, 
            // remove the check mark from the Regular menu item; 
            // if no attributes are selected, add a check mark 
            // to the Regular menu item. 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes &= (BYTE) ~IDM_REGULAR; 
            }
            else 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes = IDM_REGULAR; 
            } 
 
            return fbAttributes; 
    } 
} 
```



### <a name="example-of-using-custom-check-mark-bitmaps"></a><span data-ttu-id="04192-456">Exemplo de como usar bitmaps de marca de seleção personalizados</span><span class="sxs-lookup"><span data-stu-id="04192-456">Example of Using Custom Check-mark Bitmaps</span></span>

<span data-ttu-id="04192-457">O exemplo neste tópico atribui bitmaps de marca de seleção personalizados a itens de menu em dois menus.</span><span class="sxs-lookup"><span data-stu-id="04192-457">The example in this topic assigns custom check-mark bitmaps to menu items in two menus.</span></span> <span data-ttu-id="04192-458">Os itens de menu no primeiro menu especificam atributos de caractere: negrito, itálico e sublinhado.</span><span class="sxs-lookup"><span data-stu-id="04192-458">The menu items in the first menu specify character attributes: bold, italic, and underline.</span></span> <span data-ttu-id="04192-459">Cada item de menu pode ser selecionado ou limpo.</span><span class="sxs-lookup"><span data-stu-id="04192-459">Each menu item can be either selected or cleared.</span></span> <span data-ttu-id="04192-460">Para esses itens de menu, o exemplo usa bitmaps de marca de seleção que se assemelham aos Estados selecionado e limpo de um controle de caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="04192-460">For these menu items, the example uses check-mark bitmaps that resemble the selected and cleared states of a check box control.</span></span>

<span data-ttu-id="04192-461">Os itens de menu no segundo menu especificam as configurações de alinhamento de parágrafo: esquerda, centralizado e direita.</span><span class="sxs-lookup"><span data-stu-id="04192-461">The menu items in the second menu specify paragraph alignment settings: left, centered, and right.</span></span> <span data-ttu-id="04192-462">Somente um desses itens de menu é selecionado a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="04192-462">Only one of these menu items is selected at any time.</span></span> <span data-ttu-id="04192-463">Para esses itens de menu, o exemplo usa bitmaps de marca de seleção que se assemelham aos Estados selecionado e claro de um controle de botão de opção.</span><span class="sxs-lookup"><span data-stu-id="04192-463">For these menu items, the example uses check-mark bitmaps that resemble the selected and clear states of a radio button control.</span></span>

<span data-ttu-id="04192-464">O procedimento de janela processa a mensagem do [**WM \_ Create**](/windows/desktop/winmsg/wm-create) chamando a função OnCreate definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-464">The window procedure processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message by calling the application-defined OnCreate function.</span></span> <span data-ttu-id="04192-465">`OnCreate` cria os quatro bitmaps de marca de seleção e os atribui aos itens de menu apropriados usando a função [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) .</span><span class="sxs-lookup"><span data-stu-id="04192-465">`OnCreate` creates the four check-mark bitmaps and then assigns them to their appropriate menu items by using the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span>

<span data-ttu-id="04192-466">Para criar cada bitmap, OnCreate chama a função CreateMenuBitmaps definida pelo aplicativo, especificando um ponteiro para uma função de desenho específica de bitmap.</span><span class="sxs-lookup"><span data-stu-id="04192-466">To create each bitmap, OnCreate calls the application-defined CreateMenuBitmaps function, specifying a pointer to a bitmap-specific drawing function.</span></span> <span data-ttu-id="04192-467">O CreateMenuBitmaps cria um bitmap monocromático do tamanho necessário, seleciona-o em um contexto de dispositivo de memória e apaga o plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="04192-467">CreateMenuBitmaps creates a monochrome bitmap of the required size, selects it into a memory device context, and erases the background.</span></span> <span data-ttu-id="04192-468">Em seguida, ele chama a função de desenho especificada para preencher o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="04192-468">Then it calls the specified drawing function to fill in the foreground.</span></span>

<span data-ttu-id="04192-469">As quatro funções de desenho definidas pelo aplicativo são DrawCheck, DrawUncheck, **DrawRadioCheck** e DrawRadioUncheck.</span><span class="sxs-lookup"><span data-stu-id="04192-469">The four application-defined drawing functions are DrawCheck, DrawUncheck, **DrawRadioCheck**, and DrawRadioUncheck.</span></span> <span data-ttu-id="04192-470">Eles desenham um retângulo com um X, um retângulo vazio, uma elipse contendo uma elipse preenchida menor e uma elipse vazia, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="04192-470">They draw a rectangle with an X, an empty rectangle, an ellipse containing a smaller filled ellipse, and an empty ellipse, respectively.</span></span>

<span data-ttu-id="04192-471">O procedimento de janela processa a mensagem do [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) excluindo os bitmaps de marca de seleção.</span><span class="sxs-lookup"><span data-stu-id="04192-471">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message by deleting the check-mark bitmaps.</span></span> <span data-ttu-id="04192-472">Ele recupera cada identificador de bitmap usando a função [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) e, em seguida, passa um identificador para a função.</span><span class="sxs-lookup"><span data-stu-id="04192-472">It retrieves each bitmap handle by using the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function and then passes a handle to the function.</span></span>

<span data-ttu-id="04192-473">Quando o usuário escolhe um item de menu, uma mensagem de [**\_ comando do WM**](wm-command.md) é enviada para a janela do proprietário.</span><span class="sxs-lookup"><span data-stu-id="04192-473">When the user chooses a menu item, a [**WM\_COMMAND**](wm-command.md) message is sent to the owner window.</span></span> <span data-ttu-id="04192-474">Para itens de menu no menu de **caracteres** , o procedimento de janela chama a função CheckCharacterItem definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-474">For menu items on the **Character** menu, the window procedure calls the application-defined CheckCharacterItem function.</span></span> <span data-ttu-id="04192-475">Para itens no menu de **parágrafo** , o procedimento de janela chama a função CheckParagraphItem definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-475">For items on the **Paragraph** menu, the window procedure calls the application-defined CheckParagraphItem function.</span></span>

<span data-ttu-id="04192-476">Cada item no menu de **caracteres** pode ser selecionado e limpo de forma independente.</span><span class="sxs-lookup"><span data-stu-id="04192-476">Each item on the **Character** menu can be selected and cleared independently.</span></span> <span data-ttu-id="04192-477">Portanto, CheckCharacterItem simplesmente alterna o estado de verificação do item de menu especificado.</span><span class="sxs-lookup"><span data-stu-id="04192-477">Therefore, CheckCharacterItem simply switches the specified menu item's check state.</span></span> <span data-ttu-id="04192-478">Primeiro, a função chama a função [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) para obter o estado do item de menu atual.</span><span class="sxs-lookup"><span data-stu-id="04192-478">First, the function calls the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function to get the current menu item state.</span></span> <span data-ttu-id="04192-479">Em seguida, ele alterna o sinalizador de estado **\_ verificado do MFS** e define o novo estado chamando a função [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="04192-479">Then it switches the **MFS\_CHECKED** state flag and sets the new state by calling the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="04192-480">Ao contrário dos atributos de caractere, somente um alinhamento de parágrafo pode ser selecionado de cada vez.</span><span class="sxs-lookup"><span data-stu-id="04192-480">Unlike character attributes, only one paragraph alignment can be selected at a time.</span></span> <span data-ttu-id="04192-481">Portanto, CheckParagraphItem verifica o item de menu especificado e remove a marca de seleção de todos os outros itens no menu.</span><span class="sxs-lookup"><span data-stu-id="04192-481">Therefore, CheckParagraphItem checks the specified menu item and removes the check mark from all other items on the menu.</span></span> <span data-ttu-id="04192-482">Para fazer isso, ele chama a função [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) .</span><span class="sxs-lookup"><span data-stu-id="04192-482">To do so, it calls the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function.</span></span>

<span data-ttu-id="04192-483">A seguir estão as partes relevantes do arquivo de cabeçalho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04192-483">Following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_BOLD      11 
#define IDM_ITALIC    12 
#define IDM_UNDERLINE 13 
 
// Menu-item identifiers for the Paragraph menu 
 
#define IDM_PARAGRAPH 20 
#define IDM_LEFT      21 
#define IDM_CENTER    22 
#define IDM_RIGHT     23 
 
// Function-pointer type for drawing functions 
 
typedef VOID (WINAPI * DRAWFUNC)(HDC hdc, SIZE size); 
 
```



<span data-ttu-id="04192-484">A seguir estão as partes relevantes do procedimento de janela do aplicativo e funções relacionadas.</span><span class="sxs-lookup"><span data-stu-id="04192-484">The following are the relevant portions of the application's window procedure and related functions.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_UNDERLINE: 
                    CheckCharacterItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                case IDM_LEFT: 
                case IDM_CENTER: 
                case IDM_RIGHT: 
                    CheckParagraphItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                // Process other commands here. 
 
            } 
            break; 
 
        // Process other messages here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
VOID WINAPI CheckCharacterItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the state of the specified menu item. 
 
    mii.fMask = MIIM_STATE;    // information to get 
    GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
 
    // Toggle the checked state. 
 
    mii.fState ^= MFS_CHECKED; 
    SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
} 
 
VOID WINAPI CheckParagraphItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Check the specified item and uncheck all the others. 
 
    CheckMenuRadioItem( 
            hmenuPopup,         // handle to menu 
            IDM_LEFT,           // first item in range 
            IDM_RIGHT,          // last item in range 
            uID,                // item to check 
            MF_BYCOMMAND        // IDs, not positions 
            ); 
} 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    HBITMAP hbmChecked; 
    HBITMAP hbmUnchecked; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_BOLD; uID <= IDM_UNDERLINE; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Get a handle to the Paragraph pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawRadioCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawRadioUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_LEFT; uID <= IDM_RIGHT; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Initially check the IDM_LEFT paragraph item. 
 
    CheckMenuRadioItem(hmenuPopup, IDM_LEFT, IDM_RIGHT, 
            IDM_LEFT, MF_BYCOMMAND); 
    return TRUE; 
} 
 
HBITMAP WINAPI CreateMenuBitmap(DRAWFUNC lpfnDraw) 
{ 
    // Create a DC compatible with the desktop window's DC. 
 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
 
    // Determine the required bitmap size. 
 
    SIZE size = { GetSystemMetrics(SM_CXMENUCHECK), 
                  GetSystemMetrics(SM_CYMENUCHECK) }; 
 
    // Create a monochrome bitmap and select it. 
 
    HBITMAP hbm = CreateBitmap(size.cx, size.cy, 1, 1, NULL); 
    HBITMAP hbmOld = SelectObject(hdcMem, hbm); 
 
    // Erase the background and call the drawing function. 
 
    PatBlt(hdcMem, 0, 0, size.cx, size.cy, WHITENESS); 
    (*lpfnDraw)(hdcMem, size); 
 
    // Clean up. 
 
    SelectObject(hdcMem, hbmOld); 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
    return hbm; 
} 
 
VOID WINAPI DrawCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    MoveToEx(hdc, 0, 0, NULL); 
    LineTo(hdc, size.cx, size.cy); 
    MoveToEx(hdc, 0, size.cy - 1, NULL); 
    LineTo(hdc, size.cx - 1, 0); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, GetStockObject(BLACK_BRUSH)); 
    Ellipse(hdc, 2, 2, size.cx - 2, size.cy - 2); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_BOLD, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_LEFT, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
} 
```



 

 