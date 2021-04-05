---
title: Código de notificação de NM_CUSTOMDRAW (exibição em árvore) (commctrl. h)
description: Enviado por um controle de exibição de árvore para notificar sua janela pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- Código de notificação de NM_CUSTOMDRAW (exibição de árvore) controles do Windows
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3f7b44748c2ac9c5b9651c079a8b90df0c508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824166"
---
# <a name="nm_customdraw-tree-view-notification-code"></a><span data-ttu-id="4ec6d-105">\_Código de notificação nm CUSTOMDRAW (exibição em árvore)</span><span class="sxs-lookup"><span data-stu-id="4ec6d-105">NM\_CUSTOMDRAW (tree view) notification code</span></span>

<span data-ttu-id="4ec6d-106">Enviado por um controle de exibição de árvore para notificar sua janela pai sobre operações de desenho.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-106">Sent by a tree-view control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="4ec6d-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4ec6d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="4ec6d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ec6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ec6d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ec6d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ec6d-110">Ponteiro para uma estrutura [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) que contém e recebe informações sobre a operação de desenho.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-110">Pointer to an [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure that contains and receives information about the drawing operation.</span></span> <span data-ttu-id="4ec6d-111">O membro **dwItemSpec** do membro **nmcd** dessa estrutura contém o identificador do item que está sendo desenhado.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-111">The **dwItemSpec** member of the **nmcd** member of this structure contains the handle of the item being drawn.</span></span> <span data-ttu-id="4ec6d-112">O membro **lItemlParam** do membro **nmcd** dessa estrutura contém o *lParam* do item que está sendo desenhado.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-112">The **lItemlParam** member of the **nmcd** member of this structure contains the *lParam* of the item being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ec6d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ec6d-113">Return value</span></span>

<span data-ttu-id="4ec6d-114">O valor que seu aplicativo pode retornar depende do estágio de desenho atual.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="4ec6d-115">O membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica o estágio de desenho.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="4ec6d-116">Você deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-116">You must return one of the following values.</span></span>



| <span data-ttu-id="4ec6d-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4ec6d-117">Return code</span></span>                                                                                            | <span data-ttu-id="4ec6d-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ec6d-118">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4ec6d-119"><dt>**dopadrão CDRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4ec6d-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="4ec6d-120">O controle se desenha.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-120">The control draws itself.</span></span> <span data-ttu-id="4ec6d-121">Ele não envia nenhum código [ \_ CUSTOMDRAW de nm](nm-customdraw.md) adicional para este ciclo de pintura.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-121">It does not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) codes for this paint cycle.</span></span> <span data-ttu-id="4ec6d-122">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="4ec6d-123"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="4ec6d-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="4ec6d-124">O controle notifica o pai de qualquer operação de desenho relacionada a itens.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-124">The control notifies the parent of any item-related drawing operations.</span></span> <span data-ttu-id="4ec6d-125">Ele envia códigos de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) antes e depois de itens de desenho.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-125">It sends [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="4ec6d-126">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                |
| <dl> <span data-ttu-id="4ec6d-127"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="4ec6d-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="4ec6d-128">O controle notifica o pai depois de apagar um item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-128">The control notifies the parent after erasing an item.This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="4ec6d-129"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="4ec6d-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="4ec6d-130">O controle notifica o pai depois de pintar um item.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-130">The control notifies the parent after painting an item.</span></span> <span data-ttu-id="4ec6d-131">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="4ec6d-132"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="4ec6d-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | [<span data-ttu-id="4ec6d-133">Versão 4,71.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-133">Version 4.71.</span></span>](common-control-versions.md) <span data-ttu-id="4ec6d-134">O controle notifica o pai quando um subitem de exibição de lista está sendo desenhado.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-134">The control notifies the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="4ec6d-135">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="4ec6d-136"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="4ec6d-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="4ec6d-137">Seu aplicativo especificou uma nova fonte para o item; o controle usará a nova fonte.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="4ec6d-138">Para obter mais informações sobre como alterar fontes, consulte [alterando fontes e cores](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="4ec6d-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="4ec6d-139">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="4ec6d-140"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="4ec6d-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="4ec6d-141">Seu aplicativo desenhou o item manualmente.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-141">Your application drew the item manually.</span></span> <span data-ttu-id="4ec6d-142">O controle não vai desenhar o item.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-142">The control will not draw the item.</span></span> <span data-ttu-id="4ec6d-143">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="4ec6d-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ec6d-144">Remarks</span></span>

[<span data-ttu-id="4ec6d-145">Versão 5,80.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-145">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="4ec6d-146">Se você alterar a fonte retornando [**CDRF \_ NEWFONT**](cdrf-constants.md), o controle de exibição de árvore poderá exibir o texto recortado.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-146">If you change the font by returning [**CDRF\_NEWFONT**](cdrf-constants.md), the tree-view control might display clipped text.</span></span> <span data-ttu-id="4ec6d-147">Esse comportamento é necessário para compatibilidade com versões anteriores dos controles comuns.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-147">This behavior is necessary for backward compatibility with earlier versions of the common controls.</span></span> <span data-ttu-id="4ec6d-148">Se você quiser alterar a fonte de um controle de exibição de árvore, obterá resultados melhores se enviar uma mensagem [**CCM \_ SetVersion**](ccm-setversion.md) com o valor *wParam* definido como 5 antes de adicionar qualquer item ao controle.</span><span class="sxs-lookup"><span data-stu-id="4ec6d-148">If you want to change the font of a tree-view control, you will get better results if you send a [**CCM\_SETVERSION**](ccm-setversion.md) message with the *wParam* value set to 5 before adding any items to the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ec6d-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ec6d-149">Requirements</span></span>



| <span data-ttu-id="4ec6d-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ec6d-150">Requirement</span></span> | <span data-ttu-id="4ec6d-151">Valor</span><span class="sxs-lookup"><span data-stu-id="4ec6d-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ec6d-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ec6d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4ec6d-153">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ec6d-153">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4ec6d-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ec6d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4ec6d-155">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4ec6d-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ec6d-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ec6d-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ec6d-157"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ec6d-157"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ec6d-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ec6d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec6d-159">Usando o desenho personalizado</span><span class="sxs-lookup"><span data-stu-id="4ec6d-159">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





