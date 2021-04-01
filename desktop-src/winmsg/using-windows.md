---
description: Os exemplos nesta seção descrevem como executar tarefas associadas ao uso do Windows.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Usando o Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bebe537f82de65efddc086ee457e1abe47a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836874"
---
# <a name="using-windows"></a><span data-ttu-id="92903-103">Usando o Windows</span><span class="sxs-lookup"><span data-stu-id="92903-103">Using Windows</span></span>

<span data-ttu-id="92903-104">Os exemplos nesta seção descrevem como executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="92903-104">The examples in this section describe how to perform the following tasks:</span></span>

-   [<span data-ttu-id="92903-105">Criando uma janela principal</span><span class="sxs-lookup"><span data-stu-id="92903-105">Creating a Main Window</span></span>](#creating-a-main-window)
-   [<span data-ttu-id="92903-106">Criando, enumerando e dimensionando janelas filhas</span><span class="sxs-lookup"><span data-stu-id="92903-106">Creating, Enumerating, and Sizing Child Windows</span></span>](#creating-enumerating-and-sizing-child-windows)
-   [<span data-ttu-id="92903-107">Destruindo uma janela</span><span class="sxs-lookup"><span data-stu-id="92903-107">Destroying a Window</span></span>](#destroying-a-window)
-   [<span data-ttu-id="92903-108">Usando janelas em camadas</span><span class="sxs-lookup"><span data-stu-id="92903-108">Using Layered Windows</span></span>](#using-layered-windows)

## <a name="creating-a-main-window"></a><span data-ttu-id="92903-109">Criando uma janela principal</span><span class="sxs-lookup"><span data-stu-id="92903-109">Creating a Main Window</span></span>

<span data-ttu-id="92903-110">A primeira janela que um aplicativo cria normalmente é a janela principal.</span><span class="sxs-lookup"><span data-stu-id="92903-110">The first window an application creates is typically the main window.</span></span> <span data-ttu-id="92903-111">Você cria a janela principal usando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , especificando a classe da janela, o nome da janela, os estilos de janela, o tamanho, a posição, o identificador de menu, o identificador de instância e os dados de criação.</span><span class="sxs-lookup"><span data-stu-id="92903-111">You create the main window by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function, specifying the window class, window name, window styles, size, position, menu handle, instance handle, and creation data.</span></span> <span data-ttu-id="92903-112">Uma janela principal pertence a uma classe de janela definida pelo aplicativo, portanto, você deve registrar a classe Window e fornecer um procedimento de janela para a classe antes de criar a janela principal.</span><span class="sxs-lookup"><span data-stu-id="92903-112">A main window belongs to an application-defined window class, so you must register the window class and provide a window procedure for the class before creating the main window.</span></span>

<span data-ttu-id="92903-113">A maioria dos aplicativos normalmente usa o estilo [**WS \_ OVERLAPPEDWINDOW**](window-styles.md) para criar a janela principal.</span><span class="sxs-lookup"><span data-stu-id="92903-113">Most applications typically use the [**WS\_OVERLAPPEDWINDOW**](window-styles.md) style to create the main window.</span></span> <span data-ttu-id="92903-114">Esse estilo dá à janela uma barra de título, um menu de janela, uma borda de dimensionamento e os botões minimizar e maximizar.</span><span class="sxs-lookup"><span data-stu-id="92903-114">This style gives the window a title bar, a window menu, a sizing border, and minimize and maximize buttons.</span></span> <span data-ttu-id="92903-115">A função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) retorna um identificador que identifica exclusivamente a janela.</span><span class="sxs-lookup"><span data-stu-id="92903-115">The [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function returns a handle that uniquely identifies the window.</span></span>

<span data-ttu-id="92903-116">O exemplo a seguir cria uma janela principal que pertence a uma classe de janela definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92903-116">The following example creates a main window belonging to an application-defined window class.</span></span> <span data-ttu-id="92903-117">O nome da janela, **janela principal**, aparecerá na barra de título da janela.</span><span class="sxs-lookup"><span data-stu-id="92903-117">The window name, **Main Window**, will appear in the window's title bar.</span></span> <span data-ttu-id="92903-118">Ao combinar os [**estilos \_ WS VSCROLL**](window-styles.md) e **WS \_ HSCROLL** com o estilo **WS \_ OVERLAPPEDWINDOW** , o aplicativo cria uma janela principal com barras de rolagem horizontal e vertical, além dos componentes fornecidos pelo estilo **WS \_ OVERLAPPEDWINDOW** .</span><span class="sxs-lookup"><span data-stu-id="92903-118">By combining the [**WS\_VSCROLL**](window-styles.md) and **WS\_HSCROLL** styles with the **WS\_OVERLAPPEDWINDOW** style, the application creates a main window with horizontal and vertical scroll bars in addition to the components provided by the **WS\_OVERLAPPEDWINDOW** style.</span></span> <span data-ttu-id="92903-119">As quatro ocorrências da constante **\_ USEDEFAULT de PV** definem o tamanho inicial e a posição da janela para os valores padrão definidos pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="92903-119">The four occurrences of the **CW\_USEDEFAULT** constant set the initial size and position of the window to the system-defined default values.</span></span> <span data-ttu-id="92903-120">Ao especificar **NULL** em vez de um identificador de menu, a janela terá o menu definido para a classe de janela.</span><span class="sxs-lookup"><span data-stu-id="92903-120">By specifying **NULL** instead of a menu handle, the window will have the menu defined for the window class.</span></span>


```
HINSTANCE hinst; 
HWND hwndMain; 
 
// Create the main window. 
 
hwndMain = CreateWindowEx( 
    0,                      // no extended styles           
    "MainWClass",           // class name                   
    "Main Window",          // window name                  
    WS_OVERLAPPEDWINDOW |   // overlapped window            
             WS_HSCROLL |   // horizontal scroll bar        
             WS_VSCROLL,    // vertical scroll bar          
    CW_USEDEFAULT,          // default horizontal position  
    CW_USEDEFAULT,          // default vertical position    
    CW_USEDEFAULT,          // default width                
    CW_USEDEFAULT,          // default height               
    (HWND) NULL,            // no parent or owner window    
    (HMENU) NULL,           // class menu used              
    hinst,                  // instance handle              
    NULL);                  // no window creation data      
 
if (!hwndMain) 
    return FALSE; 
 
// Show the window using the flag specified by the program 
// that started the application, and send the application 
// a WM_PAINT message. 
 
ShowWindow(hwndMain, SW_SHOWDEFAULT); 
UpdateWindow(hwndMain); 
```



<span data-ttu-id="92903-121">Observe que o exemplo anterior chama a função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) após criar a janela principal.</span><span class="sxs-lookup"><span data-stu-id="92903-121">Notice that the preceding example calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function after creating the main window.</span></span> <span data-ttu-id="92903-122">Isso é feito porque o sistema não exibe automaticamente a janela principal depois de criá-la.</span><span class="sxs-lookup"><span data-stu-id="92903-122">This is done because the system does not automatically display the main window after creating it.</span></span> <span data-ttu-id="92903-123">Ao passar o sinalizador de configuração **\_ padrão de SW** para **janela**, o aplicativo permite que o programa que iniciou o aplicativo defina o estado de exibição inicial da janela principal.</span><span class="sxs-lookup"><span data-stu-id="92903-123">By passing the **SW\_SHOWDEFAULT** flag to **ShowWindow**, the application allows the program that started the application to set the initial show state of the main window.</span></span> <span data-ttu-id="92903-124">A função [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) envia a janela sua primeira mensagem do [**WM \_ Paint**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="92903-124">The [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) function sends the window its first [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span>

## <a name="creating-enumerating-and-sizing-child-windows"></a><span data-ttu-id="92903-125">Criando, enumerando e dimensionando janelas filhas</span><span class="sxs-lookup"><span data-stu-id="92903-125">Creating, Enumerating, and Sizing Child Windows</span></span>

<span data-ttu-id="92903-126">Você pode dividir a área do cliente de uma janela em diferentes áreas funcionais usando as janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="92903-126">You can divide a window's client area into different functional areas by using child windows.</span></span> <span data-ttu-id="92903-127">A criação de uma janela filho é como criar uma janela principal — você usa a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="92903-127">Creating a child window is like creating a main window—you use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="92903-128">Para criar uma janela de uma classe de janela definida pelo aplicativo, você deve registrar a classe Window e fornecer um procedimento de janela antes de criar a janela filho.</span><span class="sxs-lookup"><span data-stu-id="92903-128">To create a window of an application-defined window class, you must register the window class and provide a window procedure before creating the child window.</span></span> <span data-ttu-id="92903-129">Você deve dar à janela filho o estilo de [**WS \_ filho**](window-styles.md) e especificar uma janela pai para a janela filho ao criá-la.</span><span class="sxs-lookup"><span data-stu-id="92903-129">You must give the child window the [**WS\_CHILD**](window-styles.md) style and specify a parent window for the child window when you create it.</span></span>

<span data-ttu-id="92903-130">O exemplo a seguir divide a área do cliente da janela principal de um aplicativo em três áreas funcionais criando três janelas filhas de tamanho igual.</span><span class="sxs-lookup"><span data-stu-id="92903-130">The following example divides the client area of an application's main window into three functional areas by creating three child windows of equal size.</span></span> <span data-ttu-id="92903-131">Cada janela filho tem a mesma altura que a área do cliente da janela principal, mas cada uma é uma terceira de sua largura.</span><span class="sxs-lookup"><span data-stu-id="92903-131">Each child window is the same height as the main window's client area, but each is one-third its width.</span></span> <span data-ttu-id="92903-132">A janela principal cria as janelas filhas em resposta à mensagem [**de \_ criação do WM**](wm-create.md) , que a janela principal recebe durante seu próprio processo de criação de janela.</span><span class="sxs-lookup"><span data-stu-id="92903-132">The main window creates the child windows in response to the [**WM\_CREATE**](wm-create.md) message, which the main window receives during its own window-creation process.</span></span> <span data-ttu-id="92903-133">Como cada janela filho tem o estilo de [**\_ borda WS**](window-styles.md) , cada uma tem uma borda de linha fina.</span><span class="sxs-lookup"><span data-stu-id="92903-133">Because each child window has the [**WS\_BORDER**](window-styles.md) style, each has a thin line border.</span></span> <span data-ttu-id="92903-134">Além disso, como o estilo do **WS \_ Visible** não é especificado, cada janela filho é inicialmente oculta.</span><span class="sxs-lookup"><span data-stu-id="92903-134">Also, because the **WS\_VISIBLE** style is not specified, each child window is initially hidden.</span></span> <span data-ttu-id="92903-135">Observe também que cada janela filho recebe um identificador de janela filho.</span><span class="sxs-lookup"><span data-stu-id="92903-135">Notice also that each child window is assigned a child-window identifier.</span></span>

<span data-ttu-id="92903-136">A janela principal dimensiona e posiciona as janelas filhas em resposta à mensagem [**de \_ tamanho do WM**](wm-size.md) , que a janela principal recebe quando seu tamanho é alterado.</span><span class="sxs-lookup"><span data-stu-id="92903-136">The main window sizes and positions the child windows in response to the [**WM\_SIZE**](wm-size.md) message, which the main window receives when its size changes.</span></span> <span data-ttu-id="92903-137">Em resposta ao **\_ tamanho do WM**, a janela principal recupera as dimensões de sua área de cliente usando a função [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) e, em seguida, passa as dimensões para a função [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) .</span><span class="sxs-lookup"><span data-stu-id="92903-137">In response to **WM\_SIZE**, the main window retrieves the dimensions of its client area by using the [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) function and then passes the dimensions to the [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) function.</span></span> <span data-ttu-id="92903-138">**EnumChildWindows** passa o identificador para cada janela filho, por sua vez, para a função de retorno de chamada [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92903-138">**EnumChildWindows** passes the handle to each child window, in turn, to the application-defined [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) callback function.</span></span> <span data-ttu-id="92903-139">Essa função dimensiona e posiciona cada janela filho chamando a função [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) ; o tamanho e a posição são baseados nas dimensões da área do cliente da janela principal e no identificador da janela filho.</span><span class="sxs-lookup"><span data-stu-id="92903-139">This function sizes and positions each child window by calling the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function; the size and position are based on the dimensions of the main window's client area and the identifier of the child window.</span></span> <span data-ttu-id="92903-140">Depois disso, **EnumChildProc** chama a função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) para tornar a janela visível.</span><span class="sxs-lookup"><span data-stu-id="92903-140">Afterward, **EnumChildProc** calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function to make the window visible.</span></span>


```
#define ID_FIRSTCHILD  100 
#define ID_SECONDCHILD 101 
#define ID_THIRDCHILD  102 
 
LONG APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rcClient; 
    int i; 
 
    switch(uMsg) 
    { 
        case WM_CREATE: // creating main window  
 
            // Create three invisible child windows. 

            for (i = 0; i < 3; i++) 
            { 
                CreateWindowEx(0, 
                               "ChildWClass", 
                               (LPCTSTR) NULL, 
                               WS_CHILD | WS_BORDER, 
                               0,0,0,0, 
                               hwnd, 
                               (HMENU) (int) (ID_FIRSTCHILD + i), 
                               hinst, 
                               NULL); 
            }
 
            return 0; 
 
        case WM_SIZE:   // main window changed size 
 
            // Get the dimensions of the main window's client 
            // area, and enumerate the child windows. Pass the 
            // dimensions to the child windows during enumeration. 
 
            GetClientRect(hwnd, &rcClient); 
            EnumChildWindows(hwnd, EnumChildProc, (LPARAM) &rcClient); 
            return 0; 

        // Process other messages. 
    } 
    return DefWindowProc(hwnd, uMsg, wParam, lParam); 
} 
 
BOOL CALLBACK EnumChildProc(HWND hwndChild, LPARAM lParam) 
{ 
    LPRECT rcParent; 
    int i, idChild; 
 
    // Retrieve the child-window identifier. Use it to set the 
    // position of the child window. 
 
    idChild = GetWindowLong(hwndChild, GWL_ID); 
 
    if (idChild == ID_FIRSTCHILD) 
        i = 0; 
    else if (idChild == ID_SECONDCHILD) 
        i = 1; 
    else 
        i = 2; 
 
    // Size and position the child window.  
 
    rcParent = (LPRECT) lParam; 
    MoveWindow(hwndChild, 
               (rcParent->right / 3) * i, 
               0, 
               rcParent->right / 3, 
               rcParent->bottom, 
               TRUE); 
 
    // Make sure the child window is visible. 
 
    ShowWindow(hwndChild, SW_SHOW); 
 
    return TRUE;
}
```



## <a name="destroying-a-window"></a><span data-ttu-id="92903-141">Destruindo uma janela</span><span class="sxs-lookup"><span data-stu-id="92903-141">Destroying a Window</span></span>

<span data-ttu-id="92903-142">Você pode usar a função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) para destruir uma janela.</span><span class="sxs-lookup"><span data-stu-id="92903-142">You can use the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function to destroy a window.</span></span> <span data-ttu-id="92903-143">Normalmente, um aplicativo envia a mensagem de [**\_ fechamento do WM**](wm-close.md) antes de destruir uma janela, dando à janela a oportunidade de solicitar a confirmação do usuário antes que a janela seja destruída.</span><span class="sxs-lookup"><span data-stu-id="92903-143">Typically, an application sends the [**WM\_CLOSE**](wm-close.md) message before destroying a window, giving the window the opportunity to prompt the user for confirmation before the window is destroyed.</span></span> <span data-ttu-id="92903-144">Uma janela que inclui um menu de janela recebe automaticamente a mensagem de **\_ fechamento do WM** quando o usuário clica em **Fechar** no menu janela.</span><span class="sxs-lookup"><span data-stu-id="92903-144">A window that includes a window menu automatically receives the **WM\_CLOSE** message when the user clicks **Close** from the window menu.</span></span> <span data-ttu-id="92903-145">Se o usuário confirmar que a janela deve ser destruída, o aplicativo chamará **DestroyWindow**.</span><span class="sxs-lookup"><span data-stu-id="92903-145">If the user confirms that the window should be destroyed, the application calls **DestroyWindow**.</span></span> <span data-ttu-id="92903-146">O sistema envia a mensagem de [**\_ destruição do WM**](wm-destroy.md) para a janela depois de removê-la da tela.</span><span class="sxs-lookup"><span data-stu-id="92903-146">The system sends the [**WM\_DESTROY**](wm-destroy.md) message to the window after removing it from the screen.</span></span> <span data-ttu-id="92903-147">Em resposta ao **WM \_ Destroy**, a janela salva seus dados e libera todos os recursos alocados.</span><span class="sxs-lookup"><span data-stu-id="92903-147">In response to **WM\_DESTROY**, the window saves its data and frees any resources it allocated.</span></span> <span data-ttu-id="92903-148">Uma janela principal conclui seu processamento do **WM \_ Destroy** chamando a função [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) para sair do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92903-148">A main window concludes its processing of **WM\_DESTROY** by calling the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to quit the application.</span></span>

<span data-ttu-id="92903-149">O exemplo a seguir mostra como solicitar a confirmação do usuário antes de destruir uma janela.</span><span class="sxs-lookup"><span data-stu-id="92903-149">The following example shows how to prompt for user confirmation before destroying a window.</span></span> <span data-ttu-id="92903-150">Em resposta à [**\_ fechamento do WM**](wm-close.md), o exemplo exibe uma caixa de diálogo que contém os botões **Sim**, **não** e **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="92903-150">In response to [**WM\_CLOSE**](wm-close.md), the example displays a dialog box that contains **Yes**, **No**, and **Cancel** buttons.</span></span> <span data-ttu-id="92903-151">Se o usuário clicar em **Sim**, [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) será chamado; caso contrário, a janela não será destruída.</span><span class="sxs-lookup"><span data-stu-id="92903-151">If the user clicks **Yes**, [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) is called; otherwise, the window is not destroyed.</span></span> <span data-ttu-id="92903-152">Como a janela que está sendo destruída é uma janela principal, o exemplo chama [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) em resposta ao [**WM \_ Destroy**](wm-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="92903-152">Because the window being destroyed is a main window, the example calls [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) in response to [**WM\_DESTROY**](wm-destroy.md).</span></span>


```
case WM_CLOSE: 
 
    // Create the message box. If the user clicks 
    // the Yes button, destroy the main window. 
 
    if (MessageBox(hwnd, szConfirm, szAppName, MB_YESNOCANCEL) == IDYES) 
        DestroyWindow(hwndMain); 
    else 
        return 0; 
 
case WM_DESTROY: 
 
    // Post the WM_QUIT message to 
    // quit the application terminate. 
 
    PostQuitMessage(0); 
    return 0;
```



## <a name="using-layered-windows"></a><span data-ttu-id="92903-153">Usando janelas em camadas</span><span class="sxs-lookup"><span data-stu-id="92903-153">Using Layered Windows</span></span>

<span data-ttu-id="92903-154">Para que uma caixa de diálogo seja exibida como uma janela translúcida, primeiro crie o diálogo como de costume.</span><span class="sxs-lookup"><span data-stu-id="92903-154">To have a dialog box come up as a translucent window, first create the dialog as usual.</span></span> <span data-ttu-id="92903-155">Em seguida, no [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md), defina o bit em camadas do estilo estendido da janela e chame [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) com o valor alfa desejado.</span><span class="sxs-lookup"><span data-stu-id="92903-155">Then, on [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md), set the layered bit of the window's extended style and call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) with the desired alpha value.</span></span> <span data-ttu-id="92903-156">O código pode ser assim:</span><span class="sxs-lookup"><span data-stu-id="92903-156">The code might look like this:</span></span>


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



<span data-ttu-id="92903-157">Observe que o terceiro parâmetro de [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) é um valor que varia de 0 a 255, com 0 tornando a janela completamente transparente e 255 tornando-a completamente opaca.</span><span class="sxs-lookup"><span data-stu-id="92903-157">Note that the third parameter of [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) is a value that ranges from 0 to 255, with 0 making the window completely transparent and 255 making it completely opaque.</span></span> <span data-ttu-id="92903-158">Esse parâmetro imita a [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) mais versátil da função [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .</span><span class="sxs-lookup"><span data-stu-id="92903-158">This parameter mimics the more versatile [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) of the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>

<span data-ttu-id="92903-159">Para tornar essa janela completamente opaca novamente, remova o bit **WS \_ ex em \_ camadas** chamando [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) e, em seguida, peça que a janela seja redesenhada.</span><span class="sxs-lookup"><span data-stu-id="92903-159">To make this window completely opaque again, remove the **WS\_EX\_LAYERED** bit by calling [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) and then ask the window to repaint.</span></span> <span data-ttu-id="92903-160">Remover o bit é desejado para permitir que o sistema saiba que ele pode liberar memória associada a camadas e redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="92903-160">Removing the bit is desired to let the system know that it can free up some memory associated with layering and redirection.</span></span> <span data-ttu-id="92903-161">O código pode ser assim:</span><span class="sxs-lookup"><span data-stu-id="92903-161">The code might look like this:</span></span>


```
// Remove WS_EX_LAYERED from this window styles
SetWindowLong(hwnd, 
              GWL_EXSTYLE,
              GetWindowLong(hwnd, GWL_EXSTYLE) & ~WS_EX_LAYERED);

// Ask the window and its children to repaint
RedrawWindow(hwnd, 
             NULL, 
             NULL, 
             RDW_ERASE | RDW_INVALIDATE | RDW_FRAME | RDW_ALLCHILDREN);
```



<span data-ttu-id="92903-162">Para usar janelas filho em camadas, o aplicativo precisa declarar o reconhecimento do Windows 8 no manifesto.</span><span class="sxs-lookup"><span data-stu-id="92903-162">In order to use layered child windows, the application has to declare itself Windows 8-aware in the manifest.</span></span>

 

 
