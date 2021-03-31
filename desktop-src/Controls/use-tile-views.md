---
title: Como usar exibições de bloco
description: Este tópico demonstra como definir o modo de exibição de bloco para um controle de exibição de lista.
ms.assetid: BDE17F4B-3A15-48BB-8160-036AD0DC3B41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616a9bb8a2c1707d903f0ebe2b6de86511dc6ce4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917793"
---
# <a name="how-to-use-tile-views"></a>Como usar exibições de bloco

Este tópico demonstra como definir o modo de exibição de bloco para um controle de exibição de lista. No modo de exibição de bloco, cada item é representado por um ícone grande com uma ou mais linhas do texto que o acompanha. Para obter uma ilustração, consulte [sobre controles de List-View](list-view-controls-overview.md).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Defina os parâmetros de exibição gerais para exibição de bloco usando a macro [**\_ SetTileViewInfo do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) . Use a estrutura [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) que é passada para esta macro para especificar a posição do texto em relação ao ícone, o tamanho de cada bloco (incluindo o texto de acompanhamento) e o número máximo de linhas de texto.

Se você não quiser que os blocos sejam dimensionados automaticamente, você deve definir **LVTVIF \_ FIXEDSIZE** no membro **dwFlags** e **LVTVIM \_ tileize** no membro **dwMask** de [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), bem como fornecendo as dimensões no membro **sizeTile** .

O exemplo de código C++ a seguir define as informações de exibição de bloco para um controle de exibição de lista para que um máximo de dois subitens sejam exibidos para cada item. Ele também define o tamanho de cada bloco.


```C++
    SIZE size = { 100, 50 };
    LVTILEVIEWINFO tileViewInfo = {0};

    tileViewInfo.cbSize   = sizeof(tileViewInfo);
    tileViewInfo.dwFlags  = LVTVIF_FIXEDSIZE;
    tileViewInfo.dwMask   = LVTVIM_COLUMNS | LVTVIM_TILESIZE;
    tileViewInfo.cLines   = 2;
    tileViewInfo.sizeTile = size;

    ListView_SetTileViewInfo(hWndListView, &tileViewInfo);

```



Para cada item na lista, você pode definir parâmetros adicionais quando o item é inserido na lista ou posteriormente. A estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que é usada com [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contém membros que especificam quais colunas de dados serão exibidas abaixo do item e seu alinhamento. Esses mesmos parâmetros de exibição também são encontrados na estrutura [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) usada com [**ListView \_ SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).

> [!Note]  
> "Columns" aqui refere-se a não exibir colunas no modo de exibição de bloco, mas em subitens, que são exibidos em colunas na exibição de detalhes.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle de exibição de lista](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Sobre controles de List-View](list-view-controls-overview.md)
</dt> <dt>

[Usando controles de List-View](using-list-view-controls.md)
</dt> </dl>

 

 




