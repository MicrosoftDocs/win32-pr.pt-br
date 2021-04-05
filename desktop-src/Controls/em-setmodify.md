---
title: Mensagem de EM_SETMODIFY (WinUser. h)
description: Define ou limpa o sinalizador de modificação para um controle de edição. O sinalizador de modificação indica se o texto dentro do controle de edição foi modificado. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Controles de EM_SETMODIFY de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591b57dbc5441e96c1c6d3963172864713ed939f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824526"
---
# <a name="em_setmodify-message"></a><span data-ttu-id="51e1c-106">\_Mensagem em SETmodify</span><span class="sxs-lookup"><span data-stu-id="51e1c-106">EM\_SETMODIFY message</span></span>

<span data-ttu-id="51e1c-107">Define ou limpa o sinalizador de modificação para um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="51e1c-107">Sets or clears the modification flag for an edit control.</span></span> <span data-ttu-id="51e1c-108">O sinalizador de modificação indica se o texto dentro do controle de edição foi modificado.</span><span class="sxs-lookup"><span data-stu-id="51e1c-108">The modification flag indicates whether the text within the edit control has been modified.</span></span> <span data-ttu-id="51e1c-109">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="51e1c-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="51e1c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51e1c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e1c-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51e1c-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51e1c-112">O novo valor para o sinalizador de modificação.</span><span class="sxs-lookup"><span data-stu-id="51e1c-112">The new value for the modification flag.</span></span> <span data-ttu-id="51e1c-113">Um valor **true** indica que o texto foi modificado e um valor **false** indica que ele não foi modificado.</span><span class="sxs-lookup"><span data-stu-id="51e1c-113">A value of **TRUE** indicates the text has been modified, and a value of **FALSE** indicates it has not been modified.</span></span>

</dd> <dt>

<span data-ttu-id="51e1c-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51e1c-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51e1c-115">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="51e1c-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e1c-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51e1c-116">Return value</span></span>

<span data-ttu-id="51e1c-117">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="51e1c-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51e1c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="51e1c-118">Remarks</span></span>

<span data-ttu-id="51e1c-119">O sistema limpa automaticamente o sinalizador de modificação para zero quando o controle é criado.</span><span class="sxs-lookup"><span data-stu-id="51e1c-119">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="51e1c-120">Se o usuário alterar o texto do controle, o sistema definirá o sinalizador como diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="51e1c-120">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="51e1c-121">Você pode enviar a mensagem em [**\_ GetModify**](em-getmodify.md) para o controle de edição para recuperar o estado atual do sinalizador.</span><span class="sxs-lookup"><span data-stu-id="51e1c-121">You can send the [**EM\_GETMODIFY**](em-getmodify.md) message to the edit control to retrieve the current state of the flag.</span></span>

<span data-ttu-id="51e1c-122">**Edição avançada 1,0:** Os objetos criados sem o sinalizador de **\_ dinâmica REO** bloquearão suas extensões quando o sinalizador de modificação for definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="51e1c-122">**Rich Edit 1.0:** Objects created without the **REO\_DYNAMICSIZE** flag will lock in their extents when the modify flag is set to **FALSE**.</span></span>

<span data-ttu-id="51e1c-123">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="51e1c-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="51e1c-124">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="51e1c-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51e1c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51e1c-125">Requirements</span></span>



| <span data-ttu-id="51e1c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="51e1c-126">Requirement</span></span> | <span data-ttu-id="51e1c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="51e1c-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51e1c-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51e1c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="51e1c-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51e1c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="51e1c-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51e1c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="51e1c-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51e1c-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="51e1c-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51e1c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="51e1c-133"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51e1c-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51e1c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="51e1c-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="51e1c-135">**Referência**</span><span class="sxs-lookup"><span data-stu-id="51e1c-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="51e1c-136">**em \_ GETmodify**</span><span class="sxs-lookup"><span data-stu-id="51e1c-136">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> <dt>

[<span data-ttu-id="51e1c-137">**Reobjeto**</span><span class="sxs-lookup"><span data-stu-id="51e1c-137">**REOBJECT**</span></span>](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





