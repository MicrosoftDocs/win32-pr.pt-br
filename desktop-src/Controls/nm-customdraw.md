---
title: NM_CUSTOMDRAW código de notificação (commctrl. h)
description: Notifica uma janela pai do controle sobre as operações de desenho personalizadas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- NM_CUSTOMDRAW de código de notificação controles do Windows
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
ms.openlocfilehash: d5f91f5197c7ecaf0ae4356fe00c48221a83ebd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454626"
---
# <a name="nm_customdraw-notification-code"></a><span data-ttu-id="2d3cc-105">\_Código de notificação nm CUSTOMDRAW</span><span class="sxs-lookup"><span data-stu-id="2d3cc-105">NM\_CUSTOMDRAW notification code</span></span>

<span data-ttu-id="2d3cc-106">Notifica uma janela pai do controle sobre as operações de desenho personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-106">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="2d3cc-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2d3cc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

#ifdef LIST_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;

#elif TOOL_TIPS_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;

#elif TREE_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;

#elif TOOL_BAR_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTBCUSTOMDRAW) lParam;

#else

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;

#endif
```



## <a name="parameters"></a><span data-ttu-id="2d3cc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d3cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d3cc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d3cc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d3cc-110">Um ponteiro para uma estrutura relacionada ao empate personalizada que contém informações sobre a operação de desenho.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-110">A pointer to a custom draw-related structure that contains information about the drawing operation.</span></span> <span data-ttu-id="2d3cc-111">A lista a seguir especifica os controles e suas estruturas associadas.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-111">The following list specifies the controls and their associated structures.</span></span>



| <span data-ttu-id="2d3cc-112">Control</span><span class="sxs-lookup"><span data-stu-id="2d3cc-112">Control</span></span>                     | <span data-ttu-id="2d3cc-113">Estrutura de desenho Personalizada</span><span class="sxs-lookup"><span data-stu-id="2d3cc-113">Custom Draw Structure</span></span>                    |
|-----------------------------|------------------------------------------|
| <span data-ttu-id="2d3cc-114">Rebar, TrackBar e header</span><span class="sxs-lookup"><span data-stu-id="2d3cc-114">Rebar, trackbar, and header</span></span> | [<span data-ttu-id="2d3cc-115">**NMCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="2d3cc-115">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| <span data-ttu-id="2d3cc-116">Modo de exibição de lista</span><span class="sxs-lookup"><span data-stu-id="2d3cc-116">List view</span></span>                   | [<span data-ttu-id="2d3cc-117">**NMLVCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="2d3cc-117">**NMLVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| <span data-ttu-id="2d3cc-118">Dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="2d3cc-118">Tooltip</span></span>                     | [<span data-ttu-id="2d3cc-119">**NMTTCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="2d3cc-119">**NMTTCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| <span data-ttu-id="2d3cc-120">Exibição em árvore</span><span class="sxs-lookup"><span data-stu-id="2d3cc-120">Tree view</span></span>                   | [<span data-ttu-id="2d3cc-121">**NMTVCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="2d3cc-121">**NMTVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| <span data-ttu-id="2d3cc-122">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="2d3cc-122">Toolbar</span></span>                     | [<span data-ttu-id="2d3cc-123">**NMTBCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="2d3cc-123">**NMTBCUSTOMDRAW**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d3cc-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d3cc-124">Return value</span></span>

<span data-ttu-id="2d3cc-125">O valor que seu aplicativo pode retornar depende do estágio de desenho atual.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-125">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="2d3cc-126">O membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica o estágio de desenho.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-126">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="2d3cc-127">Você deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-127">You must return one of the following values.</span></span>



| <span data-ttu-id="2d3cc-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2d3cc-128">Return code</span></span>                                                                                            | <span data-ttu-id="2d3cc-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d3cc-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d3cc-130"><dt>**dopadrão CDRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d3cc-130"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="2d3cc-131">O controle será desenhado em si mesmo.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-131">The control will draw itself.</span></span> <span data-ttu-id="2d3cc-132">Ele não enviará códigos de notificação [ \_ CUSTOMDRAW de nm](nm-customdraw.md) adicionais para este ciclo de pintura.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-132">It will not send additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="2d3cc-133">Esse sinalizador não pode ser usado com nenhum outro sinalizador.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-133">This flag cannot be used with any other flag.</span></span> <br/>                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="2d3cc-134"><dt>**doborracha CDRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d3cc-134"><dt>**CDRF\_DOERASE**</dt></span></span> </dl>           | <span data-ttu-id="2d3cc-135">O controle só desenhará o plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-135">The control will only draw the background.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="2d3cc-136"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="2d3cc-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="2d3cc-137">Seu aplicativo especificou uma nova fonte para o item; o controle usará a nova fonte.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="2d3cc-138">Para obter mais informações sobre como alterar fontes, consulte [alterando fontes e cores](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="2d3cc-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="2d3cc-139">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="2d3cc-140"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="2d3cc-140"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="2d3cc-141">O controle notificará o pai de qualquer operação de desenho relacionada a itens.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-141">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="2d3cc-142">Ele enviará códigos de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) antes e depois de itens de desenho.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-142">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="2d3cc-143">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-143">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="2d3cc-144"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="2d3cc-144"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="2d3cc-145">O controle notificará o pai depois de apagar um item.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-145">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="2d3cc-146">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-146">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="2d3cc-147"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="2d3cc-147"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="2d3cc-148">O controle enviará um código de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) quando o ciclo de pintura de todo o controle for concluído.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-148">The control will send an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code when the painting cycle for the entire control is complete.</span></span> <span data-ttu-id="2d3cc-149">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-149">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="2d3cc-150"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="2d3cc-150"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="2d3cc-151">Seu aplicativo receberá um código de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) com **dwDrawStage** definido como CDDs \_ ITEMPREPAINT \| CDDs \_ subitem antes de cada subitem de exibição de lista ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-151">Your application will receive an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code with **dwDrawStage** set to CDDS\_ITEMPREPAINT \| CDDS\_SUBITEM before each list-view subitem is drawn.</span></span> <span data-ttu-id="2d3cc-152">Em seguida, você pode especificar a fonte e a cor de cada subitem separadamente ou retornar [**CDRF \_ DODEFAULT**](cdrf-constants.md) para processamento padrão.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-152">You can then specify font and color for each subitem separately or return [**CDRF\_DODEFAULT**](cdrf-constants.md) for default processing.</span></span> <span data-ttu-id="2d3cc-153">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="2d3cc-154"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="2d3cc-154"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="2d3cc-155">Seu aplicativo desenhou o item manualmente.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-155">Your application drew the item manually.</span></span> <span data-ttu-id="2d3cc-156">O controle não vai desenhar o item.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-156">The control will not draw the item.</span></span> <span data-ttu-id="2d3cc-157">Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-157">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="2d3cc-158"><dt>**CDRF \_ SKIPPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="2d3cc-158"><dt>**CDRF\_SKIPPOSTPAINT**</dt></span></span> </dl>     | <span data-ttu-id="2d3cc-159">O controle não desenhará o retângulo de foco em um item.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-159">The control will not draw the focus rectangle around an item.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="2d3cc-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d3cc-160">Remarks</span></span>

<span data-ttu-id="2d3cc-161">Atualmente, os seguintes controles dão suporte à funcionalidade de desenho Personalizada: cabeçalho, exibição de lista, Rebar, barra de ferramentas, dica de ferramenta, TrackBar e modo de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-161">Currently, the following controls support custom draw functionality: header, list view, rebar, toolbar, tooltip, trackbar, and tree view.</span></span> <span data-ttu-id="2d3cc-162">O desenho personalizado também terá suporte para controles de botão se você tiver um manifesto de aplicativo para garantir que Comctl32.dll versão 6 esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-162">Custom draw is also supported for button controls if you have an application manifest to ensure that Comctl32.dll version 6 is available.</span></span>

<span data-ttu-id="2d3cc-163">Se essa mensagem for tratada em um procedimento de caixa de diálogo, você deverá definir o valor de retorno como parte dos dados da janela antes de retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-163">If this message is handled in a dialog procedure, you must set the return value as part of the window data before returning **TRUE**.</span></span> <span data-ttu-id="2d3cc-164">Para obter mais informações, consulte [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).</span><span class="sxs-lookup"><span data-stu-id="2d3cc-164">For more information, see [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d3cc-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d3cc-165">Requirements</span></span>



| <span data-ttu-id="2d3cc-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d3cc-166">Requirement</span></span> | <span data-ttu-id="2d3cc-167">Valor</span><span class="sxs-lookup"><span data-stu-id="2d3cc-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d3cc-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d3cc-168">Minimum supported client</span></span><br/> | <span data-ttu-id="2d3cc-169">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d3cc-169">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d3cc-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d3cc-170">Minimum supported server</span></span><br/> | <span data-ttu-id="2d3cc-171">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2d3cc-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d3cc-172">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d3cc-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d3cc-173"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d3cc-173"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d3cc-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d3cc-174">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d3cc-175">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="2d3cc-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2d3cc-176">Desenho personalizado</span><span class="sxs-lookup"><span data-stu-id="2d3cc-176">Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

