---
title: Como criar um Owner-Drawn caixa de combinação
description: Este tópico demonstra como usar uma caixa de combinação de desenho proprietário.
ms.assetid: D866DE82-9734-4E8A-A366-5870C25B7C7B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5355dd33fe0067165308e9e6e5885b76edbe7ceb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008399"
---
# <a name="how-to-create-an-owner-drawn-combo-box"></a>Como criar um Owner-Drawn caixa de combinação

Este tópico demonstra como usar uma caixa de combinação de desenho proprietário. O exemplo de código C++ usa uma caixa de listagem suspensa desenhada pelo proprietário para exibir os quatro grupos de alimentos, cada um representado por um bitmap e um nome. Selecionar um grupo de alimentos faz com que o pratos nesse grupo apareça em uma lista.

![captura de tela mostrando uma caixa de diálogo com uma caixa de listagem e uma caixa de listagem suspensa expandida mostrando um ícone e um rótulo para cada item](images/cscbx-01.png)

A caixa de diálogo também contém uma caixa de listagem (IDLIST) e dois botões: **OK** (IDOK) e **Cancel** (IDCANCEL). As constantes IDOK e IDCANCEL são definidas pelos arquivos de cabeçalho do SDK. A constante IDLIST é definida no arquivo de cabeçalho do aplicativo, assim como o identificador de controle, IDCOMBO. Para obter mais informações sobre caixas de diálogo, consulte [caixas de diálogo](/windows/desktop/dlgbox/dialog-boxes).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="step-1-create-the-owner-drawn-dialog-box"></a>Etapa 1: criar a caixa de diálogo Owner-Drawn

O exemplo de código usa a função [**caixa**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) para criar uma caixa de diálogo modal. O modelo de caixa de diálogo, IDD \_ SQMEAL, define os estilos de janela, os botões e os identificadores de controle da caixa de combinação. A caixa de combinação neste exemplo usa os estilos de [**CBS \_ DROPDOWNLIST**](combo-box-styles.md), [**CBS \_ OwnerDrawFixed**](combo-box-styles.md), CBS [**\_ Sort**](combo-box-styles.md), [**CBS \_ HASSTRINGS**](combo-box-styles.md), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)e [**WS \_ TabStop**](/windows/desktop/winmsg/window-styles) .


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a>Etapa 2: processar as mensagens do WM \_ INITDIALOG e do WM \_ Destroy em uma caixa de diálogo.

Quando você usa uma caixa de combinação em uma caixa de diálogo, geralmente responde a uma mensagem do [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) inicializando a caixa de combinação. O aplicativo carrega os bitmaps usados para a caixa de combinação desenhada pelo proprietário e, em seguida, chama a função definida pelo aplicativo `InitGroupList` para inicializar a caixa de combinação. Ele também seleciona o primeiro item de lista na caixa de combinação e, em seguida, chama a função definida pelo aplicativo `InitFoodList` para inicializar a caixa de listagem.

No exemplo, a caixa de combinação desenhada pelo proprietário é uma caixa de listagem suspensa que contém os nomes de cada um dos quatro grupos de alimentos. `InitGroupList` Adiciona o nome de cada grupo de alimentos e usa a mensagem [**CB \_ SETITEMDATA**](cb-setitemdata.md) para associar um identificador de bitmap a cada item de lista que identifica um grupo de alimentos.

A caixa de listagem no exemplo contém os nomes de pratos no grupo de alimentos selecionado. **InitFoodList** redefine o conteúdo da caixa de listagem e, em seguida, adiciona os nomes da seleção de alimentos atual na caixa de listagem suspensa grupo de alimentos atual.


```C++
case WM_INITDIALOG:

    // Call an application-defined function to load bitmap resources.
    if (!LoadIconBitmaps())
    {
        EndDialog(hDlg, -1);
        break;
    }

    // Initialize the food groups combo box and select the first item.
    InitGroupList(hDlg);
    SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

    // Initialize the food list box and select the first item.
    InitFoodList(hDlg);
    SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

     return (INT_PTR)TRUE;
```



