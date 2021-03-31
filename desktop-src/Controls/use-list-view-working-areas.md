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
# <a name="how-to-use-list-view-working-areas"></a>Como usar List-View áreas de trabalho

Este tópico demonstra como trabalhar com áreas de trabalho do modo de exibição de lista. Áreas de trabalho são áreas virtuais retangulares que podem ser usadas para organizar itens em um controle List-exibição. Uma área de trabalho não é uma janela e não pode ter uma borda visível. Por padrão, o controle de exibição de lista não tem áreas de trabalho. Ao criar uma área de trabalho, você pode criar uma borda vazia à esquerda, à parte superior ou à direita dos itens ou fazer com que uma barra de rolagem horizontal seja exibida quando normalmente não haveria uma.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="create-a-working-area"></a>Criar uma área de trabalho

O exemplo de código C++ a seguir demonstra como criar uma área de trabalho com uma borda vazia de 25 pixels nos lados superior, esquerda e direito.


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



### <a name="create-multiple-working-areas"></a>Criar várias áreas de trabalho

O exemplo de código C++ a seguir demonstra como criar duas áreas de trabalho em um controle. Cada área de trabalho usa cerca de metade da área do cliente e é circundada por uma borda vazia de 25 pixels.


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



### <a name="determine-the-working-area-to-which-an-item-belongs"></a>Determinar a área de trabalho à qual um item pertence

Uma maneira de determinar qual área de trabalho um item pertence é fazer o seguinte:

-   Recupere a lista de coordenadas de todas as áreas de trabalho no controle de exibição de lista.
-   Recupere as coordenadas do item.
-   Determine se as coordenadas de item estão dentro das coordenadas de uma das áreas de trabalho.

A função definida pelo aplicativo no exemplo de código C++ a seguir retorna o índice da área de trabalho à qual o item pertence. Se a função falhar, ela retornará – 1. Se a função for realizada com sucesso, mas o item não estiver dentro de nenhuma das áreas de trabalho, a função retornará 0, porque todos os itens que não estão dentro de uma área de trabalho se tornam automaticamente um membro da área de trabalho zero.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle de exibição de lista](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Sobre controles de List-View](list-view-controls-overview.md)
</dt> <dt>

[Usando controles de List-View](using-list-view-controls.md)
</dt> </dl>

 

 




