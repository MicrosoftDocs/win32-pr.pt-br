---
title: Como usar List-View áreas de trabalho
description: Este tópico demonstra como trabalhar com áreas de trabalho do modo de exibição de lista. Áreas de trabalho são áreas virtuais retangulares que podem ser usadas para organizar itens em um controle List-exibição.
ms.assetid: 7A803B66-7827-49A3-8D87-6A037C09A19A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d3ed4142e6933e662f03f268723db145c7eb00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005350"
---
# <a name="how-to-use-list-view-working-areas"></a><span data-ttu-id="81307-104">Como usar List-View áreas de trabalho</span><span class="sxs-lookup"><span data-stu-id="81307-104">How to Use List-View Working Areas</span></span>

<span data-ttu-id="81307-105">Este tópico demonstra como trabalhar com áreas de trabalho do modo de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="81307-105">This topic demonstrates how to work with list-view working areas.</span></span> <span data-ttu-id="81307-106">Áreas de trabalho são áreas virtuais retangulares que podem ser usadas para organizar itens em um controle List-exibição.</span><span class="sxs-lookup"><span data-stu-id="81307-106">Working areas are rectangular virtual areas that can be used to arrange items in a list-vew control.</span></span> <span data-ttu-id="81307-107">Uma área de trabalho não é uma janela e não pode ter uma borda visível.</span><span class="sxs-lookup"><span data-stu-id="81307-107">A working area is not a window and cannot have a visible border.</span></span> <span data-ttu-id="81307-108">Por padrão, o controle de exibição de lista não tem áreas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="81307-108">By default, the list-view control has no working areas.</span></span> <span data-ttu-id="81307-109">Ao criar uma área de trabalho, você pode criar uma borda vazia à esquerda, à parte superior ou à direita dos itens ou fazer com que uma barra de rolagem horizontal seja exibida quando normalmente não haveria uma.</span><span class="sxs-lookup"><span data-stu-id="81307-109">By creating a working area, you can create an empty border on the left, top, or right of the items or cause a horizontal scroll bar to be displayed when there normally would not be one.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="81307-110">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="81307-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="81307-111">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="81307-111">Technologies</span></span>

