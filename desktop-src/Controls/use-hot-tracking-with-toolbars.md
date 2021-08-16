---
title: Como usar Hot-Tracking com barras de ferramentas
description: Quando um ponteiro do mouse passa sobre um item, o item fica quente. Se o acompanhamento de quente estiver habilitado, o item ativo será realçado. Uma barra de ferramentas criada com o \_ estilo simples TBSTYLE, ou uma que usa estilos visuais, dá suporte ao acompanhamento de acesso por padrão.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd735828675ca360cfa91aceefb2d76d34252a96aa7b5edb776e3d48a1fcdc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829077"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a>Como usar Hot-Tracking com barras de ferramentas

Quando um ponteiro do mouse passa sobre um item, o item fica quente. Se o acompanhamento de quente estiver habilitado, o item ativo será realçado. Uma barra de ferramentas criada com o [**estilo \_ simples TBSTYLE**](toolbar-control-and-button-styles.md) , ou uma que usa [estilos visuais](themes-overview.md), dá suporte ao acompanhamento de acesso por padrão.

O acompanhamento dinâmico exige que você crie listas de imagens; Portanto, você não pode usar a mensagem de [**TB \_ AddBitmap**](tb-addbitmap.md) ou a função [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) para criar sua barra de ferramentas.

Quando o mouse passa sobre um botão da barra de ferramentas, o botão é destacado para realçá-lo. A ilustração a seguir mostra uma barra de ferramentas com o controle de acesso habilitado; o ponteiro do mouse estava focalizando o botão salvar quando a captura de tela foi tomada.

![captura de tela de uma caixa de diálogo com uma barra de ferramentas de três itens; o ícone selecionado é descrito](images/tb-withstyles.png)

Se você quiser que um bitmap de botão da barra de ferramentas seja alterado quando o estado do controle for alterado, armazene as diferentes imagens em [listas de imagens](image-lists.md). Por exemplo, alguns aplicativos têm botões de barra de ferramentas pretos e brancos que se tornam coloridos quando são selecionados. As duas imagens diferentes são armazenadas em listas de imagens. As barras de ferramentas dão suporte ao uso de até três listas de imagens. Normalmente, um aplicativo tem uma lista de imagens padrão, desabilitada e de rastreamento dinâmico. Para definir e recuperar listas de imagens para botões da barra de ferramentas quente, use as mensagens [**TB \_ SETHOTIMAGELIST**](tb-sethotimagelist.md) e [**TB \_ GETHOTIMAGELIST**](tb-gethotimagelist.md) .

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções

### <a name="use-hot-tracking-with-a-toolbar"></a>Usar Hot-Tracking com uma barra de ferramentas

O exemplo de código a seguir cria, preenche e atribui uma lista de imagens para botões quentes.


```C++
// Create the image list, himlHot.
g_himlHot = ImageList_Create(MYICON_CX,MYICON_CY,ILC_COLOR8,0,4);

// Load a bitmap from a resource file, and add the images to the image list.
// Note that the bitmap contains four images.

hBitmapHot = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_HOT));

ImageList_Add(g_himlHot, hBitmapHot, NULL);
   
// Set the image list. 
SendMessage(hwndTB, TB_SETHOTIMAGELIST, 0, (LPARAM)g_himlHot);
   
// Loop to fill the array of TBBUTTON structures.  
for(i=0;i<MAX_BUTTONS;i++)
{
    tbArray[i].iBitmap   = i;                   // Bitmap from image list.
    tbArray[i].idCommand = IDM_BUTTONSTART + i;
    tbArray[i].fsState   = TBSTATE_ENABLED;
    tbArray[i].fsStyle   = BTNS_DROPDOWN;
    tbArray[i].dwData    = 0;
    tbArray[i].iString   = i;
}

DeleteObject(hBitmapHot);    // Delete the loaded bitmap.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles da barra de ferramentas](using-toolbar-controls.md)
</dt> <dt>

[Windows de demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




