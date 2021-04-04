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
# <a name="using-custom-draw"></a><span data-ttu-id="aeab7-103">Usando o desenho personalizado</span><span class="sxs-lookup"><span data-stu-id="aeab7-103">Using Custom Draw</span></span>

<span data-ttu-id="aeab7-104">Esta seção contém exemplos que demonstram como implementar o desenho personalizado.</span><span class="sxs-lookup"><span data-stu-id="aeab7-104">This section contains examples that demonstrate how to implement custom draw.</span></span>

<span data-ttu-id="aeab7-105">O fragmento de código a seguir é uma parte de um manipulador de [**\_ notificação do WM**](wm-notify.md) que ilustra como lidar com notificações de desenho personalizadas enviadas a um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="aeab7-105">The following code fragment is a portion of a [**WM\_NOTIFY**](wm-notify.md) handler that illustrates how to handle custom draw notifications sent to a list-view control.</span></span>


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



<span data-ttu-id="aeab7-106">A primeira notificação de [ \_ CUSTOMDRAW nm](nm-customdraw.md) tem o membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) definida como **CDDs \_ PrePaint**.</span><span class="sxs-lookup"><span data-stu-id="aeab7-106">The first [NM\_CUSTOMDRAW](nm-customdraw.md) notification has the **dwDrawStage** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure set to **CDDS\_PREPAINT**.</span></span> <span data-ttu-id="aeab7-107">O manipulador retorna [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) para indicar que deseja modificar um ou mais itens individualmente.</span><span class="sxs-lookup"><span data-stu-id="aeab7-107">The handler returns [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) to indicate that it wishes to modify one or more items individually.</span></span>

<span data-ttu-id="aeab7-108">Se [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) for retornado na etapa anterior, a próxima notificação [de \_ CUSTOMDRAW do nm](nm-customdraw.md) terá **dwDrawStage** definido como **CDDs \_ ITEMPREPAINT**.</span><span class="sxs-lookup"><span data-stu-id="aeab7-108">If [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) was returned in the previous step, the next [NM\_CUSTOMDRAW](nm-customdraw.md) notification has **dwDrawStage** set to **CDDS\_ITEMPREPAINT**.</span></span> <span data-ttu-id="aeab7-109">O manipulador recupera a cor atual e os valores de fonte.</span><span class="sxs-lookup"><span data-stu-id="aeab7-109">The handler retrieves the current color and font values.</span></span> <span data-ttu-id="aeab7-110">Neste ponto, você pode especificar novos valores para os modos pequeno, ícone grande e lista.</span><span class="sxs-lookup"><span data-stu-id="aeab7-110">At this point, you can specify new values for small icon, large icon, and list modes.</span></span> <span data-ttu-id="aeab7-111">Se o controle estiver no modo de relatório, você também poderá especificar novos valores que serão aplicados a todos os subitens do item.</span><span class="sxs-lookup"><span data-stu-id="aeab7-111">If the control is in report mode, you can also specify new values that will apply to all subitems of the item.</span></span> <span data-ttu-id="aeab7-112">Se você alterou alguma coisa, retorne [**CDRF \_ NEWFONT**](cdrf-constants.md).</span><span class="sxs-lookup"><span data-stu-id="aeab7-112">If you have changed anything, return [**CDRF\_NEWFONT**](cdrf-constants.md).</span></span> <span data-ttu-id="aeab7-113">Se o controle estiver no modo de relatório e você quiser manipular os subitens individualmente, retorne **CDRF \_ NOTIFYSUBITEMDRAW**.</span><span class="sxs-lookup"><span data-stu-id="aeab7-113">If the control is in report mode and you want to handle the subitems individually, return **CDRF\_NOTIFYSUBITEMDRAW**.</span></span>

<span data-ttu-id="aeab7-114">A notificação final só será enviada se o controle estiver no modo de relatório e você tiver retornado **CDRF \_ NOTIFYSUBITEMDRAW** na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="aeab7-114">The final notification is only sent if the control is in report mode and you returned **CDRF\_NOTIFYSUBITEMDRAW** in the previous step.</span></span> <span data-ttu-id="aeab7-115">O procedimento para alterar fontes e cores é o mesmo que essa etapa, mas só se aplica a um único subitem.</span><span class="sxs-lookup"><span data-stu-id="aeab7-115">The procedure for changing fonts and colors is the same as that step, but it only applies to a single subitem.</span></span> <span data-ttu-id="aeab7-116">Retorne [**CDRF \_ NEWFONT**](cdrf-constants.md) para notificar o controle se a cor ou a fonte foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="aeab7-116">Return [**CDRF\_NEWFONT**](cdrf-constants.md) to notify the control if the color or font was changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aeab7-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aeab7-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="aeab7-118">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="aeab7-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aeab7-119">Sobre o desenho personalizado</span><span class="sxs-lookup"><span data-stu-id="aeab7-119">About Custom Draw</span></span>](about-custom-draw.md)
</dt> <dt>

[<span data-ttu-id="aeab7-120">Referência de desenho Personalizada</span><span class="sxs-lookup"><span data-stu-id="aeab7-120">Custom Draw Reference</span></span>](custom-draw-reference.md)
</dt> <dt>

<span data-ttu-id="aeab7-121">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="aeab7-121">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="aeab7-122">EXEMPLO: CustDTv ilustra o desenho personalizado em um TreeView (Q248496)</span><span class="sxs-lookup"><span data-stu-id="aeab7-122">SAMPLE: CustDTv Illustrates Custom Draw in a TreeView (Q248496)</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




