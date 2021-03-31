---
title: Como trabalhar com índices de imagem de estado
description: Geralmente, há confusão sobre como definir e recuperar o índice de imagem de estado em um controle de exibição de árvore.
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be84035907b69ba98ed60a33046f1a58fd2b47b2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103640192"
---
# <a name="how-to-work-with-state-image-indexes"></a>Como trabalhar com índices de imagem de estado

Geralmente, há confusão sobre como definir e recuperar o índice de imagem de estado em um controle de exibição de árvore. Os exemplos a seguir demonstram o método apropriado para configurar e recuperar o índice de imagem de estado. Os exemplos supõem que haja apenas dois índices de imagem de estado no controle de exibição de árvore, desmarcado e marcado. Se seu aplicativo contiver mais de duas, será necessário modificar essas funções para lidar com esse caso.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="set-a-tree-view-items-check-state"></a>Definir o estado de verificação do item de Tree-View

O exemplo a seguir demonstra como definir um estado de verificação do item de exibição de árvore.


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



### <a name="retrieve-a-tree-view-items-check-state"></a>Recuperar o estado de verificação do item de Tree-View

O exemplo a seguir demonstra como recuperar um estado de verificação do item de exibição de árvore.


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

[Usando controles de Tree-View](using-treeview.md)
</dt> <dt>

[O exemplo de CustDTv ilustra o desenho personalizado em um controle de Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




