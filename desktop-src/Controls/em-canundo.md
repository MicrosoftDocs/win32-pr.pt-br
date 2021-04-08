---
title: Mensagem de EM_CANUNDO (WinUser. h)
description: Determina se há alguma ação em uma fila de desfazer do controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- Controles de EM_CANUNDO de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345367b25790051a444363bb9bbc02af3d6fb0fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085830"
---
# <a name="em_canundo-message"></a><span data-ttu-id="f7d7f-105">\_Mensagem em CANundo</span><span class="sxs-lookup"><span data-stu-id="f7d7f-105">EM\_CANUNDO message</span></span>

<span data-ttu-id="f7d7f-106">Determina se há alguma ação em uma fila de desfazer do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="f7d7f-106">Determines whether there are any actions in an edit control's undo queue.</span></span> <span data-ttu-id="f7d7f-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="f7d7f-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7d7f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7d7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7d7f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7d7f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7d7f-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f7d7f-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f7d7f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7d7f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7d7f-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f7d7f-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7d7f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7d7f-113">Return value</span></span>

<span data-ttu-id="f7d7f-114">Se houver ações na fila de desfazer do controle, o valor de retorno será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="f7d7f-114">If there are actions in the control's undo queue, the return value is nonzero.</span></span>

<span data-ttu-id="f7d7f-115">Se a fila de desfazer estiver vazia, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="f7d7f-115">If the undo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7d7f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7d7f-116">Remarks</span></span>

<span data-ttu-id="f7d7f-117">Se a fila de desfazer não estiver vazia, você poderá enviar a mensagem em [**\_ desfazer**](em-undo.md) para o controle para desfazer a operação mais recente.</span><span class="sxs-lookup"><span data-stu-id="f7d7f-117">If the undo queue is not empty, you can send the [**EM\_UNDO**](em-undo.md) message to the control to undo the most recent operation.</span></span>

<span data-ttu-id="f7d7f-118">**Editar controles e edição avançada 1,0:** A fila de desfazer contém apenas a operação mais recente.</span><span class="sxs-lookup"><span data-stu-id="f7d7f-118">**Edit controls and Rich Edit 1.0:** The undo queue contains only the most recent operation.</span></span>

<span data-ttu-id="f7d7f-119">**Edição avançada 2,0 e posterior:** A fila de desfazer pode conter várias operações.</span><span class="sxs-lookup"><span data-stu-id="f7d7f-119">**Rich Edit 2.0 and later:** The undo queue can contain multiple operations.</span></span>

<span data-ttu-id="f7d7f-120">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="f7d7f-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="f7d7f-121">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f7d7f-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7d7f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7d7f-122">Requirements</span></span>



| <span data-ttu-id="f7d7f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7d7f-123">Requirement</span></span> | <span data-ttu-id="f7d7f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f7d7f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d7f-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7d7f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d7f-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7d7f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f7d7f-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7d7f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d7f-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f7d7f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f7d7f-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f7d7f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7d7f-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7d7f-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7d7f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7d7f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7d7f-132">**em \_ desfazer**</span><span class="sxs-lookup"><span data-stu-id="f7d7f-132">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





