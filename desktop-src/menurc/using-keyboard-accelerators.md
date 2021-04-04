---
title: Usando aceleradores de teclado
description: Esta seção aborda as tarefas associadas a aceleradores de teclado.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- entrada do usuário, aceleradores de teclado
- capturando entrada do usuário, aceleradores de teclado
- aceleradores de teclado
- aceleradores
- tabelas do acelerador
- recursos da tabela de aceleração
- função de acelerador de conversão
- WM_COMMAND mensagem
- WM_SYS mensagem de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2241ba828ea9e6be5e4bb0b7471adcc3130940ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007535"
---
# <a name="using-keyboard-accelerators"></a>Usando aceleradores de teclado

Esta seção aborda as tarefas associadas a aceleradores de teclado.

-   [Usando um recurso de tabela de acelerador](#using-an-accelerator-table-resource)
    -   [Criando o recurso de tabela de acelerador](#creating-the-accelerator-table-resource)
    -   [Carregando o recurso de tabela de acelerador](#loading-the-accelerator-table-resource)
    -   [Chamando a função acelerador de conversão](#calling-the-translate-accelerator-function)
    -   [Processando \_ mensagens de comando do WM](/windows)
    -   [Destruindo o recurso de tabela de acelerador](#destroying-the-accelerator-table-resource)
    -   [Criando aceleradores para atributos de fonte](#creating-accelerators-for-font-attributes)
-   [Usando uma tabela de acelerador criada em tempo de execução](#using-an-accelerator-table-created-at-run-time)
    -   [Criando uma tabela de acelerador de Run-Time](#creating-a-run-time-accelerator-table)
    -   [Aceleradores de processamento](#processing-accelerators)
    -   [Destruindo uma tabela de acelerador de Run-Time](#destroying-a-run-time-accelerator-table)
    -   [Criando aceleradores editáveis do usuário](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a>Usando um recurso de tabela de acelerador

A maneira mais comum de adicionar suporte a acelerador a um aplicativo é incluir um recurso de tabela de acelerador com o arquivo executável do aplicativo e, em seguida, carregar o recurso em tempo de execução.

Esta seção aborda os tópicos a seguir.

-   [Criando o recurso de tabela de acelerador](#creating-the-accelerator-table-resource)
-   [Carregando o recurso de tabela de acelerador](#loading-the-accelerator-table-resource)
-   [Chamando a função acelerador de conversão](#calling-the-translate-accelerator-function)
-   [Processando \_ mensagens de comando do WM](/windows)
-   [Destruindo o recurso de tabela de acelerador](#destroying-the-accelerator-table-resource)
-   [Criando aceleradores para atributos de fonte](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a>Criando o recurso de tabela de acelerador

Você cria um recurso de tabela de aceleração usando [a instrução](./accelerators-resource.md) Accelerators no arquivo de definição de recurso do aplicativo. Você deve atribuir um nome ou identificador de recurso à tabela de aceleração, preferencialmente, ao contrário de qualquer outro recurso. O sistema usa esse identificador para carregar o recurso em tempo de execução.

Cada acelerador que você define requer uma entrada separada na tabela do acelerador. Em cada entrada, você define o pressionamento de teclas (um código de caractere ASCII ou o código de chave virtual) que gera o acelerador e o identificador do acelerador. Você também deve especificar se o pressionamento de tecla deve ser usado em alguma combinação com as teclas ALT, SHIFT ou CTRL. Para obter mais informações sobre chaves virtuais, consulte [entrada de teclado](/windows/desktop/inputdev/keyboard-input).

Uma tecla ASCII é especificada colocando o caractere ASCII entre aspas duplas ou usando o valor inteiro do caractere em combinação com o sinalizador ASCII. Os exemplos a seguir mostram como definir aceleradores ASCII.

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

Um pressionamento de tecla de código de chave virtual é especificado de forma diferente, dependendo se a tecla de pressionamento é uma chave alfanumérica ou não alfanumérica. Para uma chave alfanumérica, a letra ou o número da chave, entre aspas duplas, é combinado com o sinalizador **VIRTKEY** . Para uma chave não alfanumérica, o código de chave virtual para a chave específica é combinado com o sinalizador **VIRTKEY** . Os exemplos a seguir mostram como definir aceleradores de código de chave virtual.

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

O exemplo a seguir mostra um recurso de tabela de aceleração que define aceleradores para operações de arquivo. O nome do recurso é *FileAccel*.

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

Se você quiser que o usuário pressione as teclas ALT, SHIFT ou CTRL em alguma combinação com o pressionamento de teclas do acelerador, especifique os sinalizadores ALT, SHIFT e CONTROL na definição do acelerador. Estes são alguns exemplos:

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

Por padrão, quando uma chave de acelerador corresponde a um item de menu, o sistema realça o item de menu. Você pode usar o sinalizador **inverter** para evitar o realce de um acelerador individual. O exemplo a seguir mostra como usar o sinalizador **Invert** :

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

Para definir os aceleradores que correspondem aos itens de menu em seu aplicativo, inclua os aceleradores no texto dos itens de menu. O exemplo a seguir mostra como incluir aceleradores no texto do item de menu em um arquivo de definição de recurso.

``` syntax
FilePopup MENU 
BEGIN 
    POPUP   "&File" 
    BEGIN 
        MENUITEM    "&New..",           IDM_NEW 
        MENUITEM    "&Open\tCtrl+F12",  IDM_OPEN 
        MENUITEM    "&Close\tAlt+F4"    IDM_CLOSE 
        MENUITEM    "&Save\tShift+F12", IDM_SAVE 
        MENUITEM    "Save &As...\tF12", IDM_SAVEAS 
    END 
END 
```

### <a name="loading-the-accelerator-table-resource"></a>Carregando o recurso de tabela de acelerador

Um aplicativo carrega um recurso de tabela de aceleração chamando a função [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) e especificando o identificador de instância para o aplicativo cujo arquivo executável contém o recurso e o nome ou identificador do recurso. O **LoadAccelerators** carrega a tabela de acelerador especificada na memória e retorna o identificador para a tabela de acelerador.

Um aplicativo pode carregar um recurso de tabela de aceleração a qualquer momento. Normalmente, um aplicativo de thread único carrega sua tabela de acelerador antes de inserir seu loop de mensagem principal. Um aplicativo que usa vários threads normalmente carrega o recurso de tabela de aceleração para um thread antes de inserir o loop de mensagem para o thread. Um aplicativo ou thread também pode usar várias tabelas de acelerador, cada uma associada a uma janela específica no aplicativo. Esse aplicativo carregaria a tabela de acelerador para a janela cada vez que o usuário ativou a janela. Para obter mais informações sobre threads, consulte [processos e threads](/windows/desktop/ProcThread/processes-and-threads).

### <a name="calling-the-translate-accelerator-function"></a>Chamando a função acelerador de conversão

Para os aceleradores de processo, o loop de mensagem de um aplicativo (ou de thread) deve conter uma chamada para a função [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) . **TranslateAccelerator** compara pressionamentos de teclas em uma tabela de acelerador e, se encontrar uma correspondência, converte os pressionamentos de tecla em uma mensagem de [**\_ comando do WM**](wm-command.md) (ou [**WM \_ SYSCOMMAND**](wm-syscommand.md)). Em seguida, a função envia a mensagem a um procedimento de janela. Os parâmetros da função **TranslateAccelerator** incluem o identificador para a janela que deve receber as mensagens de **\_ comando do WM** , o identificador para a tabela de acelerador usada para converter Aceleradores e um ponteiro para uma estrutura de [**msg**](/windows/win32/api/winuser/ns-winuser-msg) que contém uma mensagem da fila. O exemplo a seguir mostra como chamar **TranslateAccelerator** de dentro de um loop de mensagem.


```
MSG msg;
BOOL bRet;

while ( (bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1) 
    {
        // handle the error and possibly exit
    }
    else
    { 
        // Check for accelerator keystrokes. 
     
        if (!TranslateAccelerator( 
                hwndMain,      // handle to receiving window 
                haccel,        // handle to active accelerator table 
                &msg))         // message data 
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



### <a name="processing-wm_command-messages"></a>Processando \_ mensagens de comando do WM

Quando um acelerador é usado, a janela especificada na função [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) recebe um [**\_ comando do WM**](wm-command.md) ou uma mensagem do [**WM \_ SYSCOMMAND**](wm-syscommand.md) . A palavra de ordem inferior do parâmetro *wParam* contém o identificador do acelerador. O procedimento de janela examina o identificador para determinar a origem da mensagem **de \_ comando do WM** e processa a mensagem de acordo.

Normalmente, se um acelerador corresponder a um item de menu no aplicativo, o acelerador e o item de menu serão atribuídos ao mesmo identificador. Se você precisar saber se uma mensagem [**de \_ comando do WM**](wm-command.md) foi gerada por um acelerador ou por um item de menu, poderá examinar a palavra de ordem superior do parâmetro *wParam* . Se um acelerador gerar a mensagem, a palavra de ordem superior será 1; se um item de menu gerou a mensagem, a palavra de ordem superior será 0.

### <a name="destroying-the-accelerator-table-resource"></a>Destruindo o recurso de tabela de acelerador

O sistema destrói automaticamente os recursos da tabela de aceleradores carregados pela função [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) , removendo o recurso da memória depois que o aplicativo é fechado.

### <a name="creating-accelerators-for-font-attributes"></a>Criando aceleradores para atributos de fonte

O exemplo nesta seção mostra como executar as seguintes tarefas:

-   Crie um recurso de tabela de aceleração.
-   Carregue a tabela do acelerador em tempo de execução.
-   Converter aceleradores em um loop de mensagem.
-   Processar mensagens de [**\_ comando do WM**](wm-command.md) geradas pelos aceleradores.

Essas tarefas são demonstradas no contexto de um aplicativo que inclui um menu de **caracteres** e aceleradores correspondentes que permitem ao usuário selecionar atributos da fonte atual.

A seguinte parte de um arquivo de definição de recurso define o menu de **caracteres** e a tabela de acelerador associada. Observe que os itens de menu mostram os pressionamentos de teclas do acelerador e que cada acelerador tem o mesmo identificador de seu item de menu associado.


```
#include <windows.h> 
#include "acc.h" 
 
MainMenu MENU 
{ 
    POPUP   "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```



As seções a seguir do arquivo de origem do aplicativo mostram como implementar os aceleradores.


```
HWND hwndMain;      // handle to main window 
HANDLE hinstAcc;    // handle to application instance 
int WINAPI WinMain(HINSTANCE hinst, HINSTANCE hinstPrev, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg;            // application messages 
    BOOL bRet;          // for return value of GetMessage
    HACCEL haccel;      // handle to accelerator table 
 
    // Perform the initialization procedure. 
 
    // Create a main window for this application instance. 
 
    hwndMain = CreateWindowEx(0L, "MainWindowClass", 
        "Sample Application", WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, 
        hinst, NULL ); 
 
    // If a window cannot be created, return "failure." 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Make the window visible and update its client area. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Load the accelerator table. 
 
    haccel = LoadAccelerators(hinstAcc, "FontAccel"); 
    if (haccel == NULL) 
        HandleAccelErr(ERR_LOADING);     // application defined 
 
    // Get and dispatch messages until a WM_QUIT message is 
    // received. 
 
    while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        { 
            // Check for accelerator keystrokes. 
     
            if (!TranslateAccelerator( 
                    hwndMain,  // handle to receiving window 
                    haccel,    // handle to active accelerator table 
                    &msg))         // message data 
            {
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
        } 
    }
    return msg.wParam; 
} 
 
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    BYTE fbFontAttrib;        // array of font-attribute flags 
    static HMENU hmenu;       // handle to main menu 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Add a check mark to the Regular menu item to 
            // indicate that it is the default. 
 
            hmenu = GetMenu(hwndMain); 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the accelerator and menu commands. 
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // GetFontAttributes is an application-defined 
                    // function that sets the menu-item check marks 
                    // and returns the user-selected font attributes. 
 
                    fbFontAttrib = GetFontAttributes( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // SetFontAttributes is an application-defined 
                    // function that creates a font with the 
                    // user-specified attributes the font with 
                    // the main window's device context. 
 
                    SetFontAttributes(fbFontAttrib); 
                    break; 
 
                default: 
                    break; 
            } 
            break; 
 
            // Process other messages. 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="using-an-accelerator-table-created-at-run-time"></a>Usando uma tabela de acelerador criada em tempo de execução

Este tópico discute como usar tabelas de acelerador criadas em tempo de execução.

-   [Criando uma tabela de acelerador de Run-Time](#creating-a-run-time-accelerator-table)
-   [Aceleradores de processamento](#processing-accelerators)
-   [Destruindo uma tabela de acelerador de Run-Time](#destroying-a-run-time-accelerator-table)
-   [Criando aceleradores editáveis do usuário](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a>Criando uma tabela de acelerador de Run-Time

A primeira etapa na criação de uma tabela aceleradora em tempo de execução está preenchendo uma matriz de estruturas [**da aceleração extra**](/windows/win32/api/winuser/ns-winuser-accel) . Cada estrutura na matriz define um acelerador na tabela. A definição de um acelerador inclui seus sinalizadores, sua chave e seu identificador. A estrutura **da aceleração extra** tem o seguinte formato.

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

Você define um pressionamento de teclas do acelerador especificando um código de caractere ASCII ou um código de chave virtual no membro de **chave** da estrutura [**da aceleração extra**](/windows/win32/api/winuser/ns-winuser-accel) . Se você especificar um código de chave virtual, deverá primeiro incluir o sinalizador **FVIRTKEY** no membro **fVirt** ; caso contrário, o sistema interpretará o código como um código de caractere ASCII. Você pode incluir o sinalizador **FCONTROL**, **FALT** ou **FSHIFT** , ou todos os três, para combinar a tecla CTRL, ALT ou Shift com o pressionamento de teclas.

Para criar a tabela de acelerador, passe um ponteiro para a matriz de estruturas [**da aceleração extra**](/windows/win32/api/winuser/ns-winuser-accel) para a função [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) . **CreateAcceleratorTable** cria a tabela de acelerador e retorna o identificador para a tabela.

### <a name="processing-accelerators"></a>Aceleradores de processamento

O processo de carregar e chamar aceleradores fornecidos por uma tabela de acelerador criada em tempo de execução é o mesmo que processar os fornecidos por um recurso de tabela de aceleração. Para obter mais informações, consulte [carregando o recurso de tabela de acelerador](#loading-the-accelerator-table-resource) por meio do [processamento de mensagens de \_ comando do WM](/windows).

### <a name="destroying-a-run-time-accelerator-table"></a>Destruindo uma tabela de acelerador de Run-Time

O sistema destrói automaticamente as tabelas aceleradoras criadas em tempo de execução, removendo os recursos da memória depois que o aplicativo é fechado. Você pode destruir uma tabela de acelerador e removê-la da memória anteriormente passando o identificador da tabela para a função [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .

### <a name="creating-user-editable-accelerators"></a>Criando aceleradores editáveis do usuário

Este exemplo mostra como construir uma caixa de diálogo que permite ao usuário alterar o acelerador associado a um item de menu. A caixa de diálogo consiste em uma caixa de combinação que contém itens de menu, uma caixa de combinação que contém os nomes das chaves e as caixas de seleção para selecionar as teclas CTRL, ALT e SHIFT. A ilustração a seguir mostra a caixa de diálogo.

![caixa de diálogo com caixas de combinação e caixas de seleção](images/useredit.gif)

O exemplo a seguir mostra como a caixa de diálogo é definida no arquivo de definição de recurso.

``` syntax
EdAccelBox DIALOG 5, 17, 193, 114 
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Edit Accelerators" 
BEGIN 
    COMBOBOX        IDD_MENUITEMS, 10, 22, 52, 53, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    CONTROL         "Control", IDD_CNTRL, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 35, 40, 10 
    CONTROL         "Alt", IDD_ALT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 48, 40, 10 
    CONTROL         "Shift", IDD_SHIFT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 61, 40, 10 
    COMBOBOX        IDD_KEYSTROKES, 124, 22, 58, 58, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    PUSHBUTTON      "Ok", IDOK, 43, 92, 40, 14 
    PUSHBUTTON      "Cancel", IDCANCEL, 103, 92, 40, 14 
    LTEXT           "Select Item:", 101, 10, 12, 43, 8 
    LTEXT           "Select Keystroke:", 102, 123, 12, 60, 8 
END
```

A barra de menus do aplicativo contém um submenu de **caracteres** cujos itens têm aceleradores associados a eles.

``` syntax
MainMenu MENU 
{ 
    POPUP "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```

Os valores de item de menu para o modelo de menu são constantes definidas da seguinte maneira no arquivo de cabeçalho do aplicativo.

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

A caixa de diálogo usa uma matriz de estruturas VKEY definidas pelo aplicativo, cada uma contendo uma cadeia de caracteres de texto de pressionamento de tecla e uma cadeia de texto de acelerador. Quando a caixa de diálogo é criada, ela analisa a matriz e adiciona cada cadeia de caracteres de texto de pressionamento de tecla à caixa de combinação **selecionar pressionamentos** de teclas. Quando o usuário clica no botão **OK** , a caixa de diálogo procura a cadeia de caracteres de texto de pressionamento de teclas selecionada e recupera a cadeia de caracteres de texto de acelerador correspondente. A caixa de diálogo acrescenta a cadeia de texto Accelerator-Text ao texto do item de menu selecionado pelo usuário. O exemplo a seguir mostra a matriz de estruturas VKEY:


```
// VKey Lookup Support 
 
#define MAXKEYS 25 
 
typedef struct _VKEYS { 
    char *pKeyName; 
    char *pKeyString; 
} VKEYS; 
 
VKEYS vkeys[MAXKEYS] = { 
    "BkSp",     "Back Space", 
    "PgUp",     "Page Up", 
    "PgDn",     "Page Down", 
    "End",      "End", 
    "Home",     "Home", 
    "Lft",      "Left", 
    "Up",       "Up", 
    "Rgt",      "Right", 
    "Dn",       "Down", 
    "Ins",      "Insert", 
    "Del",      "Delete", 
    "Mult",     "Multiply", 
    "Add",      "Add", 
    "Sub",      "Subtract", 
    "DecPt",    "Decimal Point", 
    "Div",      "Divide", 
    "F2",       "F2", 
    "F3",       "F3", 
    "F5",       "F5", 
    "F6",       "F6", 
    "F7",       "F7", 
    "F8",       "F8", 
    "F9",       "F9", 
    "F11",      "F11", 
    "F12",      "F12" 
};
```



O procedimento de inicialização da caixa de diálogo preenche as caixas de combinação **selecionar item** e **selecionar pressionamentos de teclas** . Depois que o usuário seleciona um item de menu e um acelerador associado, a caixa de diálogo examina os controles na caixa de diálogo para obter a seleção do usuário, atualiza o texto do item de menu e cria uma nova tabela de acelerador que contém o novo acelerador definido pelo usuário. O exemplo a seguir mostra o procedimento da caixa de diálogo. Observe que você deve inicializar em seu procedimento de janela.


```
// Global variables 
 
HWND hwndMain;      // handle to main window 
HACCEL haccel;      // handle to accelerator table 
 
// Dialog-box procedure 
 
BOOL CALLBACK EdAccelProc(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    int nCurSel;            // index of list box item 
    UINT idItem;            // menu-item identifier 
    UINT uItemPos;          // menu-item position 
    UINT i, j = 0;          // loop counters 
    static UINT cItems;     // count of items in menu 
    char szTemp[32];        // temporary buffer 
    char szAccelText[32];   // buffer for accelerator text 
    char szKeyStroke[16];   // buffer for keystroke text 
    static char szItem[32]; // buffer for menu-item text 
    HWND hwndCtl;           // handle to control window 
    static HMENU hmenu;     // handle to "Character" menu 
    PCHAR pch, pch2;        // pointers for string copying 
    WORD wVKCode;           // accelerator virtual-key code 
    BYTE fAccelFlags;       // fVirt flags for ACCEL structure 
    LPACCEL lpaccelNew;     // pointer to new accelerator table 
    HACCEL haccelOld;       // handle to old accelerator table 
    int cAccelerators;      // number of accelerators in table 
    static BOOL fItemSelected = FALSE; // item selection flag 
    static BOOL fKeySelected = FALSE;  // key selection flag 
    HRESULT hr;
    INT numTCHAR;           // TCHARs in listbox text
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
 
            // Get the handle to the menu-item combo box. 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_MENUITEMS); 
 
            // Get the handle to the Character submenu and
            // count the number of items it has. In this example, 
            // the menu has position 0. You must alter this value 
            // if you add additional menus. 
            hmenu = GetSubMenu(GetMenu(hwndMain), 0); 
            cItems = GetMenuItemCount(hmenu); 
 
            // Get the text of each item, strip out the '&' and 
            // the accelerator text, and add the text to the 
            // menu-item combo box. 
 
            for (i = 0; i < cItems; i++) 
            { 
                if (!(GetMenuString(hmenu, i, szTemp, 
                        sizeof(szTemp)/sizeof(TCHAR), MF_BYPOSITION))) 
                    continue; 
                for (pch = szTemp, pch2 = szItem; *pch != '\0'; ) 
                { 
                    if (*pch != '&') 
                    { 
                        if (*pch == '\t') 
                        { 
                            *pch = '\0'; 
                            *pch2 = '\0'; 
                        } 
                        else *pch2++ = *pch++; 
                    } 
                    else pch++; 
                } 
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) szItem); 
            } 
 
            // Now fill the keystroke combo box with the list of 
            // keystrokes that will be allowed for accelerators. 
            // The list of keystrokes is in the application-defined 
            // structure called "vkeys". 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
            for (i = 0; i < MAXKEYS; i++) 
            {
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) vkeys[i].pKeyString); 
            }
 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDD_MENUITEMS: 
 
                    // The user must select an item from the combo 
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fItemSelected = TRUE; 
                    return 0; 
 
                case IDD_KEYSTROKES: 
 
                    // The user must select an item from the combo
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fKeySelected = TRUE; 
 
                    return 0; 
 
                case IDOK: 
 
                    // If the user has not selected a menu item 
                    // and a keystroke, display a reminder in a 
                    // message box. 
 
                    if (!fItemSelected || !fKeySelected) 
                    { 
                        MessageBox(hwndDlg, 
                            "Item or key not selected.", NULL, 
                            MB_OK); 
                        return 0; 
                    } 
 
                    // Determine whether the CTRL, ALT, and SHIFT 
                    // keys are selected. Concatenate the 
                    // appropriate strings to the accelerator- 
                    // text buffer, and set the appropriate 
                    // accelerator flags. 
 
                    szAccelText[0] = '\0'; 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_CNTRL); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Ctl+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FCONTROL; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_ALT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Alt+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FALT; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_SHIFT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    {
                        hr = StringCchCat(szAccelText, 32, "Shft+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FSHIFT; 
                    } 
 
                    // Get the selected keystroke, and look up the 
                    // accelerator text and the virtual-key code 
                    // for the keystroke in the vkeys structure. 
 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
                    nCurSel = (int) SendMessage(hwndCtl, 
                        CB_GETCURSEL, 0, 0);
                    numTCHAR = SendMessage(hwndCtl, CB_GETLBTEXTLEN, 
                        nCursel, 0); 
                    if (numTCHAR <= 15)
                        {                   
                        SendMessage(hwndCtl, CB_GETLBTEXT, 
                            nCurSel, (LONG) (LPSTR) szKeyStroke);
                        }
                    else
                        {
                        // TODO: writer error handler
                        }
                         
                    for (i = 0; i < MAXKEYS; i++) 
                    {
                    //
                    // lstrcmp requires that both parameters are
                    // null-terminated.
                    //
                        if(lstrcmp(vkeys[i].pKeyString, szKeyStroke) 
                            == 0) 
                        { 
                            hr = StringCchCopy(szKeyStroke, 16, vkeys[i].pKeyName);
                            if (FAILED(hr))
                            {
                            // TODO: write error handler
                            }
                            break; 
                        } 
                    } 
 
                    // Concatenate the keystroke text to the 
                    // "Ctl+","Alt+", or "Shft+" string. 
 
                        hr = StringCchCat(szAccelText, 32, szKeyStroke);
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
 
                    // Determine the position in the menu of the 
                    // selected menu item. Menu items in the 
                    // "Character" menu have positions 0,2,3, and 4.
                    // Note: the lstrcmp parameters must be
                    // null-terminated. 
 
                    if (lstrcmp(szItem, "Regular") == 0) 
                        uItemPos = 0; 
                    else if (lstrcmp(szItem, "Bold") == 0) 
                        uItemPos = 2; 
                    else if (lstrcmp(szItem, "Italic") == 0) 
                        uItemPos = 3; 
                    else if (lstrcmp(szItem, "Underline") == 0) 
                        uItemPos = 4; 
 
                    // Get the string that corresponds to the 
                    // selected item. 
 
                    GetMenuString(hmenu, uItemPos, szItem, 
                        sizeof(szItem)/sizeof(TCHAR), MF_BYPOSITION); 
 
                    // Append the new accelerator text to the 
                    // menu-item text. 
 
                    for (pch = szItem; *pch != '\t'; pch++); 
                        ++pch; 
 
                    for (pch2 = szAccelText; *pch2 != '\0'; pch2++) 
                        *pch++ = *pch2; 
                    *pch = '\0'; 
 
                    // Modify the menu item to reflect the new 
                    // accelerator text. 
 
                    idItem = GetMenuItemID(hmenu, uItemPos); 
                    ModifyMenu(hmenu, idItem, MF_BYCOMMAND | 
                        MF_STRING, idItem, szItem); 
 
                    // Reset the selection flags. 
 
                    fItemSelected = FALSE; 
                    fKeySelected = FALSE; 
 
                    // Save the current accelerator table. 
 
                    haccelOld = haccel; 
 
                    // Count the number of entries in the current 
                    // table, allocate a buffer for the table, and 
                    // then copy the table into the buffer. 
 
                    cAccelerators = CopyAcceleratorTable( 
                        haccelOld, NULL, 0); 
                    lpaccelNew = (LPACCEL) LocalAlloc(LPTR, 
                        cAccelerators * sizeof(ACCEL)); 
 
                    if (lpaccelNew != NULL) 
                    {
                        CopyAcceleratorTable(haccel, lpaccelNew, 
                            cAccelerators); 
                    }
 
                    // Find the accelerator that the user modified 
                    // and change its flags and virtual-key code 
                    // as appropriate. 
 
                    for (i = 0; i < (UINT) cAccelerators; i++) 
                    { 
                           if (lpaccelNew[i].cmd == (WORD) idItem)
                        {
                            lpaccelNew[i].fVirt = fAccelFlags; 
                            lpaccelNew[i].key = wVKCode; 
                        }
                    } 
 
                    // Create the new accelerator table, and 
                    // destroy the old one. 
 
                    DestroyAcceleratorTable(haccelOld); 
                    haccel = CreateAcceleratorTable(lpaccelNew, 
                        cAccelerators); 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hwndDlg, TRUE); 
                    return 0; 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    break; 
            } 
        default: 
            break; 
    } 
    return FALSE; 
}
```



 

 