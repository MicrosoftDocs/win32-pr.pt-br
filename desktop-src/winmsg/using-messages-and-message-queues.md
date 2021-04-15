---
description: Os exemplos de código a seguir demonstram como executar as seguintes tarefas associadas a mensagens e filas de mensagens do Windows.
ms.assetid: 62b4616c-37bf-4d9f-8891-7010c7035d18
title: Usando mensagens e filas de mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a33f422a1a7c77f2c2fcd5913f931168a350a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754059"
---
# <a name="using-messages-and-message-queues"></a><span data-ttu-id="bb68b-103">Usando mensagens e filas de mensagens</span><span class="sxs-lookup"><span data-stu-id="bb68b-103">Using Messages and Message Queues</span></span>

<span data-ttu-id="bb68b-104">Os exemplos de código a seguir demonstram como executar as seguintes tarefas associadas a mensagens e filas de mensagens do Windows.</span><span class="sxs-lookup"><span data-stu-id="bb68b-104">The following code examples demonstrate how to perform the following tasks associated with Windows messages and message queues.</span></span>

-   [<span data-ttu-id="bb68b-105">Criando um loop de mensagem</span><span class="sxs-lookup"><span data-stu-id="bb68b-105">Creating a Message Loop</span></span>](#creating-a-message-loop)
-   [<span data-ttu-id="bb68b-106">Examinando uma fila de mensagens</span><span class="sxs-lookup"><span data-stu-id="bb68b-106">Examining a Message Queue</span></span>](#examining-a-message-queue)
-   [<span data-ttu-id="bb68b-107">Postando uma mensagem</span><span class="sxs-lookup"><span data-stu-id="bb68b-107">Posting a Message</span></span>](#posting-a-message)
-   [<span data-ttu-id="bb68b-108">Enviando uma mensagem</span><span class="sxs-lookup"><span data-stu-id="bb68b-108">Sending a Message</span></span>](#sending-a-message)

## <a name="creating-a-message-loop"></a><span data-ttu-id="bb68b-109">Criando um loop de mensagem</span><span class="sxs-lookup"><span data-stu-id="bb68b-109">Creating a Message Loop</span></span>

<span data-ttu-id="bb68b-110">O sistema não cria automaticamente uma fila de mensagens para cada thread.</span><span class="sxs-lookup"><span data-stu-id="bb68b-110">The system does not automatically create a message queue for each thread.</span></span> <span data-ttu-id="bb68b-111">Em vez disso, o sistema cria uma fila de mensagens somente para threads que executam operações que exigem uma fila de mensagens.</span><span class="sxs-lookup"><span data-stu-id="bb68b-111">Instead, the system creates a message queue only for threads that perform operations which require a message queue.</span></span> <span data-ttu-id="bb68b-112">Se o thread criar uma ou mais janelas, um loop de mensagem deverá ser fornecido; Esse loop de mensagem recupera mensagens da fila de mensagens do thread e as expede para os procedimentos de janela apropriados.</span><span class="sxs-lookup"><span data-stu-id="bb68b-112">If the thread creates one or more windows, a message loop must be provided; this message loop retrieves messages from the thread's message queue and dispatches them to the appropriate window procedures.</span></span>

<span data-ttu-id="bb68b-113">Como o sistema direciona mensagens para janelas individuais em um aplicativo, um thread deve criar pelo menos uma janela antes de iniciar seu loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb68b-113">Because the system directs messages to individual windows in an application, a thread must create at least one window before starting its message loop.</span></span> <span data-ttu-id="bb68b-114">A maioria dos aplicativos contém um único thread que cria o Windows.</span><span class="sxs-lookup"><span data-stu-id="bb68b-114">Most applications contain a single thread that creates windows.</span></span> <span data-ttu-id="bb68b-115">Um aplicativo típico registra a classe Window para sua janela principal, cria e mostra a janela principal e, em seguida, inicia seu loop de mensagem — tudo na função [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="bb68b-115">A typical application registers the window class for its main window, creates and shows the main window, and then starts its message loop — all in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span>

<span data-ttu-id="bb68b-116">Você cria um loop de mensagem usando as funções [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .</span><span class="sxs-lookup"><span data-stu-id="bb68b-116">You create a message loop by using the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) functions.</span></span> <span data-ttu-id="bb68b-117">Se seu aplicativo precisar obter a entrada de caractere do usuário, inclua a função [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) no loop.</span><span class="sxs-lookup"><span data-stu-id="bb68b-117">If your application must obtain character input from the user, include the [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) function in the loop.</span></span> <span data-ttu-id="bb68b-118">**TranslateMessage** converte mensagens de chave virtual em mensagens de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bb68b-118">**TranslateMessage** translates virtual-key messages into character messages.</span></span> <span data-ttu-id="bb68b-119">O exemplo a seguir mostra o loop de mensagem na função [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) de um aplicativo simples baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="bb68b-119">The following example shows the message loop in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function of a simple Windows-based application.</span></span>


```
HINSTANCE hinst; 
HWND hwndMain; 
 
int PASCAL WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, 
    LPSTR lpszCmdLine, int nCmdShow) 
{ 
    MSG msg;
    BOOL bRet; 
    WNDCLASS wc; 
    UNREFERENCED_PARAMETER(lpszCmdLine); 
 
    // Register the window class for the main window. 
 
    if (!hPrevInstance) 
    { 
        wc.style = 0; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
        wc.cbClsExtra = 0; 
        wc.cbWndExtra = 0; 
        wc.hInstance = hInstance; 
        wc.hIcon = LoadIcon((HINSTANCE) NULL, 
            IDI_APPLICATION); 
        wc.hCursor = LoadCursor((HINSTANCE) NULL, 
            IDC_ARROW); 
        wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
        wc.lpszMenuName =  "MainMenu"; 
        wc.lpszClassName = "MainWndClass"; 
 
        if (!RegisterClass(&wc)) 
            return FALSE; 
    } 
 
    hinst = hInstance;  // save instance handle 
 
    // Create the main window. 
 
    hwndMain = CreateWindow("MainWndClass", "Sample", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, (HWND) NULL, 
        (HMENU) NULL, hinst, (LPVOID) NULL); 
 
    // If the main window cannot be created, terminate 
    // the application. 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Show the window and paint its contents. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Start the message loop. 
 
    while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
    { 
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
 
    // Return the exit code to the system. 
 
    return msg.wParam; 
} 
```



<span data-ttu-id="bb68b-120">O exemplo a seguir mostra um loop de mensagem para um thread que usa Aceleradores e exibe uma caixa de diálogo sem janela restrita.</span><span class="sxs-lookup"><span data-stu-id="bb68b-120">The following example shows a message loop for a thread that uses accelerators and displays a modeless dialog box.</span></span> <span data-ttu-id="bb68b-121">Quando [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) ou [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) retorna **true** (indicando que a mensagem foi processada), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) e [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) não são chamados.</span><span class="sxs-lookup"><span data-stu-id="bb68b-121">When [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) or [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) returns **TRUE** (indicating that the message has been processed), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) are not called.</span></span> <span data-ttu-id="bb68b-122">O motivo disso é que **TranslateAccelerator** e **IsDialogMessage** executam todas as traduções necessárias e a expedição de mensagens.</span><span class="sxs-lookup"><span data-stu-id="bb68b-122">The reason for this is that **TranslateAccelerator** and **IsDialogMessage** perform all necessary translating and dispatching of messages.</span></span>


```
HWND hwndMain; 
HWND hwndDlgModeless = NULL; 
MSG msg;
BOOL bRet; 
HACCEL haccel; 
// 
// Perform initialization and create a main window. 
// 
 
while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
{ 
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else
    {
        if (hwndDlgModeless == (HWND) NULL || 
                !IsDialogMessage(hwndDlgModeless, &msg) && 
                !TranslateAccelerator(hwndMain, haccel, 
                    &msg)) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
} 
```



## <a name="examining-a-message-queue"></a><span data-ttu-id="bb68b-123">Examinando uma fila de mensagens</span><span class="sxs-lookup"><span data-stu-id="bb68b-123">Examining a Message Queue</span></span>

<span data-ttu-id="bb68b-124">Ocasionalmente, um aplicativo precisa examinar o conteúdo da fila de mensagens de um thread de fora do loop de mensagem do thread.</span><span class="sxs-lookup"><span data-stu-id="bb68b-124">Occasionally, an application needs to examine the contents of a thread's message queue from outside the thread's message loop.</span></span> <span data-ttu-id="bb68b-125">Por exemplo, se o procedimento de janela de um aplicativo executar uma operação demorada de desenho, talvez você queira que o usuário possa interromper a operação.</span><span class="sxs-lookup"><span data-stu-id="bb68b-125">For example, if an application's window procedure performs a lengthy drawing operation, you may want the user to be able to interrupt the operation.</span></span> <span data-ttu-id="bb68b-126">A menos que seu aplicativo examine periodicamente a fila de mensagens durante a operação para mensagens do mouse e do teclado, ele não responderá à entrada do usuário até que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="bb68b-126">Unless your application periodically examines the message queue during the operation for mouse and keyboard messages, it will not respond to user input until after the operation has completed.</span></span> <span data-ttu-id="bb68b-127">O motivo disso é que a função [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) no loop de mensagem do thread não retorna até que o procedimento de janela termine de processar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb68b-127">The reason for this is that the [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) function in the thread's message loop does not return until the window procedure finishes processing a message.</span></span>

<span data-ttu-id="bb68b-128">Você pode usar a função [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) para examinar uma fila de mensagens durante uma operação demorada.</span><span class="sxs-lookup"><span data-stu-id="bb68b-128">You can use the [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function to examine a message queue during a lengthy operation.</span></span> <span data-ttu-id="bb68b-129">**PeekMessage** é semelhante à função [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ; ambos verificam uma fila de mensagens em busca de uma mensagem que corresponda aos critérios de filtro e, em seguida, copia a mensagem em uma estrutura de [**msg**](/windows/win32/api/winuser/ns-winuser-msg) .</span><span class="sxs-lookup"><span data-stu-id="bb68b-129">**PeekMessage** is similar to the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function; both check a message queue for a message that matches the filter criteria and then copy the message to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure.</span></span> <span data-ttu-id="bb68b-130">A principal diferença entre as duas funções é que **GetMessage** não retorna até que uma mensagem que corresponda aos critérios de filtro seja colocada na fila, enquanto **PeekMessage** retorna imediatamente, independentemente de uma mensagem estar na fila.</span><span class="sxs-lookup"><span data-stu-id="bb68b-130">The main difference between the two functions is that **GetMessage** does not return until a message matching the filter criteria is placed in the queue, whereas **PeekMessage** returns immediately regardless of whether a message is in the queue.</span></span>

<span data-ttu-id="bb68b-131">O exemplo a seguir mostra como usar o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) para examinar uma fila de mensagens para cliques do mouse e entrada de teclado durante uma operação demorada.</span><span class="sxs-lookup"><span data-stu-id="bb68b-131">The following example shows how to use [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) to examine a message queue for mouse clicks and keyboard input during a lengthy operation.</span></span>


```
HWND hwnd; 
BOOL fDone; 
MSG msg; 
 
// Begin the operation and continue until it is complete 
// or until the user clicks the mouse or presses a key. 
 
fDone = FALSE; 
while (!fDone) 
{ 
    fDone = DoLengthyOperation(); // application-defined function 
 
    // Remove any messages that may be in the queue. If the 
    // queue contains any mouse or keyboard 
    // messages, end the operation. 
 
    while (PeekMessage(&msg, hwnd,  0, 0, PM_REMOVE)) 
    { 
        switch(msg.message) 
        { 
            case WM_LBUTTONDOWN: 
            case WM_RBUTTONDOWN: 
            case WM_KEYDOWN: 
                // 
                // Perform any required cleanup. 
                // 
                fDone = TRUE; 
        } 
    } 
} 
```



<span data-ttu-id="bb68b-132">Outras funções, incluindo [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) e [**getinputstate**](/windows/win32/api/winuser/nf-winuser-getinputstate), também permitem que você examine o conteúdo da fila de mensagens de um thread.</span><span class="sxs-lookup"><span data-stu-id="bb68b-132">Other functions, including [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) and [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate), also allow you to examine the contents of a thread's message queue.</span></span> <span data-ttu-id="bb68b-133">**GetQueueStatus** retorna uma matriz de sinalizadores que indica os tipos de mensagens na fila; usar essa é a maneira mais rápida de descobrir se a fila contém todas as mensagens.</span><span class="sxs-lookup"><span data-stu-id="bb68b-133">**GetQueueStatus** returns an array of flags that indicates the types of messages in the queue; using it is the fastest way to discover whether the queue contains any messages.</span></span> <span data-ttu-id="bb68b-134">**Getinputstate** retornará **true** se a fila contiver mensagens de mouse ou de teclado.</span><span class="sxs-lookup"><span data-stu-id="bb68b-134">**GetInputState** returns **TRUE** if the queue contains mouse or keyboard messages.</span></span> <span data-ttu-id="bb68b-135">Ambas as funções podem ser usadas para determinar se a fila contém mensagens que precisam ser processadas.</span><span class="sxs-lookup"><span data-stu-id="bb68b-135">Both of these functions can be used to determine whether the queue contains messages that need to be processed.</span></span>

## <a name="posting-a-message"></a><span data-ttu-id="bb68b-136">Postando uma mensagem</span><span class="sxs-lookup"><span data-stu-id="bb68b-136">Posting a Message</span></span>

<span data-ttu-id="bb68b-137">Você pode postar uma mensagem em uma fila de mensagens usando a função [**CreateMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) .</span><span class="sxs-lookup"><span data-stu-id="bb68b-137">You can post a message to a message queue by using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function.</span></span> <span data-ttu-id="bb68b-138">A **mensagem** de espera coloca uma mensagem no final da fila de mensagens de um thread e retorna imediatamente, sem esperar que o thread processe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb68b-138">**PostMessage** places a message at the end of a thread's message queue and returns immediately, without waiting for the thread to process the message.</span></span> <span data-ttu-id="bb68b-139">Os parâmetros da função incluem um identificador de janela, um identificador de mensagem e dois parâmetros de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb68b-139">The function's parameters include a window handle, a message identifier, and two message parameters.</span></span> <span data-ttu-id="bb68b-140">O sistema copia esses parâmetros para uma estrutura de [**msg**](/windows/win32/api/winuser/ns-winuser-msg) , preenche os membros de **hora** e **pt** da estrutura e coloca a estrutura na fila de mensagens.</span><span class="sxs-lookup"><span data-stu-id="bb68b-140">The system copies these parameters to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure, fills the **time** and **pt** members of the structure, and places the structure in the message queue.</span></span>

<span data-ttu-id="bb68b-141">O sistema usa o identificador de janela passado com a função [**CreateMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) para determinar qual fila de mensagens de thread deve receber a mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb68b-141">The system uses the window handle passed with the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to determine which thread message queue should receive the message.</span></span> <span data-ttu-id="bb68b-142">Se o identificador for o HWND de mais **\_ alto**, o sistema posta a mensagem nas filas de mensagens de thread de todas as janelas de nível superior.</span><span class="sxs-lookup"><span data-stu-id="bb68b-142">If the handle is **HWND\_TOPMOST**, the system posts the message to the thread message queues of all top-level windows.</span></span>

<span data-ttu-id="bb68b-143">Você pode usar a função [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) para postar uma mensagem em uma fila de mensagens de thread específica.</span><span class="sxs-lookup"><span data-stu-id="bb68b-143">You can use the [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) function to post a message to a specific thread message queue.</span></span> <span data-ttu-id="bb68b-144">**PostThreadMessage** é semelhante a [**CreateMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), exceto que o primeiro parâmetro é um identificador de thread em vez de um identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="bb68b-144">**PostThreadMessage** is similar to [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), except the first parameter is a thread identifier rather than a window handle.</span></span> <span data-ttu-id="bb68b-145">Você pode recuperar o identificador de thread chamando a função [**GetCurrentThreadID**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) .</span><span class="sxs-lookup"><span data-stu-id="bb68b-145">You can retrieve the thread identifier by calling the [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) function.</span></span>

<span data-ttu-id="bb68b-146">Use a função [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) para sair de um loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb68b-146">Use the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to exit a message loop.</span></span> <span data-ttu-id="bb68b-147">**PostQuitMessage** posta a mensagem do [**WM \_ Quit**](wm-quit.md) para o thread em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="bb68b-147">**PostQuitMessage** posts the [**WM\_QUIT**](wm-quit.md) message to the currently executing thread.</span></span> <span data-ttu-id="bb68b-148">O loop de mensagem do thread é encerrado e retorna o controle ao sistema quando ele encontra a mensagem de **\_ quitação do WM** .</span><span class="sxs-lookup"><span data-stu-id="bb68b-148">The thread's message loop terminates and returns control to the system when it encounters the **WM\_QUIT** message.</span></span> <span data-ttu-id="bb68b-149">Um aplicativo normalmente chama **PostQuitMessage** em resposta à mensagem [**de \_ destruição do WM**](wm-destroy.md) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="bb68b-149">An application usually calls **PostQuitMessage** in response to the [**WM\_DESTROY**](wm-destroy.md) message, as shown in the following example.</span></span>


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a><span data-ttu-id="bb68b-150">Enviando uma mensagem</span><span class="sxs-lookup"><span data-stu-id="bb68b-150">Sending a Message</span></span>

<span data-ttu-id="bb68b-151">A função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) é usada para enviar uma mensagem diretamente a um procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="bb68b-151">The [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function is used to send a message directly to a window procedure.</span></span> <span data-ttu-id="bb68b-152">**SendMessage** chama um procedimento de janela e aguarda esse procedimento para processar a mensagem e retornar um resultado.</span><span class="sxs-lookup"><span data-stu-id="bb68b-152">**SendMessage** calls a window procedure and waits for that procedure to process the message and return a result.</span></span>

<span data-ttu-id="bb68b-153">Uma mensagem pode ser enviada para qualquer janela no sistema; Tudo o que é necessário é um identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="bb68b-153">A message can be sent to any window in the system; all that is required is a window handle.</span></span> <span data-ttu-id="bb68b-154">O sistema usa o identificador para determinar qual procedimento de janela deve receber a mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb68b-154">The system uses the handle to determine which window procedure should receive the message.</span></span>

<span data-ttu-id="bb68b-155">Antes de processar uma mensagem que pode ter sido enviada de outro thread, um procedimento de janela deve primeiro chamar a função [**insendmessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) .</span><span class="sxs-lookup"><span data-stu-id="bb68b-155">Before processing a message that may have been sent from another thread, a window procedure should first call the [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) function.</span></span> <span data-ttu-id="bb68b-156">Se essa função retornar **true**, o procedimento de janela deverá chamar [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) antes de qualquer função que faça com que o thread gere controle, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="bb68b-156">If this function returns **TRUE**, the window procedure should call [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) before any function that causes the thread to yield control, as shown in the following example.</span></span>


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



<span data-ttu-id="bb68b-157">Várias mensagens podem ser enviadas a controles em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bb68b-157">A number of messages can be sent to controls in a dialog box.</span></span> <span data-ttu-id="bb68b-158">Essas mensagens de controle definem a aparência, o comportamento e o conteúdo de controles ou recuperam informações sobre controles.</span><span class="sxs-lookup"><span data-stu-id="bb68b-158">These control messages set the appearance, behavior, and content of controls or retrieve information about controls.</span></span> <span data-ttu-id="bb68b-159">Por exemplo, a [**mensagem \_ createstring CB**](../controls/cb-addstring.md) pode adicionar uma cadeia de caracteres a uma caixa de combinação e a mensagem [**\_ SetCheck BM**](../controls/bm-setcheck.md) pode definir o estado de verificação de uma caixa de seleção ou um botão de opção.</span><span class="sxs-lookup"><span data-stu-id="bb68b-159">For example, the [**CB\_ADDSTRING**](../controls/cb-addstring.md) message can add a string to a combo box, and the [**BM\_SETCHECK**](../controls/bm-setcheck.md) message can set the check state of a check box or radio button.</span></span>

<span data-ttu-id="bb68b-160">Use a função [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) para enviar uma mensagem a um controle, especificando o identificador do controle e o identificador da janela da caixa de diálogo que contém o controle.</span><span class="sxs-lookup"><span data-stu-id="bb68b-160">Use the [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) function to send a message to a control, specifying the identifier of the control and the handle of the dialog box window that contains the control.</span></span> <span data-ttu-id="bb68b-161">O exemplo a seguir, extraído de um procedimento de caixa de diálogo, copia uma cadeia de caracteres do controle de edição de uma caixa de combinação para sua caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="bb68b-161">The following example, taken from a dialog box procedure, copies a string from a combo box's edit control into its list box.</span></span> <span data-ttu-id="bb68b-162">O exemplo usa **SendDlgItemMessage** para enviar uma [**mensagem \_ createstring CB**](../controls/cb-addstring.md) para a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="bb68b-162">The example uses **SendDlgItemMessage** to send a [**CB\_ADDSTRING**](../controls/cb-addstring.md) message to the combo box.</span></span>


```
HWND hwndCombo; 
int cTxtLen; 
PSTR pszMem; 
 
switch (uMsg) 
{ 
    case WM_COMMAND: 
        switch (LOWORD(wParam)) 
        { 
            case IDD_ADDCBITEM: 
                // Get the handle of the combo box and the 
                // length of the string in the edit control 
                // of the combo box. 
 
                hwndCombo = GetDlgItem(hwndDlg, IDD_COMBO); 
                cTxtLen = GetWindowTextLength(hwndCombo); 
 
                // Allocate memory for the string and copy 
                // the string into the memory. 
 
                pszMem = (PSTR) VirtualAlloc((LPVOID) NULL, 
                    (DWORD) (cTxtLen + 1), MEM_COMMIT, 
                    PAGE_READWRITE); 
                GetWindowText(hwndCombo, pszMem, 
                    cTxtLen + 1); 
 
                // Add the string to the list box of the 
                // combo box and remove the string from the 
                // edit control of the combo box. 
 
                if (pszMem != NULL) 
                { 
                    SendDlgItemMessage(hwndDlg, IDD_COMBO, 
                        CB_ADDSTRING, 0, 
                        (DWORD) ((LPSTR) pszMem)); 
                    SetWindowText(hwndCombo, (LPSTR) NULL); 
                } 
 
                // Free the memory and return. 
 
                VirtualFree(pszMem, 0, MEM_RELEASE); 
                return TRUE; 
            // 
            // Process other dialog box commands. 
            // 
 
        } 
    // 
    // Process other dialog box messages. 
    // 
 
}
```



 

 
