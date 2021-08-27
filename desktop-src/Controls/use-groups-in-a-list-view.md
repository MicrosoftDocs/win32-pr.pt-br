---
title: Como usar grupos em um List-View
description: Este tópico descreve como criar uma instância de um grupo e adicioná-la a um controle de exibição de lista.
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edaad657d9ea6b71bac1d06a34a0aa29b99c26e204629e503a9e55531da162b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132116"
---
# <a name="how-to-use-groups-in-a-list-view"></a>Como usar grupos em um List-View

Este tópico descreve como criar uma instância de um grupo e adicioná-la a um controle de exibição de lista. O agrupamento permite que um usuário organize listas em grupos de itens que são divididos visualmente na página, usando um divisor horizontal e um título de grupo.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções


Para usar grupos em um controle de exibição de lista, verifique se o controle inclui o estilo de janela [**LVS \_ ALIGNTOP.**](list-view-window-styles.md)

Ao adicionar um item à lista, atribua-o a um grupo definindo o membro **iGroupId** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) do item como o valor do **membro iGroupId** da estrutura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) dos grupos. Um item que não está atribuído a um grupo não aparece na lista quando a exibição de grupo está habilitada. Para habilitar ou desabilitar a exibição de grupo, use a macro [**ListView \_ EnableGroupView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview)

O exemplo a seguir mostra como criar um grupo com um header e adicioná-lo a um controle de exibição de lista.


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

[Sobre List-View controles](list-view-controls-overview.md)
</dt> <dt>

[Usando List-View controles](using-list-view-controls.md)
</dt> </dl>

 

 




