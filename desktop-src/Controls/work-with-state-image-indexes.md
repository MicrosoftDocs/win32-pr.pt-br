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
# <a name="how-to-work-with-state-image-indexes"></a><span data-ttu-id="505ed-103">Como trabalhar com índices de imagem de estado</span><span class="sxs-lookup"><span data-stu-id="505ed-103">How to Work With State Image Indexes</span></span>

<span data-ttu-id="505ed-104">Geralmente, há confusão sobre como definir e recuperar o índice de imagem de estado em um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="505ed-104">There is often confusion about how to set and retrieve the state image index in a tree-view control.</span></span> <span data-ttu-id="505ed-105">Os exemplos a seguir demonstram o método apropriado para configurar e recuperar o índice de imagem de estado.</span><span class="sxs-lookup"><span data-stu-id="505ed-105">The following examples demonstrate the proper method for setting and retrieving the state image index.</span></span> <span data-ttu-id="505ed-106">Os exemplos supõem que haja apenas dois índices de imagem de estado no controle de exibição de árvore, desmarcado e marcado.</span><span class="sxs-lookup"><span data-stu-id="505ed-106">The examples assume that there are only two state image indexes in the tree-view control, unchecked and checked.</span></span> <span data-ttu-id="505ed-107">Se seu aplicativo contiver mais de duas, será necessário modificar essas funções para lidar com esse caso.</span><span class="sxs-lookup"><span data-stu-id="505ed-107">If your application contains more than two, these functions will need to be modified to handle that case.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="505ed-108">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="505ed-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="505ed-109">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="505ed-109">Technologies</span></span>

-   [<span data-ttu-id="505ed-110">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="505ed-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="505ed-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="505ed-111">Prerequisites</span></span>

-   <span data-ttu-id="505ed-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="505ed-112">C/C++</span></span>
-   <span data-ttu-id="505ed-113">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="505ed-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="505ed-114">Instruções</span><span class="sxs-lookup"><span data-stu-id="505ed-114">Instructions</span></span>

### <a name="set-a-tree-view-items-check-state"></a><span data-ttu-id="505ed-115">Definir o estado de verificação do item de Tree-View</span><span class="sxs-lookup"><span data-stu-id="505ed-115">Set a Tree-View Item's Check State</span></span>

<span data-ttu-id="505ed-116">O exemplo a seguir demonstra como definir um estado de verificação do item de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="505ed-116">The following example demonstrates how to set a tree-view item's check state.</span></span>


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



### <a name="retrieve-a-tree-view-items-check-state"></a><span data-ttu-id="505ed-117">Recuperar o estado de verificação do item de Tree-View</span><span class="sxs-lookup"><span data-stu-id="505ed-117">Retrieve a Tree-View Item's Check State</span></span>

<span data-ttu-id="505ed-118">O exemplo a seguir demonstra como recuperar um estado de verificação do item de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="505ed-118">The following example demonstrates how to retrieve a tree-view item's check state.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="505ed-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="505ed-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="505ed-120">Usando controles de Tree-View</span><span class="sxs-lookup"><span data-stu-id="505ed-120">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="505ed-121">O exemplo de CustDTv ilustra o desenho personalizado em um controle de Tree-View</span><span class="sxs-lookup"><span data-stu-id="505ed-121">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




