---
title: Como adicionar itens e subitens de List-View
description: Este tópico demonstra como adicionar itens e subitens a um controle de exibição de lista.
ms.assetid: B7E204DC-FD08-4639-985D-1459A1AC0ED6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b3d20008edc10fda810261427507c77e9cfe34
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104085006"
---
# <a name="how-to-add-list-view-items-and-subitems"></a><span data-ttu-id="50ea8-103">Como adicionar itens e subitens de List-View</span><span class="sxs-lookup"><span data-stu-id="50ea8-103">How to Add List-View Items and Subitems</span></span>

<span data-ttu-id="50ea8-104">Este tópico demonstra como adicionar itens e subitens a um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="50ea8-104">This topic demonstrates how to add items and subitems to a list-view control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="50ea8-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="50ea8-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="50ea8-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="50ea8-106">Technologies</span></span>

-   [<span data-ttu-id="50ea8-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="50ea8-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="50ea8-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="50ea8-108">Prerequisites</span></span>

-   <span data-ttu-id="50ea8-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="50ea8-109">C/C++</span></span>
-   <span data-ttu-id="50ea8-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="50ea8-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="50ea8-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="50ea8-111">Instructions</span></span>


<span data-ttu-id="50ea8-112">Para adicionar um item a um controle de exibição de lista, um aplicativo deve primeiro definir uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) e, em seguida, enviar uma mensagem [**LVM \_ INSERTITEM**](lvm-insertitem.md) , especificando o endereço da estrutura **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="50ea8-112">To add an item to a list-view control, an application must first define an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure and then send an [**LVM\_INSERTITEM**](lvm-insertitem.md) message, specifying the address of the **LVITEM** structure.</span></span> <span data-ttu-id="50ea8-113">Se um aplicativo usar o modo de exibição de relatório, o texto do subitem deverá ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="50ea8-113">If an application uses report view, subitem text must be provided.</span></span>

<span data-ttu-id="50ea8-114">O exemplo de código C++ a seguir preenche uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) e adiciona os itens de exibição de lista usando a mensagem [**LVM \_ INSERTITEM**](lvm-insertitem.md) ou o [**\_ INSERTITEM de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem)de macro correspondente.</span><span class="sxs-lookup"><span data-stu-id="50ea8-114">The following C++ code example fills an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure and adds the list-view items by using the [**LVM\_INSERTITEM**](lvm-insertitem.md) message or the corresponding macro [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem).</span></span> <span data-ttu-id="50ea8-115">Como o aplicativo salva seu próprio texto, ele especifica o \_ valor de **PSZTEXT** do LPSTR para o membro da estrutura **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="50ea8-115">Because the application saves its own text, it specifies the LPSTR\_TEXTCALLBACK value for the **pszText** member of the **LVITEM** structure.</span></span> <span data-ttu-id="50ea8-116">A especificação do \_ valor de USERcallback de LPSTR faz com que o controle envie um código de notificação [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) para sua janela do proprietário sempre que precisar exibir um item.</span><span class="sxs-lookup"><span data-stu-id="50ea8-116">Specifying the LPSTR\_TEXTCALLBACK value causes the control to send an [**LVN\_GETDISPINFO**](lvn-getdispinfo.md) notification code to its owner window whenever it needs to display an item.</span></span>


```C++
// InsertListViewItems: Inserts items into a list view. 
// hWndListView:        Handle to the list-view control.
// cItems:              Number of items to insert.
// Returns TRUE if successful, and FALSE otherwise.
BOOL InsertListViewItems(HWND hWndListView, int cItems)
{
    LVITEM lvI;

    // Initialize LVITEM members that are common to all items.
    lvI.pszText   = LPSTR_TEXTCALLBACK; // Sends an LVN_GETDISPINFO message.
    lvI.mask      = LVIF_TEXT | LVIF_IMAGE |LVIF_STATE;
    lvI.stateMask = 0;
    lvI.iSubItem  = 0;
    lvI.state     = 0;

    // Initialize LVITEM members that are different for each item.
    for (int index = 0; index < cItems; index++)
    {
        lvI.iItem  = index;
        lvI.iImage = index;
    
        // Insert items into the list.
        if (ListView_InsertItem(hWndListView, &lvI) == -1)
            return FALSE;
    }

    return TRUE;
}

// HandleWM_NOTIFY - Handles the LVN_GETDISPINFO notification code that is 
//         sent in a WM_NOTIFY to the list view parent window. The function 
//        provides display strings for list view items and subitems.
//
// lParam - The LPARAM parameter passed with the WM_NOTIFY message.
// rgPetInfo - A global array of structures, defined as follows:
//         struct PETINFO
//        {
//            TCHAR szKind[10];
//            TCHAR szBreed[50];
//            TCHAR szPrice[20];
//        };
//
//        PETINFO rgPetInfo[ ] = 
//        {
//            {TEXT("Dog"),  TEXT("Poodle"),     TEXT("$300.00")},
//            {TEXT("Cat"),  TEXT("Siamese"),    TEXT("$100.00")},
//            {TEXT("Fish"), TEXT("Angel Fish"), TEXT("$10.00")},
//            {TEXT("Bird"), TEXT("Parakeet"),   TEXT("$5.00")},
//            {TEXT("Toad"), TEXT("Woodhouse"),  TEXT("$0.25")},
//        };
//
void HandleWM_NOTIFY(LPARAM lParam)
{
    NMLVDISPINFO* plvdi;

    switch (((LPNMHDR) lParam)->code)
    {
        case LVN_GETDISPINFO:

            plvdi = (NMLVDISPINFO*)lParam;

            switch (plvdi->item.iSubItem)
            {
                case 0:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szKind;
                    break;
                      
                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;
                
                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;
                
                default:
                    break;
            }

        break;

    }
    // NOTE: In addition to setting pszText to point to the item text, you could 
    // copy the item text into pszText using StringCchCopy. For example:
    //
    // StringCchCopy(plvdi->item.pszText, 
    //                         plvdi->item.cchTextMax, 
    //                         rgPetInfo[plvdi->item.iItem].szKind);

    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="50ea8-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50ea8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50ea8-118">Referência de controle de exibição de lista</span><span class="sxs-lookup"><span data-stu-id="50ea8-118">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="50ea8-119">Sobre controles de List-View</span><span class="sxs-lookup"><span data-stu-id="50ea8-119">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="50ea8-120">Usando controles de List-View</span><span class="sxs-lookup"><span data-stu-id="50ea8-120">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




