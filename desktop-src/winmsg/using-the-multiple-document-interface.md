---
description: Esta seção explica como executar tarefas associadas à interface de vários documentos.
ms.assetid: 024744d3-362f-4162-8d0a-d4dac61de808
title: Usando a interface de vários documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e24aed7abc3640b441345520203c8a02e025e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769122"
---
# <a name="using-the-multiple-document-interface"></a><span data-ttu-id="0ec84-103">Usando a interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="0ec84-103">Using the Multiple Document Interface</span></span>

<span data-ttu-id="0ec84-104">Esta seção explica como executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="0ec84-104">This section explains how to perform the following tasks:</span></span>

-   [<span data-ttu-id="0ec84-105">Registrando classes de janela filho e de quadro</span><span class="sxs-lookup"><span data-stu-id="0ec84-105">Registering Child and Frame Window Classes</span></span>](#registering-child-and-frame-window-classes)
-   [<span data-ttu-id="0ec84-106">Criando janelas de quadro e filho</span><span class="sxs-lookup"><span data-stu-id="0ec84-106">Creating Frame and Child Windows</span></span>](#creating-frame-and-child-windows)
-   [<span data-ttu-id="0ec84-107">Escrevendo o loop de mensagem principal</span><span class="sxs-lookup"><span data-stu-id="0ec84-107">Writing the Main Message Loop</span></span>](#writing-the-main-message-loop)
-   [<span data-ttu-id="0ec84-108">Escrevendo o procedimento da janela do quadro</span><span class="sxs-lookup"><span data-stu-id="0ec84-108">Writing the Frame Window Procedure</span></span>](#writing-the-frame-window-procedure)
-   [<span data-ttu-id="0ec84-109">Escrevendo o procedimento de janela filho</span><span class="sxs-lookup"><span data-stu-id="0ec84-109">Writing the Child Window Procedure</span></span>](#writing-the-child-window-procedure)
-   [<span data-ttu-id="0ec84-110">Criando uma janela filho</span><span class="sxs-lookup"><span data-stu-id="0ec84-110">Creating a Child Window</span></span>](#creating-a-child-window)

<span data-ttu-id="0ec84-111">Para ilustrar essas tarefas, esta seção inclui exemplos do Multipad, um aplicativo típico de MDI (interface de vários documentos).</span><span class="sxs-lookup"><span data-stu-id="0ec84-111">To illustrate these tasks, this section includes examples from Multipad, a typical multiple-document interface (MDI) application.</span></span>

## <a name="registering-child-and-frame-window-classes"></a><span data-ttu-id="0ec84-112">Registrando classes de janela filho e de quadro</span><span class="sxs-lookup"><span data-stu-id="0ec84-112">Registering Child and Frame Window Classes</span></span>

<span data-ttu-id="0ec84-113">Um aplicativo MDI típico deve registrar duas classes de janela: uma para sua janela de quadro e outra para suas janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="0ec84-113">A typical MDI application must register two window classes: one for its frame window and one for its child windows.</span></span> <span data-ttu-id="0ec84-114">Se um aplicativo oferecer suporte a mais de um tipo de documento (por exemplo, uma planilha e um gráfico), ele deverá registrar uma classe de janela para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="0ec84-114">If an application supports more than one type of document (for example, a spreadsheet and a chart), it must register a window class for each type.</span></span>

<span data-ttu-id="0ec84-115">A estrutura de classe da janela do quadro é semelhante à estrutura de classe da janela principal em aplicativos não MDI.</span><span class="sxs-lookup"><span data-stu-id="0ec84-115">The class structure for the frame window is similar to the class structure for the main window in non–MDI applications.</span></span> <span data-ttu-id="0ec84-116">A estrutura de classe para as janelas filho MDI difere ligeiramente da estrutura para janelas filhas em aplicativos não-MDI, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0ec84-116">The class structure for the MDI child windows differs slightly from the structure for child windows in non–MDI applications as follows:</span></span>

-   <span data-ttu-id="0ec84-117">A estrutura de classe deve ter um ícone, porque o usuário pode minimizar uma janela filho MDI como se fosse uma janela de aplicativo normal.</span><span class="sxs-lookup"><span data-stu-id="0ec84-117">The class structure should have an icon, because the user can minimize an MDI child window as if it were a normal application window.</span></span>
-   <span data-ttu-id="0ec84-118">O nome do menu deve ser **nulo**, pois uma janela filho MDI não pode ter seu próprio menu.</span><span class="sxs-lookup"><span data-stu-id="0ec84-118">The menu name should be **NULL**, because an MDI child window cannot have its own menu.</span></span>
-   <span data-ttu-id="0ec84-119">A estrutura de classe deve reservar espaço extra na estrutura de janela.</span><span class="sxs-lookup"><span data-stu-id="0ec84-119">The class structure should reserve extra space in the window structure.</span></span> <span data-ttu-id="0ec84-120">Com esse espaço, o aplicativo pode associar dados, como um nome de arquivo, a uma janela filho específica.</span><span class="sxs-lookup"><span data-stu-id="0ec84-120">With this space, the application can associate data, such as a filename, with a particular child window.</span></span>

<span data-ttu-id="0ec84-121">O exemplo a seguir mostra como o Multipad registra suas classes de quadro e janela filho.</span><span class="sxs-lookup"><span data-stu-id="0ec84-121">The following example shows how Multipad registers its frame and child window classes.</span></span>


```
BOOL WINAPI InitializeApplication() 
{ 
    WNDCLASS wc; 
 
    // Register the frame window class. 
 
    wc.style         = 0; 
    wc.lpfnWndProc   = (WNDPROC) MPFrameWndProc; 
    wc.cbClsExtra    = 0; 
    wc.cbWndExtra    = 0; 
    wc.hInstance     = hInst; 
    wc.hIcon         = LoadIcon(hInst, IDMULTIPAD); 
    wc.hCursor       = LoadCursor((HANDLE) NULL, IDC_ARROW); 
    wc.hbrBackground = (HBRUSH) (COLOR_APPWORKSPACE + 1); 
    wc.lpszMenuName  = IDMULTIPAD; 
    wc.lpszClassName = szFrame; 
 
    if (!RegisterClass (&wc) ) 
        return FALSE; 
 
    // Register the MDI child window class. 
 
    wc.lpfnWndProc   = (WNDPROC) MPMDIChildWndProc; 
    wc.hIcon         = LoadIcon(hInst, IDNOTE); 
    wc.lpszMenuName  = (LPCTSTR) NULL; 
    wc.cbWndExtra    = CBWNDEXTRA; 
    wc.lpszClassName = szChild; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    return TRUE; 
} 
```



## <a name="creating-frame-and-child-windows"></a><span data-ttu-id="0ec84-122">Criando janelas de quadro e filho</span><span class="sxs-lookup"><span data-stu-id="0ec84-122">Creating Frame and Child Windows</span></span>

<span data-ttu-id="0ec84-123">Depois de registrar suas classes de janela, um aplicativo MDI pode criar suas janelas.</span><span class="sxs-lookup"><span data-stu-id="0ec84-123">After registering its window classes, an MDI application can create its windows.</span></span> <span data-ttu-id="0ec84-124">Primeiro, ele cria sua janela de quadros usando a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="0ec84-124">First, it creates its frame window by using the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="0ec84-125">Depois de criar sua janela de quadros, o aplicativo cria a janela do cliente novamente usando **CreateWindow** ou **CreateWindowEx**.</span><span class="sxs-lookup"><span data-stu-id="0ec84-125">After creating its frame window, the application creates its client window, again by using **CreateWindow** or **CreateWindowEx**.</span></span> <span data-ttu-id="0ec84-126">O aplicativo deve especificar MDICLIENT como o nome da classe da janela do cliente; **MdiClient** é uma classe de janela preregistrada definida pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="0ec84-126">The application should specify MDICLIENT as the client window's class name; **MDICLIENT** is a preregistered window class defined by the system.</span></span> <span data-ttu-id="0ec84-127">O parâmetro *lpvParam* de **CreateWindow** ou **CreateWindowEx** deve apontar para uma estrutura [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) .</span><span class="sxs-lookup"><span data-stu-id="0ec84-127">The *lpvParam* parameter of **CreateWindow** or **CreateWindowEx** should point to a [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) structure.</span></span> <span data-ttu-id="0ec84-128">Essa estrutura contém os membros descritos na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="0ec84-128">This structure contains the members described in the following table:</span></span>



| <span data-ttu-id="0ec84-129">Membro</span><span class="sxs-lookup"><span data-stu-id="0ec84-129">Member</span></span>           | <span data-ttu-id="0ec84-130">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="0ec84-130">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ec84-131">**hWindowMenu**</span><span class="sxs-lookup"><span data-stu-id="0ec84-131">**hWindowMenu**</span></span>  | <span data-ttu-id="0ec84-132">Identificador para o menu de janela usado para controlar janelas filhas MDI.</span><span class="sxs-lookup"><span data-stu-id="0ec84-132">Handle to the window menu used for controlling MDI child windows.</span></span> <span data-ttu-id="0ec84-133">À medida que as janelas filhas são criadas, o aplicativo adiciona seus títulos ao menu janela como itens de menu.</span><span class="sxs-lookup"><span data-stu-id="0ec84-133">As child windows are created, the application adds their titles to the window menu as menu items.</span></span> <span data-ttu-id="0ec84-134">Em seguida, o usuário pode ativar uma janela filho clicando em seu título no menu janela.</span><span class="sxs-lookup"><span data-stu-id="0ec84-134">The user can then activate a child window by clicking its title on the window menu.</span></span>                                                               |
| <span data-ttu-id="0ec84-135">**idFirstChild**</span><span class="sxs-lookup"><span data-stu-id="0ec84-135">**idFirstChild**</span></span> | <span data-ttu-id="0ec84-136">Especifica o identificador da primeira janela filho MDI.</span><span class="sxs-lookup"><span data-stu-id="0ec84-136">Specifies the identifier of the first MDI child window.</span></span> <span data-ttu-id="0ec84-137">A primeira janela filho MDI criada é atribuída a esse identificador.</span><span class="sxs-lookup"><span data-stu-id="0ec84-137">The first MDI child window created is assigned this identifier.</span></span> <span data-ttu-id="0ec84-138">Janelas adicionais são criadas com identificadores de janela incrementados.</span><span class="sxs-lookup"><span data-stu-id="0ec84-138">Additional windows are created with incremented window identifiers.</span></span> <span data-ttu-id="0ec84-139">Quando uma janela filho é destruída, o sistema reatribui imediatamente os identificadores de janela para manter seu intervalo contíguo.</span><span class="sxs-lookup"><span data-stu-id="0ec84-139">When a child window is destroyed, the system immediately reassigns the window identifiers to keep their range contiguous.</span></span> |



 

<span data-ttu-id="0ec84-140">Quando o título de uma janela filho é adicionado ao menu janela, o sistema atribui um identificador à janela filho.</span><span class="sxs-lookup"><span data-stu-id="0ec84-140">When a child window's title is added to the window menu, the system assigns an identifier to the child window.</span></span> <span data-ttu-id="0ec84-141">Quando o usuário clica no título de uma janela filho, a janela do quadro recebe uma mensagem de [**\_ comando do WM**](../menurc/wm-command.md) com o identificador no parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="0ec84-141">When the user clicks a child window's title, the frame window receives a [**WM\_COMMAND**](../menurc/wm-command.md) message with the identifier in the *wParam* parameter.</span></span> <span data-ttu-id="0ec84-142">Você deve especificar um valor para o membro **idFirstChild** que não esteja em conflito com identificadores de item de menu no menu da janela do quadro.</span><span class="sxs-lookup"><span data-stu-id="0ec84-142">You should specify a value for the **idFirstChild** member that does not conflict with menu-item identifiers in the frame window's menu.</span></span>

<span data-ttu-id="0ec84-143">O procedimento da janela do quadro do Multipad cria a janela do cliente MDI durante o processamento da mensagem de [**\_ criação do WM**](wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="0ec84-143">Multipad's frame window procedure creates the MDI client window while processing the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="0ec84-144">O exemplo a seguir mostra como a janela do cliente é criada.</span><span class="sxs-lookup"><span data-stu-id="0ec84-144">The following example shows how the client window is created.</span></span>


```
case WM_CREATE: 
    { 
        CLIENTCREATESTRUCT ccs; 
 
        // Retrieve the handle to the window menu and assign the 
        // first child window identifier. 
 
        ccs.hWindowMenu = GetSubMenu(GetMenu(hwnd), WINDOWMENU); 
        ccs.idFirstChild = IDM_WINDOWCHILD; 
 
        // Create the MDI client window. 
 
        hwndMDIClient = CreateWindow( "MDICLIENT", (LPCTSTR) NULL, 
            WS_CHILD | WS_CLIPCHILDREN | WS_VSCROLL | WS_HSCROLL, 
            0, 0, 0, 0, hwnd, (HMENU) 0xCAC, hInst, (LPSTR) &ccs); 
 
        ShowWindow(hwndMDIClient, SW_SHOW); 
    } 
    break; 
```



<span data-ttu-id="0ec84-145">Os títulos das janelas filhas são adicionados à parte inferior do menu janela.</span><span class="sxs-lookup"><span data-stu-id="0ec84-145">Titles of child windows are added to the bottom of the window menu.</span></span> <span data-ttu-id="0ec84-146">Se o aplicativo adicionar cadeias de caracteres ao menu de janela usando a função [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) , essas cadeias de caracteres poderão ser substituídas pelos títulos das janelas filhas quando o menu janela for redesenhado (sempre que uma janela filho for criada ou destruída).</span><span class="sxs-lookup"><span data-stu-id="0ec84-146">If the application adds strings to the window menu by using the [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function, these strings can be overwritten by the titles of the child windows when the window menu is repainted (whenever a child window is created or destroyed).</span></span> <span data-ttu-id="0ec84-147">Um aplicativo MDI que adiciona cadeias de caracteres ao menu de janela deve usar a função [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) e verificar se os títulos das janelas filhas não substituíram essas novas cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0ec84-147">An MDI application that adds strings to its window menu should use the [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) function and verify that the titles of child windows have not overwritten these new strings.</span></span>

<span data-ttu-id="0ec84-148">Use o estilo **WS \_ CLIPCHILDREN** para criar a janela do cliente MDI para impedir que a janela pinte sobre suas janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="0ec84-148">Use the **WS\_CLIPCHILDREN** style to create the MDI client window to prevent the window from painting over its child windows.</span></span>

## <a name="writing-the-main-message-loop"></a><span data-ttu-id="0ec84-149">Escrevendo o loop de mensagem principal</span><span class="sxs-lookup"><span data-stu-id="0ec84-149">Writing the Main Message Loop</span></span>

<span data-ttu-id="0ec84-150">O loop de mensagem principal de um aplicativo MDI é semelhante ao de uma chave do acelerador de manipulação de aplicativos não MDI.</span><span class="sxs-lookup"><span data-stu-id="0ec84-150">The main message loop of an MDI application is similar to that of a non-MDI application handling accelerator keys.</span></span> <span data-ttu-id="0ec84-151">A diferença é que o loop de mensagem MDI chama a função [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) antes de verificar se há chaves de acelerador definidas pelo aplicativo ou antes de expedir a mensagem.</span><span class="sxs-lookup"><span data-stu-id="0ec84-151">The difference is that the MDI message loop calls the [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function before checking for application-defined accelerator keys or before dispatching the message.</span></span>

<span data-ttu-id="0ec84-152">O exemplo a seguir mostra o loop de mensagem de um aplicativo MDI típico.</span><span class="sxs-lookup"><span data-stu-id="0ec84-152">The following example shows the message loop of a typical MDI application.</span></span> <span data-ttu-id="0ec84-153">Observe que [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) pode retornar-1 se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="0ec84-153">Note that [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) can return -1 if there is an error.</span></span>


```
MSG msg;
BOOL bRet;

while ((bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else 
    { 
        if (!TranslateMDISysAccel(hwndMDIClient, &msg) && 
                !TranslateAccelerator(hwndFrame, hAccel, &msg))
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



<span data-ttu-id="0ec84-154">A função [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) converte as mensagens do [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md) em mensagens do [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) e as envia para a janela filho MDI ativa.</span><span class="sxs-lookup"><span data-stu-id="0ec84-154">The [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function translates [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) messages into [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) messages and sends them to the active MDI child window.</span></span> <span data-ttu-id="0ec84-155">Se a mensagem não for uma mensagem de acelerador de MDI, a função retornará **false**; nesse caso, o aplicativo usará a função [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) para determinar se alguma das teclas de aceleração definidas pelo aplicativo foi pressionada.</span><span class="sxs-lookup"><span data-stu-id="0ec84-155">If the message is not an MDI accelerator message, the function returns **FALSE**, in which case the application uses the [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function to determine whether any of the application-defined accelerator keys were pressed.</span></span> <span data-ttu-id="0ec84-156">Caso contrário, o loop expedirá a mensagem para o procedimento de janela apropriado.</span><span class="sxs-lookup"><span data-stu-id="0ec84-156">If not, the loop dispatches the message to the appropriate window procedure.</span></span>

## <a name="writing-the-frame-window-procedure"></a><span data-ttu-id="0ec84-157">Escrevendo o procedimento da janela do quadro</span><span class="sxs-lookup"><span data-stu-id="0ec84-157">Writing the Frame Window Procedure</span></span>

<span data-ttu-id="0ec84-158">O procedimento de janela para uma janela de quadro MDI é semelhante ao de uma janela principal do aplicativo não-MDI.</span><span class="sxs-lookup"><span data-stu-id="0ec84-158">The window procedure for an MDI frame window is similar to that of a non–MDI application's main window.</span></span> <span data-ttu-id="0ec84-159">A diferença é que um procedimento de janela de quadro passa todas as mensagens que ele não manipula para a função [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) em vez de para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="0ec84-159">The difference is that a frame window procedure passes all messages it does not handle to the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="0ec84-160">Além disso, o procedimento de janela do quadro também deve passar algumas mensagens que ele manipula, incluindo aquelas listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0ec84-160">In addition, the frame window procedure must also pass some messages that it does handle, including those listed in the following table.</span></span>



| <span data-ttu-id="0ec84-161">Mensagem</span><span class="sxs-lookup"><span data-stu-id="0ec84-161">Message</span></span>                                  | <span data-ttu-id="0ec84-162">Resposta</span><span class="sxs-lookup"><span data-stu-id="0ec84-162">Response</span></span>                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ec84-163">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0ec84-163">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)     | <span data-ttu-id="0ec84-164">Ativa a janela filho MDI que o usuário escolhe.</span><span class="sxs-lookup"><span data-stu-id="0ec84-164">Activates the MDI child window that the user chooses.</span></span> <span data-ttu-id="0ec84-165">Essa mensagem é enviada quando o usuário escolhe uma janela filho MDI no menu janela da janela do quadro MDI.</span><span class="sxs-lookup"><span data-stu-id="0ec84-165">This message is sent when the user chooses an MDI child window from the window menu of the MDI frame window.</span></span> <span data-ttu-id="0ec84-166">O identificador de janela que acompanha essa mensagem identifica a janela filho MDI a ser ativada.</span><span class="sxs-lookup"><span data-stu-id="0ec84-166">The window identifier accompanying this message identifies the MDI child window to be activated.</span></span> |
| [<span data-ttu-id="0ec84-167">**MENUCHAR do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0ec84-167">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)   | <span data-ttu-id="0ec84-168">Abre o menu janela da janela filho MDI ativa quando o usuário pressiona a combinação de teclas ALT + – (menos).</span><span class="sxs-lookup"><span data-stu-id="0ec84-168">Opens the window menu of the active MDI child window when the user presses the ALT+ – (minus) key combination.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="0ec84-169">**WM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="0ec84-169">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md) | <span data-ttu-id="0ec84-170">Passa o foco do teclado para a janela do cliente MDI, que, por sua vez, passa para a janela filho MDI ativa.</span><span class="sxs-lookup"><span data-stu-id="0ec84-170">Passes the keyboard focus to the MDI client window, which in turn passes it to the active MDI child window.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="0ec84-171">**tamanho do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0ec84-171">**WM\_SIZE**</span></span>](wm-size.md)              | <span data-ttu-id="0ec84-172">Redimensiona a janela do cliente MDI para caber na área do cliente da janela do novo quadro.</span><span class="sxs-lookup"><span data-stu-id="0ec84-172">Resizes the MDI client window to fit in the new frame window's client area.</span></span> <span data-ttu-id="0ec84-173">Se o procedimento da janela do quadro dimensionar a janela do cliente MDI para um tamanho diferente, ele não deverá passar a mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="0ec84-173">If the frame window procedure sizes the MDI client window to a different size, it should not pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>                   |



 

<span data-ttu-id="0ec84-174">O procedimento de janela do quadro em Multipad é chamado de MPFrameWndProc.</span><span class="sxs-lookup"><span data-stu-id="0ec84-174">The frame window procedure in Multipad is called MPFrameWndProc.</span></span> <span data-ttu-id="0ec84-175">O tratamento de outras mensagens por MPFrameWndProc é semelhante ao dos aplicativos não-MDI.</span><span class="sxs-lookup"><span data-stu-id="0ec84-175">The handling of other messages by MPFrameWndProc is similar to that of non–MDI applications.</span></span> <span data-ttu-id="0ec84-176">[**WM \_**](../menurc/wm-command.md) As mensagens de comando em Multipad são manipuladas pela função CommandHandler definida localmente.</span><span class="sxs-lookup"><span data-stu-id="0ec84-176">[**WM\_COMMAND**](../menurc/wm-command.md) messages in Multipad are handled by the locally defined CommandHandler function.</span></span> <span data-ttu-id="0ec84-177">Para mensagens de comando Multipad não manipula, CommandHandler chama a função [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) .</span><span class="sxs-lookup"><span data-stu-id="0ec84-177">For command messages Multipad does not handle, CommandHandler calls the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function.</span></span> <span data-ttu-id="0ec84-178">Se Multipad não usar **DefFrameProc** por padrão, o usuário não poderá ativar uma janela filho no menu janela, pois a mensagem **de \_ comando do WM** enviada clicando no item de menu da janela seria perdida.</span><span class="sxs-lookup"><span data-stu-id="0ec84-178">If Multipad does not use **DefFrameProc** by default, the user can't activate a child window from the window menu, because the **WM\_COMMAND** message sent by clicking the window's menu item would be lost.</span></span>

## <a name="writing-the-child-window-procedure"></a><span data-ttu-id="0ec84-179">Escrevendo o procedimento de janela filho</span><span class="sxs-lookup"><span data-stu-id="0ec84-179">Writing the Child Window Procedure</span></span>

<span data-ttu-id="0ec84-180">Assim como o procedimento de janela do quadro, um procedimento de janela filho MDI usa uma função especial para processar mensagens por padrão.</span><span class="sxs-lookup"><span data-stu-id="0ec84-180">Like the frame window procedure, an MDI child window procedure uses a special function for processing messages by default.</span></span> <span data-ttu-id="0ec84-181">Todas as mensagens que o procedimento da janela filho não trata devem ser passadas para a função [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) em vez de para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="0ec84-181">All messages that the child window procedure does not handle must be passed to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="0ec84-182">Além disso, algumas mensagens de gerenciamento de janelas devem ser passadas para **DefMDIChildProc**, mesmo que o aplicativo manipule a mensagem, para que o MDI funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="0ec84-182">In addition, some window-management messages must be passed to **DefMDIChildProc**, even if the application handles the message, in order for MDI to function correctly.</span></span> <span data-ttu-id="0ec84-183">A seguir estão as mensagens que o aplicativo deve passar para **DefMDIChildProc**.</span><span class="sxs-lookup"><span data-stu-id="0ec84-183">Following are the messages the application must pass to **DefMDIChildProc**.</span></span>



| <span data-ttu-id="0ec84-184">Mensagem</span><span class="sxs-lookup"><span data-stu-id="0ec84-184">Message</span></span>                                       | <span data-ttu-id="0ec84-185">Resposta</span><span class="sxs-lookup"><span data-stu-id="0ec84-185">Response</span></span>                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ec84-186">**CHILDACTIVATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0ec84-186">**WM\_CHILDACTIVATE**</span></span>](wm-childactivate.md) | <span data-ttu-id="0ec84-187">Executa o processamento de ativação quando janelas filho MDI são dimensionadas, movidas ou exibidas.</span><span class="sxs-lookup"><span data-stu-id="0ec84-187">Performs activation processing when MDI child windows are sized, moved, or displayed.</span></span> <span data-ttu-id="0ec84-188">Esta mensagem deve ser passada.</span><span class="sxs-lookup"><span data-stu-id="0ec84-188">This message must be passed.</span></span>                                                                                                                                        |
| [<span data-ttu-id="0ec84-189">**GETMINMAXINFO do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0ec84-189">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md) | <span data-ttu-id="0ec84-190">Calcula o tamanho de uma janela filho MDI maximizada, com base no tamanho atual da janela do cliente MDI.</span><span class="sxs-lookup"><span data-stu-id="0ec84-190">Calculates the size of a maximized MDI child window, based on the current size of the MDI client window.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="0ec84-191">**MENUCHAR do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0ec84-191">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)        | <span data-ttu-id="0ec84-192">Passa a mensagem para a janela do quadro MDI.</span><span class="sxs-lookup"><span data-stu-id="0ec84-192">Passes the message to the MDI frame window.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="0ec84-193">**movimentação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0ec84-193">**WM\_MOVE**</span></span>](wm-move.md)                   | <span data-ttu-id="0ec84-194">Recalcula as barras de rolagem do cliente MDI, se estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="0ec84-194">Recalculates MDI client scroll bars, if they are present.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="0ec84-195">**WM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="0ec84-195">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)      | <span data-ttu-id="0ec84-196">Ativa a janela filho, se não for a janela filho MDI ativa.</span><span class="sxs-lookup"><span data-stu-id="0ec84-196">Activates the child window, if it is not the active MDI child window.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="0ec84-197">**tamanho do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0ec84-197">**WM\_SIZE**</span></span>](wm-size.md)                   | <span data-ttu-id="0ec84-198">Executa operações necessárias para alterar o tamanho de uma janela, especialmente para maximizar ou restaurar uma janela filho MDI.</span><span class="sxs-lookup"><span data-stu-id="0ec84-198">Performs operations necessary for changing the size of a window, especially for maximizing or restoring an MDI child window.</span></span> <span data-ttu-id="0ec84-199">A falha ao passar essa mensagem para a função [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) produz resultados altamente indesejáveis.</span><span class="sxs-lookup"><span data-stu-id="0ec84-199">Failing to pass this message to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function produces highly undesirable results.</span></span> |
| [<span data-ttu-id="0ec84-200">**SYSCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0ec84-200">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)    | <span data-ttu-id="0ec84-201">Manipula comandos de menu Window (anteriormente conhecidos como System) **: SC \_ NEXTWINDOW**, **sc \_ PREVWINDOW**, **sc \_ mover**, **sc \_ size** e **sc \_ Maxim**.</span><span class="sxs-lookup"><span data-stu-id="0ec84-201">Handles window (formerly known as system) menu commands: **SC\_NEXTWINDOW**, **SC\_PREVWINDOW**, **SC\_MOVE**, **SC\_SIZE**, and **SC\_MAXIMIZE**.</span></span>                                                                                                        |



 

## <a name="creating-a-child-window"></a><span data-ttu-id="0ec84-202">Criando uma janela filho</span><span class="sxs-lookup"><span data-stu-id="0ec84-202">Creating a Child Window</span></span>

<span data-ttu-id="0ec84-203">Para criar uma janela filho MDI, um aplicativo pode chamar a função [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) ou enviar uma mensagem do [**WM \_ MDICREATE**](wm-mdicreate.md) para a janela do cliente MDI.</span><span class="sxs-lookup"><span data-stu-id="0ec84-203">To create an MDI child window, an application can either call the [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) function or send an [**WM\_MDICREATE**](wm-mdicreate.md) message to the MDI client window.</span></span> <span data-ttu-id="0ec84-204">(O aplicativo pode usar a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) com o estilo **WS \_ ex \_ MDICHILD** para criar janelas filho MDI.) Um aplicativo MDI de thread único pode usar qualquer um dos métodos para criar uma janela filho.</span><span class="sxs-lookup"><span data-stu-id="0ec84-204">(The application can use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function with the **WS\_EX\_MDICHILD** style to create MDI child windows.) A single-threaded MDI application can use either method to create a child window.</span></span> <span data-ttu-id="0ec84-205">Um thread em um aplicativo MDI multithread deve usar a função **CreateMDIWindow** ou **CreateWindowEx** para criar uma janela filho em um thread diferente.</span><span class="sxs-lookup"><span data-stu-id="0ec84-205">A thread in a multithreaded MDI application must use the **CreateMDIWindow** or **CreateWindowEx** function to create a child window in a different thread.</span></span>

<span data-ttu-id="0ec84-206">O parâmetro *lParam* de uma mensagem do [**WM \_ MDICREATE**](wm-mdicreate.md) é um ponteiro distante para uma estrutura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) .</span><span class="sxs-lookup"><span data-stu-id="0ec84-206">The *lParam* parameter of a [**WM\_MDICREATE**](wm-mdicreate.md) message is a far pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="0ec84-207">A estrutura inclui quatro membros de dimensão: **x** e **y**, que indicam as posições horizontal e vertical da janela, e **CX** e **CY**, que indicam as extensões horizontais e verticais da janela.</span><span class="sxs-lookup"><span data-stu-id="0ec84-207">The structure includes four dimension members: **x** and **y**, which indicate the horizontal and vertical positions of the window, and **cx** and **cy**, which indicate the horizontal and vertical extents of the window.</span></span> <span data-ttu-id="0ec84-208">Qualquer um desses membros pode ser atribuído explicitamente pelo aplicativo, ou pode ser definido para USEDEFAULT de **peso \_ variável**; nesse caso, o sistema seleciona uma posição, tamanho ou ambos, de acordo com um algoritmo em cascata.</span><span class="sxs-lookup"><span data-stu-id="0ec84-208">Any of these members may be assigned explicitly by the application, or they may be set to **CW\_USEDEFAULT**, in which case the system selects a position, size, or both, according to a cascading algorithm.</span></span> <span data-ttu-id="0ec84-209">Em qualquer caso, todos os quatro membros devem ser inicializados.</span><span class="sxs-lookup"><span data-stu-id="0ec84-209">In any case, all four members must be initialized.</span></span> <span data-ttu-id="0ec84-210">Multipad usa **\_ USEDEFAULT de PV** para todas as dimensões.</span><span class="sxs-lookup"><span data-stu-id="0ec84-210">Multipad uses **CW\_USEDEFAULT** for all dimensions.</span></span>

<span data-ttu-id="0ec84-211">O último membro da estrutura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) é o membro **Style** , que pode conter bits de estilo para a janela.</span><span class="sxs-lookup"><span data-stu-id="0ec84-211">The last member of the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure is the **style** member, which may contain style bits for the window.</span></span> <span data-ttu-id="0ec84-212">Para criar uma janela filho MDI que pode ter qualquer combinação de estilos de janela, especifique o estilo de janela **MDIS \_ ALLCHILDSTYLES** .</span><span class="sxs-lookup"><span data-stu-id="0ec84-212">To create an MDI child window that can have any combination of window styles, specify the **MDIS\_ALLCHILDSTYLES** window style.</span></span> <span data-ttu-id="0ec84-213">Quando esse estilo não é especificado, uma janela filho MDI tem os **estilos \_ WS minimize**, **WS \_ Maxim**, WS **\_ HSCROLL** e **WS \_ VSCROLL** como configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="0ec84-213">When this style is not specified, an MDI child window has the **WS\_MINIMIZE**, **WS\_MAXIMIZE**, **WS\_HSCROLL**, and **WS\_VSCROLL** styles as default settings.</span></span>

<span data-ttu-id="0ec84-214">O Multipad cria suas janelas filho MDI usando sua função AddFile definida localmente (localizada no arquivo de origem MPFILE. C).</span><span class="sxs-lookup"><span data-stu-id="0ec84-214">Multipad creates its MDI child windows by using its locally defined AddFile function (located in the source file MPFILE.C).</span></span> <span data-ttu-id="0ec84-215">A função AddFile define o título da janela filho atribuindo o membro **szTitle** da estrutura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) da janela ao nome do arquivo que está sendo editado ou "sem título".</span><span class="sxs-lookup"><span data-stu-id="0ec84-215">The AddFile function sets the title of the child window by assigning the **szTitle** member of the window's [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure to either the name of the file being edited or to "Untitled."</span></span> <span data-ttu-id="0ec84-216">O membro **szClass** é definido como o nome da classe de janela filho MDI registrada na função InitializeApplication do Multipad.</span><span class="sxs-lookup"><span data-stu-id="0ec84-216">The **szClass** member is set to the name of the MDI child window class registered in Multipad's InitializeApplication function.</span></span> <span data-ttu-id="0ec84-217">O membro **hOwner** é definido como o identificador de instância do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0ec84-217">The **hOwner** member is set to the application's instance handle.</span></span>

<span data-ttu-id="0ec84-218">O exemplo a seguir mostra a função AddFile em Multipad.</span><span class="sxs-lookup"><span data-stu-id="0ec84-218">The following example shows the AddFile function in Multipad.</span></span>


```
HWND APIENTRY AddFile(pName) 
TCHAR * pName; 
{ 
    HWND hwnd; 
    TCHAR sz[160]; 
    MDICREATESTRUCT mcs; 
 
    if (!pName) 
    { 
 
        // If the pName parameter is NULL, load the "Untitled" 
        // string from the STRINGTABLE resource and set the szTitle 
        // member of MDICREATESTRUCT. 
 
        LoadString(hInst, IDS_UNTITLED, sz, sizeof(sz)/sizeof(TCHAR)); 
        mcs.szTitle = (LPCTSTR) sz; 
    } 
    else 
 
        // Title the window with the full path and filename, 
        // obtained by calling the OpenFile function with the 
        // OF_PARSE flag, which is called before AddFile(). 
 
        mcs.szTitle = of.szPathName; 
 
    mcs.szClass = szChild; 
    mcs.hOwner  = hInst; 
 
    // Use the default size for the child window. 
 
    mcs.x = mcs.cx = CW_USEDEFAULT; 
    mcs.y = mcs.cy = CW_USEDEFAULT; 
 
    // Give the child window the default style. The styleDefault 
    // variable is defined in MULTIPAD.C. 
 
    mcs.style = styleDefault; 
 
    // Tell the MDI client window to create the child window. 
 
    hwnd = (HWND) SendMessage (hwndMDIClient, WM_MDICREATE, 0, 
        (LONG) (LPMDICREATESTRUCT) &mcs); 
 
    // If the file is found, read its contents into the child 
    // window's client area. 
 
    if (pName) 
    { 
        if (!LoadFile(hwnd, pName)) 
        { 
 
            // Cannot load the file; close the window. 
 
            SendMessage(hwndMDIClient, WM_MDIDESTROY, 
                (DWORD) hwnd, 0L); 
        } 
    } 
    return hwnd; 
} 
```



<span data-ttu-id="0ec84-219">O ponteiro passado no parâmetro *lParam* da mensagem [**\_ MDICREATE do WM**](wm-mdicreate.md) é passado para a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) e aparece como o primeiro membro na estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) , passado na mensagem de [**\_ criação do WM**](wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="0ec84-219">The pointer passed in the *lParam* parameter of the [**WM\_MDICREATE**](wm-mdicreate.md) message is passed to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function and appears as the first member in the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure, passed in the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="0ec84-220">No Multipad, a janela filho se inicializa durante o **WM \_ criar** processamento de mensagens Inicializando variáveis de documento em seus dados extras e criando a janela filho do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="0ec84-220">In Multipad, the child window initializes itself during **WM\_CREATE** message processing by initializing document variables in its extra data and by creating the edit control's child window.</span></span>

 

 
