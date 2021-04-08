---
title: Código de notificação NM_CUSTOMDRAW (TrackBar) (commctrl. h)
description: Enviado por um controle TrackBar para notificar suas janelas pai sobre as operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- TrackBar (código de notificação de NM_CUSTOMDRAW) controles do Windows
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
ms.openlocfilehash: 68ebbffd531fb44e2491d72954ce111db208f2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086536"
---
# <a name="nm_customdraw-trackbar-notification-code"></a><span data-ttu-id="96077-105">\_Código de notificação nm CUSTOMDRAW (TrackBar)</span><span class="sxs-lookup"><span data-stu-id="96077-105">NM\_CUSTOMDRAW (trackbar) notification code</span></span>

<span data-ttu-id="96077-106">Enviado por um controle TrackBar para notificar suas janelas pai sobre as operações de desenho.</span><span class="sxs-lookup"><span data-stu-id="96077-106">Sent by a trackbar control to notify its parent windows about drawing operations.</span></span> <span data-ttu-id="96077-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="96077-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="96077-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96077-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96077-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96077-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96077-110">Ponteiro para uma estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contém informações sobre a operação de desenho.</span><span class="sxs-lookup"><span data-stu-id="96077-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="96077-111">O membro **dwItemSpec** dessa estrutura conterá um dos [valores personalizados Draw](custom-draw-values.md) que indica qual parte do controle está sendo desenhada.</span><span class="sxs-lookup"><span data-stu-id="96077-111">The **dwItemSpec** member of this structure will contain one of the [Custom Draw Values](custom-draw-values.md) that indicates which part of the control is being drawn.</span></span> <span data-ttu-id="96077-112">Os controles TrackBar inserem os seguintes valores no membro **dwItemSpec** dessa estrutura para identificar a parte do controle que está sendo desenhado:</span><span class="sxs-lookup"><span data-stu-id="96077-112">Trackbar controls insert the following values into the **dwItemSpec** member of this structure to identify the portion of the control being drawn:</span></span>



| <span data-ttu-id="96077-113">Valor</span><span class="sxs-lookup"><span data-stu-id="96077-113">Value</span></span>                                                                                                                                                      | <span data-ttu-id="96077-114">Significado</span><span class="sxs-lookup"><span data-stu-id="96077-114">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="96077-115"><dt>**\_canal TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="96077-115"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="96077-116">Identifica o canal no qual o marcador de Thumb do controle de TrackBar desliza.</span><span class="sxs-lookup"><span data-stu-id="96077-116">Identifies the channel that the trackbar control's thumb marker slides along.</span></span> <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="96077-117"><dt>**TBCD \_ Thumb**</dt></span><span class="sxs-lookup"><span data-stu-id="96077-117"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="96077-118">Identifica o marcador de miniatura do controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="96077-118">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="96077-119">Essa é a parte do controle que o usuário move.</span><span class="sxs-lookup"><span data-stu-id="96077-119">This is the portion of the control that the user moves.</span></span> <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="96077-120"><dt>**TBCD \_ TICS**</dt></span><span class="sxs-lookup"><span data-stu-id="96077-120"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="96077-121">Identifica as marcas de escala de incremento que aparecem ao longo da borda do controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="96077-121">Identifies the increment tick marks that appear along the edge of the trackbar control.</span></span> <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96077-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96077-122">Return value</span></span>

<span data-ttu-id="96077-123">O valor que seu aplicativo pode retornar depende do estágio de desenho atual.</span><span class="sxs-lookup"><span data-stu-id="96077-123">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="96077-124">O membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica o estágio de desenho.</span><span class="sxs-lookup"><span data-stu-id="96077-124">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="96077-125">Você deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="96077-125">You must return one of the following values.</span></span>



| <span data-ttu-id="96077-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="96077-126">Return code</span></span>                                                                                            | <span data-ttu-id="96077-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="96077-127">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96077-128"><dt>**dopadrão CDRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="96077-128"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="96077-129">O controle será desenhado em si mesmo.</span><span class="sxs-lookup"><span data-stu-id="96077-129">The control will draw itself.</span></span> <span data-ttu-id="96077-130">Ele não enviará nenhum código de notificação [ \_ CUSTOMDRAW de nm](nm-customdraw.md) adicional para este ciclo de pintura.</span><span class="sxs-lookup"><span data-stu-id="96077-130">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="96077-131">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="96077-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="96077-132"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="96077-132"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="96077-133">O controle notificará o pai de qualquer operação de desenho relacionada a itens.</span><span class="sxs-lookup"><span data-stu-id="96077-133">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="96077-134">Ele enviará códigos de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) antes e depois de itens de desenho.</span><span class="sxs-lookup"><span data-stu-id="96077-134">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="96077-135">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="96077-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                         |
| <dl> <span data-ttu-id="96077-136"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="96077-136"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="96077-137">O controle notificará o pai depois de apagar um item.</span><span class="sxs-lookup"><span data-stu-id="96077-137">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="96077-138">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="96077-138">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="96077-139"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="96077-139"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="96077-140">O controle notificará o pai depois de pintar um item.</span><span class="sxs-lookup"><span data-stu-id="96077-140">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="96077-141">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="96077-141">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="96077-142"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="96077-142"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="96077-143">[Versão 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="96077-143">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="96077-144">O controle notificará o pai quando um subitem de exibição de lista estiver sendo desenhado.</span><span class="sxs-lookup"><span data-stu-id="96077-144">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="96077-145">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="96077-145">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="96077-146"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="96077-146"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="96077-147">Seu aplicativo especificou uma nova fonte para o item; o controle usará a nova fonte.</span><span class="sxs-lookup"><span data-stu-id="96077-147">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="96077-148">Para obter mais informações sobre como alterar fontes, consulte [alterando fontes e cores](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="96077-148">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="96077-149">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="96077-149">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="96077-150"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="96077-150"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="96077-151">Seu aplicativo desenhou o item manualmente.</span><span class="sxs-lookup"><span data-stu-id="96077-151">Your application drew the item manually.</span></span> <span data-ttu-id="96077-152">O controle não vai desenhar o item.</span><span class="sxs-lookup"><span data-stu-id="96077-152">The control will not draw the item.</span></span> <span data-ttu-id="96077-153">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="96077-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="96077-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96077-154">Requirements</span></span>



| <span data-ttu-id="96077-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="96077-155">Requirement</span></span> | <span data-ttu-id="96077-156">Valor</span><span class="sxs-lookup"><span data-stu-id="96077-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96077-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96077-157">Minimum supported client</span></span><br/> | <span data-ttu-id="96077-158">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96077-158">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96077-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96077-159">Minimum supported server</span></span><br/> | <span data-ttu-id="96077-160">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96077-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96077-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96077-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="96077-162"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="96077-162"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96077-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="96077-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96077-164">Usando o desenho personalizado</span><span class="sxs-lookup"><span data-stu-id="96077-164">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





