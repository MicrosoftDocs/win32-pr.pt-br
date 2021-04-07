---
title: Mensagem de SBM_GETRANGE (WinUser. h)
description: A \_ mensagem GETrange do SBM é enviada para recuperar os valores mínimo e máximo da posição para o controle da barra de rolagem.
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- Controles de SBM_GETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ca47e0474152a9771d2787c4a039fb2c868b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918861"
---
# <a name="sbm_getrange-message"></a><span data-ttu-id="16593-104">SBM \_ mensagem GETrange</span><span class="sxs-lookup"><span data-stu-id="16593-104">SBM\_GETRANGE message</span></span>

<span data-ttu-id="16593-105">A **mensagem \_ GetRange do SBM** é enviada para recuperar os valores mínimo e máximo da posição para o controle da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="16593-105">The **SBM\_GETRANGE** message is sent to retrieve the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="16593-106">Os aplicativos não devem enviar essa mensagem diretamente.</span><span class="sxs-lookup"><span data-stu-id="16593-106">Applications should not send this message directly.</span></span> <span data-ttu-id="16593-107">Em vez disso, eles devem usar a função [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) .</span><span class="sxs-lookup"><span data-stu-id="16593-107">Instead, they should use the [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) function.</span></span> <span data-ttu-id="16593-108">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="16593-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="16593-109">Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **GetScrollRange** funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="16593-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="16593-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16593-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16593-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16593-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16593-112">Ponteiro para uma variável que recebe a posição de rolagem mínima.</span><span class="sxs-lookup"><span data-stu-id="16593-112">Pointer to a variable that receives the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="16593-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16593-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16593-114">Ponteiro para uma variável que recebe a posição de rolagem máxima.</span><span class="sxs-lookup"><span data-stu-id="16593-114">Pointer to a variable that receives the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16593-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16593-115">Return value</span></span>

<span data-ttu-id="16593-116">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="16593-116">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="16593-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16593-117">Requirements</span></span>



| <span data-ttu-id="16593-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="16593-118">Requirement</span></span> | <span data-ttu-id="16593-119">Valor</span><span class="sxs-lookup"><span data-stu-id="16593-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16593-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16593-120">Minimum supported client</span></span><br/> | <span data-ttu-id="16593-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16593-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="16593-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16593-122">Minimum supported server</span></span><br/> | <span data-ttu-id="16593-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="16593-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="16593-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16593-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="16593-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16593-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16593-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="16593-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="16593-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="16593-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="16593-128">**SBM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="16593-128">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="16593-129">**SBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="16593-129">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="16593-130">**\_SETRANGE SBM**</span><span class="sxs-lookup"><span data-stu-id="16593-130">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="16593-131">**SBM \_ SETRANGEREDRAW**</span><span class="sxs-lookup"><span data-stu-id="16593-131">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