Quando recebe a mensagem do [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , o aplicativo exclui os bitmaps na caixa de combinação do desenho proprietário.


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a>Etapa 3: processar a mensagem do WM \_ MEASUREITEM.

Uma caixa de combinação desenhada pelo proprietário envia a mensagem do [**WM \_ MEASUREITEM**](wm-measureitem.md) para sua janela pai ou procedimento de caixa de diálogo para que o aplicativo possa definir as dimensões de cada item de lista. Como a caixa de combinação de exemplo tem o estilo [**\_ OwnerDrawFixed do CBS**](combo-box-styles.md) , o sistema envia a mensagem do **WM \_ MEASUREITEM** apenas uma vez. As caixas de combinação com o estilo [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) enviam uma mensagem do **WM \_ MEASUREITEM** para cada item de lista.

O parâmetro *lParam* é um ponteiro para uma estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que identifica o controle e o item de lista. Ele também contém as dimensões padrão do item de lista. O exemplo modifica o membro da estrutura **ItemHeight** para garantir que os itens da lista sejam altos o suficiente para acomodar os bitmaps do grupo de alimentos.


```C++
case WM_MEASUREITEM:
    {
    // Set the height of the items in the food groups combo box.
    LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

    if (lpmis->itemHeight < CY_BITMAP + 2)
        lpmis->itemHeight = CY_BITMAP + 2;

    break;
    }
```



### <a name="step-4-process-the-wm_drawitem-message"></a>Etapa 4: processar a mensagem do WM \_ DRAWITEM.

Uma caixa de combinação desenhada pelo proprietário envia a mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) para sua janela pai ou procedimento de caixa de diálogo cada vez que o aplicativo deve redesenhar um item de lista. O parâmetro *lParam* é um ponteiro para uma estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que identifica o controle e o item de lista. Ele também contém as informações necessárias para pintar o item.

O aplicativo de exemplo exibe o texto do item de lista e o bitmap associado ao grupo de alimentos. Se o item tiver o foco, ele também desenha um retângulo de foco. Antes de exibir o texto, o exemplo define as cores de primeiro e segundo plano, com base no item selecionado. Como a caixa de combinação tem o estilo [**\_ HASSTRINGS do CBS**](combo-box-styles.md) , a caixa de combinação mantém o texto para cada item de lista que pode ser recuperado usando a mensagem [**CB \_ GETLBTEXT**](cb-getlbtext.md) .

Os bitmaps usados para o item de lista dependem do grupo de alimentos. `InitGroupList` usa a [**mensagem \_ SETITEMDATA CB**](cb-setitemdata.md) para associar um identificador de bitmap a cada item de lista. O procedimento de janela recupera o identificador de bitmap do membro de **dados** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . O sistema usa dois bitmaps para cada símbolo de grupo de alimentos: um bitmap monocromático com a operação de varredura SRCAND para apagar a região irregular por trás da imagem e um bitmap de cor com a operação de varredura SRCPAINT para pintar a imagem.


```C++
case WM_DRAWITEM:
    {
    COLORREF clrBackground;
    COLORREF clrForeground;
    TEXTMETRIC tm;
    int x;
    int y;
    HRESULT hr;
    size_t cch;

    LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
       
    if (lpdis->itemID == -1) // Empty item)
        break;

    // Get the food icon from the item data.
    hbmIcon = (HBITMAP) lpdis->itemData;

    // The colors depend on whether the item is selected.
    clrForeground = SetTextColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

    clrBackground = SetBkColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHT : COLOR_WINDOW));

    // Calculate the vertical and horizontal position.
    GetTextMetrics(lpdis->hDC, &tm);
    y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
    x = LOWORD(GetDialogBaseUnits()) / 4;

    // Get and display the text for the list item.
    SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
        lpdis->itemID, (LPARAM) achTemp);

    hr = StringCchLength(achTemp, 256, &cch);
    if (FAILED(hr))
    {
        // TODO: Write error handler.
    }

    ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
        ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
        achTemp, (UINT)cch, NULL);

    // Restore the previous colors.
    SetTextColor(lpdis->hDC, clrForeground);
    SetBkColor(lpdis->hDC, clrBackground);
    
    //  Draw the food icon for the item. 
    HDC hdc = CreateCompatibleDC(lpdis->hDC); 
    if (hdc == NULL) 
        break; 
 
    SelectObject(hdc, hbmMask); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
    SelectObject(hdc, hbmIcon); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
    DeleteDC(hdc); 
  
    // If the item has the focus, draw the focus rectangle.
    if (lpdis->itemState & ODS_FOCUS)
        DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

    break;
    }
```



### <a name="step-5-process-the-wm_command-message"></a>Etapa 5: processar a mensagem de comando do WM \_ .

Quando um evento ocorre em um controle de caixa de diálogo, o controle notifica o procedimento da caixa de diálogo por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) . O exemplo processa mensagens de notificação da caixa de combinação, da caixa de listagem e do botão **OK** . O identificador de controle está na palavra de ordem inferior de *wParam* e o código de notificação está na palavra de ordem superior de *wParam*.

Se o identificador de controle for IDCOMBO, ocorrerá um evento na caixa de combinação. Em resposta, o procedimento da caixa de diálogo ignora todos os outros eventos da caixa de combinação, exceto [**CBN \_ SELENDOK**](cbn-selendok.md), que indica que uma seleção foi feita, a caixa de listagem suspensa foi fechada e as alterações feitas devem ser aceitas. O procedimento da caixa de diálogo chama `InitFoodList` para redefinir o conteúdo da caixa de listagem e adicionar os nomes das seleções atuais na caixa de listagem suspensa.

