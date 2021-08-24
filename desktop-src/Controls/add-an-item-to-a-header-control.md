---
title: Como adicionar um item a um controle de header
description: Este tópico demonstra como adicionar um item a um controle de header.
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4face974c1b04021afdc9e26976c023e1287439eb3d6d63c7ea7f9f34c5b27f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922046"
---
# <a name="how-to-add-an-item-to-a-header-control"></a>Como adicionar um item a um controle de header

Este tópico demonstra como adicionar um item a um controle de header. Um controle de header normalmente tem vários itens de header que definem as colunas do controle. Você pode adicionar um item a um controle de header enviando a mensagem [**\_ INSERTITEM do HDM**](hdm-insertitem.md) para o controle.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções


Use a [**mensagem HDM \_ INSERTITEM**](hdm-insertitem.md) para adicionar um item ao controle de header. A mensagem deve incluir o endereço de uma [**estrutura HDITEM.**](/windows/win32/api/commctrl/ns-commctrl-hditema) Essa estrutura define as propriedades do item de header, que podem incluir uma cadeia de caracteres, uma imagem mapeada, um tamanho inicial e um valor de 32 bits definido pelo aplicativo.

O exemplo a seguir ilustra como usar a mensagem [**\_ INSERTITEM do HDM**](hdm-insertitem.md) e a estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) para adicionar um item a um controle de header. O novo item consiste em uma cadeia de caracteres justificada à esquerda dentro do retângulo do item.



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre controles de header](header-controls.md)
</dt> <dt>

[Referência de controle de header](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Usando controles de header](using-header-controls.md)
</dt> </dl>

 

 




