---
title: Como inserir controles de não botão em barras de ferramentas
description: Barras de ferramentas dão suporte apenas a botões; Portanto, se seu aplicativo exigir um tipo diferente de controle, você deverá criar uma janela filho. A ilustração a seguir mostra uma barra de ferramentas com um controle de edição inserido.
ms.assetid: 7B4DACEF-96BB-447E-AE8F-F55401C665E9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ae2189350b9ea2f4aaa0c3ea0b49727bd3415
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103823612"
---
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a>Como inserir controles de não botão em barras de ferramentas

Barras de ferramentas dão suporte apenas a botões; Portanto, se seu aplicativo exigir um tipo diferente de controle, você deverá criar uma janela filho. A ilustração a seguir mostra uma barra de ferramentas com um controle de edição inserido.

![captura de tela de uma caixa de diálogo com um controle de edição na barra de ferramentas, antecedendo três ícones da barra de ferramentas](images/tb-withedit.png)

> [!Note]  
> Considere o uso de [controles Rebar](rebar-controls.md) em vez de colocar controles em barras de ferramentas.

 

Qualquer tipo de janela pode ser colocado em uma barra de ferramentas. O código de exemplo a seguir adiciona um controle de edição como um filho da janela de controle da barra de ferramentas. Como a barra de ferramentas é criada e, em seguida, o controle de edição foi adicionado, você deve fornecer espaço para o controle de edição. Uma maneira de fazer isso é adicionar um separador como um espaço reservado na barra de ferramentas, definindo a largura do separador como o número de pixels que você deseja reservar.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a>Inserir um controle de não botão em uma barra de ferramentas

O trecho de código a seguir cria a barra de ferramentas na ilustração anterior.


```C++
// IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.

HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarWithEdit(HWND hWndParent)
{
    const int ImageListID = 0;    // Define some constants.
    const int bitmapSize  = 16;
    
    const int cx_edit = 100;      // Dimensions of edit control.
    const int cy_edit = 35;  

    TBBUTTON tbButtons[] =        // Toolbar buttons.
    {
        // The separator is set to the width of the edit control. 
        
        {cx_edit, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, -1},
        {STD_FILENEW, IDM_NEW, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {0, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, 0},
    };

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, L"Toolbar", 
                                      WS_CHILD | WS_VISIBLE | WS_BORDER, 
                                      0, 0, 0, 0,
                                      hWndParent, NULL, HINST_COMMCTRL, NULL);

    if (!hWndToolbar)
        return NULL;
    
    int numButtons = sizeof(tbButtons) / sizeof(TBBUTTON);

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    0,                      // Flags.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, (WPARAM)ImageListID, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Create the edit control child window.    
    HWND hWndEdit = CreateWindowEx(0L, L"Edit", NULL, 
                                   WS_CHILD | WS_BORDER | WS_VISIBLE | ES_LEFT | ES_AUTOVSCROLL | ES_MULTILINE, 
                                   0, 0, cx_edit, cy_edit, 
                                   hWndToolbar, (HMENU) IDM_EDIT, g_hInst, 0 );
    
    if (!hWndEdit)
    {
        DestroyWindow(hWndToolbar);
        ImageList_Destroy(g_hImageList);
        
        return NULL;
    }
    
    return hWndToolbar;    // Return the toolbar with the embedded edit control.
}
```



Este exemplo codifica as dimensões da janela filho; no entanto, para criar um aplicativo mais robusto, determine o tamanho da barra de ferramentas e faça com que a janela de controle de edição caiba.

Talvez você queira que as notificações de controle de edição vá para outra janela, como o pai da barra de ferramentas. Para fazer isso, crie o controle de edição como um filho da janela pai da barra de ferramentas. Em seguida, altere o pai do controle de edição para a barra de ferramentas da seguinte maneira.


```
SetParent (hWndEdit, hWndToolbar);
```



As notificações vão para o pai original. Portanto, as mensagens de controle de edição vão para o pai da barra de ferramentas, embora a janela de edição resida na janela da barra de ferramentas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles da barra de ferramentas](using-toolbar-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




