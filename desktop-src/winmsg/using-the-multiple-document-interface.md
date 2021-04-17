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
# <a name="using-the-multiple-document-interface"></a>Usando a interface de vários documentos

Esta seção explica como executar as seguintes tarefas:

-   [Registrando classes de janela filho e de quadro](#registering-child-and-frame-window-classes)
-   [Criando janelas de quadro e filho](#creating-frame-and-child-windows)
-   [Escrevendo o loop de mensagem principal](#writing-the-main-message-loop)
-   [Escrevendo o procedimento da janela do quadro](#writing-the-frame-window-procedure)
-   [Escrevendo o procedimento de janela filho](#writing-the-child-window-procedure)
-   [Criando uma janela filho](#creating-a-child-window)

Para ilustrar essas tarefas, esta seção inclui exemplos do Multipad, um aplicativo típico de MDI (interface de vários documentos).

## <a name="registering-child-and-frame-window-classes"></a>Registrando classes de janela filho e de quadro

Um aplicativo MDI típico deve registrar duas classes de janela: uma para sua janela de quadro e outra para suas janelas filhas. Se um aplicativo oferecer suporte a mais de um tipo de documento (por exemplo, uma planilha e um gráfico), ele deverá registrar uma classe de janela para cada tipo.

A estrutura de classe da janela do quadro é semelhante à estrutura de classe da janela principal em aplicativos não MDI. A estrutura de classe para as janelas filho MDI difere ligeiramente da estrutura para janelas filhas em aplicativos não-MDI, da seguinte maneira:

-   A estrutura de classe deve ter um ícone, porque o usuário pode minimizar uma janela filho MDI como se fosse uma janela de aplicativo normal.
-   O nome do menu deve ser **nulo**, pois uma janela filho MDI não pode ter seu próprio menu.
-   A estrutura de classe deve reservar espaço extra na estrutura de janela. Com esse espaço, o aplicativo pode associar dados, como um nome de arquivo, a uma janela filho específica.

O exemplo a seguir mostra como o Multipad registra suas classes de quadro e janela filho.


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



## <a name="creating-frame-and-child-windows"></a>Criando janelas de quadro e filho

Depois de registrar suas classes de janela, um aplicativo MDI pode criar suas janelas. Primeiro, ele cria sua janela de quadros usando a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Depois de criar sua janela de quadros, o aplicativo cria a janela do cliente novamente usando **CreateWindow** ou **CreateWindowEx**. O aplicativo deve especificar MDICLIENT como o nome da classe da janela do cliente; **MdiClient** é uma classe de janela preregistrada definida pelo sistema. O parâmetro *lpvParam* de **CreateWindow** ou **CreateWindowEx** deve apontar para uma estrutura [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) . Essa estrutura contém os membros descritos na tabela a seguir:



| Membro           | DESCRIÇÃO                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hWindowMenu**  | Identificador para o menu de janela usado para controlar janelas filhas MDI. À medida que as janelas filhas são criadas, o aplicativo adiciona seus títulos ao menu janela como itens de menu. Em seguida, o usuário pode ativar uma janela filho clicando em seu título no menu janela.                                                               |
| **idFirstChild** | Especifica o identificador da primeira janela filho MDI. A primeira janela filho MDI criada é atribuída a esse identificador. Janelas adicionais são criadas com identificadores de janela incrementados. Quando uma janela filho é destruída, o sistema reatribui imediatamente os identificadores de janela para manter seu intervalo contíguo. |



 

Quando o título de uma janela filho é adicionado ao menu janela, o sistema atribui um identificador à janela filho. Quando o usuário clica no título de uma janela filho, a janela do quadro recebe uma mensagem de [**\_ comando do WM**](../menurc/wm-command.md) com o identificador no parâmetro *wParam* . Você deve especificar um valor para o membro **idFirstChild** que não esteja em conflito com identificadores de item de menu no menu da janela do quadro.

O procedimento da janela do quadro do Multipad cria a janela do cliente MDI durante o processamento da mensagem de [**\_ criação do WM**](wm-create.md) . O exemplo a seguir mostra como a janela do cliente é criada.


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



Os títulos das janelas filhas são adicionados à parte inferior do menu janela. Se o aplicativo adicionar cadeias de caracteres ao menu de janela usando a função [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) , essas cadeias de caracteres poderão ser substituídas pelos títulos das janelas filhas quando o menu janela for redesenhado (sempre que uma janela filho for criada ou destruída). Um aplicativo MDI que adiciona cadeias de caracteres ao menu de janela deve usar a função [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) e verificar se os títulos das janelas filhas não substituíram essas novas cadeias de caracteres.

Use o estilo **WS \_ CLIPCHILDREN** para criar a janela do cliente MDI para impedir que a janela pinte sobre suas janelas filhas.

## <a name="writing-the-main-message-loop"></a>Escrevendo o loop de mensagem principal

O loop de mensagem principal de um aplicativo MDI é semelhante ao de uma chave do acelerador de manipulação de aplicativos não MDI. A diferença é que o loop de mensagem MDI chama a função [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) antes de verificar se há chaves de acelerador definidas pelo aplicativo ou antes de expedir a mensagem.

O exemplo a seguir mostra o loop de mensagem de um aplicativo MDI típico. Observe que [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) pode retornar-1 se houver um erro.


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



A função [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) converte as mensagens do [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md) em mensagens do [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) e as envia para a janela filho MDI ativa. Se a mensagem não for uma mensagem de acelerador de MDI, a função retornará **false**; nesse caso, o aplicativo usará a função [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) para determinar se alguma das teclas de aceleração definidas pelo aplicativo foi pressionada. Caso contrário, o loop expedirá a mensagem para o procedimento de janela apropriado.

## <a name="writing-the-frame-window-procedure"></a>Escrevendo o procedimento da janela do quadro

O procedimento de janela para uma janela de quadro MDI é semelhante ao de uma janela principal do aplicativo não-MDI. A diferença é que um procedimento de janela de quadro passa todas as mensagens que ele não manipula para a função [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) em vez de para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Além disso, o procedimento de janela do quadro também deve passar algumas mensagens que ele manipula, incluindo aquelas listadas na tabela a seguir.



| Mensagem                                  | Resposta                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**comando do WM \_**](../menurc/wm-command.md)     | Ativa a janela filho MDI que o usuário escolhe. Essa mensagem é enviada quando o usuário escolhe uma janela filho MDI no menu janela da janela do quadro MDI. O identificador de janela que acompanha essa mensagem identifica a janela filho MDI a ser ativada. |
| [**MENUCHAR do WM \_**](../menurc/wm-menuchar.md)   | Abre o menu janela da janela filho MDI ativa quando o usuário pressiona a combinação de teclas ALT + – (menos).                                                                                                                                                      |
| [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md) | Passa o foco do teclado para a janela do cliente MDI, que, por sua vez, passa para a janela filho MDI ativa.                                                                                                                                                         |
| [**tamanho do WM \_**](wm-size.md)              | Redimensiona a janela do cliente MDI para caber na área do cliente da janela do novo quadro. Se o procedimento da janela do quadro dimensionar a janela do cliente MDI para um tamanho diferente, ele não deverá passar a mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .                   |



 

O procedimento de janela do quadro em Multipad é chamado de MPFrameWndProc. O tratamento de outras mensagens por MPFrameWndProc é semelhante ao dos aplicativos não-MDI. [**WM \_**](../menurc/wm-command.md) As mensagens de comando em Multipad são manipuladas pela função CommandHandler definida localmente. Para mensagens de comando Multipad não manipula, CommandHandler chama a função [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) . Se Multipad não usar **DefFrameProc** por padrão, o usuário não poderá ativar uma janela filho no menu janela, pois a mensagem **de \_ comando do WM** enviada clicando no item de menu da janela seria perdida.

## <a name="writing-the-child-window-procedure"></a>Escrevendo o procedimento de janela filho

Assim como o procedimento de janela do quadro, um procedimento de janela filho MDI usa uma função especial para processar mensagens por padrão. Todas as mensagens que o procedimento da janela filho não trata devem ser passadas para a função [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) em vez de para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Além disso, algumas mensagens de gerenciamento de janelas devem ser passadas para **DefMDIChildProc**, mesmo que o aplicativo manipule a mensagem, para que o MDI funcione corretamente. A seguir estão as mensagens que o aplicativo deve passar para **DefMDIChildProc**.



| Mensagem                                       | Resposta                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHILDACTIVATE do WM \_**](wm-childactivate.md) | Executa o processamento de ativação quando janelas filho MDI são dimensionadas, movidas ou exibidas. Esta mensagem deve ser passada.                                                                                                                                        |
| [**GETMINMAXINFO do WM \_**](wm-getminmaxinfo.md) | Calcula o tamanho de uma janela filho MDI maximizada, com base no tamanho atual da janela do cliente MDI.                                                                                                                                                  |
| [**MENUCHAR do WM \_**](../menurc/wm-menuchar.md)        | Passa a mensagem para a janela do quadro MDI.                                                                                                                                                                                                               |
| [**movimentação do WM \_**](wm-move.md)                   | Recalcula as barras de rolagem do cliente MDI, se estiverem presentes.                                                                                                                                                                                                 |
| [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md)      | Ativa a janela filho, se não for a janela filho MDI ativa.                                                                                                                                                                                     |
| [**tamanho do WM \_**](wm-size.md)                   | Executa operações necessárias para alterar o tamanho de uma janela, especialmente para maximizar ou restaurar uma janela filho MDI. A falha ao passar essa mensagem para a função [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) produz resultados altamente indesejáveis. |
| [**SYSCOMMAND do WM \_**](../menurc/wm-syscommand.md)    | Manipula comandos de menu Window (anteriormente conhecidos como System) **: SC \_ NEXTWINDOW**, **sc \_ PREVWINDOW**, **sc \_ mover**, **sc \_ size** e **sc \_ Maxim**.                                                                                                        |



 

## <a name="creating-a-child-window"></a>Criando uma janela filho

Para criar uma janela filho MDI, um aplicativo pode chamar a função [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) ou enviar uma mensagem do [**WM \_ MDICREATE**](wm-mdicreate.md) para a janela do cliente MDI. (O aplicativo pode usar a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) com o estilo **WS \_ ex \_ MDICHILD** para criar janelas filho MDI.) Um aplicativo MDI de thread único pode usar qualquer um dos métodos para criar uma janela filho. Um thread em um aplicativo MDI multithread deve usar a função **CreateMDIWindow** ou **CreateWindowEx** para criar uma janela filho em um thread diferente.

O parâmetro *lParam* de uma mensagem do [**WM \_ MDICREATE**](wm-mdicreate.md) é um ponteiro distante para uma estrutura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) . A estrutura inclui quatro membros de dimensão: **x** e **y**, que indicam as posições horizontal e vertical da janela, e **CX** e **CY**, que indicam as extensões horizontais e verticais da janela. Qualquer um desses membros pode ser atribuído explicitamente pelo aplicativo, ou pode ser definido para USEDEFAULT de **peso \_ variável**; nesse caso, o sistema seleciona uma posição, tamanho ou ambos, de acordo com um algoritmo em cascata. Em qualquer caso, todos os quatro membros devem ser inicializados. Multipad usa **\_ USEDEFAULT de PV** para todas as dimensões.

O último membro da estrutura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) é o membro **Style** , que pode conter bits de estilo para a janela. Para criar uma janela filho MDI que pode ter qualquer combinação de estilos de janela, especifique o estilo de janela **MDIS \_ ALLCHILDSTYLES** . Quando esse estilo não é especificado, uma janela filho MDI tem os **estilos \_ WS minimize**, **WS \_ Maxim**, WS **\_ HSCROLL** e **WS \_ VSCROLL** como configurações padrão.

O Multipad cria suas janelas filho MDI usando sua função AddFile definida localmente (localizada no arquivo de origem MPFILE. C). A função AddFile define o título da janela filho atribuindo o membro **szTitle** da estrutura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) da janela ao nome do arquivo que está sendo editado ou "sem título". O membro **szClass** é definido como o nome da classe de janela filho MDI registrada na função InitializeApplication do Multipad. O membro **hOwner** é definido como o identificador de instância do aplicativo.

O exemplo a seguir mostra a função AddFile em Multipad.


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



O ponteiro passado no parâmetro *lParam* da mensagem [**\_ MDICREATE do WM**](wm-mdicreate.md) é passado para a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) e aparece como o primeiro membro na estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) , passado na mensagem de [**\_ criação do WM**](wm-create.md) . No Multipad, a janela filho se inicializa durante o **WM \_ criar** processamento de mensagens Inicializando variáveis de documento em seus dados extras e criando a janela filho do controle de edição.

 

 
