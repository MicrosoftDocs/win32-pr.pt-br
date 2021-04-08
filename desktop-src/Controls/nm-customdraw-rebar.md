---
title: Código de notificação do NM_CUSTOMDRAW (rebar) (commctrl. h)
description: Enviado pelo controle rebar para notificar sua janela pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 3ba9bb59-f297-4af1-a9a9-d8789def5bde
keywords:
- Controles do Windows de código de notificação de NM_CUSTOMDRAW (rebar)
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
ms.openlocfilehash: 329f3e9abfb20dbca8cebd3a6bf02673ad00f904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086537"
---
# <a name="nm_customdraw-rebar-notification-code"></a><span data-ttu-id="94bf2-105">\_Código de notificação do CUSTOMDRAW nm (rebar)</span><span class="sxs-lookup"><span data-stu-id="94bf2-105">NM\_CUSTOMDRAW (rebar) notification code</span></span>

<span data-ttu-id="94bf2-106">Enviado pelo controle rebar para notificar sua janela pai sobre operações de desenho.</span><span class="sxs-lookup"><span data-stu-id="94bf2-106">Sent by the rebar control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="94bf2-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="94bf2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="94bf2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94bf2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94bf2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94bf2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94bf2-110">Ponteiro para uma estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contém informações sobre a operação de desenho.</span><span class="sxs-lookup"><span data-stu-id="94bf2-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="94bf2-111">O membro **dwItemSpec** dessa estrutura contém o identificador da banda que está sendo desenhada.</span><span class="sxs-lookup"><span data-stu-id="94bf2-111">The **dwItemSpec** member of this structure contains the identifier of the band being drawn.</span></span> <span data-ttu-id="94bf2-112">O membro **lItemlParam** dessa estrutura contém o *lParam* da banda que está sendo desenhada.</span><span class="sxs-lookup"><span data-stu-id="94bf2-112">The **lItemlParam** member of this structure contains the *lParam* of the band being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94bf2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94bf2-113">Return value</span></span>

<span data-ttu-id="94bf2-114">O valor que seu aplicativo pode retornar depende do estágio de desenho atual.</span><span class="sxs-lookup"><span data-stu-id="94bf2-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="94bf2-115">O membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica o estágio de desenho.</span><span class="sxs-lookup"><span data-stu-id="94bf2-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="94bf2-116">Você deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="94bf2-116">You must return one of the following values.</span></span>



| <span data-ttu-id="94bf2-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="94bf2-117">Return code</span></span>                                                                                            | <span data-ttu-id="94bf2-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="94bf2-118">Description</span></span>                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="94bf2-119"><dt>**dopadrão CDRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="94bf2-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="94bf2-120">O controle será desenhado em si mesmo.</span><span class="sxs-lookup"><span data-stu-id="94bf2-120">The control will draw itself.</span></span> <span data-ttu-id="94bf2-121">Ele não enviará nenhuma notificação [de \_ CUSTOMDRAW nm](nm-customdraw.md) adicional para este ciclo de pintura.</span><span class="sxs-lookup"><span data-stu-id="94bf2-121">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notifications for this paint cycle.</span></span> <span data-ttu-id="94bf2-122">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="94bf2-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="94bf2-123"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="94bf2-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="94bf2-124">O controle notificará o pai de qualquer operação de desenho relacionada a itens.</span><span class="sxs-lookup"><span data-stu-id="94bf2-124">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="94bf2-125">Ele enviará códigos de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) antes e depois de itens de desenho.</span><span class="sxs-lookup"><span data-stu-id="94bf2-125">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="94bf2-126">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="94bf2-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="94bf2-127"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="94bf2-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="94bf2-128">O controle notificará o pai depois de apagar um item.</span><span class="sxs-lookup"><span data-stu-id="94bf2-128">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="94bf2-129">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="94bf2-129">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="94bf2-130"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="94bf2-130"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="94bf2-131">O controle notificará o pai depois de pintar um item.</span><span class="sxs-lookup"><span data-stu-id="94bf2-131">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="94bf2-132">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="94bf2-132">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="94bf2-133"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="94bf2-133"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="94bf2-134">O controle notificará o pai de qualquer operação de desenho relacionada a itens.</span><span class="sxs-lookup"><span data-stu-id="94bf2-134">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="94bf2-135">Ele enviará códigos de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) antes e depois de itens de desenho.</span><span class="sxs-lookup"><span data-stu-id="94bf2-135">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="94bf2-136">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="94bf2-136">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="94bf2-137"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="94bf2-137"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="94bf2-138">O aplicativo especificou uma nova fonte para o item; o controle usará a nova fonte.</span><span class="sxs-lookup"><span data-stu-id="94bf2-138">The application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="94bf2-139">Para obter mais informações sobre como alterar fontes, consulte [alterando fontes e cores](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="94bf2-139">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="94bf2-140">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="94bf2-140">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="94bf2-141"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="94bf2-141"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="94bf2-142">O aplicativo desenhou o item manualmente.</span><span class="sxs-lookup"><span data-stu-id="94bf2-142">The application drew the item manually.</span></span> <span data-ttu-id="94bf2-143">O controle não vai desenhar o item.</span><span class="sxs-lookup"><span data-stu-id="94bf2-143">The control will not draw the item.</span></span> <span data-ttu-id="94bf2-144">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="94bf2-144">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="94bf2-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94bf2-145">Requirements</span></span>



| <span data-ttu-id="94bf2-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="94bf2-146">Requirement</span></span> | <span data-ttu-id="94bf2-147">Valor</span><span class="sxs-lookup"><span data-stu-id="94bf2-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94bf2-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94bf2-148">Minimum supported client</span></span><br/> | <span data-ttu-id="94bf2-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94bf2-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="94bf2-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94bf2-150">Minimum supported server</span></span><br/> | <span data-ttu-id="94bf2-151">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="94bf2-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="94bf2-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94bf2-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="94bf2-153"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="94bf2-153"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94bf2-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="94bf2-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94bf2-155">Usando o desenho personalizado</span><span class="sxs-lookup"><span data-stu-id="94bf2-155">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





