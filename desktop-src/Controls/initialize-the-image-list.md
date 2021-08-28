---
title: Como inicializar a lista de imagens
description: Cada item em um controle de exibição de árvore pode ter duas imagens associadas a ele.
ms.assetid: 3683DB35-D70F-4181-9181-95354599B9FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b8edcff0d07f46aa6eb8612ddbbfa37145c5ab26ab463a7d57e9e6543430e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019344"
---
# <a name="how-to-initialize-the-image-list"></a>Como inicializar a lista de imagens

Cada item em um controle de exibição de árvore pode ter duas imagens associadas a ele. Um item exibe uma imagem quando está selecionada e a outra quando não está. Para incluir imagens com itens de exibição de árvore, primeiro use as funções Listas [de](image-lists.md) Imagens para criar uma lista de imagens e adicionar imagens a ela. Em seguida, associe a lista de imagens ao controle de exibição de árvore usando a mensagem [**\_ TVM SETIMAGELIST.**](tvm-setimagelist.md)

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="initialize-the-image-list"></a>Inicializar a lista de imagens

O exemplo a seguir cria uma lista de imagens, adiciona três bitmaps à lista e associa a lista de imagens a um controle de exibição de árvore.


```C++
// InitTreeViewImageLists - creates an image list, adds three bitmaps 
// to it, and associates the image list with a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 
//
// Global variables and constants: 
// g_hInst - the global instance handle.
// g_nOpen, g_nClosed, and g_nDocument - global indexes of the images. 
// CX_BITMAP and CY_BITMAP - width and height of an icon. 
// NUM_BITMAPS - number of bitmaps to add to the image list. 
// IDB_OPEN_FILE, IDB_CLOSED_FILE, IDB_DOCUMENT -
//     resource identifiers of the bitmaps.

BOOL InitTreeViewImageLists(HWND hwndTV) 
{ 
    HIMAGELIST himl;  // handle to image list 
    HBITMAP hbmp;     // handle to bitmap 

    // Create the image list. 
    if ((himl = ImageList_Create(CX_BITMAP, 
                                 CY_BITMAP,
                                 FALSE, 
                                 NUM_BITMAPS, 0)) == NULL) 
        return FALSE; 

    // Add the open file, closed file, and document bitmaps. 
    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_OPEN_FILE)); 
    g_nOpen = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_CLOSED_FILE)); 
    g_nClosed = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_DOCUMENT)); 
    g_nDocument = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    // Fail if not all of the images were added. 
    if (ImageList_GetImageCount(himl) < 3) 
        return FALSE; 

    // Associate the image list with the tree-view control. 
    TreeView_SetImageList(hwndTV, himl, TVSIL_NORMAL); 

    return TRUE; 
} 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando Tree-View controles](using-treeview.md)
</dt> <dt>

[O exemplo de CustDTv ilustra o desenho personalizado em um Tree-View controle](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




