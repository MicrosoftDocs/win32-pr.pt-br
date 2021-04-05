---
title: Mensagem de EM_UNDO (WinUser. h)
description: Essa mensagem desfaz a última operação de controle de edição na fila de desfazer do controle. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- Controles de EM_UNDO de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c75d79e7ed25e582682830b1323c27878bbdbb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644669"
---
# <a name="em_undo-message"></a><span data-ttu-id="3a2d1-105">\_Mensagem em desfazer</span><span class="sxs-lookup"><span data-stu-id="3a2d1-105">EM\_UNDO message</span></span>

<span data-ttu-id="3a2d1-106">Essa mensagem desfaz a última operação de controle de edição na fila de desfazer do controle.</span><span class="sxs-lookup"><span data-stu-id="3a2d1-106">This message undoes the last edit control operation in the control's undo queue.</span></span> <span data-ttu-id="3a2d1-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="3a2d1-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a2d1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a2d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a2d1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a2d1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a2d1-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3a2d1-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3a2d1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a2d1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a2d1-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3a2d1-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a2d1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a2d1-113">Return value</span></span>

<span data-ttu-id="3a2d1-114">Para um controle de edição de linha única, o valor de retorno é sempre **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="3a2d1-114">For a single-line edit control, the return value is always **TRUE**.</span></span>

<span data-ttu-id="3a2d1-115">Para um controle de edição de várias linhas, o valor de retorno será **true** se a operação de desfazer for bem-sucedida ou **false** se a operação de desfazer falhar.</span><span class="sxs-lookup"><span data-stu-id="3a2d1-115">For a multiline edit control, the return value is **TRUE** if the undo operation is successful, or **FALSE** if the undo operation fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a2d1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a2d1-116">Remarks</span></span>

<span data-ttu-id="3a2d1-117">**Editar controles e edição avançada 1,0:** Uma operação de desfazer também pode ser desfeita.</span><span class="sxs-lookup"><span data-stu-id="3a2d1-117">**Edit controls and Rich Edit 1.0:** An undo operation can also be undone.</span></span> <span data-ttu-id="3a2d1-118">Por exemplo, você pode restaurar texto excluído com a primeira mensagem em **\_ desfazer** e remover o texto novamente com uma segunda mensagem **em \_ desfazer** , contanto que não haja uma operação de edição intermediária.</span><span class="sxs-lookup"><span data-stu-id="3a2d1-118">For example, you can restore deleted text with the first **EM\_UNDO** message, and remove the text again with a second **EM\_UNDO** message as long as there is no intervening edit operation.</span></span>

<span data-ttu-id="3a2d1-119">**Edição avançada 2,0 e posterior:** O recurso de desfazer é de vários níveis e, portanto, enviar duas mensagens em **\_ desfazer** fará com que as duas últimas operações na fila de desfazer sejam desfeitas.</span><span class="sxs-lookup"><span data-stu-id="3a2d1-119">**Rich Edit 2.0 and later:** The undo feature is multilevel so sending two **EM\_UNDO** messages will undo the last two operations in the undo queue.</span></span> <span data-ttu-id="3a2d1-120">Para refazer uma operação, envie a mensagem em [**\_ refazer**](em-redo.md) .</span><span class="sxs-lookup"><span data-stu-id="3a2d1-120">To redo an operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

<span data-ttu-id="3a2d1-121">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="3a2d1-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="3a2d1-122">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="3a2d1-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2d1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a2d1-123">Requirements</span></span>



| <span data-ttu-id="3a2d1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a2d1-124">Requirement</span></span> | <span data-ttu-id="3a2d1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3a2d1-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2d1-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a2d1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3a2d1-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a2d1-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3a2d1-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a2d1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3a2d1-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3a2d1-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3a2d1-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a2d1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a2d1-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a2d1-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a2d1-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a2d1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2d1-133">**em \_ CANcelamento**</span><span class="sxs-lookup"><span data-stu-id="3a2d1-133">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> </dl>

 

 





