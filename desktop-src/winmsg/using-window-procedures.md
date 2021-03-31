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
# <a name="using-window-procedures"></a>Usando os procedimentos de janela

Esta seção explica como executar as seguintes tarefas associadas a procedimentos de janela.

-   [Criando um procedimento de janela](#designing-a-window-procedure)
-   [Associando um procedimento de janela a uma classe de janela](#associating-a-window-procedure-with-a-window-class)
-   [Subclasse de uma janela](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a>Criando um procedimento de janela

O exemplo a seguir mostra a estrutura de um procedimento de janela típico. O procedimento de janela usa o argumento Message em uma instrução **switch** com mensagens individuais manipuladas por instruções **Case** separadas. Observe que cada caso retorna um valor específico para cada mensagem. Para mensagens que não são processadas, o procedimento de janela chama a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .


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



A mensagem do [**WM \_ NCCREATE**](wm-nccreate.md) é enviada logo após a sua janela ser criada, mas se um aplicativo responder a essa mensagem retornando **false**, a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) falhará. A mensagem de [**\_ criação do WM**](wm-create.md) é enviada depois que a janela já está criada.

A mensagem de [**\_ destruição do WM**](wm-destroy.md) é enviada quando a janela está prestes a ser destruída. A função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) cuida da destruição de todas as janelas filhas da janela que está sendo destruída. A mensagem do [**WM \_ NCDESTROY**](wm-ncdestroy.md) é enviada logo antes de uma janela ser destruída.

Na pior das hipóteses, um procedimento de janela deve processar a mensagem do [**WM \_ Paint**](../gdi/wm-paint.md) para se desenhar. Normalmente, ele também deve lidar com mensagens de mouse e teclado. Consulte as descrições de mensagens individuais para determinar se o procedimento de janela deve tratá-las.

Seu aplicativo pode chamar a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como parte do processamento de uma mensagem. Nesse caso, o aplicativo pode modificar os parâmetros da mensagem antes de passar a mensagem para **DefWindowProc** ou pode continuar com o processamento padrão depois de executar suas próprias operações.

Um procedimento de caixa de diálogo recebe uma mensagem do [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) em vez de uma mensagem de [**\_ criação do WM**](wm-create.md) e não passa mensagens não processadas para a função [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) . Caso contrário, um procedimento de caixa de diálogo é exatamente o mesmo que um procedimento de janela.

## <a name="associating-a-window-procedure-with-a-window-class"></a>Associando um procedimento de janela a uma classe de janela

Você associa um procedimento de janela a uma classe de janela ao registrar a classe. Você deve preencher uma estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) com informações sobre a classe e o membro **lpfnWndProc** deve especificar o endereço do procedimento de janela. Para registrar a classe, passe o endereço da estrutura **WNDCLASS** para a função [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . Depois que a classe Window tiver sido registrada, o procedimento de janela será automaticamente associado a cada nova janela criada com essa classe.

O exemplo a seguir mostra como associar o procedimento de janela no exemplo anterior a uma classe de janela.


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



## <a name="subclassing-a-window"></a>Subclasse de uma janela

Para subclasse de uma instância de uma janela, chame a função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) e especifique o identificador para a janela para subclasse o \_ sinalizador GWL WndProc e um ponteiro para o procedimento de subclasse. **SetWindowLong** retorna um ponteiro para o procedimento de janela original; Use esse ponteiro para passar mensagens para o procedimento original. O procedimento de janela de subclasse deve usar a função [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) para chamar o procedimento de janela original.

> [!Note]  
> Para escrever um código compatível com as versões de 32 bits e 64 bits do Windows, use a função [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) .

 

O exemplo a seguir mostra como subclasse de uma instância de um controle de edição em uma caixa de diálogo. O procedimento de janela de subclasse permite que o controle de edição receba todas as entradas de teclado, incluindo as teclas ENTER e TAB, sempre que o controle tiver o foco de entrada.


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



 

 
