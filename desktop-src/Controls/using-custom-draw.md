---
title: Usando o desenho personalizado
description: Esta seção contém exemplos que demonstram como implementar o desenho personalizado.
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0b8a2585103aa27a27f0138a49885cc726d3b1
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104007170"
---
# <a name="using-custom-draw"></a>Usando o desenho personalizado

Esta seção contém exemplos que demonstram como implementar o desenho personalizado.

O fragmento de código a seguir é uma parte de um manipulador de [**\_ notificação do WM**](wm-notify.md) que ilustra como lidar com notificações de desenho personalizadas enviadas a um controle de exibição de lista.


```C++
        
LPNMLISTVIEW  pnm  = (LPNMLISTVIEW)lParam;

switch (pnm->hdr.code){
...
case NM_CUSTOMDRAW:

    LPNMLVCUSTOMDRAW  lplvcd = (LPNMLVCUSTOMDRAW)lParam;

    switch(lplvcd->nmcd.dwDrawStage) {

    case CDDS_PREPAINT :
        return CDRF_NOTIFYITEMDRAW;

    case CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForItem(lplvcd->nmcd.dwItemSpec,
                                    lplvcd->nmcd.lItemlParam) );
        lplvcd->clrText = GetColorForItem(lplvcd->nmcd.dwItemSpec,
                                          lplvcd->nmcd.lItemlParam);
        lplvcd->clrTextBk = GetBkColorForItem(lplvcd->nmcd.dwItemSpec,
                                              lplvcd->nmcd.lItemlParam);

/* At this point, you can change the background colors for the item
and any subitems and return CDRF_NEWFONT. If the list-view control
is in report mode, you can simply return CDRF_NOTIFYSUBITEMDRAW
to customize the item's subitems individually */
        ...

        return CDRF_NEWFONT;
    //  or return CDRF_NOTIFYSUBITEMDRAW;

    case CDDS_SUBITEM | CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForSubItem(lplvcd->nmcd.dwItemSpec,
                                       lplvcd->nmcd.lItemlParam,
                                       lplvcd->iSubItem));
        lplvcd->clrText = GetColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                             lplvcd->nmcd.lItemlParam,
                                             lplvcd->iSubItem));
        lplvcd->clrTextBk = GetBkColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                                 lplvcd->nmcd.lItemlParam,
                                                 lplvcd->iSubItem));

/* This notification is received only if you are in report mode and
returned CDRF_NOTIFYSUBITEMDRAW in the previous step. At
this point, you can change the background colors for the
subitem and return CDRF_NEWFONT.*/
        ...
        return CDRF_NEWFONT;    
    }
...
}
        
```



A primeira notificação de [ \_ CUSTOMDRAW nm](nm-customdraw.md) tem o membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) definida como **CDDs \_ PrePaint**. O manipulador retorna [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) para indicar que deseja modificar um ou mais itens individualmente.

Se [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) for retornado na etapa anterior, a próxima notificação [de \_ CUSTOMDRAW do nm](nm-customdraw.md) terá **dwDrawStage** definido como **CDDs \_ ITEMPREPAINT**. O manipulador recupera a cor atual e os valores de fonte. Neste ponto, você pode especificar novos valores para os modos pequeno, ícone grande e lista. Se o controle estiver no modo de relatório, você também poderá especificar novos valores que serão aplicados a todos os subitens do item. Se você alterou alguma coisa, retorne [**CDRF \_ NEWFONT**](cdrf-constants.md). Se o controle estiver no modo de relatório e você quiser manipular os subitens individualmente, retorne **CDRF \_ NOTIFYSUBITEMDRAW**.

A notificação final só será enviada se o controle estiver no modo de relatório e você tiver retornado **CDRF \_ NOTIFYSUBITEMDRAW** na etapa anterior. O procedimento para alterar fontes e cores é o mesmo que essa etapa, mas só se aplica a um único subitem. Retorne [**CDRF \_ NEWFONT**](cdrf-constants.md) para notificar o controle se a cor ou a fonte foram alteradas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Sobre o desenho personalizado](about-custom-draw.md)
</dt> <dt>

[Referência de desenho Personalizada](custom-draw-reference.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[EXEMPLO: CustDTv ilustra o desenho personalizado em um TreeView (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




