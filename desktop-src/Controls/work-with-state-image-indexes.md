---
title: Como trabalhar com índices de imagem de estado
description: Geralmente, há confusão sobre como definir e recuperar o índice de imagem de estado em um controle de exibição de árvore.
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04504019f79a388b6c21f940724de884d8516263daf6d410a841a96fc2e557b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059296"
---
# <a name="how-to-work-with-state-image-indexes"></a>Como trabalhar com índices de imagem de estado

Geralmente, há confusão sobre como definir e recuperar o índice de imagem de estado em um controle de exibição de árvore. Os exemplos a seguir demonstram o método adequado para definir e recuperar o índice de imagem de estado. Os exemplos supõem que há apenas dois índices de imagem de estado no controle de exibição de árvore, desmarcados e verificados. Se o aplicativo contiver mais de duas, essas funções precisarão ser modificadas para lidar com esse caso.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="set-a-tree-view-items-check-state"></a>Definir um Tree-View estado de verificação de um item de configuração

O exemplo a seguir demonstra como definir o estado de verificação de um item de exibição de árvore.


```C++
  BOOL TreeView_SetCheckState(HWND hwndTreeView, HTREEITEM hItem, BOOL fCheck)
  {
      TVITEM tvItem;

      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Image 1 in the tree-view check box image list is the unchecked box. 
      // Image 2 is the checked box.

      tvItem.state = INDEXTOSTATEIMAGEMASK((fCheck ? 2 : 1));

      return TreeView_SetItem(hwndTreeView, &tvItem);
  }
```



### <a name="retrieve-a-tree-view-items-check-state"></a>Recuperar um Tree-View estado de verificação do item

O exemplo a seguir demonstra como recuperar o estado de verificação de um item de exibição de árvore.


```C++
  BOOL TreeView_GetCheckState(HWND hwndTreeView, HTREEITEM hItem)
  {
      TVITEM tvItem;

      // Prepare to receive the desired information.
      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Request the information.
      TreeView_GetItem(hwndTreeView, &tvItem);

      // Return zero if it's not checked, or nonzero otherwise.
      return ((BOOL)(tvItem.state >> 12) - 1);
  }
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando Tree-View controles](using-treeview.md)
</dt> <dt>

[O exemplo de CustDTv ilustra o desenho personalizado em um Tree-View controle](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




