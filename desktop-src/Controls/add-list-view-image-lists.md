---
title: Como adicionar List-View listas de imagens
description: Este tópico demonstra como adicionar listas de imagens a um controle de exibição de lista.
ms.assetid: 3C282FBC-5E37-4D8E-A2C4-B2876874E9A7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f6f5b483ea80b412ab7638c9aceafcac4c5e6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294609"
---
# <a name="how-to-add-list-view-image-lists"></a>Como adicionar List-View listas de imagens

Este tópico demonstra como adicionar listas de imagens a um controle de exibição de lista.

Você cria apenas as listas de imagens que o controle usa. Por exemplo, se seu aplicativo não permitir que o usuário alterne para a exibição de ícone, você não precisará criar e atribuir uma lista de ícones grandes. Se você criar listas de imagens grandes e pequenas, elas deverão conter as mesmas imagens na mesma ordem, porque um único valor é usado para identificar um ícone de item de exibição de lista em ambas as listas de imagens.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Para exibir imagens de itens, você deve atribuir uma lista de imagens ao controle de exibição de lista. Para fazer isso, use a mensagem do [**LVM \_ SetImageList**](lvm-setimagelist.md) ou a macro [**ListView \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist)correspondente, especificando se a lista de imagens contém ícones de tamanho completo, ícones pequenos ou imagens de estado. Para recuperar o identificador para uma lista de imagens que está atualmente atribuída a um controle de exibição de lista, use a mensagem [**LVM \_ GetImageList**](lvm-getimagelist.md) . Você pode usar a função [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) para determinar as dimensões apropriadas para os ícones de tamanho completo e pequeno.

No exemplo de código C++ a seguir, a função definida pelo aplicativo primeiro cria listas de imagens e as atribui a um controle de exibição de lista.


```C++
// InitListViewImageLists: Creates image lists for a list-view control.
// This function only creates image lists. It does not insert the items into
// the control, which is necessary for the control to be visible.   
//
// Returns TRUE if successful, or FALSE otherwise. 
//
// hWndListView: Handle to the list-view control. 
// global variable g_hInst: The handle to the module of either a 
// dynamic-link library (DLL) or executable (.exe) that contains
// the image to be loaded. If loading a standard or system
// icon, set g_hInst to NULL.
//
BOOL InitListViewImageLists(HWND hWndListView) 
{ 
    HICON hiconItem;     // Icon for list-view items.
    HIMAGELIST hLarge;   // Image list for icon view.
    HIMAGELIST hSmall;   // Image list for other views.

    // Create the full-sized icon image lists. 
    hLarge = ImageList_Create(GetSystemMetrics(SM_CXICON), 
                              GetSystemMetrics(SM_CYICON), 
                              ILC_MASK, 1, 1); 

    hSmall = ImageList_Create(GetSystemMetrics(SM_CXSMICON), 
                              GetSystemMetrics(SM_CYSMICON), 
                              ILC_MASK, 1, 1); 
    
    // Add an icon to each image list.  
    hiconItem = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ITEM));

    ImageList_AddIcon(hLarge, hiconItem);
    ImageList_AddIcon(hSmall, hiconItem);

    DestroyIcon(hiconItem);
 
// When you are dealing with multiple icons, you can use the previous four lines of 
// code inside a loop. The following code shows such a loop. The 
// icons are defined in the application's header file as resources, which 
// are numbered consecutively starting with IDS_FIRSTICON. The number of 
// icons is defined in the header file as C_ICONS.
/*    
    for(index = 0; index < C_ICONS; index++)
    {
        hIconItem = LoadIcon (g_hinst, MAKEINTRESOURCE(IDS_FIRSTICON + index));
        ImageList_AddIcon(hSmall, hIconItem);
        ImageList_AddIcon(hLarge, hIconItem);
        Destroy(hIconItem);
    }
*/
    
    // Assign the image lists to the list-view control. 
    ListView_SetImageList(hWndListView, hLarge, LVSIL_NORMAL); 
    ListView_SetImageList(hWndListView, hSmall, LVSIL_SMALL); 
    
    return TRUE; 
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle de exibição de lista](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Sobre controles de List-View](list-view-controls-overview.md)
</dt> <dt>

[Usando controles de List-View](using-list-view-controls.md)
</dt> </dl>

 

 