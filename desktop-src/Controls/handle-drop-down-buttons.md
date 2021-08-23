---
title: Como lidar com botões de lista listada
description: Um botão de lista listada pode apresentar aos usuários uma lista de opções.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74443b0d29b3ab39255d7417fd13677769f6a762ebe176e8301a76029db0c37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544937"
---
# <a name="how-to-handle-drop-down-buttons"></a>Como lidar com botões de lista listada

Um botão de lista listada pode apresentar aos usuários uma lista de opções. Para criar esse estilo de botão, especifique o estilo [**SUSPENSO BTNS \_**](toolbar-control-and-button-styles.md) (também chamado [**TBSTYLE \_ DROPDOWN**](toolbar-control-and-button-styles.md) para compatibilidade com versões anteriores dos controles comuns). Para mostrar um botão de lista listada com uma seta, você também deve definir o estilo da barra de ferramentas [**TBSTYLE \_ EX \_ DRAWDDARROWS**](toolbar-extended-styles.md) enviando uma mensagem [**TB \_ SETEXTENDEDSTYLE.**](tb-setextendedstyle.md)

A ilustração a seguir mostra um botão suspenso "Abrir" com o menu de contexto aberto e mostrando uma lista de arquivos. Neste exemplo, a barra de ferramentas tem o [**estilo TBSTYLE \_ EX \_ DRAWDDARROWS.**](toolbar-extended-styles.md)

![captura de tela de uma caixa de diálogo com três itens da barra de ferramentas representados por ícones; um tem uma seta para baixo expandida e um menu de contexto de três itens](images/tb-dropdown.png)

A ilustração a seguir mostra a mesma barra de ferramentas, desta vez sem o estilo [**TBSTYLE \_ EX \_ DRAWDDARROWS.**](toolbar-extended-styles.md)

![captura de tela de uma caixa de diálogo anterior, mas o ícone com o menu de contexto não tem seta para baixo](images/tb-dropdown2.png)

Quando os usuários clicam em um botão de barra de ferramentas que usa o estilo [**BTNS \_ DROPDOWN,**](toolbar-control-and-button-styles.md) o controle da barra de ferramentas envia à janela pai um código de notificação [ \_ DROPDOWN do TBN.](tbn-dropdown.md)

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="handle-a-drop-down-button"></a>Manipular um botão de lista listada

O exemplo de código a seguir demonstra como um aplicativo pode dar suporte a um botão de lista listada em um controle de barra de ferramentas.


```C++
BOOL DoNotify(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{

    #define lpnm   ((LPNMHDR)lParam)
    #define lpnmTB ((LPNMTOOLBAR)lParam)

    switch(lpnm->code)
    {
        case TBN_DROPDOWN:
        {
            // Get the coordinates of the button.
            RECT rc;
            SendMessage(lpnmTB->hdr.hwndFrom, TB_GETRECT, (WPARAM)lpnmTB->iItem, (LPARAM)&rc);

            // Convert to screen coordinates.            
            MapWindowPoints(lpnmTB->hdr.hwndFrom, HWND_DESKTOP, (LPPOINT)&rc, 2);                         
        
            // Get the menu.
            HMENU hMenuLoaded = LoadMenu(g_hinst, MAKEINTRESOURCE(IDR_POPUP)); 
         
            // Get the submenu for the first menu item.
            HMENU hPopupMenu = GetSubMenu(hMenuLoaded, 0);

            // Set up the pop-up menu.
            // In case the toolbar is too close to the bottom of the screen, 
            // set rcExclude equal to the button rectangle and the menu will appear above 
            // the button, and not below it.
         
            TPMPARAMS tpm;
         
            tpm.cbSize    = sizeof(TPMPARAMS);
            tpm.rcExclude = rc;
         
            // Show the menu and wait for input. 
            // If the user selects an item, its WM_COMMAND is sent.
         
            TrackPopupMenuEx(hPopupMenu, 
                             TPM_LEFTALIGN | TPM_LEFTBUTTON | TPM_VERTICAL, 
                             rc.left, rc.bottom, g_hwndMain, &tpm);

            DestroyMenu(hMenuLoaded);
         
        return (FALSE);
      
        }
    }
   
    return FALSE;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles da barra de ferramentas](using-toolbar-controls.md)
</dt> <dt>

[Windows demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




