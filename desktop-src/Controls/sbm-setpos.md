---
title: Mensagem de SBM_SETPOS (WinUser. h)
description: A \_ mensagem SBM SETPOS é enviada para definir a posição da caixa de rolagem (Thumb) e, se solicitado, redesenhar a barra de rolagem para refletir a nova posição da caixa de rolagem.
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- Controles de SBM_SETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_SETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a7dc99da5f4b3dbb301f15ddd722f1d664932f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455959"
---
# <a name="sbm_setpos-message"></a><span data-ttu-id="19a6f-104">\_Mensagem SBM SETPOS</span><span class="sxs-lookup"><span data-stu-id="19a6f-104">SBM\_SETPOS message</span></span>

<span data-ttu-id="19a6f-105">A mensagem **SBM \_ SETPOS** é enviada para definir a posição da caixa de rolagem (Thumb) e, se solicitado, redesenhar a barra de rolagem para refletir a nova posição da caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="19a6f-105">The **SBM\_SETPOS** message is sent to set the position of the scroll box (thumb) and, if requested, redraw the scroll bar to reflect the new position of the scroll box.</span></span>

<span data-ttu-id="19a6f-106">Os aplicativos não devem enviar essa mensagem diretamente.</span><span class="sxs-lookup"><span data-stu-id="19a6f-106">Applications should not send this message directly.</span></span> <span data-ttu-id="19a6f-107">Em vez disso, eles devem usar a função [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="19a6f-107">Instead, they should use the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span> <span data-ttu-id="19a6f-108">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="19a6f-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="19a6f-109">Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **SetScrollPos** funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="19a6f-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollPos** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="19a6f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19a6f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19a6f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19a6f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19a6f-112">Especifica a nova posição da caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="19a6f-112">Specifies the new position of the scroll box.</span></span> <span data-ttu-id="19a6f-113">Ele deve estar dentro do intervalo de rolagem.</span><span class="sxs-lookup"><span data-stu-id="19a6f-113">It must be within the scrolling range.</span></span> <span data-ttu-id="19a6f-114">Se esse parâmetro estiver fora do intervalo de rolagem, o valor será arredondado para cima ou para baixo até o valor válido mais próximo.</span><span class="sxs-lookup"><span data-stu-id="19a6f-114">If this parameter is outside of the scrolling range, the value is rounded up or down to the nearest valid value.</span></span>

</dd> <dt>

<span data-ttu-id="19a6f-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19a6f-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19a6f-116">Especifica se a barra de rolagem deve ser redesenhada para refletir a nova posição da caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="19a6f-116">Specifies whether the scroll bar should be redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="19a6f-117">Se esse parâmetro for **true**, a barra de rolagem será redesenhada.</span><span class="sxs-lookup"><span data-stu-id="19a6f-117">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="19a6f-118">Se for **false**, a barra de rolagem não será redesenhada.</span><span class="sxs-lookup"><span data-stu-id="19a6f-118">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19a6f-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19a6f-119">Return value</span></span>

<span data-ttu-id="19a6f-120">**ComCtl32.dll versão 5,0**: se a posição da caixa de rolagem foi alterada, o valor de retorno será a posição anterior da caixa de rolagem; caso contrário, será zero.</span><span class="sxs-lookup"><span data-stu-id="19a6f-120">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="19a6f-121">**ComCtl32.dll versão 6,0**: a posição atual da caixa de rolagem, independentemente se ela foi alterada.</span><span class="sxs-lookup"><span data-stu-id="19a6f-121">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="19a6f-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="19a6f-122">Remarks</span></span>

<span data-ttu-id="19a6f-123">Se o controle da barra de rolagem for redesenhado por uma chamada subsequente para outra função, a definição do parâmetro *lParam* como **false** será útil.</span><span class="sxs-lookup"><span data-stu-id="19a6f-123">If the scroll bar control is redrawn by a subsequent call to another function, setting the *lParam* parameter to **FALSE** is useful.</span></span>

## <a name="requirements"></a><span data-ttu-id="19a6f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19a6f-124">Requirements</span></span>



| <span data-ttu-id="19a6f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="19a6f-125">Requirement</span></span> | <span data-ttu-id="19a6f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="19a6f-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a6f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19a6f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="19a6f-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19a6f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="19a6f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19a6f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="19a6f-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19a6f-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="19a6f-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19a6f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="19a6f-132"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19a6f-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19a6f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="19a6f-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="19a6f-134">**Referência**</span><span class="sxs-lookup"><span data-stu-id="19a6f-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="19a6f-135">**SBM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="19a6f-135">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="19a6f-136">**GetRange SBM \_**</span><span class="sxs-lookup"><span data-stu-id="19a6f-136">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="19a6f-137">**\_SETRANGE SBM**</span><span class="sxs-lookup"><span data-stu-id="19a6f-137">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="19a6f-138">**SBM \_ SETRANGEREDRAW**</span><span class="sxs-lookup"><span data-stu-id="19a6f-138">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

