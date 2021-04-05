---
title: Mensagem de SBM_GETPOS (WinUser. h)
description: A \_ mensagem SBM GETPOS é enviada para recuperar a posição atual da caixa de rolagem de um controle de barra de rolagem.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- Controles de SBM_GETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d088fc790985e57928f1ab56cd42254b1a087dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918862"
---
# <a name="sbm_getpos-message"></a><span data-ttu-id="7c6cc-104">\_Mensagem SBM GETPOS</span><span class="sxs-lookup"><span data-stu-id="7c6cc-104">SBM\_GETPOS message</span></span>

<span data-ttu-id="7c6cc-105">A mensagem **SBM \_ GETPOS** é enviada para recuperar a posição atual da caixa de rolagem de um controle de barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-105">The **SBM\_GETPOS** message is sent to retrieve the current position of the scroll box of a scroll bar control.</span></span> <span data-ttu-id="7c6cc-106">A posição atual é um valor relativo que depende do intervalo de rolagem atual.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-106">The current position is a relative value that depends on the current scrolling range.</span></span> <span data-ttu-id="7c6cc-107">Por exemplo, se o intervalo de rolagem for de 0 a 100 e a caixa de rolagem estiver no meio da barra, a posição atual será 50.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-107">For example, if the scrolling range is 0 through 100 and the scroll box is in the middle of the bar, the current position is 50.</span></span>

<span data-ttu-id="7c6cc-108">Os aplicativos não devem enviar essa mensagem diretamente.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-108">Applications should not send this message directly.</span></span> <span data-ttu-id="7c6cc-109">Em vez disso, eles devem usar a função [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="7c6cc-109">Instead, they should use the [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) function.</span></span> <span data-ttu-id="7c6cc-110">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7c6cc-110">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="7c6cc-111">Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **GetScrollPos** funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-111">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollPos** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c6cc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c6cc-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c6cc-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c6cc-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6cc-114">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-114">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7c6cc-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c6cc-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6cc-116">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-116">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c6cc-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c6cc-117">Return value</span></span>

<span data-ttu-id="7c6cc-118">O valor de retorno é a posição atual da caixa de rolagem na barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-118">The return value is the current position of the scroll box in the scroll bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c6cc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c6cc-119">Requirements</span></span>



| <span data-ttu-id="7c6cc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c6cc-120">Requirement</span></span> | <span data-ttu-id="7c6cc-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7c6cc-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6cc-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c6cc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7c6cc-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c6cc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7c6cc-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c6cc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7c6cc-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c6cc-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7c6cc-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c6cc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c6cc-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c6cc-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c6cc-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c6cc-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c6cc-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7c6cc-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7c6cc-130">**GetRange SBM \_**</span><span class="sxs-lookup"><span data-stu-id="7c6cc-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="7c6cc-131">**SBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="7c6cc-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="7c6cc-132">**\_SETRANGE SBM**</span><span class="sxs-lookup"><span data-stu-id="7c6cc-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="7c6cc-133">**SBM \_ SETRANGEREDRAW**</span><span class="sxs-lookup"><span data-stu-id="7c6cc-133">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