Se o identificador de controle for IDLIST, ocorrerá um evento na caixa de listagem. Isso faz com que o procedimento da caixa de diálogo ignore todos os eventos da caixa de listagem, exceto [**lbn \_ DBLCLK**](lbn-dblclk.md), que indica que o usuário clicou duas vezes em um item de lista. Esse evento é processado da mesma maneira como se um botão **OK** tivesse sido escolhido.

Se o identificador de controle for IDOK, o usuário escolheu o botão **OK** . Em resposta, o procedimento da caixa de diálogo insere o nome da comida selecionada no controle de edição de várias linhas do aplicativo e, em seguida, chama a função [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) para fechar a caixa de diálogo.

Se o identificador de controle for IDCANCEL, o usuário clicou no botão **Cancelar** . Em resposta, o procedimento da caixa de diálogo chama [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) para fechar a caixa de diálogo.


```C++
case WM_COMMAND:
        switch (LOWORD(wParam)) 
        { 
            case IDCOMBO: 
                if (HIWORD(wParam) == CBN_SELENDOK) 
                { 
                    InitFoodList(hDlg); 
                    SendDlgItemMessage(hDlg, IDLIST, 
                        LB_SETCURSEL, 0, 0); 
                } 
                break; 
 
            case IDLIST: 
                if (HIWORD(wParam) != LBN_DBLCLK) 
                    break; 
 
            // For a double-click, process the OK case. 
            case IDOK: 
 
                // Get the text for the selected list item. 
                hwnd = GetDlgItem(hDlg, IDLIST); 

                // Here it is assumed the text can fit into achTemp.
                // If there is doubt, call LB_GETTEXTLENGTH first.
                SendMessage(hwnd, LB_GETTEXT, 
                    SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                    (LPARAM) achTemp); 
 
                // TODO: Do something with the selected text.
 
                EndDialog(hDlg, 0); 
                break; 
 
            case IDCANCEL: 
                hwnd = GetDlgItem(hDlg, IDCOMBO); 
                if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                    SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                else EndDialog(hDlg, 0); 
        } 
        break; 
```



## <a name="complete-example"></a>Exemplo completo

A seguir está o procedimento da caixa de diálogo e as funções de suporte para a caixa de diálogo **refeição quadrada** .


```C++
#define ID_BREAD 0
#define ID_DAIRY 1
#define ID_FRUIT 2
#define ID_MEAT  3

#define CX_BITMAP 24
#define CY_BITMAP 24

HBITMAP hbmBread;
HBITMAP hbmDairy;
HBITMAP hbmMeat;
HBITMAP hbmFruit;
HBITMAP hbmMask;

HBITMAP hbmIcon;
```

