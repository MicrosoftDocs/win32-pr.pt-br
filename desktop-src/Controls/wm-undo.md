---
title: Mensagem de WM_UNDO (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de desfazer do WM para um controle de edição para desfazer a última operação. Quando essa mensagem é enviada a um controle de edição, o texto excluído anteriormente é restaurado ou o texto adicionado anteriormente é excluído.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- Controles de WM_UNDO de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c5eb9182b6d8d3fc1360565f6661e989f3b6d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455416"
---
# <a name="wm_undo-message"></a><span data-ttu-id="3a073-105">Mensagem de desfazer do WM \_</span><span class="sxs-lookup"><span data-stu-id="3a073-105">WM\_UNDO message</span></span>

<span data-ttu-id="3a073-106">Um aplicativo envia uma mensagem de **\_ desfazer do WM** para um controle de edição para desfazer a última operação.</span><span class="sxs-lookup"><span data-stu-id="3a073-106">An application sends a **WM\_UNDO** message to an edit control to undo the last operation.</span></span> <span data-ttu-id="3a073-107">Quando essa mensagem é enviada a um controle de edição, o texto excluído anteriormente é restaurado ou o texto adicionado anteriormente é excluído.</span><span class="sxs-lookup"><span data-stu-id="3a073-107">When this message is sent to an edit control, the previously deleted text is restored or the previously added text is deleted.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a073-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a073-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a073-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a073-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a073-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3a073-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3a073-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a073-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a073-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3a073-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a073-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a073-113">Return value</span></span>

<span data-ttu-id="3a073-114">Se a mensagem tiver sucesso, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="3a073-114">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="3a073-115">Se a mensagem falhar, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="3a073-115">If the message fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a073-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a073-116">Remarks</span></span>

<span data-ttu-id="3a073-117">**Edição avançada:** É recomendável que [**em \_ desfazer**](em-undo.md) seja usado em vez do **WM \_ desfazer**.</span><span class="sxs-lookup"><span data-stu-id="3a073-117">**Rich Edit:** It is recommended that [**EM\_UNDO**](em-undo.md) be used instead of **WM\_UNDO**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a073-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a073-118">Requirements</span></span>



| <span data-ttu-id="3a073-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a073-119">Requirement</span></span> | <span data-ttu-id="3a073-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3a073-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a073-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a073-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a073-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a073-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3a073-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a073-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3a073-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3a073-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3a073-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a073-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a073-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a073-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a073-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a073-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a073-128">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="3a073-128">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3a073-129">**limpeza do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3a073-129">**WM\_CLEAR**</span></span>](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[<span data-ttu-id="3a073-130">**cópia do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3a073-130">**WM\_COPY**</span></span>](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[<span data-ttu-id="3a073-131">**recorte do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3a073-131">**WM\_CUT**</span></span>](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[<span data-ttu-id="3a073-132">**colar do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3a073-132">**WM\_PASTE**</span></span>](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

