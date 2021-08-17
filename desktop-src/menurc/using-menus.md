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
ms.openlocfilehash: 61f3a71a580a323fa2058613f8c9a14d9c2782bd3ba139e5d182750e5047fe74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971925"
---
# <a name="using-menus"></a>Uso de Menus

Esta seção descreve as seguintes tarefas:

-   [Usando um recurso Menu-Template](#using-a-menu-template-resource)
    -   [Formato de Menu-Template estendido](#extended-menu-template-format)
    -   [Antigo formato de Menu-Template](#old-menu-template-format)
    -   [Carregando um recurso de Menu-Template](#loading-a-menu-template-resource)
    -   [Criando um menu de classe](#creating-a-class-menu)
-   [Criando um menu de atalho](#creating-a-shortcut-menu)
    -   [Processando a \_ mensagem CONTEXTMENU do WM](/windows)
    -   [Criando um menu de Font-Attributes de atalho](#creating-a-shortcut-font-attributes-menu)
    -   [Exibindo um menu de atalho](#displaying-a-shortcut-menu)
-   [Usando Menu-Item bitmaps](#using-menu-item-bitmaps)
    -   [Configurando o sinalizador de tipo de bitmap](#setting-the-bitmap-type-flag)
    -   [Criando o bitmap](#creating-the-bitmap)
    -   [Adicionando linhas e grafos a um menu](#adding-lines-and-graphs-to-a-menu)
    -   [Exemplo de bitmaps de Menu-Item](#example-of-menu-item-bitmaps)
-   [Criando Owner-Drawn itens de menu](#creating-owner-drawn-menu-items)
    -   [Definindo o sinalizador de Owner-Drawn](#setting-the-owner-drawn-flag)
    -   [Menus desenhados pelo proprietário e a mensagem do WM \_ MEASUREITEM](/windows)
    -   [Menus desenhados pelo proprietário e a mensagem do WM \_ DRAWITEM](/windows)
    -   [Menus desenhados pelo proprietário e a mensagem do WM \_ MENUCHAR](/windows)
    -   [Definindo fontes para Menu-Item cadeias de caracteres de texto](#setting-fonts-for-menu-item-text-strings)
    -   [Exemplo de itens de menu Owner-Drawn](#example-of-owner-drawn-menu-items)
-   [Usando bitmaps de marca de seleção personalizados](#using-custom-check-mark-bitmaps)
    -   [Criando bitmaps de marca de seleção personalizados](#creating-custom-check-mark-bitmaps)
    -   [Associando bitmaps a um item de menu](#associating-bitmaps-with-a-menu-item)
    -   [Definindo o atributo de marca de seleção](#setting-the-check-mark-attribute)
    -   [Simulando caixas de seleção em um menu](#simulating-check-boxes-in-a-menu)
    -   [Exemplo de como usar bitmaps de marca de seleção personalizados](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a>Usando um recurso Menu-Template

Normalmente, você inclui um menu em um aplicativo Criando um recurso de modelo de menu e, em seguida, carregando o menu em tempo de execução. Esta seção descreve o formato de um modelo de menu e explica como carregar um recurso de modelo de menu e usá-lo em seu aplicativo. Para obter informações sobre como criar um recurso de modelo de menu, consulte a documentação incluída com suas ferramentas de desenvolvimento.

-   [Formato de Menu-Template estendido](#extended-menu-template-format)
-   [Antigo formato de Menu-Template](#old-menu-template-format)
-   [Carregando um recurso de Menu-Template](#loading-a-menu-template-resource)
-   [Criando um menu de classe](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a>Formato de Menu-Template estendido

O formato de modelo de menu estendido dá suporte à funcionalidade de menu adicional. Como os recursos de modelo de menu padrão, os recursos de modelo de menu estendido têm o tipo de recurso de **\_ menu RT** . O sistema distingue os dois formatos de recurso pelo número de versão, que é o primeiro membro do cabeçalho de recurso.

Um modelo de menu estendido consiste em uma estrutura de [**\_ \_ cabeçalho de modelo MENUEX**](menuex-template-header.md) seguida por uma ou mais estruturas de definição de item de [**\_ \_ item de modelo MENUEX**](menuex-template-item.md) .

### <a name="old-menu-template-format"></a>Antigo formato de Menu-Template

um modelo de menu antigo (Microsoft Windows NT 3,51 e anterior) define um menu, mas não oferece suporte à nova funcionalidade de menu. Um recurso de modelo de menu antigo tem o tipo de recurso de **\_ menu RT** .

Um modelo de menu antigo consiste em uma estrutura [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) seguida por uma ou mais estruturas [**MenuItemTemplate**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) .

### <a name="loading-a-menu-template-resource"></a>Carregando um recurso de Menu-Template

Para carregar um recurso de modelo de menu, use a função [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) , especificando um identificador para o módulo que contém o recurso e o identificador do modelo de menu. A função **LoadMenu** retorna um identificador de menu que você pode usar para atribuir o menu a uma janela. Essa janela torna-se a janela do proprietário do menu, recebendo todas as mensagens geradas pelo menu.

Para criar um menu a partir de um modelo de menu que já está na memória, use a função [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) . Isso será útil se o aplicativo gerar modelos de menu dinamicamente.

Para atribuir um menu a uma janela, use a função [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) ou especifique o identificador do menu no parâmetro *HMenu* da função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ao criar uma janela. Outra maneira de atribuir um menu a uma janela é especificar um modelo de menu ao registrar uma classe de janela; o modelo identifica o menu especificado como o menu de classe para essa classe de janela.

Para que o sistema atribua automaticamente um menu específico a uma janela, especifique o modelo do menu ao registrar a classe da janela. O modelo identifica o menu especificado como o menu de classe para essa classe de janela. Em seguida, quando você cria uma janela da classe especificada, o sistema atribui automaticamente o menu especificado à janela.

Você não pode atribuir um menu a uma janela que seja uma janela filho.

Para criar um menu de classe, inclua o identificador do recurso de modelo de menu como o membro **lpszMenuName** de uma estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) e, em seguida, passe um ponteiro para a estrutura para a função [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) .

### <a name="creating-a-class-menu"></a>Criando um menu de classe

O exemplo a seguir mostra como criar um menu de classe para um aplicativo, criar uma janela que usa o menu de classe e processar comandos de menu no procedimento de janela.

A seguir está a parte relevante do arquivo de cabeçalho do aplicativo:


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



A seguir estão as partes relevantes do próprio aplicativo:


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



## <a name="creating-a-shortcut-menu"></a>Criando um menu de atalho

Para usar um menu de atalho em um aplicativo, passe seu identificador para a função [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) . Um aplicativo normalmente chama **TrackPopupMenuEx** em um procedimento de janela em resposta a uma mensagem gerada pelo usuário, como o [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) ou o [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown).

Além do identificador do menu pop-up, o [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) exige que você especifique um identificador para a janela do proprietário, a posição do menu de atalho (nas coordenadas da tela) e o botão do mouse que o usuário pode usar para escolher um item.

A função [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) mais antiga ainda tem suporte, mas novos aplicativos devem usar a função [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) . A função **TrackPopupMenuEx** requer os mesmos parâmetros que **TrackPopupMenu**, mas também permite que você especifique uma parte da tela que o menu não deve obscurecer. Normalmente, um aplicativo chama essas funções em um procedimento de janela ao processar a mensagem [**\_ CONTEXTMENU do WM**](wm-contextmenu.md) .

Você pode especificar a posição de um menu de atalho fornecendo coordenadas x e y juntamente com o sinalizador **TPM \_ CENTERALIGN**, **TPM \_ LEFTALIGN** ou **TPM \_ RIGHTALIGN** . O sinalizador especifica a posição do menu de atalho em relação às coordenadas x e y.

Você deve permitir que o usuário escolha um item em um menu de atalho usando o mesmo botão do mouse usado para exibir o menu. Para fazer isso, especifique o sinalizador **TPM \_ LEFTBUTTON** ou **TPM \_ RIGHTBUTTON** para indicar qual botão do mouse o usuário pode usar para escolher um item de menu.

-   [Processando a \_ mensagem CONTEXTMENU do WM](/windows)
-   [Criando um menu de Font-Attributes de atalho](#creating-a-shortcut-font-attributes-menu)
-   [Exibindo um menu de atalho](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a>Processando a \_ mensagem CONTEXTMENU do WM

A mensagem de [**\_ CONTEXTMENU do WM**](wm-contextmenu.md) é gerada quando um procedimento de janela do aplicativo passa a mensagem do [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) ou do [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . O aplicativo pode processar essa mensagem para exibir um menu de atalho apropriado para uma parte específica de sua tela. Se o aplicativo não exibir um menu de atalho, ele deverá passar a mensagem para **DefWindowProc** para tratamento padrão.

A seguir está um exemplo de processamento de mensagens [**WM \_ CONTEXTMENU,**](wm-contextmenu.md) pois ele pode aparecer no procedimento de janela de um aplicativo. As palavras de ordem baixa e alta do parâmetro *lParam* especificam as coordenadas de tela do mouse quando o botão direito do mouse é liberado (observe que essas coordenadas podem receber valores negativos em sistemas com vários monitores). A função **OnContextMenu** definida pelo aplicativo retornará **TRUE** se exibir um menu de contexto ou **FALSE** se não exibir.


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



A função OnContextMenu definida pelo aplicativo a seguir exibirá um menu de atalho se a posição especificada do mouse estiver dentro da área do cliente da janela. Uma função mais sofisticada pode exibir um dos vários menus diferentes, dependendo de qual parte da área do cliente é especificada. Para exibir o menu de atalho, este exemplo chama uma função definida pelo aplicativo chamada DisplayContextMenu. Para uma descrição dessa função, consulte [Exibindo um menu de atalho](#displaying-a-shortcut-menu).


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



### <a name="creating-a-shortcut-font-attributes-menu"></a>Criando um menu de Font-Attributes atalho

O exemplo nesta seção contém partes de código de um aplicativo que cria e exibe um menu de atalho que permite ao usuário definir fontes e atributos de fonte. O aplicativo exibe o menu na área do cliente da janela principal sempre que o usuário clica no botão esquerdo do mouse.

Este é o modelo de menu para o menu de atalho fornecido no arquivo de definição de recursos do aplicativo.


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



O exemplo a seguir fornece o procedimento de janela e as funções de suporte usadas para criar e exibir o menu de atalho.


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



### <a name="displaying-a-shortcut-menu"></a>Exibindo um menu de atalho

A função mostrada no exemplo a seguir exibe um menu de atalho.

O aplicativo inclui um recurso de menu identificado pela cadeia de caracteres "ShortcutExample". A barra de menus simplesmente contém um nome de menu. O aplicativo usa a [**função TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) para exibir o menu associado a este item de menu. (A barra de menus em si não é exibida porque **TrackPopupMenu** requer um alça para um menu, submenu ou menu de atalho.)


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



## <a name="using-menu-item-bitmaps"></a>Usando Menu-Item bitmaps

O sistema pode usar um bitmap em vez de uma cadeia de caracteres de texto para exibir um item de menu. Para usar um bitmap, você deve definir o sinalizador **\_ BITMAP MIIM** para o item de menu e especificar um alça para o bitmap que o sistema deve exibir para o item de menu no membro **hbmpItem** da estrutura [**MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) Esta seção descreve como usar bitmaps para itens de menu.

-   [Definindo o sinalizador de tipo bitmap](#setting-the-bitmap-type-flag)
-   [Criando o Bitmap](#creating-the-bitmap)
-   [Adicionando linhas e grafos a um menu](#adding-lines-and-graphs-to-a-menu)
-   [Exemplo de Menu-Item Bitmaps](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a>Definindo o sinalizador de tipo bitmap

O **sinalizador \_ BITMAP ou** **\_ MF BITMAP** do MIIM informa ao sistema para usar um bitmap em vez de uma cadeia de caracteres de texto para exibir um item de menu. O **\_ bitmap miim** de um item de menu ou o sinalizador **\_ BITMAP MF** devem ser definidos em tempo de executar; você não pode defini-lo no arquivo de definição de recurso.

Para novos aplicativos, você pode usar a [**função SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) ou [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) para definir o sinalizador de tipo **\_ BITMAP MIIM.** Para alterar um item de menu de um item de texto para um item de bitmap, use **SetMenuItemInfo**. Para adicionar um novo item de bitmap a um menu, use a **função InsertMenuItem.**

Os aplicativos escritos para versões anteriores do sistema podem continuar a usar as funções [**ModifyMenu,**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)ou [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) para definir o **sinalizador MF \_ BITMAP.** Para alterar um item de menu de um item de cadeia de caracteres de texto para um item de bitmap, use **ModifyMenu**. Para adicionar um novo item de bitmap a um menu, use o sinalizador **\_ MF BITMAP** com a função **InsertMenu** ou **AppendMenu.**

### <a name="creating-the-bitmap"></a>Criando o Bitmap

Ao definir o sinalizador de tipo **\_ BITMAP miim** ou **\_ MF BITMAP** para um item de menu, você também deve especificar um identificador para o bitmap que o sistema deve exibir para o item de menu. Você pode fornecer o bitmap como um recurso de bitmap ou criar o bitmap em tempo de executar. Se você usar um recurso de bitmap, poderá usar a [**função LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) para carregar o bitmap e obter seu handle.

Para criar o bitmap em tempo de executar, use funções Windows Graphics Device Interface (GDI). A GDI fornece várias maneiras de criar um bitmap em tempo de executar, mas os desenvolvedores normalmente usam o seguinte método:

1.  Use a [**função CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) para criar um contexto de dispositivo compatível com o contexto do dispositivo usado pela janela principal do aplicativo.
2.  Use a [**função CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) para criar um bitmap compatível com a janela principal do aplicativo ou use a [**função CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) para criar um bitmap monocromático.
3.  Use a [**função SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) para selecionar o bitmap no contexto do dispositivo compatível.
4.  Use funções de desenho GDI, como [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) e [**LineTo,**](/windows/desktop/api/wingdi/nf-wingdi-lineto)para desenhar uma imagem no bitmap.

Para obter mais informações, consulte [Bitmaps](/windows/desktop/gdi/bitmaps).

### <a name="adding-lines-and-graphs-to-a-menu"></a>Adicionando linhas e grafos a um menu

O exemplo de código a seguir mostra como criar um menu que contém bitmaps de item de menu. Ele cria dois menus. A primeira é um menu Gráfico que contém três bitmaps de item de menu: um gráfico de pizza, um gráfico de linhas e um gráfico de barras. O exemplo demonstra como carregar esses bitmaps do arquivo de recurso do aplicativo e, em seguida, usar as funções [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) e [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) para criar os itens de menu e menu.

O segundo menu é um menu Linhas. Ele contém bitmaps mostrando os estilos de linha fornecidos pela caneta predefinida no sistema. Os bitmaps de estilo de linha são criados em tempo de execução usando funções GDI.

Aqui estão as definições dos recursos de bitmap no arquivo de definição de recursos do aplicativo.


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



Aqui estão as partes relevantes do arquivo de header do aplicativo.


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



O exemplo a seguir mostra como menus e bitmaps de item de menu são criados em um aplicativo.


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



### <a name="example-of-menu-item-bitmaps"></a>Exemplo de Menu-Item Bitmaps

O exemplo neste tópico cria dois menus, cada um contendo vários itens de menu bitmap. Para cada menu, o aplicativo adiciona um nome de menu correspondente à barra de menus da janela principal.

O primeiro menu contém itens de menu mostrando cada um dos três tipos de gráfico: pizza, linha e barra. Os bitmaps para esses itens de menu são definidos como recursos e carregados usando a [**função LoadBitmap.**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) Associado a esse menu, há um nome de menu "Gráfico" na barra de menus.

O segundo menu contém itens de menu mostrando cada um dos cinco estilos de linha usados com a função [**CreatePen:**](/windows/desktop/api/wingdi/nf-wingdi-createpen) **PS \_ SOLID,** **PS \_ DASH,** **PS \_ DOT,** **PS \_ DASHDOT** e **PS \_ DASHDOTDOT.** O aplicativo cria os bitmaps para esses itens de menu em tempo de executar usando funções de desenho GDI. Associado a esse menu, há um **nome de** menu Linhas na barra de menus.

Definidas no procedimento de janela do aplicativo são duas matrizes estáticas de alças de bitmap. Uma matriz contém os alças dos três bitmaps usados para **o** menu Gráfico. O outro contém os alças dos cinco bitmaps usados para **o** menu Linhas. Ao processar a mensagem [**WM \_ CREATE,**](/windows/desktop/winmsg/wm-create) o procedimento de janela carrega os bitmaps do gráfico, cria os bitmaps de linha e adiciona os itens de menu correspondentes. Ao processar a mensagem [**WM \_ DESTROY,**](/windows/desktop/winmsg/wm-destroy) o procedimento de janela exclui todos os bitmaps.

A seguir estão as partes relevantes do arquivo de header do aplicativo.


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



A seguir estão as partes relevantes do procedimento de janela. O procedimento de janela executa a maior parte de sua inicialização chamando as funções LoadChartBitmaps, CreateLineBitmaps e AddBitmapMenu definidas pelo aplicativo, descritas posteriormente neste tópico.


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



A função LoadChartBitmaps definida pelo aplicativo carrega os recursos de bitmap para o menu do gráfico chamando a [**função LoadBitmap,**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) da seguinte forma.


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



A função CreateLineBitmaps definida pelo aplicativo cria os bitmaps para o menu Linhas usando funções de desenho GDI. A função cria um DC (contexto de dispositivo de memória) com as mesmas propriedades que o DC da janela da área de trabalho. Para cada estilo de linha, a função cria um bitmap, seleciona-o no DC de memória e desenha nele.


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



A função AddBitmapMenu definida pelo aplicativo cria um menu e adiciona o número especificado de itens de menu bitmap a ele. Em seguida, ele adiciona um nome de menu correspondente à barra de menus da janela especificada.


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



## <a name="creating-owner-drawn-menu-items"></a>Criando Owner-Drawn de menu

Se você precisar de controle total sobre a aparência de um item de menu, poderá usar um item de menu desenhado pelo proprietário em seu aplicativo. Esta seção descreve as etapas envolvidas na criação e no uso de um item de menu desenhado pelo proprietário.

-   [Definindo o sinalizador Owner-Drawn de dados](#setting-the-owner-drawn-flag)
-   [Menus desenhados pelo proprietário e a mensagem WM \_ MEASUREITEM](/windows)
-   [Menus desenhados pelo proprietário e a mensagem WM \_ DRAWITEM](/windows)
-   [Menus desenhados pelo proprietário e a mensagem \_ WM MENUCHAR](/windows)
-   [Definindo fontes para cadeias Menu-Item de texto](#setting-fonts-for-menu-item-text-strings)
-   [Exemplo de itens Owner-Drawn menu](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a>Definindo o sinalizador Owner-Drawn de dados

Não é possível definir um item de menu desenhado pelo proprietário no arquivo de definição de recursos do aplicativo. Em vez disso, você deve criar um novo item de menu ou modificar um existente usando o sinalizador de menu **MFT \_ OWNERDRAW.**

Você pode usar a [**função InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) ou [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) para especificar um item de menu desenhado pelo proprietário. Use **InsertMenuItem** para inserir um novo item de menu na posição especificada em uma barra de menus ou menu. Use **SetMenuItemInfo** para alterar o conteúdo de um menu.

Ao chamar essas duas funções, você deve especificar um ponteiro para uma estrutura [**MENUITEMINFO,**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) que especifica as propriedades do novo item de menu ou as propriedades que você deseja alterar para um item de menu existente. Para tornar um item um item desenhado pelo proprietário, especifique o valor **MIIM \_ FTYPE** para o membro **fMask** e o **valor \_ MFT OWNERDRAW** para o **membro fType.**

Ao definir os membros apropriados da estrutura [**MENUITEMINFO,**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) você pode associar um valor definido pelo aplicativo, que é chamado de dados de **item**, a cada item de menu. Para fazer isso, especifique o **valor MIIM \_ DATA** para o membro **fMask** e o valor definido pelo aplicativo para o **membro dwItemData.**

Você pode usar dados de item com qualquer tipo de item de menu, mas é particularmente útil para itens desenhados pelo proprietário. Por exemplo, suponha que uma estrutura contenha informações usadas para desenhar um item de menu. Um aplicativo pode usar os dados do item para um item de menu para armazenar um ponteiro para a estrutura. Os dados do item são enviados para a janela do proprietário do menu com as mensagens do [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) e do [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) . Para recuperar os dados do item para um menu a qualquer momento, use a função [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .

Os aplicativos escritos para versões anteriores do sistema podem continuar a chamar [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)ou [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) para atribuir o sinalizador **MF \_ OWNERDRAW** a um item de menu desenhado pelo proprietário.

Ao chamar qualquer uma dessas três funções, você pode passar um valor como o parâmetro *lpNewItem* . Esse valor pode representar qualquer informação que seja significativa para seu aplicativo e que estará disponível para seu aplicativo quando o item for exibido. Por exemplo, o valor pode conter um ponteiro para uma estrutura; a estrutura, por sua vez, pode conter uma cadeia de texto e um identificador para a fonte lógica que seu aplicativo usará para desenhar a cadeia de caracteres.

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a>Owner-Drawn menus e a mensagem do WM \_ MEASUREITEM

Antes que o sistema exiba um item de menu desenhado pelo proprietário pela primeira vez, ele envia a mensagem do [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) para o procedimento de janela da janela que possui o menu do item. Essa mensagem contém um ponteiro para uma estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que identifica o item e contém os dados do item que um aplicativo pode ter atribuído a ele. O procedimento de janela deve preencher os membros de **ItemHeight** e **dowidth** da estrutura antes de retornar do processamento da mensagem. O sistema usa as informações nesses membros ao criar o retângulo delimitador no qual um aplicativo desenha o item de menu. Ele também usa as informações para detectar quando o usuário escolhe o item.

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a>Owner-Drawn menus e a mensagem do WM \_ DRAWITEM

Sempre que o item deve ser desenhado (por exemplo, quando é exibido pela primeira vez ou quando o usuário o seleciona), o sistema envia a mensagem do [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) para o procedimento de janela da janela do proprietário do menu. Essa mensagem contém um ponteiro para uma estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , que contém informações sobre o item, incluindo os dados do item que um aplicativo pode ter atribuído a ele. Além disso, **DRAWITEMSTRUCT** contém sinalizadores que indicam o estado do item (como se ele está esmaecido ou selecionado), bem como um retângulo delimitador e um contexto de dispositivo que o aplicativo usa para desenhar o item.

Um aplicativo deve fazer o seguinte durante o processamento da mensagem do [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) :

-   Determine o tipo de desenho necessário. Para fazer isso, verifique o membro de **ação** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .
-   Desenhe o item de menu adequadamente, usando o retângulo delimitador e o contexto do dispositivo obtido na estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . O aplicativo deve ser desenhado somente dentro do retângulo delimitador. Por motivos de desempenho, o sistema não corta partes da imagem que são desenhadas fora do retângulo.
-   Restaurar todos os objetos GDI selecionados para o contexto do dispositivo do item de menu.

Se o usuário selecionar o item de menu, o sistema definirá o membro de **ação** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) como o valor de **\_ seleção de Oda** e definirá o valor de **ODS \_ selecionado** no membro **ItemState** . Esta é a indicação de um aplicativo para redesenhar o item de menu para indicar que ele está selecionado.

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a>Owner-Drawn menus e a mensagem do WM \_ MENUCHAR

Menus diferentes de menus desenhados pelo proprietário podem especificar um mnemônico de menu inserindo um sublinhado ao lado de um caractere na cadeia de menu. Isso permite que o usuário selecione o menu pressionando ALT e pressionando o caractere de menu mnemônico. No entanto, nos menus desenhados pelo proprietário, você não pode especificar um mnemônico de menu dessa maneira. Em vez disso, seu aplicativo deve processar a mensagem [**\_ MENUCHAR do WM**](wm-menuchar.md) para fornecer menus desenhados pelo proprietário com mnemônicos de menu.

A mensagem do [**WM \_ MENUCHAR**](wm-menuchar.md) é enviada quando o usuário digita um mnemônico do menu que não corresponde a nenhum dos mnemônicos predefinidos do menu atual. O valor contido em *wParam* especifica o caractere ASCII que corresponde à chave que o usuário pressionou com a tecla Alt. A palavra de ordem inferior de *wParam* especifica o tipo do menu selecionado e pode ser um dos seguintes valores:

-   **MF \_ POPUP** se o menu atual for um submenu.
-   **MF \_ SYSMENU** se o menu for o menu do sistema.

A palavra de ordem superior de *wParam* contém o identificador de menu para o menu atual. A janela com os menus desenhados pelo proprietário pode processar o [**WM \_ MENUCHAR**](wm-menuchar.md) da seguinte maneira:


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



Os dois na palavra de ordem superior do valor de retorno informam ao sistema que a palavra de ordem inferior do valor de retorno contém o índice de base zero do item de menu a ser selecionado.

As constantes a seguir correspondem aos possíveis valores de retorno da mensagem do [**WM \_ MENUCHAR**](wm-menuchar.md) .



| Constante         | Valor | Significado                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ignorar MNC**  | 0     | O sistema deve descartar o caractere que o usuário pressionou e criar um bipe curto no alto-falante do sistema.                                                       |
| **MNC \_ fechar**   | 1     | O sistema deve fechar o menu ativo.                                                                                                                      |
| **MNC \_ executar** | 2     | O sistema deve escolher o item especificado na palavra de ordem inferior do valor de retorno. A janela do proprietário recebe uma mensagem de [**\_ comando do WM**](wm-command.md) . |
| **MNC \_ selecionar**  | 3     | O sistema deve selecionar o item especificado na palavra de ordem inferior do valor de retorno.                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a>Definindo fontes para Menu-Item cadeias de caracteres de texto

Este tópico contém um exemplo de um aplicativo que usa itens de menu de desenho proprietário em um menu. O menu contém itens que definem os atributos da fonte atual e os itens são exibidos usando o atributo de fonte apropriado.

Veja como o menu é definido no arquivo de definição de recurso. Observe que as cadeias de caracteres dos itens de menu regular, negrito, itálico e sublinhado são atribuídas em tempo de execução, portanto, suas cadeias de caracteres estão vazias no arquivo de definição de recurso.


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



O procedimento de janela do aplicativo processa as mensagens envolvidas no uso de itens de menu extraídos pelo proprietário. O aplicativo usa a mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) para fazer o seguinte:

-   Defina o sinalizador **MF \_ OWNERDRAW** para os itens de menu.
-   Defina as cadeias de caracteres de texto para os itens de menu.
-   Obter identificadores das fontes usadas para desenhar os itens.
-   Obter os valores de cor de plano de fundo e texto para itens de menu selecionados.

As cadeias de caracteres de texto e os identificadores de fonte são armazenados em uma matriz de estruturas MYITEM definidas pelo aplicativo. A função GetAFont definida pelo aplicativo cria uma fonte que corresponde ao atributo de fonte especificado e retorna um identificador para a fonte. Os identificadores são destruídos durante o processamento da mensagem do [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .

Durante o processamento da mensagem do [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) , o exemplo obtém a largura e a altura de uma cadeia de caracteres de item de menu e copia esses valores na estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) . O sistema usa os valores de largura e altura para calcular o tamanho do menu.

Durante o processamento da mensagem do [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) , a cadeia de caracteres do item de menu é desenhada com a sala à esquerda ao lado da cadeia de caracteres do bitmap de marca de seleção. Se o usuário selecionar o item, o texto selecionado e as cores de plano de fundo serão usadas para desenhar o item.


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



### <a name="example-of-owner-drawn-menu-items"></a>Exemplo de itens de menu Owner-Drawn

O exemplo neste tópico usa itens de menu de desenho proprietário em um menu. Os itens de menu selecionam atributos de fonte específicos e o aplicativo exibe cada item de menu usando uma fonte que tem o atributo correspondente. Por exemplo, o item de menu **itálico** é exibido em uma fonte em itálico. O nome do menu de **caracteres** na barra de menus abre o menu.

A barra de menus e o menu suspenso são definidos inicialmente por um recurso de modelo de menu estendido. Como um modelo de menu não pode especificar itens desenhados pelo proprietário, o menu inicialmente contém quatro itens de menu de texto com as seguintes cadeias de caracteres: "regular", "negrito", "itálico" e "sublinhado". O procedimento de janela do aplicativo altera essas mensagens para itens desenhados pelo proprietário ao processar a mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) . Quando recebe a mensagem **de \_ criação do WM** , o procedimento de janela chama a função OnCreate definida pelo aplicativo, que executa as seguintes etapas para cada item de menu:

-   Aloca uma estrutura MYITEM definida pelo aplicativo.
-   Obtém o texto do item de menu e o salva na estrutura MYITEM definida pelo aplicativo.
-   Cria a fonte usada para exibir o item de menu e salva seu identificador na estrutura MYITEM definida pelo aplicativo.
-   Altera o tipo de item de menu para **MFT \_ OWNERDRAW** e salva um ponteiro para a estrutura MYITEM definida pelo aplicativo como dados de item.

Como um ponteiro para cada estrutura MYITEM definida pelo aplicativo é salvo como dados do item, ele é passado para o procedimento de janela em conjunto com as mensagens do [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) e do [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) para o item de menu correspondente. O ponteiro está contido no membro de todos os **dados** das estruturas [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) e [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .

Uma mensagem do [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) é enviada para cada item de menu desenhado pelo proprietário na primeira vez que é exibido. O aplicativo processa essa mensagem selecionando a fonte do item de menu em um contexto de dispositivo e, em seguida, determinando o espaço necessário para exibir o texto do item de menu nessa fonte. O texto do item de fonte e de menu são ambos especificados pela estrutura do item de menu `MYITEM` (a estrutura definida pelo aplicativo). O aplicativo determina o tamanho do texto usando a função [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) .

O procedimento de janela processa a mensagem do [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) exibindo o texto do item de menu na fonte apropriada. O texto do item de fonte e de menu são ambos especificados pela estrutura do item de menu `MYITEM` . O aplicativo seleciona as cores de texto e de plano de fundo apropriadas ao estado do item de menu.

O procedimento de janela processa a mensagem de [**\_ destruição do WM**](/windows/desktop/winmsg/wm-destroy) para destruir fontes e liberar memória. O aplicativo exclui a fonte e libera a estrutura MYITEM definida pelo aplicativo para cada item de menu.

A seguir estão as partes relevantes do arquivo de header do aplicativo.


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



A seguir estão as partes relevantes do procedimento de janela do aplicativo e suas funções associadas.


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



## <a name="using-custom-check-mark-bitmaps"></a>Usando bitmaps de marca de seleção personalizados

O sistema fornece um bitmap de marca de seleção padrão para exibição ao lado de um item de menu selecionado. Você pode personalizar um item de menu individual fornecendo um par de bitmaps para substituir o bitmap de marca de seleção padrão. O sistema exibe um bitmap quando o item é selecionado e o outro quando está claro. Esta seção descreve as etapas envolvidas na criação e no uso de bitmaps de marca de seleção personalizados.

-   [Criando bitmaps de marca de seleção personalizados](#creating-custom-check-mark-bitmaps)
-   [Associando bitmaps a um item de menu](#associating-bitmaps-with-a-menu-item)
-   [Definindo o atributo check-mark](#setting-the-check-mark-attribute)
-   [Simulando caixas de seleção em um menu](#simulating-check-boxes-in-a-menu)
-   [Exemplo de como usar bitmaps de marca de seleção personalizados](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a>Criando bitmaps de marca de seleção personalizados

Um bitmap de marca de seleção personalizado deve ter o mesmo tamanho que o bitmap de marca de seleção padrão. Você pode recuperar o tamanho da marca de seleção padrão do bitmap chamando a [**função GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) A palavra de ordem baixa do valor de retorno dessa função especifica a largura; a palavra de ordem alta especifica a altura.

Você pode usar recursos de bitmap para fornecer bitmaps de marca de seleção. No entanto, como o tamanho do bitmap necessário varia dependendo do tipo de exibição, talvez seja necessário reestilizar o bitmap em tempo de operação usando a [**função StretchBlt.**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) Dependendo do bitmap, a distorção causada peloizing pode produzir resultados inaceitáveis.

Em vez de usar um recurso de bitmap, você pode criar um bitmap em tempo de executar usando funções GDI.

**Para criar um bitmap em tempo de executar**

1.  Use a [**função CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) para criar um contexto de dispositivo compatível com aquele usado pela janela principal do aplicativo.

    O parâmetro *hdc* da função pode especificar **NULL** ou o valor de retorno da função. [**CreateCompatibleDC retorna**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) um handle para o contexto do dispositivo compatível.

2.  Use a [**função CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) para criar um bitmap compatível com a janela principal do aplicativo.

    Os parâmetros *nWidth* e *nHeight* dessa função definirão o tamanho do bitmap; eles devem especificar as informações de largura e altura retornadas pela [**função GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)

    > [!Note]  
    > Você também pode usar a [**função CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) para criar um bitmap monocromático.

     

3.  Use a [**função SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) para selecionar o bitmap no contexto do dispositivo compatível.
4.  Use funções de desenho GDI, como [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) e [**LineTo,**](/windows/desktop/api/wingdi/nf-wingdi-lineto)para desenhar uma imagem no bitmap ou usar funções como [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) e [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) para copiar uma imagem no bitmap.

Para obter mais informações, consulte [Bitmaps](/windows/desktop/gdi/bitmaps).

### <a name="associating-bitmaps-with-a-menu-item"></a>Associando bitmaps a um item de menu

Você associa um par de bitmaps de marca de seleção a um item de menu passando os alças dos bitmaps para a [**função SetMenuItemBitmaps.**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) O *parâmetro hBitmapUnchecked* identifica o bitmap claro e o parâmetro *hBitmapChecked* identifica o bitmap selecionado. Se você quiser remover uma ou ambas as marcas de seleção de um item de menu, poderá definir o parâmetro *hBitmapUnchecked* ou *hBitmapChecked* ou ambos como **NULL.**

### <a name="setting-the-check-mark-attribute"></a>Definindo o atributo check-mark

A [**função CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) define o atributo de marca de seleção de um item de menu como selecionado ou limpo. Você pode especificar o **valor MF \_ CHECKED** para definir o atributo de marca de seleção como selecionado e o **valor MF \_ UNCHECKED** para defini-lo como desmarcado.

Você também pode definir o estado de verificação de um item de menu usando a [**função SetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)

Às vezes, um grupo de itens de menu representa um conjunto de opções mutuamente exclusivas. Usando a [**função CheckMenuRadioItem,**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) você pode verificar um item de menu ao remover simultaneamente a marca de seleção de todos os outros itens de menu no grupo.

### <a name="simulating-check-boxes-in-a-menu"></a>Simulando caixas de seleção em um menu

Este tópico contém um exemplo que mostra como simular caixas de seleção em um menu. O exemplo contém um menu Caractere cujos itens permitem ao usuário definir os atributos em negrito, itálico e sublinhado da fonte atual. Quando um atributo de fonte está em vigor, uma marca de seleção é exibida na caixa de seleção ao lado do item de menu correspondente; caso contrário, uma caixa de seleção vazia será exibida ao lado do item.

O exemplo substitui o bitmap de marca de seleção padrão por dois bitmaps: um bitmap com uma caixa de seleção selecionada e o bitmap por uma caixa vazia. O bitmap da caixa de seleção selecionado é exibido ao lado do item de menu Negrito, Itálico ou Sublinhado quando o atributo de marca de seleção do item é definido como **MF \_ CHECKED.** O bitmap de caixa de seleção desmarcado ou vazio é exibido quando o atributo de marca de seleção é definido como **MF \_ UNCHECKED**.

O sistema fornece um bitmap predefinido que contém as imagens usadas para caixas de seleção e botões de rádio. O exemplo isola as caixas de seleção selecionadas e vazias, copia-as para dois bitmaps separados e, em seguida, os usa como os bitmaps selecionados e limpos para itens no **menu** Caractere.

Para recuperar um handle para o bitmap da caixa de seleção definido pelo sistema, o exemplo chama a função [**LoadBitmap,**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) especificando **NULL** como o parâmetro *hInstance* e **OBM \_ CHECKBOXES** como o parâmetro *lpBitmapName.* Como as imagens no bitmap têm o mesmo tamanho, o exemplo pode isolá-las dividindo a largura e a altura do bitmap pelo número de imagens em suas linhas e colunas.

A parte a seguir de um arquivo de definição de recurso mostra como os itens de menu **no** menu Caractere são definidos. Observe que nenhum atributo de fonte está em vigor inicialmente, portanto, o atributo de marca de seleção para o item **Regular** é definido como selecionado e, por padrão, o atributo de marca de seleção dos itens restantes está definido como limpo.


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



Aqui estão os conteúdos relevantes do arquivo de header do aplicativo.


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



O exemplo a seguir mostra as partes do procedimento de janela que criam os bitmaps de marca de seleção; definir o atributo de marca de seleção dos itens de menu **Negrito,** **Itálico** e **Sublinhado;** e destruir bitmaps de marca de seleção.


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



### <a name="example-of-using-custom-check-mark-bitmaps"></a>Exemplo de como usar bitmaps de marca de seleção personalizados

O exemplo neste tópico atribui bitmaps de marca de seleção personalizados a itens de menu em dois menus. Os itens de menu no primeiro menu especificam atributos de caractere: negrito, itálico e sublinhado. Cada item de menu pode ser selecionado ou limpo. Para esses itens de menu, o exemplo usa bitmaps de marca de seleção que se assemelham aos estados selecionados e limpos de um controle de caixa de seleção.

Os itens de menu no segundo menu especificam as configurações de alinhamento de parágrafo: esquerda, centralizada e direita. Somente um desses itens de menu é selecionado a qualquer momento. Para esses itens de menu, o exemplo usa bitmaps de marca de seleção que se assemelham aos estados selecionados e claros de um controle de botão de opção.

O procedimento de janela [**processa a mensagem WM \_ CREATE**](/windows/desktop/winmsg/wm-create) chamando a função OnCreate definida pelo aplicativo. `OnCreate`cria os quatro bitmaps de marca de seleção e os atribui a seus itens de menu apropriados usando a [**função SetMenuItemBitmaps.**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps)

Para criar cada bitmap, OnCreate chama a função CreateMenuBitmaps definida pelo aplicativo, especificando um ponteiro para uma função de desenho específica do bitmap. CreateMenuBitmaps cria um bitmap monocromático do tamanho necessário, seleciona-o em um contexto de dispositivo de memória e apaga a tela de fundo. Em seguida, ele chama a função de desenho especificada para preencher o primeiro plano.

As quatro funções de desenho definidas pelo aplicativo são DrawCheck, DrawUncheck, **DrawRadioCheck** e DrawRadioUncheck. Eles desenham um retângulo com um X, um retângulo vazio, uma elipse que contém uma elipse preenchida menor e uma elipse vazia, respectivamente.

O procedimento de janela processa [**a mensagem WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy) excluindo os bitmaps de marca de seleção. Ele recupera cada alça de bitmap usando a [**função GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) e, em seguida, passa um alça para a função .

Quando o usuário escolhe um item de menu, uma mensagem [**WM \_ COMMAND**](wm-command.md) é enviada para a janela do proprietário. Para itens de menu no menu **Caractere,** o procedimento de janela chama a função CheckCharacterItem definida pelo aplicativo. Para itens no menu **Parágrafo,** o procedimento de janela chama a função CheckParagraphItem definida pelo aplicativo.

Cada item no menu **Caractere** pode ser selecionado e limpo independentemente. Portanto, CheckCharacterItem simplesmente alterna o estado de verificação do item de menu especificado. Primeiro, a função chama a [**função GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) para obter o estado do item de menu atual. Em seguida, ele alterna o sinalizador **de estado \_ MFS CHECKED** e define o novo estado chamando a função [**SetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)

Ao contrário dos atributos de caractere, apenas um alinhamento de parágrafo pode ser selecionado por vez. Portanto, CheckParagraphItem verifica o item de menu especificado e remove a marca de seleção de todos os outros itens no menu. Para fazer isso, ele chama a [**função CheckMenuRadioItem.**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)

A seguir estão as partes relevantes do arquivo de header do aplicativo.


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



A seguir estão as partes relevantes do procedimento de janela do aplicativo e funções relacionadas.


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



 

 