-   [<span data-ttu-id="81307-112">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="81307-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="81307-113">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="81307-113">Prerequisites</span></span>

-   <span data-ttu-id="81307-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="81307-114">C/C++</span></span>
-   <span data-ttu-id="81307-115">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="81307-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="81307-116">Instruções</span><span class="sxs-lookup"><span data-stu-id="81307-116">Instructions</span></span>

### <a name="create-a-working-area"></a><span data-ttu-id="81307-117">Criar uma área de trabalho</span><span class="sxs-lookup"><span data-stu-id="81307-117">Create a Working Area</span></span>

<span data-ttu-id="81307-118">O exemplo de código C++ a seguir demonstra como criar uma área de trabalho com uma borda vazia de 25 pixels nos lados superior, esquerda e direito.</span><span class="sxs-lookup"><span data-stu-id="81307-118">The following C++ code example demonstrates how to create a working area with a 25-pixel empty border on its top, left, and right sides.</span></span>


```C++
void SetWorkAreas1(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    
    GetClientRect(hWndListView, &rcClient);
    
    rcClient.left  +=  EMPTY_SPACE;
    rcClient.top   +=  EMPTY_SPACE;
    rcClient.right -= (EMPTY_SPACE * 2);
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 1, (LPARAM)&rcClient);

    return;
}
```



### <a name="create-multiple-working-areas"></a><span data-ttu-id="81307-119">Criar várias áreas de trabalho</span><span class="sxs-lookup"><span data-stu-id="81307-119">Create Multiple Working Areas</span></span>

<span data-ttu-id="81307-120">O exemplo de código C++ a seguir demonstra como criar duas áreas de trabalho em um controle.</span><span class="sxs-lookup"><span data-stu-id="81307-120">The following C++ code example demonstrates how to create two working areas in a control.</span></span> <span data-ttu-id="81307-121">Cada área de trabalho usa cerca de metade da área do cliente e é circundada por uma borda vazia de 25 pixels.</span><span class="sxs-lookup"><span data-stu-id="81307-121">Each working area uses about half of the client area, and is surrounded by a 25-pixel empty border.</span></span>


```C++
void SetWorkAreas2(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    RECT  rcWork[2];
    
    GetClientRect(hWndListView, &rcClient);
    
    rcWork[0].left   = rcClient.left +      EMPTY_SPACE;
    rcWork[0].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[0].right  = (rcClient.right/2) - EMPTY_SPACE;
    rcWork[0].bottom = rcClient.bottom;
    
    rcWork[1].left   = (rcClient.right/2) + EMPTY_SPACE;
    rcWork[1].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[1].right  = rcClient.right -     EMPTY_SPACE;
    rcWork[1].bottom = rcClient.bottom;
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 2, (LPARAM)rcWork);

    return;
}
```



### <a name="determine-the-working-area-to-which-an-item-belongs"></a><span data-ttu-id="81307-122">Determinar a área de trabalho à qual um item pertence</span><span class="sxs-lookup"><span data-stu-id="81307-122">Determine the Working Area to Which an Item Belongs</span></span>

<span data-ttu-id="81307-123">Uma maneira de determinar qual área de trabalho um item pertence é fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="81307-123">One way to determine which working area an item belongs is to do the following:</span></span>

-   <span data-ttu-id="81307-124">Recupere a lista de coordenadas de todas as áreas de trabalho no controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="81307-124">Retrieve the list of coordinates of all of the working areas in the list-view control.</span></span>
-   <span data-ttu-id="81307-125">Recupere as coordenadas do item.</span><span class="sxs-lookup"><span data-stu-id="81307-125">Retrieve the coordinates of the item.</span></span>
-   <span data-ttu-id="81307-126">Determine se as coordenadas de item estão dentro das coordenadas de uma das áreas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="81307-126">Determine whether the item coordinates lie within the coordinates of one of the working areas.</span></span>

<span data-ttu-id="81307-127">A função definida pelo aplicativo no exemplo de código C++ a seguir retorna o índice da área de trabalho à qual o item pertence.</span><span class="sxs-lookup"><span data-stu-id="81307-127">The application-defined function in the following C++ code example returns the index of the working area to which the item belongs.</span></span> <span data-ttu-id="81307-128">Se a função falhar, ela retornará – 1.</span><span class="sxs-lookup"><span data-stu-id="81307-128">If the function fails, it returns –1.</span></span> <span data-ttu-id="81307-129">Se a função for realizada com sucesso, mas o item não estiver dentro de nenhuma das áreas de trabalho, a função retornará 0, porque todos os itens que não estão dentro de uma área de trabalho se tornam automaticamente um membro da área de trabalho zero.</span><span class="sxs-lookup"><span data-stu-id="81307-129">If the function succeeds, but the item is not inside any of the working areas, the function returns 0, because all items that are not inside a working area automatically become a member of working area zero.</span></span>


```C++
int GetItemWorkingArea(HWND hWndListView, int iItem)
{
    UINT     uWorkAreas = 0;
    int      nReturn = -1;
    LPRECT   pRects;
    POINT    pt;
    
    if(!ListView_GetItemPosition(hWndListView, iItem, &pt))
        return nReturn;
    
    ListView_GetNumberOfWorkAreas(hWndListView, &uWorkAreas);
    
    if(uWorkAreas)
    {
        pRects = (LPRECT)GlobalAlloc(GPTR, sizeof(RECT) * uWorkAreas);
        
        if(pRects)
        {
            UINT  i;
            nReturn = 0;
    
            ListView_GetWorkAreas(hWndListView, uWorkAreas, pRects);
          
            for(i = 0; i < uWorkAreas; i++)
            {
                if(PtInRect((pRects + i), pt))
                {
                    nReturn = i;
                    break;
                }
            }
            GlobalFree((HGLOBAL)pRects);
        }
    }
    return nReturn;
}

```



## <a name="related-topics"></a><span data-ttu-id="81307-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="81307-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81307-131">Referência de controle de exibição de lista</span><span class="sxs-lookup"><span data-stu-id="81307-131">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="81307-132">Sobre controles de List-View</span><span class="sxs-lookup"><span data-stu-id="81307-132">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="81307-133">Usando controles de List-View</span><span class="sxs-lookup"><span data-stu-id="81307-133">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




