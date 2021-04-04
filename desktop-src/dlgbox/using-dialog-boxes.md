---
title: Usando caixas de diálogo
description: Use caixas de diálogo para exibir informações e solicitar entrada do usuário.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Interface do usuário do Windows, janelas
- Interface do usuário do Windows, caixas de diálogo
- janelas, caixas de diálogo
- caixas de diálogo, sobre
- caixas de diálogo, exibindo
- caixas de diálogo modais
- caixas de diálogo sem modo
- caixas de diálogo, modal
- caixas de diálogo, sem janela restrita
- caixas de diálogo, inicializando
- modelos de caixa de diálogo
- caixas de diálogo, modelos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21da47d7d59f4cadc21314566bce41a9ef3456a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007977"
---
# <a name="using-dialog-boxes"></a>Usando caixas de diálogo

Use caixas de diálogo para exibir informações e solicitar entrada do usuário. O aplicativo carrega e inicializa a caixa de diálogo, processa a entrada do usuário e destrói a caixa de diálogo quando o usuário conclui a tarefa. O processo de tratamento de caixas de diálogo varia, dependendo se a caixa de diálogo é modal ou sem janela restrita. Uma caixa de diálogo modal exige que o usuário feche a caixa de diálogo antes de ativar outra janela no aplicativo. No entanto, o usuário pode ativar o Windows em diferentes aplicativos. Uma caixa de diálogo sem janela restrita não requer uma resposta imediata do usuário. É semelhante a uma janela principal que contém controles.

As seções a seguir discutem como usar os dois tipos de caixas de diálogo.

