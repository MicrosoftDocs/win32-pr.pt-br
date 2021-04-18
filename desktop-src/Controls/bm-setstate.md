---
title: Mensagem de BM_SETSTATE (WinUser. h)
description: Define o estado de realce de um botão. O estado de realce indica se o botão é realçado como se o usuário tivesse enviado por push. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetState do botão.
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- Controles de BM_SETSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9b60231980f406b0aeb499d724dc6aa7025513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755660"
---
# <a name="bm_setstate-message"></a><span data-ttu-id="0fc90-106">\_Mensagem BM SETstate</span><span class="sxs-lookup"><span data-stu-id="0fc90-106">BM\_SETSTATE message</span></span>

<span data-ttu-id="0fc90-107">Define o estado de realce de um botão.</span><span class="sxs-lookup"><span data-stu-id="0fc90-107">Sets the highlight state of a button.</span></span> <span data-ttu-id="0fc90-108">O estado de realce indica se o botão é realçado como se o usuário tivesse enviado por push.</span><span class="sxs-lookup"><span data-stu-id="0fc90-108">The highlight state indicates whether the button is highlighted as if the user had pushed it.</span></span> <span data-ttu-id="0fc90-109">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetState do botão**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) .</span><span class="sxs-lookup"><span data-stu-id="0fc90-109">You can send this message explicitly or use the [**Button\_SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0fc90-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fc90-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fc90-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0fc90-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fc90-112">Um **bool** que especifica se o botão é realçado.</span><span class="sxs-lookup"><span data-stu-id="0fc90-112">A **BOOL** that specifies whether the button is highlighted.</span></span> <span data-ttu-id="0fc90-113">Um valor de **true** realça o botão.</span><span class="sxs-lookup"><span data-stu-id="0fc90-113">A value of **TRUE** highlights the button.</span></span> <span data-ttu-id="0fc90-114">Um valor **false** remove qualquer realce.</span><span class="sxs-lookup"><span data-stu-id="0fc90-114">A value of **FALSE** removes any highlighting.</span></span>

</dd> <dt>

<span data-ttu-id="0fc90-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0fc90-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fc90-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="0fc90-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fc90-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0fc90-117">Return value</span></span>

<span data-ttu-id="0fc90-118">Essa mensagem sempre retorna zero.</span><span class="sxs-lookup"><span data-stu-id="0fc90-118">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fc90-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fc90-119">Remarks</span></span>

<span data-ttu-id="0fc90-120">Realce afeta apenas a aparência de um botão.</span><span class="sxs-lookup"><span data-stu-id="0fc90-120">Highlighting affects only the appearance of a button.</span></span> <span data-ttu-id="0fc90-121">Ele não tem nenhum efeito no estado de verificação de um botão de opção ou caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="0fc90-121">It has no effect on the check state of a radio button or check box.</span></span>

<span data-ttu-id="0fc90-122">Um botão é realçado automaticamente quando o usuário posiciona o cursor sobre ele e pressiona e mantém o botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="0fc90-122">A button is automatically highlighted when the user positions the cursor over it and presses and holds the left mouse button.</span></span> <span data-ttu-id="0fc90-123">O realce é removido quando o usuário libera o botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="0fc90-123">The highlighting is removed when the user releases the mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fc90-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fc90-124">Requirements</span></span>



| <span data-ttu-id="0fc90-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fc90-125">Requirement</span></span> | <span data-ttu-id="0fc90-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0fc90-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc90-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fc90-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0fc90-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0fc90-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0fc90-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fc90-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0fc90-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0fc90-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0fc90-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0fc90-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fc90-132"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fc90-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fc90-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fc90-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="0fc90-134">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0fc90-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0fc90-135">**BM \_ GETstate**</span><span class="sxs-lookup"><span data-stu-id="0fc90-135">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="0fc90-136">**BM \_ SETcheck**</span><span class="sxs-lookup"><span data-stu-id="0fc90-136">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 





