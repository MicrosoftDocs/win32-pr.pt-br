---
description: Esta seção explica como executar as seguintes tarefas associadas a procedimentos de janela.
ms.assetid: acc68991-4689-44dc-8547-a7b6153b0f62
title: Usando os procedimentos de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e0508119a2ba62c813c32e8fd0c00bd3dd1e85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836875"
---
# <a name="using-window-procedures"></a><span data-ttu-id="45737-103">Usando os procedimentos de janela</span><span class="sxs-lookup"><span data-stu-id="45737-103">Using Window Procedures</span></span>

<span data-ttu-id="45737-104">Esta seção explica como executar as seguintes tarefas associadas a procedimentos de janela.</span><span class="sxs-lookup"><span data-stu-id="45737-104">This section explains how to perform the following tasks associated with window procedures.</span></span>

-   [<span data-ttu-id="45737-105">Criando um procedimento de janela</span><span class="sxs-lookup"><span data-stu-id="45737-105">Designing a Window Procedure</span></span>](#designing-a-window-procedure)
-   [<span data-ttu-id="45737-106">Associando um procedimento de janela a uma classe de janela</span><span class="sxs-lookup"><span data-stu-id="45737-106">Associating a Window Procedure with a Window Class</span></span>](#associating-a-window-procedure-with-a-window-class)
-   [<span data-ttu-id="45737-107">Subclasse de uma janela</span><span class="sxs-lookup"><span data-stu-id="45737-107">Subclassing a Window</span></span>](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a><span data-ttu-id="45737-108">Criando um procedimento de janela</span><span class="sxs-lookup"><span data-stu-id="45737-108">Designing a Window Procedure</span></span>

<span data-ttu-id="45737-109">O exemplo a seguir mostra a estrutura de um procedimento de janela típico.</span><span class="sxs-lookup"><span data-stu-id="45737-109">The following example shows the structure of a typical window procedure.</span></span> <span data-ttu-id="45737-110">O procedimento de janela usa o argumento Message em uma instrução **switch** com mensagens individuais manipuladas por instruções **Case** separadas.</span><span class="sxs-lookup"><span data-stu-id="45737-110">The window procedure uses the message argument in a **switch** statement with individual messages handled by separate **case** statements.</span></span> <span data-ttu-id="45737-111">Observe que cada caso retorna um valor específico para cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="45737-111">Notice that each case returns a specific value for each message.</span></span> <span data-ttu-id="45737-112">Para mensagens que não são processadas, o procedimento de janela chama a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="45737-112">For messages that it does not process, the window procedure calls the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```
LRESULT CALLBACK MainWndProc(
    HWND hwnd,        // handle to window
    UINT uMsg,        // message identifier
    WPARAM wParam,    // first message parameter
    LPARAM lParam)    // second message parameter
{ 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            // Initialize the window. 
            return 0; 
 
        case WM_PAINT: 
            // Paint the window's client area. 
            return 0; 
 
        case WM_SIZE: 
            // Set the size and position of the window. 
            return 0; 
 
        case WM_DESTROY: 
            // Clean up window-specific data objects. 
            return 0; 
 
        // 
        // Process other messages. 
        // 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
```



<span data-ttu-id="45737-113">A mensagem do [**WM \_ NCCREATE**](wm-nccreate.md) é enviada logo após a sua janela ser criada, mas se um aplicativo responder a essa mensagem retornando **false**, a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) falhará.</span><span class="sxs-lookup"><span data-stu-id="45737-113">The [**WM\_NCCREATE**](wm-nccreate.md) message is sent just after your window is created, but if an application responds to this message by returning **FALSE**, [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function fails.</span></span> <span data-ttu-id="45737-114">A mensagem de [**\_ criação do WM**](wm-create.md) é enviada depois que a janela já está criada.</span><span class="sxs-lookup"><span data-stu-id="45737-114">The [**WM\_CREATE**](wm-create.md) message is sent after your window is already created.</span></span>

<span data-ttu-id="45737-115">A mensagem de [**\_ destruição do WM**](wm-destroy.md) é enviada quando a janela está prestes a ser destruída.</span><span class="sxs-lookup"><span data-stu-id="45737-115">The [**WM\_DESTROY**](wm-destroy.md) message is sent when your window is about to be destroyed.</span></span> <span data-ttu-id="45737-116">A função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) cuida da destruição de todas as janelas filhas da janela que está sendo destruída.</span><span class="sxs-lookup"><span data-stu-id="45737-116">The [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function takes care of destroying any child windows of the window being destroyed.</span></span> <span data-ttu-id="45737-117">A mensagem do [**WM \_ NCDESTROY**](wm-ncdestroy.md) é enviada logo antes de uma janela ser destruída.</span><span class="sxs-lookup"><span data-stu-id="45737-117">The [**WM\_NCDESTROY**](wm-ncdestroy.md) message is sent just before a window is destroyed.</span></span>

<span data-ttu-id="45737-118">Na pior das hipóteses, um procedimento de janela deve processar a mensagem do [**WM \_ Paint**](../gdi/wm-paint.md) para se desenhar.</span><span class="sxs-lookup"><span data-stu-id="45737-118">At the very least, a window procedure should process the [**WM\_PAINT**](../gdi/wm-paint.md) message to draw itself.</span></span> <span data-ttu-id="45737-119">Normalmente, ele também deve lidar com mensagens de mouse e teclado.</span><span class="sxs-lookup"><span data-stu-id="45737-119">Typically, it should handle mouse and keyboard messages as well.</span></span> <span data-ttu-id="45737-120">Consulte as descrições de mensagens individuais para determinar se o procedimento de janela deve tratá-las.</span><span class="sxs-lookup"><span data-stu-id="45737-120">Consult the descriptions of individual messages to determine whether your window procedure should handle them.</span></span>

<span data-ttu-id="45737-121">Seu aplicativo pode chamar a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como parte do processamento de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="45737-121">Your application can call the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as part of the processing of a message.</span></span> <span data-ttu-id="45737-122">Nesse caso, o aplicativo pode modificar os parâmetros da mensagem antes de passar a mensagem para **DefWindowProc** ou pode continuar com o processamento padrão depois de executar suas próprias operações.</span><span class="sxs-lookup"><span data-stu-id="45737-122">In such a case, the application can modify the message parameters before passing the message to **DefWindowProc**, or it can continue with the default processing after performing its own operations.</span></span>

<span data-ttu-id="45737-123">Um procedimento de caixa de diálogo recebe uma mensagem do [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) em vez de uma mensagem de [**\_ criação do WM**](wm-create.md) e não passa mensagens não processadas para a função [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) .</span><span class="sxs-lookup"><span data-stu-id="45737-123">A dialog box procedure receives a [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message instead of a [**WM\_CREATE**](wm-create.md) message and does not pass unprocessed messages to the [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) function.</span></span> <span data-ttu-id="45737-124">Caso contrário, um procedimento de caixa de diálogo é exatamente o mesmo que um procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="45737-124">Otherwise, a dialog box procedure is exactly the same as a window procedure.</span></span>

## <a name="associating-a-window-procedure-with-a-window-class"></a><span data-ttu-id="45737-125">Associando um procedimento de janela a uma classe de janela</span><span class="sxs-lookup"><span data-stu-id="45737-125">Associating a Window Procedure with a Window Class</span></span>

<span data-ttu-id="45737-126">Você associa um procedimento de janela a uma classe de janela ao registrar a classe.</span><span class="sxs-lookup"><span data-stu-id="45737-126">You associate a window procedure with a window class when registering the class.</span></span> <span data-ttu-id="45737-127">Você deve preencher uma estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) com informações sobre a classe e o membro **lpfnWndProc** deve especificar o endereço do procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="45737-127">You must fill a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure with information about the class, and the **lpfnWndProc** member must specify the address of the window procedure.</span></span> <span data-ttu-id="45737-128">Para registrar a classe, passe o endereço da estrutura **WNDCLASS** para a função [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) .</span><span class="sxs-lookup"><span data-stu-id="45737-128">To register the class, pass the address of **WNDCLASS** structure to the [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="45737-129">Depois que a classe Window tiver sido registrada, o procedimento de janela será automaticamente associado a cada nova janela criada com essa classe.</span><span class="sxs-lookup"><span data-stu-id="45737-129">After the window class has been registered, the window procedure is automatically associated with each new window created with that class.</span></span>

<span data-ttu-id="45737-130">O exemplo a seguir mostra como associar o procedimento de janela no exemplo anterior a uma classe de janela.</span><span class="sxs-lookup"><span data-stu-id="45737-130">The following example shows how to associate the window procedure in the previous example with a window class.</span></span>


```
int APIENTRY WinMain( 
    HINSTANCE hinstance,  // handle to current instance 
    HINSTANCE hinstPrev,  // handle to previous instance 
    LPSTR lpCmdLine,      // address of command-line string 
    int nCmdShow)         // show-window type 
{ 
    WNDCLASS wc; 
 
    // Register the main window class. 
    wc.style = CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  "MainMenu"; 
    wc.lpszClassName = "MainWindowClass"; 
 
    if (!RegisterClass(&wc)) 
       return FALSE; 
 
    // 
    // Process other messages. 
    // 
 
} 
```



## <a name="subclassing-a-window"></a><span data-ttu-id="45737-131">Subclasse de uma janela</span><span class="sxs-lookup"><span data-stu-id="45737-131">Subclassing a Window</span></span>

<span data-ttu-id="45737-132">Para subclasse de uma instância de uma janela, chame a função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) e especifique o identificador para a janela para subclasse o \_ sinalizador GWL WndProc e um ponteiro para o procedimento de subclasse.</span><span class="sxs-lookup"><span data-stu-id="45737-132">To subclass an instance of a window, call the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function and specify the handle to the window to subclass the GWL\_WNDPROC flag and a pointer to the subclass procedure.</span></span> <span data-ttu-id="45737-133">**SetWindowLong** retorna um ponteiro para o procedimento de janela original; Use esse ponteiro para passar mensagens para o procedimento original.</span><span class="sxs-lookup"><span data-stu-id="45737-133">**SetWindowLong** returns a pointer to the original window procedure; use this pointer to pass messages to the original procedure.</span></span> <span data-ttu-id="45737-134">O procedimento de janela de subclasse deve usar a função [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) para chamar o procedimento de janela original.</span><span class="sxs-lookup"><span data-stu-id="45737-134">The subclass window procedure must use the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function to call the original window procedure.</span></span>

> [!Note]  
> <span data-ttu-id="45737-135">Para escrever um código compatível com as versões de 32 bits e 64 bits do Windows, use a função [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) .</span><span class="sxs-lookup"><span data-stu-id="45737-135">To write code that is compatible with both 32-bit and 64-bit versions of Windows, use the [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) function.</span></span>

 

<span data-ttu-id="45737-136">O exemplo a seguir mostra como subclasse de uma instância de um controle de edição em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="45737-136">The following example shows how to subclass an instance of an edit control in a dialog box.</span></span> <span data-ttu-id="45737-137">O procedimento de janela de subclasse permite que o controle de edição receba todas as entradas de teclado, incluindo as teclas ENTER e TAB, sempre que o controle tiver o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="45737-137">The subclass window procedure enables the edit control to receive all keyboard input, including the ENTER and TAB keys, whenever the control has the input focus.</span></span>


```
WNDPROC wpOrigEditProc; 
 
LRESULT APIENTRY EditBoxProc(
    HWND hwndDlg, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    HWND hwndEdit; 
 
    switch(uMsg) 
    { 
        case WM_INITDIALOG: 
            // Retrieve the handle to the edit control. 
            hwndEdit = GetDlgItem(hwndDlg, ID_EDIT); 
 
            // Subclass the edit control. 
            wpOrigEditProc = (WNDPROC) SetWindowLong(hwndEdit, 
                GWL_WNDPROC, (LONG) EditSubclassProc); 
            // 
            // Continue the initialization procedure. 
            // 
            return TRUE; 
 
        case WM_DESTROY: 
            // Remove the subclass from the edit control. 
            SetWindowLong(hwndEdit, GWL_WNDPROC, 
                (LONG) wpOrigEditProc); 
            // 
            // Continue the cleanup procedure. 
            // 
            break; 
    } 
    return FALSE; 
        UNREFERENCED_PARAMETER(lParam); 
} 
 
// Subclass procedure 
LRESULT APIENTRY EditSubclassProc(
    HWND hwnd, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    if (uMsg == WM_GETDLGCODE) 
        return DLGC_WANTALLKEYS; 
 
    return CallWindowProc(wpOrigEditProc, hwnd, uMsg, 
        wParam, lParam); 
} 
```



 

 
