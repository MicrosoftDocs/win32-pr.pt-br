---
title: Como criar um controle de Tree-View
description: Para criar um controle de exibição de árvore, use a função CreateWindowEx, especificando o \_ valor de TreeView WC para a classe Window.
ms.assetid: FEC3BF62-3085-47D4-B82E-7BD7B34B397D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ec22cc4f3f88e57266a4c2ac88df542a39429
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084939"
---
# <a name="how-to-create-a-tree-view-control"></a>Como criar um controle de Tree-View

Para criar um controle de exibição de árvore, use a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando o valor de [**\_ TreeView WC**](common-control-window-classes.md) para a classe Window. A classe de janela de exibição de árvore é registrada no espaço de endereço do aplicativo quando a DLL de controle comum é carregada. Para garantir que a DLL seja carregada, use a função [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="create-an-instance-of-a-tree-view-control"></a>Criar uma instância de um controle de Tree-View

O exemplo a seguir cria um controle de exibição de árvore que é dimensionado para se ajustar à área do cliente da janela pai. Ele também usa funções definidas pelo aplicativo para associar uma lista de imagens ao controle e adicionar itens ao controle.


```C++
// Create a tree-view control. 
// Returns the handle to the new control if successful,
// or NULL otherwise. 
// hwndParent - handle to the control's parent window. 
// lpszFileName - name of the file to parse for tree-view items.
// g_hInst - the global instance handle.
// ID_TREEVIEW - the resource ID of the control.

HWND CreateATreeView(HWND hwndParent)
{ 
    RECT rcClient;  // dimensions of client area 
    HWND hwndTV;    // handle to tree-view control 

    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Get the dimensions of the parent window's client area, and create 
    // the tree-view control. 
    GetClientRect(hwndParent, &rcClient); 
    hwndTV = CreateWindowEx(0,
                            WC_TREEVIEW,
                            TEXT("Tree View"),
                            WS_VISIBLE | WS_CHILD | WS_BORDER | TVS_HASLINES, 
                            0, 
                            0, 
                            rcClient.right, 
                            rcClient.bottom,
                            hwndParent, 
                            (HMENU)ID_TREEVIEW, 
                            g_hInst, 
                            NULL); 

    // Initialize the image list, and add items to the control. 
    // InitTreeViewImageLists and InitTreeViewItems are application- 
    // defined functions, shown later. 
    if (!InitTreeViewImageLists(hwndTV) || 
                !InitTreeViewItems(hwndTV))
    { 
        DestroyWindow(hwndTV); 
        return FALSE; 
    } 
    return hwndTV;
} 
```



## <a name="remarks"></a>Comentários

Ao criar um controle de exibição de árvore, você também pode enviá-lo para uma mensagem do [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont) para definir a fonte a ser usada para o texto. Você deve enviar esta mensagem antes de inserir qualquer item. Por padrão, um modo de exibição de árvore usa a fonte do título do ícone. Embora você possa personalizar a fonte por item usando o [desenho personalizado](custom-draw.md), o controle de exibição de árvore usa as dimensões da fonte especificada pela mensagem do **WM \_ SetFont** para determinar o espaçamento e o layout.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de Tree-View](using-treeview.md)
</dt> <dt>

[O exemplo de CustDTv ilustra o desenho personalizado em um controle de Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 