```C++
// Message handler for Square Meal dialog box.
INT_PTR CALLBACK FoodDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam)
{
    UNREFERENCED_PARAMETER(lParam);
    TCHAR achTemp[256];
    HWND hwnd;

    switch (message)
    {
    case WM_INITDIALOG:

        // Call an application-defined function to load bitmap resources.
        if (!LoadIconBitmaps())
        {
            EndDialog(hDlg, -1);
            break;
        }

        // Initialize the food groups combo box and select the first item.
        InitGroupList(hDlg);
        SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

        // Initialize the food list box and select the first item.
        InitFoodList(hDlg);
        SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

         return (INT_PTR)TRUE;
   
    case WM_MEASUREITEM:
        {
        // Set the height of the items in the food groups combo box.
        LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

        if (lpmis->itemHeight < CY_BITMAP + 2)
            lpmis->itemHeight = CY_BITMAP + 2;

        break;
        }

    case WM_DRAWITEM:
        {
        COLORREF clrBackground;
        COLORREF clrForeground;
        TEXTMETRIC tm;
        int x;
        int y;
        HRESULT hr;
        size_t cch;

        LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
           
        if (lpdis->itemID == -1) // Empty item)
            break;

        // Get the food icon from the item data.
        hbmIcon = (HBITMAP) lpdis->itemData;

        // The colors depend on whether the item is selected.
        clrForeground = SetTextColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

        clrBackground = SetBkColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHT : COLOR_WINDOW));

        // Calculate the vertical and horizontal position.
        GetTextMetrics(lpdis->hDC, &tm);
        y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
        x = LOWORD(GetDialogBaseUnits()) / 4;

        // Get and display the text for the list item.
        SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
            lpdis->itemID, (LPARAM) achTemp);

        hr = StringCchLength(achTemp, 256, &cch);
        if (FAILED(hr))
        {
            // TODO: Write error handler.
        }

        ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
            ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
            achTemp, (UINT)cch, NULL);

        // Restore the previous colors.
        SetTextColor(lpdis->hDC, clrForeground);
        SetBkColor(lpdis->hDC, clrBackground);
        
        //  Draw the food icon for the item. 
        HDC hdc = CreateCompatibleDC(lpdis->hDC); 
        if (hdc == NULL) 
            break; 
 
        SelectObject(hdc, hbmMask); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
        SelectObject(hdc, hbmIcon); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
        DeleteDC(hdc); 
      
        // If the item has the focus, draw the focus rectangle.
        if (lpdis->itemState & ODS_FOCUS)
            DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

        break;
        }

    case WM_COMMAND:
            switch (LOWORD(wParam)) 
            { 
                case IDCOMBO: 
                    if (HIWORD(wParam) == CBN_SELENDOK) 
                    { 
                        InitFoodList(hDlg); 
                        SendDlgItemMessage(hDlg, IDLIST, 
                            LB_SETCURSEL, 0, 0); 
                    } 
                    break; 
 
                case IDLIST: 
                    if (HIWORD(wParam) != LBN_DBLCLK) 
                        break; 
 
                // For a double-click, process the OK case. 
                case IDOK: 
 
                    // Get the text for the selected list item. 
                    hwnd = GetDlgItem(hDlg, IDLIST); 

                    // Here it is assumed the text can fit into achTemp.
                    // If there is doubt, call LB_GETTEXTLENGTH first.
                    SendMessage(hwnd, LB_GETTEXT, 
                        SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                        (LPARAM) achTemp); 
 
                    // TODO: Do something with the selected text.
 
                    EndDialog(hDlg, 0); 
                    break; 
 
                case IDCANCEL: 
                    hwnd = GetDlgItem(hDlg, IDCOMBO); 
                    if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                        SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                    else EndDialog(hDlg, 0); 
            } 
            break; 

    case WM_DESTROY:

        // Call the application-defined function to free the bitmap resources.
        DeleteIconBitmaps();
        break;
    }
    return (INT_PTR)FALSE;
}

// Loads string resources and adds them as items to the drop-down list of
//   the food groups combo box. The bitmap handle of each item&#39;s icon is
//   stored as item data for easy access when the item needs to be drawn.
// 
void InitGroupList(HWND hDlg)
{
    TCHAR achTemp[256];
    DWORD dwIndex;

    // Get the handle of the food groups combo box.
    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);

    LoadString(hInst, IDS_BREAD, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmBread);
    
    LoadString(hInst, IDS_DAIRY, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmDairy);

    LoadString(hInst, IDS_FRUIT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmFruit); 

    LoadString(hInst, IDS_MEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmMeat);

    return;
}

// Fills the food list based on the selected item in the food groups
//   combo box.
void InitFoodList(HWND hDlg)
{
    TCHAR achTemp[256];

    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);
    HWND hwndFoodList = GetDlgItem(hDlg, IDLIST);

    // Clear the list contents.
    SendMessage(hwndFoodList, LB_RESETCONTENT, 0, 0);

    // Find out which food group is selected.
    int idFoodGroup = SendMessage(hwndGroupsBox, CB_GETCURSEL, 0, 0);

    switch (idFoodGroup)
    {
    case ID_BREAD:
        LoadString(hInst, IDS_OAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_WHEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_RYE, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        break;

    case ID_DAIRY:
        LoadString(hInst, IDS_CHEDDAR, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_MILK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PROCESSED, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_SWISS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        
        break;

    case ID_FRUIT:
        LoadString(hInst, IDS_APPLES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_BANANAS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_ORANGES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    case ID_MEAT:
        LoadString(hInst, IDS_BEEF, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_CHICKEN, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PORK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    default:
        break;
    }

    return;
}

// Loads the food icon bitmaps from the application resources.
//
BOOL LoadIconBitmaps(void)
{
    hbmBread = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_BREAD));

    if (hbmBread != NULL)
         hbmDairy = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_DAIRY));

    if (hbmDairy != NULL)
         hbmMeat = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MEAT));

    if (hbmMeat != NULL)
        hbmFruit = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_FRUIT));
    
    if (hbmFruit != NULL)
        hbmMask = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MASK));

    if (hbmMask != NULL)
        return TRUE;
        
    return FALSE;
}

// Frees the icon bitmps.
//
void DeleteIconBitmaps(void)
{
    FreeResource(reinterpret_cast<HGLOBAL>(hbmBread));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmDairy));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMeat));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmFruit));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMask));
}
```


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando caixas de combinação](using-combo-boxes.md)
</dt> </dl>

 

 