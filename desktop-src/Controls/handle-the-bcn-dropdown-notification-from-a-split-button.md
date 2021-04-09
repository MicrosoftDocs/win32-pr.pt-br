---
title: Manipular notificações de BCN_DROPDOWN de SplitButtons
description: Este tópico descreve uma possível maneira de responder à notificação de \_ lista suspensa BCN em um procedimento de caixa de diálogo.
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084945"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a>Como manipular a \_ notificação suspensa BCN de um botão de divisão

Este tópico descreve uma possível maneira de responder à notificação [de \_ lista suspensa BCN](bcn-dropdown.md) em um procedimento de caixa de diálogo.

O aplicativo C++ recupera as coordenadas do cliente do botão do cabeçalho de notificação e as converte em coordenadas da tela. Em seguida, ele cria um menu pop-up e o exibe na parte inferior do botão. Para manter o exemplo simples, os atalhos de teclado não são implementados para o menu.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a>Etapa 1: aguardar a notificação da *\_ lista suspensa BCN* .


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a>Etapa 2: obter as coordenadas de tela do botão.

Use a função [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) para converter as coordenadas da janela da borda inferior esquerda do botão para as coordenadas da tela.


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a>Etapa 3: criar um menu e adicionar itens.

Use a função [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) para criar um menu. Use a função [**AppendMenu**](/windows/desktop/menurc/u) para adicionar itens ao menu. IDC \_ MENUCOMMAND1 e IDC \_ MENUCOMMAND2 são constantes definidas pelo aplicativo para comandos de menu.


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a>Etapa 4: exibir o menu.

A função [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) exibe um menu de atalho no local especificado e controla a seleção de itens no menu.


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a>Exemplo completo


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_Código de notificação da lista suspensa BCN](bcn-dropdown.md)
</dt> <dt>

[Sobre os botões](about-buttons.md)
</dt> <dt>

[Referência de controle de botão](bumper-button-button-control-reference.md)
</dt> <dt>

[Usando botões](using-buttons.md)
</dt> <dt>

[Botão](buttons.md)
</dt> </dl>

 

 