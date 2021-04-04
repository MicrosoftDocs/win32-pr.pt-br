---
title: Código de notificação de NM_CUSTOMDRAW (dica de ferramenta) (commctrl. h)
description: Enviado por um controle ToolTip para notificar sua janela pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 82939901-baed-452b-85bf-3c0c01e1f5df
keywords:
- Código de notificação de NM_CUSTOMDRAW (dica de ferramenta) controles do Windows
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
ms.openlocfilehash: 9ce1047f63c8580051f7d57abf3308bde37238a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645269"
---
# <a name="nm_customdraw-tooltip-notification-code"></a><span data-ttu-id="e1d8c-105">\_Código de notificação nm CUSTOMDRAW (dica de ferramenta)</span><span class="sxs-lookup"><span data-stu-id="e1d8c-105">NM\_CUSTOMDRAW (tooltip) notification code</span></span>

<span data-ttu-id="e1d8c-106">Enviado por um controle ToolTip para notificar sua janela pai sobre operações de desenho.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-106">Sent by a tooltip control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="e1d8c-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e1d8c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e1d8c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1d8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1d8c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1d8c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1d8c-110">Ponteiro para uma estrutura [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) que contém informações sobre a operação de desenho.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-110">Pointer to an [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) structure that contains information about the drawing operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1d8c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1d8c-111">Return value</span></span>

<span data-ttu-id="e1d8c-112">O valor que seu aplicativo pode retornar depende do estágio de desenho atual.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-112">The value that your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="e1d8c-113">O membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica o estágio de desenho.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-113">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="e1d8c-114">Você deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-114">You must return one of the following values.</span></span>



| <span data-ttu-id="e1d8c-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e1d8c-115">Return code</span></span>                                                                                            | <span data-ttu-id="e1d8c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1d8c-116">Description</span></span>                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e1d8c-117"><dt>**dopadrão CDRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e1d8c-117"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="e1d8c-118">O controle será desenhado em si mesmo.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-118">The control will draw itself.</span></span> <span data-ttu-id="e1d8c-119">Ele não enviará nenhum código de notificação [ \_ CUSTOMDRAW de nm](nm-customdraw.md) adicional para este ciclo de pintura.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-119">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="e1d8c-120">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-120">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="e1d8c-121"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="e1d8c-121"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="e1d8c-122">O controle notificará o pai de qualquer operação de desenho relacionada a itens.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-122">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="e1d8c-123">Ele enviará códigos de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) antes e depois de itens de desenho.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-123">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="e1d8c-124">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-124">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                            |
| <dl> <span data-ttu-id="e1d8c-125"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="e1d8c-125"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="e1d8c-126">O controle notificará o pai depois de apagar um item.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-126">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="e1d8c-127">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-127">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="e1d8c-128"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="e1d8c-128"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="e1d8c-129">O controle notificará o pai depois de pintar um item.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-129">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="e1d8c-130">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-130">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="e1d8c-131"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="e1d8c-131"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="e1d8c-132">[Versão 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="e1d8c-132">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="e1d8c-133">O controle notificará o pai quando um subitem de exibição de lista estiver sendo desenhado.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-133">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="e1d8c-134">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-134">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="e1d8c-135"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="e1d8c-135"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="e1d8c-136">Seu aplicativo especificou uma nova fonte para o item.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-136">Your application specified a new font for the item.</span></span> <span data-ttu-id="e1d8c-137">O controle usará a nova fonte.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-137">The control will use the new font.</span></span> <span data-ttu-id="e1d8c-138">Para obter mais informações sobre como alterar fontes, consulte [alterando fontes e cores](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="e1d8c-138">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="e1d8c-139">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="e1d8c-140"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="e1d8c-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="e1d8c-141">Seu aplicativo desenhou o item manualmente.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-141">Your application drew the item manually.</span></span> <span data-ttu-id="e1d8c-142">O controle não vai desenhar o item.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-142">The control will not draw the item.</span></span> <span data-ttu-id="e1d8c-143">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="e1d8c-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="e1d8c-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1d8c-144">Requirements</span></span>



| <span data-ttu-id="e1d8c-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1d8c-145">Requirement</span></span> | <span data-ttu-id="e1d8c-146">Valor</span><span class="sxs-lookup"><span data-stu-id="e1d8c-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d8c-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1d8c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="e1d8c-148">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e1d8c-148">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1d8c-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1d8c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="e1d8c-150">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1d8c-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1d8c-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1d8c-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1d8c-152"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1d8c-152"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1d8c-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1d8c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d8c-154">Usando o desenho personalizado</span><span class="sxs-lookup"><span data-stu-id="e1d8c-154">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





