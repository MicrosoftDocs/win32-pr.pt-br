---
title: Usando o desenho personalizado
description: Esta seção contém exemplos que demonstram como implementar o desenho personalizado.
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90cff5fd4d692d31b69c85980f872f3aca4504cad81a3439d0c4d31a4c73d90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655866"
---
# <a name="using-custom-draw"></a>Usando o desenho personalizado

Esta seção contém exemplos que demonstram como implementar o desenho personalizado.

O fragmento de código a seguir é uma parte de um manipulador [**WM \_ NOTIFY**](wm-notify.md) que ilustra como lidar com notificações de desenho personalizadas enviadas para um controle de exibição de lista.


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



A primeira [notificação \_ customDRAW NM](nm-customdraw.md) tem o **membro dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) definido como **CDDS \_ PREPAINT.** O manipulador retorna [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) para indicar que deseja modificar um ou mais itens individualmente.

Se [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) tiver sido retornado na etapa anterior, a próxima notificação [ \_ NM CUSTOMDRAW](nm-customdraw.md) terá **dwDrawStage** definido como **CDDS \_ ITEMPREPAINT**. O manipulador recupera os valores de fonte e cor atuais. Neste ponto, você pode especificar novos valores para ícone pequeno, ícone grande e modos de lista. Se o controle estiver no modo de relatório, você também poderá especificar novos valores que serão aplicados a todos os subitens do item. Se você tiver alterado alguma coisa, retorne [**CDRF \_ NEWFONT.**](cdrf-constants.md) Se o controle estiver no modo de relatório e você quiser manipular os subitens individualmente, retorne **CDRF \_ NOTIFYSUBITEMDRAW**.

A notificação final só será enviada se o controle estiver no modo de relatório e você tiver retornado **CDRF \_ NOTIFYSUBITEMDRAW** na etapa anterior. O procedimento para alterar fontes e cores é o mesmo que essa etapa, mas só se aplica a um único subitem. Retorne [**CDRF \_ NEWFONT para**](cdrf-constants.md) notificar o controle se a cor ou a fonte foi alterada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Sobre o desenho personalizado](about-custom-draw.md)
</dt> <dt>

[Referência de desenho personalizado](custom-draw-reference.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[EXEMPLO: CustDTv ilustra o desenho personalizado em um TreeView (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




