---
title: Mensagem de RB_ENDDRAG (commctrl. h)
description: Encerra a operação de arrastar e soltar do controle rebar. Esta mensagem não faz com que uma \_ notificação RBN endarraste seja enviada.
ms.assetid: 4991dda6-32ea-4d3e-9d39-17c2b6995f09
keywords:
- Controles de RB_ENDDRAG de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b6f201471b6f260555aacb9d89c1363492ed6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918782"
---
# <a name="rb_enddrag-message"></a><span data-ttu-id="cb619-105">Mensagem de fim de operação RB \_</span><span class="sxs-lookup"><span data-stu-id="cb619-105">RB\_ENDDRAG message</span></span>

<span data-ttu-id="cb619-106">Encerra a operação de arrastar e soltar do controle rebar.</span><span class="sxs-lookup"><span data-stu-id="cb619-106">Terminates the rebar control's drag-and-drop operation.</span></span> <span data-ttu-id="cb619-107">Esta mensagem não faz com que uma notificação [RBN \_ endarraste](rbn-enddrag.md) seja enviada.</span><span class="sxs-lookup"><span data-stu-id="cb619-107">This message does not cause an [RBN\_ENDDRAG](rbn-enddrag.md) notification to be sent.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb619-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb619-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb619-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb619-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cb619-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cb619-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cb619-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb619-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cb619-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cb619-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb619-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb619-113">Return value</span></span>

<span data-ttu-id="cb619-114">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="cb619-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb619-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb619-115">Requirements</span></span>



| <span data-ttu-id="cb619-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb619-116">Requirement</span></span> | <span data-ttu-id="cb619-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cb619-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb619-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb619-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cb619-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb619-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb619-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb619-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cb619-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb619-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb619-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb619-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb619-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb619-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb619-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb619-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb619-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="cb619-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cb619-126">**\_BEGINDRAG RB**</span><span class="sxs-lookup"><span data-stu-id="cb619-126">**RB\_BEGINDRAG**</span></span>](rb-begindrag.md)
</dt> <dt>

[<span data-ttu-id="cb619-127">**\_DRAGMOVE RB**</span><span class="sxs-lookup"><span data-stu-id="cb619-127">**RB\_DRAGMOVE**</span></span>](rb-dragmove.md)
</dt> </dl>

 

 





