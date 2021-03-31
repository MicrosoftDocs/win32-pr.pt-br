---
title: Como adicionar um item a um controle de cabeçalho
description: Este tópico demonstra como adicionar um item a um controle de cabeçalho.
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cf020c95a9dfe06bb06370533fdfd9416ddfef
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917806"
---
# <a name="how-to-add-an-item-to-a-header-control"></a>Como adicionar um item a um controle de cabeçalho

Este tópico demonstra como adicionar um item a um controle de cabeçalho. Um controle de cabeçalho normalmente tem vários itens de cabeçalho que definem as colunas do controle. Você pode adicionar um item a um controle de cabeçalho enviando a mensagem [**HDM \_ INSERTITEM**](hdm-insertitem.md) para o controle.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Use a mensagem [**HDM \_ INSERTITEM**](hdm-insertitem.md) para adicionar um item ao controle de cabeçalho. A mensagem deve incluir o endereço de uma estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) . Essa estrutura define as propriedades do item de cabeçalho, que pode incluir uma cadeia de caracteres, uma imagem de bitmap, um tamanho inicial e um valor de 32 bits definido pelo aplicativo.

O exemplo a seguir ilustra como usar a mensagem [**HDM \_ INSERTITEM**](hdm-insertitem.md) e a estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) para adicionar um item a um controle de cabeçalho. O novo item consiste em uma cadeia de caracteres que é justificada à esquerda dentro do retângulo do item.



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

[Sobre controles de cabeçalho](header-controls.md)
</dt> <dt>

[Referência de controle de cabeçalho](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Usando controles de cabeçalho](using-header-controls.md)
</dt> </dl>

 

 




