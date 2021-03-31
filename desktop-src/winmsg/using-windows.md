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
# <a name="using-windows"></a>Usando o Windows

Os exemplos nesta seção descrevem como executar as seguintes tarefas:

-   [Criando uma janela principal](#creating-a-main-window)
-   [Criando, enumerando e dimensionando janelas filhas](#creating-enumerating-and-sizing-child-windows)
-   [Destruindo uma janela](#destroying-a-window)
-   [Usando janelas em camadas](#using-layered-windows)

## <a name="creating-a-main-window"></a>Criando uma janela principal

A primeira janela que um aplicativo cria normalmente é a janela principal. Você cria a janela principal usando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , especificando a classe da janela, o nome da janela, os estilos de janela, o tamanho, a posição, o identificador de menu, o identificador de instância e os dados de criação. Uma janela principal pertence a uma classe de janela definida pelo aplicativo, portanto, você deve registrar a classe Window e fornecer um procedimento de janela para a classe antes de criar a janela principal.

A maioria dos aplicativos normalmente usa o estilo [**WS \_ OVERLAPPEDWINDOW**](window-styles.md) para criar a janela principal. Esse estilo dá à janela uma barra de título, um menu de janela, uma borda de dimensionamento e os botões minimizar e maximizar. A função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) retorna um identificador que identifica exclusivamente a janela.

O exemplo a seguir cria uma janela principal que pertence a uma classe de janela definida pelo aplicativo. O nome da janela, **janela principal**, aparecerá na barra de título da janela. Ao combinar os [**estilos \_ WS VSCROLL**](window-styles.md) e **WS \_ HSCROLL** com o estilo **WS \_ OVERLAPPEDWINDOW** , o aplicativo cria uma janela principal com barras de rolagem horizontal e vertical, além dos componentes fornecidos pelo estilo **WS \_ OVERLAPPEDWINDOW** . As quatro ocorrências da constante **\_ USEDEFAULT de PV** definem o tamanho inicial e a posição da janela para os valores padrão definidos pelo sistema. Ao especificar **NULL** em vez de um identificador de menu, a janela terá o menu definido para a classe de janela.


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



Observe que o exemplo anterior chama a função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) após criar a janela principal. Isso é feito porque o sistema não exibe automaticamente a janela principal depois de criá-la. Ao passar o sinalizador de configuração **\_ padrão de SW** para **janela**, o aplicativo permite que o programa que iniciou o aplicativo defina o estado de exibição inicial da janela principal. A função [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) envia a janela sua primeira mensagem do [**WM \_ Paint**](../gdi/wm-paint.md) .

## <a name="creating-enumerating-and-sizing-child-windows"></a>Criando, enumerando e dimensionando janelas filhas

Você pode dividir a área do cliente de uma janela em diferentes áreas funcionais usando as janelas filhas. A criação de uma janela filho é como criar uma janela principal — você usa a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Para criar uma janela de uma classe de janela definida pelo aplicativo, você deve registrar a classe Window e fornecer um procedimento de janela antes de criar a janela filho. Você deve dar à janela filho o estilo de [**WS \_ filho**](window-styles.md) e especificar uma janela pai para a janela filho ao criá-la.

O exemplo a seguir divide a área do cliente da janela principal de um aplicativo em três áreas funcionais criando três janelas filhas de tamanho igual. Cada janela filho tem a mesma altura que a área do cliente da janela principal, mas cada uma é uma terceira de sua largura. A janela principal cria as janelas filhas em resposta à mensagem [**de \_ criação do WM**](wm-create.md) , que a janela principal recebe durante seu próprio processo de criação de janela. Como cada janela filho tem o estilo de [**\_ borda WS**](window-styles.md) , cada uma tem uma borda de linha fina. Além disso, como o estilo do **WS \_ Visible** não é especificado, cada janela filho é inicialmente oculta. Observe também que cada janela filho recebe um identificador de janela filho.

A janela principal dimensiona e posiciona as janelas filhas em resposta à mensagem [**de \_ tamanho do WM**](wm-size.md) , que a janela principal recebe quando seu tamanho é alterado. Em resposta ao **\_ tamanho do WM**, a janela principal recupera as dimensões de sua área de cliente usando a função [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) e, em seguida, passa as dimensões para a função [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) . **EnumChildWindows** passa o identificador para cada janela filho, por sua vez, para a função de retorno de chamada [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) definida pelo aplicativo. Essa função dimensiona e posiciona cada janela filho chamando a função [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) ; o tamanho e a posição são baseados nas dimensões da área do cliente da janela principal e no identificador da janela filho. Depois disso, **EnumChildProc** chama a função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) para tornar a janela visível.


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



## <a name="destroying-a-window"></a>Destruindo uma janela

Você pode usar a função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) para destruir uma janela. Normalmente, um aplicativo envia a mensagem de [**\_ fechamento do WM**](wm-close.md) antes de destruir uma janela, dando à janela a oportunidade de solicitar a confirmação do usuário antes que a janela seja destruída. Uma janela que inclui um menu de janela recebe automaticamente a mensagem de **\_ fechamento do WM** quando o usuário clica em **Fechar** no menu janela. Se o usuário confirmar que a janela deve ser destruída, o aplicativo chamará **DestroyWindow**. O sistema envia a mensagem de [**\_ destruição do WM**](wm-destroy.md) para a janela depois de removê-la da tela. Em resposta ao **WM \_ Destroy**, a janela salva seus dados e libera todos os recursos alocados. Uma janela principal conclui seu processamento do **WM \_ Destroy** chamando a função [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) para sair do aplicativo.

O exemplo a seguir mostra como solicitar a confirmação do usuário antes de destruir uma janela. Em resposta à [**\_ fechamento do WM**](wm-close.md), o exemplo exibe uma caixa de diálogo que contém os botões **Sim**, **não** e **Cancelar** . Se o usuário clicar em **Sim**, [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) será chamado; caso contrário, a janela não será destruída. Como a janela que está sendo destruída é uma janela principal, o exemplo chama [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) em resposta ao [**WM \_ Destroy**](wm-destroy.md).


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



## <a name="using-layered-windows"></a>Usando janelas em camadas

Para que uma caixa de diálogo seja exibida como uma janela translúcida, primeiro crie o diálogo como de costume. Em seguida, no [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md), defina o bit em camadas do estilo estendido da janela e chame [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) com o valor alfa desejado. O código pode ser assim:


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



Observe que o terceiro parâmetro de [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) é um valor que varia de 0 a 255, com 0 tornando a janela completamente transparente e 255 tornando-a completamente opaca. Esse parâmetro imita a [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) mais versátil da função [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .

Para tornar essa janela completamente opaca novamente, remova o bit **WS \_ ex em \_ camadas** chamando [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) e, em seguida, peça que a janela seja redesenhada. Remover o bit é desejado para permitir que o sistema saiba que ele pode liberar memória associada a camadas e redirecionamento. O código pode ser assim:


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



Para usar janelas filho em camadas, o aplicativo precisa declarar o reconhecimento do Windows 8 no manifesto.

 

 
