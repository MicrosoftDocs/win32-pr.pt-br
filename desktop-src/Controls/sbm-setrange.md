---
title: Mensagem de SBM_SETRANGE (WinUser. h)
description: A \_ mensagem SETRANGE SBM é enviada para definir os valores de posição mínima e máxima para o controle barra de rolagem.
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- Controles de SBM_SETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7a720531ae58fdb0712b8f23fd1aef88b3e4caa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824718"
---
# <a name="sbm_setrange-message"></a><span data-ttu-id="034a7-104">\_Mensagem SETRANGE SBM</span><span class="sxs-lookup"><span data-stu-id="034a7-104">SBM\_SETRANGE message</span></span>

<span data-ttu-id="034a7-105">A **mensagem \_ SETRANGE SBM** é enviada para definir os valores de posição mínima e máxima para o controle barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="034a7-105">The **SBM\_SETRANGE** message is sent to set the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="034a7-106">Os aplicativos não devem enviar essa mensagem diretamente.</span><span class="sxs-lookup"><span data-stu-id="034a7-106">Applications should not send this message directly.</span></span> <span data-ttu-id="034a7-107">Em vez disso, eles devem usar a função [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) .</span><span class="sxs-lookup"><span data-stu-id="034a7-107">Instead, they should use the [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) function.</span></span> <span data-ttu-id="034a7-108">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="034a7-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="034a7-109">Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **SetScrollRange** funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="034a7-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="034a7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="034a7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="034a7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="034a7-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="034a7-112">Especifica a posição de rolagem mínima.</span><span class="sxs-lookup"><span data-stu-id="034a7-112">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="034a7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="034a7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="034a7-114">Especifica a posição máxima da rolagem.</span><span class="sxs-lookup"><span data-stu-id="034a7-114">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="034a7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="034a7-115">Return value</span></span>

<span data-ttu-id="034a7-116">**ComCtl32.dll versão 5,0**: se a posição da caixa de rolagem foi alterada, o valor de retorno será a posição anterior da caixa de rolagem; caso contrário, será zero.</span><span class="sxs-lookup"><span data-stu-id="034a7-116">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="034a7-117">**ComCtl32.dll versão 6,0**: a posição atual da caixa de rolagem, independentemente se ela foi alterada.</span><span class="sxs-lookup"><span data-stu-id="034a7-117">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="034a7-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="034a7-118">Remarks</span></span>

<span data-ttu-id="034a7-119">Os valores de posição mínimo e máximo padrão são zero.</span><span class="sxs-lookup"><span data-stu-id="034a7-119">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="034a7-120">A diferença entre os valores especificados pelos parâmetros *wParam* e *lParam* não deve ser maior que MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="034a7-120">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="034a7-121">Se os valores mínimo e máximo da posição forem iguais, o controle da barra de rolagem ficará oculto e, em vigor, desabilitado.</span><span class="sxs-lookup"><span data-stu-id="034a7-121">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="034a7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="034a7-122">Requirements</span></span>



| <span data-ttu-id="034a7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="034a7-123">Requirement</span></span> | <span data-ttu-id="034a7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="034a7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="034a7-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="034a7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="034a7-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="034a7-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="034a7-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="034a7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="034a7-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="034a7-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="034a7-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="034a7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="034a7-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="034a7-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="034a7-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="034a7-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="034a7-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="034a7-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="034a7-133">**SBM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="034a7-133">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="034a7-134">**GetRange SBM \_**</span><span class="sxs-lookup"><span data-stu-id="034a7-134">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="034a7-135">**SBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="034a7-135">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="034a7-136">**SBM \_ SETRANGEREDRAW**</span><span class="sxs-lookup"><span data-stu-id="034a7-136">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

