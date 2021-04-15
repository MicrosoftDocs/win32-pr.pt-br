---
title: Código de notificação de NM_CUSTOMDRAW (cabeçalho) (commctrl. h)
description: Enviado por um controle de cabeçalho para notificar sua janela pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 44dab54b-45ef-4fba-93b8-2a3e35cda23f
keywords:
- Código de notificação de NM_CUSTOMDRAW (cabeçalho) controles do Windows
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
ms.openlocfilehash: 89d6b35503aebed221da6cec212c6dbf614061f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753961"
---
# <a name="nm_customdraw-header-notification-code"></a><span data-ttu-id="60370-105">\_Código de notificação nm CUSTOMDRAW (Header)</span><span class="sxs-lookup"><span data-stu-id="60370-105">NM\_CUSTOMDRAW (header) notification code</span></span>

<span data-ttu-id="60370-106">Enviado por um controle de cabeçalho para notificar sua janela pai sobre operações de desenho.</span><span class="sxs-lookup"><span data-stu-id="60370-106">Sent by a header control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="60370-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="60370-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="60370-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60370-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60370-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60370-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60370-110">Um ponteiro para uma estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contém informações sobre a operação de desenho.</span><span class="sxs-lookup"><span data-stu-id="60370-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="60370-111">O membro **dwItemSpec** dessa estrutura contém o índice do item que está sendo desenhado e o membro **lItemlParam** dessa estrutura contém o *lParam* do item.</span><span class="sxs-lookup"><span data-stu-id="60370-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60370-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="60370-112">Return value</span></span>

<span data-ttu-id="60370-113">O valor que seu aplicativo pode retornar depende do estágio de desenho atual.</span><span class="sxs-lookup"><span data-stu-id="60370-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="60370-114">O membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica o estágio de desenho.</span><span class="sxs-lookup"><span data-stu-id="60370-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="60370-115">Você deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="60370-115">You must return one of the following values.</span></span>



| <span data-ttu-id="60370-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="60370-116">Return code</span></span>                                                                                            | <span data-ttu-id="60370-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="60370-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="60370-118"><dt>**dopadrão CDRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="60370-118"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="60370-119">O controle será desenhado em si mesmo.</span><span class="sxs-lookup"><span data-stu-id="60370-119">The control will draw itself.</span></span> <span data-ttu-id="60370-120">Ele não enviará nenhuma mensagem [de \_ CUSTOMDRAW de nm](nm-customdraw.md) adicional para este ciclo de pintura.</span><span class="sxs-lookup"><span data-stu-id="60370-120">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) messages for this paint cycle.</span></span> <span data-ttu-id="60370-121">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="60370-121">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="60370-122"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="60370-122"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="60370-123">O controle notificará o pai de qualquer operação de desenho relacionada a itens.</span><span class="sxs-lookup"><span data-stu-id="60370-123">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="60370-124">Ele enviará \_ códigos de notificação nm CUSTOMDRAW antes e depois de itens de desenho.</span><span class="sxs-lookup"><span data-stu-id="60370-124">It will send NM\_CUSTOMDRAW notification codes before and after drawing items.</span></span> <span data-ttu-id="60370-125">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="60370-125">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="60370-126"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="60370-126"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="60370-127">O controle notificará o pai depois de apagar um item.</span><span class="sxs-lookup"><span data-stu-id="60370-127">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="60370-128">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="60370-128">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="60370-129"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="60370-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="60370-130">O controle notificará o pai depois de pintar um item.</span><span class="sxs-lookup"><span data-stu-id="60370-130">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="60370-131">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="60370-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="60370-132"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="60370-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="60370-133">[Versões de controle comuns](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="60370-133">[Common Control Versions](common-control-versions.md).</span></span> <span data-ttu-id="60370-134">O controle notificará o pai quando um subitem de exibição de lista estiver sendo desenhado.</span><span class="sxs-lookup"><span data-stu-id="60370-134">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="60370-135">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="60370-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="60370-136"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="60370-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="60370-137">Seu aplicativo especificou uma nova fonte para o item; o controle usará a nova fonte.</span><span class="sxs-lookup"><span data-stu-id="60370-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="60370-138">Para obter mais informações sobre como alterar fontes, consulte [alterando fontes e cores](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="60370-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="60370-139">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="60370-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="60370-140"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="60370-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="60370-141">Seu aplicativo desenhou o item manualmente.</span><span class="sxs-lookup"><span data-stu-id="60370-141">Your application drew the item manually.</span></span> <span data-ttu-id="60370-142">O controle não vai desenhar o item.</span><span class="sxs-lookup"><span data-stu-id="60370-142">The control will not draw the item.</span></span> <span data-ttu-id="60370-143">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="60370-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="60370-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="60370-144">Remarks</span></span>

<span data-ttu-id="60370-145">Consulte [usando o desenho personalizado](custom-draw.md) para mais discussões.</span><span class="sxs-lookup"><span data-stu-id="60370-145">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="60370-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60370-146">Requirements</span></span>



| <span data-ttu-id="60370-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="60370-147">Requirement</span></span> | <span data-ttu-id="60370-148">Valor</span><span class="sxs-lookup"><span data-stu-id="60370-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60370-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60370-149">Minimum supported client</span></span><br/> | <span data-ttu-id="60370-150">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60370-150">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60370-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60370-151">Minimum supported server</span></span><br/> | <span data-ttu-id="60370-152">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="60370-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60370-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60370-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="60370-154"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="60370-154"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





