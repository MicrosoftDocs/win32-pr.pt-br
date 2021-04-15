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
# <a name="using-messages-and-message-queues"></a>Usando mensagens e filas de mensagens

Os exemplos de código a seguir demonstram como executar as seguintes tarefas associadas a mensagens e filas de mensagens do Windows.

-   [Criando um loop de mensagem](#creating-a-message-loop)
-   [Examinando uma fila de mensagens](#examining-a-message-queue)
-   [Postando uma mensagem](#posting-a-message)
-   [Enviando uma mensagem](#sending-a-message)

## <a name="creating-a-message-loop"></a>Criando um loop de mensagem

O sistema não cria automaticamente uma fila de mensagens para cada thread. Em vez disso, o sistema cria uma fila de mensagens somente para threads que executam operações que exigem uma fila de mensagens. Se o thread criar uma ou mais janelas, um loop de mensagem deverá ser fornecido; Esse loop de mensagem recupera mensagens da fila de mensagens do thread e as expede para os procedimentos de janela apropriados.

Como o sistema direciona mensagens para janelas individuais em um aplicativo, um thread deve criar pelo menos uma janela antes de iniciar seu loop de mensagem. A maioria dos aplicativos contém um único thread que cria o Windows. Um aplicativo típico registra a classe Window para sua janela principal, cria e mostra a janela principal e, em seguida, inicia seu loop de mensagem — tudo na função [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .

Você cria um loop de mensagem usando as funções [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) . Se seu aplicativo precisar obter a entrada de caractere do usuário, inclua a função [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) no loop. **TranslateMessage** converte mensagens de chave virtual em mensagens de caracteres. O exemplo a seguir mostra o loop de mensagem na função [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) de um aplicativo simples baseado no Windows.


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



O exemplo a seguir mostra um loop de mensagem para um thread que usa Aceleradores e exibe uma caixa de diálogo sem janela restrita. Quando [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) ou [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) retorna **true** (indicando que a mensagem foi processada), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) e [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) não são chamados. O motivo disso é que **TranslateAccelerator** e **IsDialogMessage** executam todas as traduções necessárias e a expedição de mensagens.


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



## <a name="examining-a-message-queue"></a>Examinando uma fila de mensagens

Ocasionalmente, um aplicativo precisa examinar o conteúdo da fila de mensagens de um thread de fora do loop de mensagem do thread. Por exemplo, se o procedimento de janela de um aplicativo executar uma operação demorada de desenho, talvez você queira que o usuário possa interromper a operação. A menos que seu aplicativo examine periodicamente a fila de mensagens durante a operação para mensagens do mouse e do teclado, ele não responderá à entrada do usuário até que a operação seja concluída. O motivo disso é que a função [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) no loop de mensagem do thread não retorna até que o procedimento de janela termine de processar uma mensagem.

Você pode usar a função [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) para examinar uma fila de mensagens durante uma operação demorada. **PeekMessage** é semelhante à função [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ; ambos verificam uma fila de mensagens em busca de uma mensagem que corresponda aos critérios de filtro e, em seguida, copia a mensagem em uma estrutura de [**msg**](/windows/win32/api/winuser/ns-winuser-msg) . A principal diferença entre as duas funções é que **GetMessage** não retorna até que uma mensagem que corresponda aos critérios de filtro seja colocada na fila, enquanto **PeekMessage** retorna imediatamente, independentemente de uma mensagem estar na fila.

O exemplo a seguir mostra como usar o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) para examinar uma fila de mensagens para cliques do mouse e entrada de teclado durante uma operação demorada.


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



Outras funções, incluindo [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) e [**getinputstate**](/windows/win32/api/winuser/nf-winuser-getinputstate), também permitem que você examine o conteúdo da fila de mensagens de um thread. **GetQueueStatus** retorna uma matriz de sinalizadores que indica os tipos de mensagens na fila; usar essa é a maneira mais rápida de descobrir se a fila contém todas as mensagens. **Getinputstate** retornará **true** se a fila contiver mensagens de mouse ou de teclado. Ambas as funções podem ser usadas para determinar se a fila contém mensagens que precisam ser processadas.

## <a name="posting-a-message"></a>Postando uma mensagem

Você pode postar uma mensagem em uma fila de mensagens usando a função [**CreateMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) . A **mensagem** de espera coloca uma mensagem no final da fila de mensagens de um thread e retorna imediatamente, sem esperar que o thread processe a mensagem. Os parâmetros da função incluem um identificador de janela, um identificador de mensagem e dois parâmetros de mensagem. O sistema copia esses parâmetros para uma estrutura de [**msg**](/windows/win32/api/winuser/ns-winuser-msg) , preenche os membros de **hora** e **pt** da estrutura e coloca a estrutura na fila de mensagens.

O sistema usa o identificador de janela passado com a função [**CreateMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) para determinar qual fila de mensagens de thread deve receber a mensagem. Se o identificador for o HWND de mais **\_ alto**, o sistema posta a mensagem nas filas de mensagens de thread de todas as janelas de nível superior.

Você pode usar a função [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) para postar uma mensagem em uma fila de mensagens de thread específica. **PostThreadMessage** é semelhante a [**CreateMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), exceto que o primeiro parâmetro é um identificador de thread em vez de um identificador de janela. Você pode recuperar o identificador de thread chamando a função [**GetCurrentThreadID**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) .

Use a função [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) para sair de um loop de mensagem. **PostQuitMessage** posta a mensagem do [**WM \_ Quit**](wm-quit.md) para o thread em execução no momento. O loop de mensagem do thread é encerrado e retorna o controle ao sistema quando ele encontra a mensagem de **\_ quitação do WM** . Um aplicativo normalmente chama **PostQuitMessage** em resposta à mensagem [**de \_ destruição do WM**](wm-destroy.md) , conforme mostrado no exemplo a seguir.


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a>Enviando uma mensagem

A função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) é usada para enviar uma mensagem diretamente a um procedimento de janela. **SendMessage** chama um procedimento de janela e aguarda esse procedimento para processar a mensagem e retornar um resultado.

Uma mensagem pode ser enviada para qualquer janela no sistema; Tudo o que é necessário é um identificador de janela. O sistema usa o identificador para determinar qual procedimento de janela deve receber a mensagem.

Antes de processar uma mensagem que pode ter sido enviada de outro thread, um procedimento de janela deve primeiro chamar a função [**insendmessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) . Se essa função retornar **true**, o procedimento de janela deverá chamar [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) antes de qualquer função que faça com que o thread gere controle, conforme mostrado no exemplo a seguir.


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



Várias mensagens podem ser enviadas a controles em uma caixa de diálogo. Essas mensagens de controle definem a aparência, o comportamento e o conteúdo de controles ou recuperam informações sobre controles. Por exemplo, a [**mensagem \_ createstring CB**](../controls/cb-addstring.md) pode adicionar uma cadeia de caracteres a uma caixa de combinação e a mensagem [**\_ SetCheck BM**](../controls/bm-setcheck.md) pode definir o estado de verificação de uma caixa de seleção ou um botão de opção.

Use a função [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) para enviar uma mensagem a um controle, especificando o identificador do controle e o identificador da janela da caixa de diálogo que contém o controle. O exemplo a seguir, extraído de um procedimento de caixa de diálogo, copia uma cadeia de caracteres do controle de edição de uma caixa de combinação para sua caixa de listagem. O exemplo usa **SendDlgItemMessage** para enviar uma [**mensagem \_ createstring CB**](../controls/cb-addstring.md) para a caixa de combinação.


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



 

 
