---
title: Como usar Tree-View Infotips
description: Quando você aplica o \_ estilo INFOTIP de TVs a um controle de exibição de árvore, ele gera \_ notificações TVN GETINFOTIP quando o cursor está sobre um item no modo de exibição de árvore. Ao responder a essa notificação, você pode definir o texto que aparece na InfoTip.
ms.assetid: 779BEAC1-877E-43DD-AE1C-6D71C3013384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0ef862d68cfd9f6ac5a97e82c80622e9c02121
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "105753779"
---
# <a name="how-to-use-tree-view-infotips"></a><span data-ttu-id="43a79-104">Como usar Tree-View Infotips</span><span class="sxs-lookup"><span data-stu-id="43a79-104">How to Use Tree-View Infotips</span></span>

<span data-ttu-id="43a79-105">Quando você aplica o [**estilo \_ INFOTIP de TVs**](tree-view-control-window-styles.md) a um controle de exibição de árvore, ele gera notificações [TVN \_ GETINFOTIP](tvn-getinfotip.md) quando o cursor está sobre um item no modo de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="43a79-105">When you apply the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style to a tree-view control, it generates [TVN\_GETINFOTIP](tvn-getinfotip.md) notifications when the cursor is over an item in the tree view.</span></span> <span data-ttu-id="43a79-106">Ao responder a essa notificação, você pode definir o texto que aparece na InfoTip.</span><span class="sxs-lookup"><span data-stu-id="43a79-106">By responding to this notification, you can set the text that appears in the infotip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="43a79-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="43a79-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="43a79-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="43a79-108">Technologies</span></span>

-   [<span data-ttu-id="43a79-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="43a79-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="43a79-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="43a79-110">Prerequisites</span></span>

-   <span data-ttu-id="43a79-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="43a79-111">C/C++</span></span>
-   <span data-ttu-id="43a79-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="43a79-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="43a79-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="43a79-113">Instructions</span></span>

### <a name="use-tree-view-infotips"></a><span data-ttu-id="43a79-114">Usar Tree-View Infotips</span><span class="sxs-lookup"><span data-stu-id="43a79-114">Use Tree-View Infotips</span></span>

<span data-ttu-id="43a79-115">O código de exemplo a seguir mostra como um aplicativo pode responder à notificação.</span><span class="sxs-lookup"><span data-stu-id="43a79-115">The following example code shows how an application might respond to the notification.</span></span> <span data-ttu-id="43a79-116">Para simplificar, o exemplo apenas copia o texto do item para o InfoTip.</span><span class="sxs-lookup"><span data-stu-id="43a79-116">For simplicity, the example just copies the text for the item to the infotip.</span></span>


```
  case WM_NOTIFY:
    switch (((LPNMHDR) lParam)->code)
    {
    case TVN_GETINFOTIP:
        {
          LPNMTVGETINFOTIP pTip = (LPNMTVGETINFOTIP)lParam;
          HWND hTree            = GetDlgItem(hDlg, IDC_TREE1);
          HTREEITEM item        = pTip->hItem;

          // Get the text for the item.
          TVITEM tvitem;
          tvitem.mask       = TVIF_TEXT;
          tvitem.hItem      = item;
          TCHAR temp[1024];
          tvitem.pszText    = infoTipBuf;
          tvitem.cchTextMax = sizeof(temp) / sizeof(TCHAR);
          TreeView_GetItem(hTree, &tvitem);

          // Copy the text to the infotip.
          wcscpy_s(pTip->pszText, pTip->cchTextMax, tvitem.pszText);
          break;
        }
      }
      return TRUE;
```



## <a name="related-topics"></a><span data-ttu-id="43a79-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43a79-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43a79-118">Usando controles de Tree-View</span><span class="sxs-lookup"><span data-stu-id="43a79-118">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="43a79-119">O exemplo de CustDTv ilustra o desenho personalizado em um controle de Tree-View</span><span class="sxs-lookup"><span data-stu-id="43a79-119">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