-   [Exibindo uma caixa de mensagem](#displaying-a-message-box)
-   [Criando uma caixa de diálogo modal](#creating-a-modal-dialog-box)
-   [Criando uma caixa de diálogo sem janela restrita](#creating-a-modeless-dialog-box)
-   [Inicializando uma caixa de diálogo](#initializing-a-dialog-box)
-   [Criando um modelo na memória](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a>Exibindo uma caixa de mensagem

A forma mais simples da caixa de diálogo modal é a caixa de mensagem. A maioria dos aplicativos usa caixas de mensagens para avisar o usuário sobre erros e solicitar instruções sobre como proceder após a ocorrência de um erro. Você cria uma caixa de mensagem usando a função [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) ou [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) , especificando a mensagem e o número e o tipo de botões a serem exibidos. O sistema cria uma caixa de diálogo modal, fornecendo seu próprio modelo e procedimento de caixa de diálogo. Depois que o usuário fecha a caixa de mensagem, **MessageBox** ou **MessageBoxEx** retorna um valor que identifica o botão escolhido pelo usuário para fechar a caixa de mensagem.

No exemplo a seguir, o aplicativo exibe uma caixa de mensagem que solicita ao usuário uma ação após a ocorrência de uma condição de erro. A caixa de mensagem exibe a mensagem que descreve a condição de erro e como resolvê-la. O estilo **MB \_ YesNo** direciona a [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) para fornecer dois botões com os quais o usuário pode escolher como proceder:


```
int DisplayConfirmSaveAsMessageBox()
{
    int msgboxID = MessageBox(
        NULL,
        L"temp.txt already exists.\nDo you want to replace it?",
        L"Confirm Save As",
        MB_ICONEXCLAMATION | MB_YESNO
    );

    if (msgboxID == IDYES)
    {
        // TODO: add code
    }

    return msgboxID;    
}
```



A imagem a seguir mostra a saída do exemplo de código anterior:

![caixa de mensagem](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a>Criando uma caixa de diálogo modal

Você cria uma caixa de diálogo modal usando a função [**caixa**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) . Você deve especificar o identificador ou o nome de um recurso de modelo de caixa de diálogo e um ponteiro para o procedimento da caixa de diálogo. A função **caixa** carrega o modelo, exibe a caixa de diálogo e processa todas as entradas do usuário até que o usuário feche a caixa de diálogo.

No exemplo a seguir, o aplicativo exibe uma caixa de diálogo modal quando o usuário clica em **Excluir item** de um menu de aplicativo. A caixa de diálogo contém um controle de edição (no qual o usuário insere o nome de um item) e os botões **OK** e **Cancelar** . Os identificadores de controle para esses controles são ID \_ ItemName, IDOK e IDCANCEL, respectivamente.

A primeira parte do exemplo consiste nas instruções que criam a caixa de diálogo modal. Essas instruções, no procedimento de janela da janela principal do aplicativo, criam a caixa de diálogo quando o sistema recebe uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) que tem o \_ identificador de menu DELETEITEM da IDM. A segunda parte do exemplo é o procedimento da caixa de diálogo, que recupera o conteúdo do controle de edição e fecha a caixa de diálogo após receber uma mensagem de **\_ comando do WM** .

As instruções a seguir criam a caixa de diálogo modal. O modelo de caixa de diálogo é um recurso no arquivo executável do aplicativo e tem o identificador de recurso DLG \_ DELETEITEM.


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_DELETEITEM: 
            if (DialogBox(hinst, 
                          MAKEINTRESOURCE(DLG_DELETEITEM), 
                          hwnd, 
                          (DLGPROC)DeleteItemProc)==IDOK) 
            {
                // Complete the command; szItemName contains the 
                // name of the item to delete. 
            }

            else 
            {
                // Cancel the command. 
            } 
            break; 
    } 
    return 0L; 
```



Neste exemplo, o aplicativo especifica sua janela principal como a janela do proprietário da caixa de diálogo. Quando o sistema exibe inicialmente a caixa de diálogo, sua posição é relativa ao canto superior esquerdo da área do cliente da janela do proprietário. O aplicativo usa o valor de retorno de [**caixa**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) para determinar se deseja prosseguir com a operação ou cancelá-lo. As instruções a seguir definem o procedimento da caixa de diálogo.


```
char szItemName[80]; // receives name of item to delete. 
 
BOOL CALLBACK DeleteItemProc(HWND hwndDlg, 
                             UINT message, 
                             WPARAM wParam, 
                             LPARAM lParam) 
{ 
    switch (message) 
    { 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    if (!GetDlgItemText(hwndDlg, ID_ITEMNAME, szItemName, 80)) 
                         *szItemName=0; 
 
                    // Fall through. 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, wParam); 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



Neste exemplo, o procedimento usa [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) para recuperar o texto atual do controle de edição identificado pela ID \_ ItemName. Em seguida, o procedimento chama a função [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) para definir o valor de retorno da caixa de diálogo como IDOK ou IDCANCEL, dependendo da mensagem recebida e iniciar o processo de fechamento da caixa de diálogo. Os identificadores IDOK e IDCANCEL correspondem aos botões **OK** e **Cancelar** . Depois que o procedimento chama **EndDialog**, o sistema envia mensagens adicionais ao procedimento para destruir a caixa de diálogo e retorna o valor de retorno da caixa de diálogo para a função que criou a caixa de diálogo.

## <a name="creating-a-modeless-dialog-box"></a>Criando uma caixa de diálogo sem janela restrita

Você cria uma caixa de diálogo sem janela restrita usando a função [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) , especificando o identificador ou o nome de um recurso de modelo de caixa de diálogo e um ponteiro para o procedimento da caixa de diálogo. **CreateDialog** carrega o modelo, cria a caixa de diálogo e, opcionalmente, exibe-o. Seu aplicativo é responsável por recuperar e expedir mensagens de entrada do usuário para o procedimento da caixa de diálogo.

No exemplo a seguir, o aplicativo exibe uma caixa de diálogo sem janela restrita — se ela ainda não estiver exibida — quando o usuário clicar em **ir para** de um menu de aplicativo. A caixa de diálogo contém um controle de edição, uma caixa de seleção e os botões **OK** e **Cancelar** . O modelo de caixa de diálogo é um recurso no arquivo executável do aplicativo e tem o identificador de recurso DLG \_ goto. O usuário insere um número de linha no controle de edição e marca a caixa de seleção para especificar que o número de linha é relativo à linha atual. Os identificadores de controle são ID \_ line, ID \_ ABSREL, IDOK e IDCANCEL.

As instruções na primeira parte do exemplo criam a caixa de diálogo sem janela restrita. Essas instruções, no procedimento de janela da janela principal do aplicativo, criam a caixa de diálogo quando o procedimento de janela recebe uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) que tem o identificador de menu do IDM \_ goto, mas somente se a variável global ainda não contiver um identificador válido. A segunda parte do exemplo é o loop de mensagem principal do aplicativo. O loop inclui a função [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) para garantir que o usuário possa usar a interface de teclado da caixa de diálogo nesta caixa de diálogo sem janela restrita. A terceira parte do exemplo é o procedimento da caixa de diálogo. O procedimento recupera o conteúdo do controle de edição e a caixa de seleção quando o usuário clica no botão **OK** . O procedimento destrói a caixa de diálogo quando o usuário clica no botão **Cancelar** .


```
HWND hwndGoto = NULL;  // Window handle of dialog box 
                
...

case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_GOTO: 
            if (!IsWindow(hwndGoto)) 
            { 
                hwndGoto = CreateDialog(hinst, 
                                        MAKEINTRESOURCE(DLG_GOTO), 
                                        hwnd, 
                                        (DLGPROC)GoToProc); 
                ShowWindow(hwndGoto, SW_SHOW); 
            } 
            break; 
    } 
    return 0L; 
```



Nas instruções anteriores, [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) só será chamado se não `hwndGoto` contiver um identificador de janela válido. Isso garante que o aplicativo não exiba duas caixas de diálogo ao mesmo tempo. Para dar suporte a esse método de verificação, o procedimento de caixa de diálogo deve definir como **NULL** quando destrói a caixa de diálogo.

O loop de mensagem para um aplicativo consiste nas instruções a seguir.


```
BOOL bRet;

while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0) 
{ 
    if (bRet == -1)
    {
        // Handle the error and possibly exit
    }
    else if (!IsWindow(hwndGoto) || !IsDialogMessage(hwndGoto, &msg)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
} 
```



O loop verifica a validade do identificador de janela para a caixa de diálogo e só chama a função [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) se o identificador for válido. **IsDialogMessage** só processará a mensagem se ela pertencer à caixa de diálogo. Caso contrário, ele retornará **false** e o loop expedirá a mensagem para a janela apropriada.

As instruções a seguir definem o procedimento da caixa de diálogo.


```
int iLine;             // Receives line number.
BOOL fRelative;        // Receives check box status. 
 
BOOL CALLBACK GoToProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    BOOL fError; 
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
            CheckDlgButton(hwndDlg, ID_ABSREL, fRelative); 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    fRelative = IsDlgButtonChecked(hwndDlg, ID_ABSREL); 
                    iLine = GetDlgItemInt(hwndDlg, ID_LINE, &fError, fRelative); 
                    if (fError) 
                    { 
                        MessageBox(hwndDlg, SZINVALIDNUMBER, SZGOTOERR, MB_OK); 
                        SendDlgItemMessage(hwndDlg, ID_LINE, EM_SETSEL, 0, -1L); 
                    } 
                    else 

                    // Notify the owner window to carry out the task. 
 
                    return TRUE; 
 
                case IDCANCEL: 
                    DestroyWindow(hwndDlg); 
                    hwndGoto = NULL; 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



Nas instruções anteriores, o procedimento processa as mensagens de [**\_ comando**](/windows/desktop/menurc/wm-command) do [**WM \_ INITDIALOG**](wm-initdialog.md) e do WM. Durante o processamento do **WM \_ INITDIALOG** , o procedimento Inicializa a caixa de seleção passando o valor atual da variável global para [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx). Em seguida, o procedimento retorna **true** para instruir o sistema a definir o foco de entrada padrão.

Durante o processamento de [**\_ comandos do WM**](/windows/desktop/menurc/wm-command) , o procedimento fecha a caixa de diálogo somente se o usuário clicar no botão **Cancelar** , ou seja, o botão que tem o identificador IDCANCEL. O procedimento deve chamar [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para fechar uma caixa de diálogo sem janela restrita. Observe que o procedimento também define a variável como **NULL** para garantir que outras instruções que dependem dessa variável operem corretamente.

Se o usuário clicar no botão **OK** , o procedimento recuperará o estado atual da caixa de seleção e o atribuirá à variável **fRelative** . Em seguida, ele usa a variável para recuperar o número de linha do controle de edição. [**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) converte o texto no controle de edição em um número inteiro. O valor de **fRelative** determina se a função interpreta o número como um valor assinado ou sem sinal. Se o texto do controle de edição não for um número válido, **GetDlgItemInt** definirá o valor da variável **referenciadora** como diferente de zero. O procedimento verifica esse valor para determinar se uma mensagem de erro deve ser exibida ou executar a tarefa. No caso de um erro, o procedimento da caixa de diálogo envia uma mensagem para o controle de edição, direcionando-o para selecionar o texto no controle para que o usuário possa substituí-lo facilmente. Se **GetDlgItemInt** não retornar um erro, o procedimento poderá executar a tarefa solicitada ou enviar uma mensagem para a janela do proprietário, direcionando-a para realizar a operação.

## <a name="initializing-a-dialog-box"></a>Inicializando uma caixa de diálogo

Você inicializa a caixa de diálogo e seu conteúdo durante o processamento da mensagem [**\_ INITDIALOG do WM**](wm-initdialog.md) . A tarefa mais comum é inicializar os controles para refletir as configurações da caixa de diálogo atual. Outra tarefa comum é centralizar uma caixa de diálogo na tela ou dentro de sua janela de proprietário. Uma tarefa útil para algumas caixas de diálogo é definir o foco de entrada para um controle especificado em vez de aceitar o foco de entrada padrão.

No exemplo a seguir, o procedimento da caixa de diálogo centraliza a caixa de diálogo e define o foco de entrada durante o processamento da mensagem [**\_ INITDIALOG do WM**](wm-initdialog.md) . Para centralizar a caixa de diálogo, o procedimento recupera os retângulos da janela para a caixa de diálogo e a janela do proprietário e calcula uma nova posição para a caixa de diálogo. Para definir o foco de entrada, o procedimento verifica o parâmetro *wParam* para determinar o identificador do foco de entrada padrão.


```
HWND hwndOwner; 
RECT rc, rcDlg, rcOwner; 

....
 
case WM_INITDIALOG: 

    // Get the owner window and dialog box rectangles. 

    if ((hwndOwner = GetParent(hwndDlg)) == NULL) 
    {
        hwndOwner = GetDesktopWindow(); 
    }

    GetWindowRect(hwndOwner, &rcOwner); 
    GetWindowRect(hwndDlg, &rcDlg); 
    CopyRect(&rc, &rcOwner); 

    // Offset the owner and dialog box rectangles so that right and bottom 
    // values represent the width and height, and then offset the owner again 
    // to discard space taken up by the dialog box. 

    OffsetRect(&rcDlg, -rcDlg.left, -rcDlg.top); 
    OffsetRect(&rc, -rc.left, -rc.top); 
    OffsetRect(&rc, -rcDlg.right, -rcDlg.bottom); 

    // The new position is the sum of half the remaining space and the owner's 
    // original position. 

    SetWindowPos(hwndDlg, 
                 HWND_TOP, 
                 rcOwner.left + (rc.right / 2), 
                 rcOwner.top + (rc.bottom / 2), 
                 0, 0,          // Ignores size arguments. 
                 SWP_NOSIZE); 

    if (GetDlgCtrlID((HWND) wParam) != ID_ITEMNAME) 
    { 
        SetFocus(GetDlgItem(hwndDlg, ID_ITEMNAME)); 
        return FALSE; 
    } 
    return TRUE; 
```



Nas instruções anteriores, o procedimento usa a função [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) para recuperar o identificador de janela do proprietário para uma caixa de diálogo. A função retorna o identificador de janela do proprietário para caixas de diálogo e o identificador da janela pai para janelas filhas. Como um aplicativo pode criar uma caixa de diálogo que não tem proprietário, o procedimento verifica o identificador retornado e usa a função [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) para recuperar o identificador da janela da área de trabalho, se necessário. Depois de calcular a nova posição, o procedimento usa a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para mover a caixa de diálogo, especificando o \_ valor superior de HWND para garantir que a caixa de diálogo permaneça na parte superior da janela do proprietário.

Antes de definir o foco de entrada, o procedimento verifica o identificador de controle do foco de entrada padrão. O sistema passa o identificador de janela do foco de entrada padrão no parâmetro *wParam* . A função [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) retorna o identificador do controle identificado pelo identificador de janela. Se o identificador não corresponder ao identificador correto, o procedimento usará a função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) para definir o foco de entrada. A função [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) é necessária para recuperar o identificador de janela do controle desejado.

## <a name="creating-a-template-in-memory"></a>Criando um modelo na memória

Às vezes, os aplicativos adaptam ou modificam o conteúdo das caixas de diálogo dependendo do estado atual dos dados que estão sendo processados. Nesses casos, não é prático fornecer todos os modelos de caixa de diálogo possíveis como recursos no arquivo executável do aplicativo. Mas a criação de modelos na memória proporciona ao aplicativo mais flexibilidade para se adaptar a qualquer circunstância.

No exemplo a seguir, o aplicativo cria um modelo na memória para uma caixa de diálogo modal que contém um botão de mensagem e **OK** e **ajuda** .

Em um modelo de caixa de diálogo, todas as cadeias de caracteres, como a caixa de diálogo e os títulos dos botões, devem ser cadeias Unicode. Este exemplo usa a função [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) para gerar essas cadeias de caracteres Unicode.

As estruturas [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) em um modelo de caixa de diálogo devem ser alinhadas em limites **DWORD** . Para alinhar essas estruturas, este exemplo usa uma rotina auxiliar que usa um ponteiro de entrada e retorna o ponteiro mais próximo que está alinhado em um limite **DWORD** .


```
#define ID_HELP   150
#define ID_TEXT   200

LPWORD lpwAlign(LPWORD lpIn)
{
    ULONG ul;

    ul = (ULONG)lpIn;
    ul ++;
    ul >>=1;
    ul <<=1;
    return (LPWORD)ul;
}

LRESULT DisplayMyMessage(HINSTANCE hinst, HWND hwndOwner, LPSTR lpszMessage)
{
    HGLOBAL hgbl;
    LPDLGTEMPLATE lpdt;
    LPDLGITEMTEMPLATE lpdit;
    LPWORD lpw;
    LPWSTR lpwsz;
    LRESULT ret;
    int nchar;

    hgbl = GlobalAlloc(GMEM_ZEROINIT, 1024);
    if (!hgbl)
        return -1;
 
    lpdt = (LPDLGTEMPLATE)GlobalLock(hgbl);
 
    // Define a dialog box.
 
    lpdt->style = WS_POPUP | WS_BORDER | WS_SYSMENU | DS_MODALFRAME | WS_CAPTION;
    lpdt->cdit = 3;         // Number of controls
    lpdt->x  = 10;  lpdt->y  = 10;
    lpdt->cx = 100; lpdt->cy = 100;

    lpw = (LPWORD)(lpdt + 1);
    *lpw++ = 0;             // No menu
    *lpw++ = 0;             // Predefined dialog box class (by default)

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "My Dialog", -1, lpwsz, 50);
    lpw += nchar;

    //-----------------------
    // Define an OK button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 70;
    lpdit->cx = 80; lpdit->cy = 20;
    lpdit->id = IDOK;       // OK button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_DEFPUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "OK", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a Help button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 55; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_HELP;    // Help button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_PUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class atom

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "Help", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a static text control.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_TEXT;    // Text identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | SS_LEFT;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0082;        // Static class

    for (lpwsz = (LPWSTR)lpw; *lpwsz++ = (WCHAR)*lpszMessage++;);
    lpw = (LPWORD)lpwsz;
    *lpw++ = 0;             // No creation data

    GlobalUnlock(hgbl); 
    ret = DialogBoxIndirect(hinst, 
                           (LPDLGTEMPLATE)hgbl, 
                           hwndOwner, 
                           (DLGPROC)DialogProc); 
    GlobalFree(hgbl); 
    return ret; 
}
```



 

 