---
title: Mensagem de EM_SETMARGINS (WinUser. h)
description: Define as larguras das margens esquerda e direita para um controle de edição. A mensagem redesenha o controle para refletir as novas margens. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- Controles de EM_SETMARGINS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c68f3394234a6f86b3c5ff69622b86e61afc556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918622"
---
# <a name="em_setmargins-message"></a><span data-ttu-id="59730-106">\_Mensagem em SETmargins</span><span class="sxs-lookup"><span data-stu-id="59730-106">EM\_SETMARGINS message</span></span>

<span data-ttu-id="59730-107">Define as larguras das margens esquerda e direita para um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="59730-107">Sets the widths of the left and right margins for an edit control.</span></span> <span data-ttu-id="59730-108">A mensagem redesenha o controle para refletir as novas margens.</span><span class="sxs-lookup"><span data-stu-id="59730-108">The message redraws the control to reflect the new margins.</span></span> <span data-ttu-id="59730-109">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="59730-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="59730-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59730-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59730-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59730-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59730-112">As margens a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="59730-112">The margins to set.</span></span> <span data-ttu-id="59730-113">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="59730-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="59730-114">Valor</span><span class="sxs-lookup"><span data-stu-id="59730-114">Value</span></span>                                                                                                                                                            | <span data-ttu-id="59730-115">Significado</span><span class="sxs-lookup"><span data-stu-id="59730-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <span data-ttu-id="59730-116"><dt>**LeftMargin do EC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="59730-116"><dt>**EC\_LEFTMARGIN**</dt></span></span> </dl>    | <span data-ttu-id="59730-117">Define a margem esquerda.</span><span class="sxs-lookup"><span data-stu-id="59730-117">Sets the left margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <span data-ttu-id="59730-118"><dt>**RIGHTMARGIN do EC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="59730-118"><dt>**EC\_RIGHTMARGIN**</dt></span></span> </dl> | <span data-ttu-id="59730-119">Define a margem direita.</span><span class="sxs-lookup"><span data-stu-id="59730-119">Sets the right margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <span data-ttu-id="59730-120"><dt>**USEFONTINFO do EC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="59730-120"><dt>**EC\_USEFONTINFO**</dt></span></span> </dl> | <span data-ttu-id="59730-121">**Controles de edição avançados:** Define as margens esquerda e direita com uma largura estreita calculada usando as métricas de texto da fonte atual do controle.</span><span class="sxs-lookup"><span data-stu-id="59730-121">**Rich edit controls:** Sets the left and right margins to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="59730-122">Se nenhuma fonte tiver sido definida para o controle, as margens serão definidas como zero.</span><span class="sxs-lookup"><span data-stu-id="59730-122">If no font has been set for the control, the margins are set to zero.</span></span> <span data-ttu-id="59730-123">O parâmetro *lParam* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="59730-123">The *lParam* parameter is ignored.</span></span> <br/> <span data-ttu-id="59730-124">**Controles de edição:** O valor de **\_ USEFONTINFO do EC** não pode ser usado no parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="59730-124">**Edit controls:** The **EC\_USEFONTINFO** value cannot be used in the *wParam* parameter.</span></span> <span data-ttu-id="59730-125">Ele só pode ser usado no parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="59730-125">It can only be used in the *lParam* parameter.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="59730-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59730-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59730-127">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a nova largura da margem esquerda, em pixels.</span><span class="sxs-lookup"><span data-stu-id="59730-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new width of the left margin, in pixels.</span></span> <span data-ttu-id="59730-128">Esse valor será ignorado se *wParam* não incluir o **EC \_ LeftMargin**.</span><span class="sxs-lookup"><span data-stu-id="59730-128">This value is ignored if *wParam* does not include **EC\_LEFTMARGIN**.</span></span>

<span data-ttu-id="59730-129">**Edite controles e edição avançada 3,0 e posteriores:** O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) pode especificar o valor de **\_ USEFONTINFO do EC** para definir a margem esquerda com uma largura estreita calculada usando as métricas de texto da fonte atual do controle.</span><span class="sxs-lookup"><span data-stu-id="59730-129">**Edit controls and Rich Edit 3.0 and later:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the left margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="59730-130">Se nenhuma fonte tiver sido definida para o controle, a margem será definida como zero.</span><span class="sxs-lookup"><span data-stu-id="59730-130">If no font has been set for the control, the margin is set to zero.</span></span>

<span data-ttu-id="59730-131">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a nova largura da margem direita, em pixels.</span><span class="sxs-lookup"><span data-stu-id="59730-131">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new width of the right margin, in pixels.</span></span> <span data-ttu-id="59730-132">Esse valor será ignorado se *wParam* não incluir a **\_ margem do EC**.</span><span class="sxs-lookup"><span data-stu-id="59730-132">This value is ignored if *wParam* does not include **EC\_RIGHTMARGIN**.</span></span>

<span data-ttu-id="59730-133">**Edite controles e edição avançada 3,0 e posteriores:** O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pode especificar o valor de **\_ USEFONTINFO do EC** para definir a margem direita com uma largura estreita calculada usando as métricas de texto da fonte atual do controle.</span><span class="sxs-lookup"><span data-stu-id="59730-133">**Edit controls and Rich Edit 3.0 and later:** The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the right margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="59730-134">Se nenhuma fonte tiver sido definida para o controle, a margem será definida como zero.</span><span class="sxs-lookup"><span data-stu-id="59730-134">If no font has been set for the control, the margin is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59730-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59730-135">Return value</span></span>

<span data-ttu-id="59730-136">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="59730-136">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59730-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="59730-137">Remarks</span></span>

<span data-ttu-id="59730-138">**Controles de edição:** Não é possível usar o **EC \_ USEFONTINFO** no parâmetro *wParam* , mas você pode usá-lo no parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="59730-138">**Edit controls:** You cannot use **EC\_USEFONTINFO** in the *wParam* parameter, but you can use it in the *lParam* parameter.</span></span>

<span data-ttu-id="59730-139">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="59730-139">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="59730-140">Todas as versões de edição avançadas dão suporte ao uso do **EC \_ USEFONTINFO** no parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="59730-140">All rich edit versions support the use of **EC\_USEFONTINFO** in the *wParam* parameter.</span></span> <span data-ttu-id="59730-141">No entanto, somente o Microsoft Rich Edit 3,0 e versões posteriores dão suporte ao uso do **EC \_ USEFONTINFO** no parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="59730-141">However, only Microsoft Rich Edit 3.0 and later support the use of **EC\_USEFONTINFO** in the *lParam* parameter.</span></span> <span data-ttu-id="59730-142">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="59730-142">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59730-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59730-143">Requirements</span></span>



| <span data-ttu-id="59730-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="59730-144">Requirement</span></span> | <span data-ttu-id="59730-145">Valor</span><span class="sxs-lookup"><span data-stu-id="59730-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59730-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59730-146">Minimum supported client</span></span><br/> | <span data-ttu-id="59730-147">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59730-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="59730-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59730-148">Minimum supported server</span></span><br/> | <span data-ttu-id="59730-149">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59730-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="59730-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59730-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="59730-151"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59730-151"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59730-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="59730-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59730-153">**em \_ GETmargins**</span><span class="sxs-lookup"><span data-stu-id="59730-153">**EM\_GETMARGINS**</span></span>](em-getmargins.md)
</dt> </dl>

 

