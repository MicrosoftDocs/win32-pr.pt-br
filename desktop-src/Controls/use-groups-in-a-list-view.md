---
title: Como usar grupos em um List-View
description: Este tópico descreve como criar uma instância de um grupo e adicioná-lo a um controle de exibição de lista.
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec47d73c3e8b808eaf1909bdafb015c7eebc37de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103824070"
---
# <a name="how-to-use-groups-in-a-list-view"></a>Como usar grupos em um List-View

Este tópico descreve como criar uma instância de um grupo e adicioná-lo a um controle de exibição de lista. O agrupamento permite que um usuário organize listas em grupos de itens que são visualmente divididos na página, usando um divisor horizontal e um título de grupo.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Para usar grupos em um controle de exibição de lista, verifique se o controle inclui o estilo de janela [**LVS \_ ALIGNTOP**](list-view-window-styles.md) .

Quando você adiciona um item à lista, você o atribui a um grupo definindo o membro **iGroupId** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) do item como o valor do membro **iGroupId** da estrutura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) dos grupos. Um item que não está atribuído a um grupo não aparece na lista quando o modo de exibição de grupo está habilitado. Para habilitar ou desabilitar a exibição de grupo, use a macro [**\_ EnableGroupView do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) .

O exemplo a seguir mostra como criar um grupo com um cabeçalho e adicioná-lo a um controle de exibição de lista.


```C++
    LVGROUP group;

    group.cbSize    = sizeof(LVGROUP);
    group.mask      = LVGF_HEADER | LVGF_GROUPID;
    group.pszHeader = TEXT("Dogs");
    group.iGroupId  = 1;

    ListView_InsertGroup(hWndListView, -1, &group);

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle de exibição de lista](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Sobre controles de List-View](list-view-controls-overview.md)
</dt> <dt>

[Usando controles de List-View](using-list-view-controls.md)
</dt> </dl>

 

 




