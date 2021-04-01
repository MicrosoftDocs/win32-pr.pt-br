---
title: Mensagem de TTM_TRACKACTIVATE (commctrl. h)
description: Ativa ou desativa uma dica de ferramenta de rastreamento.
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- Controles de TTM_TRACKACTIVATE de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918695"
---
# <a name="ttm_trackactivate-message"></a><span data-ttu-id="2c8e0-104">\_Mensagem TTM TRACKACTIVATE</span><span class="sxs-lookup"><span data-stu-id="2c8e0-104">TTM\_TRACKACTIVATE message</span></span>

<span data-ttu-id="2c8e0-105">Ativa ou desativa uma dica de ferramenta de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-105">Activates or deactivates a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c8e0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c8e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c8e0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c8e0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c8e0-108">Valor que especifica se o rastreamento está sendo ativado ou desativado.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-108">Value specifying whether tracking is being activated or deactivated.</span></span> <span data-ttu-id="2c8e0-109">Este valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="2c8e0-109">This value can be one of the following:</span></span>



| <span data-ttu-id="2c8e0-110">Valor</span><span class="sxs-lookup"><span data-stu-id="2c8e0-110">Value</span></span>                                                                                                                                | <span data-ttu-id="2c8e0-111">Significado</span><span class="sxs-lookup"><span data-stu-id="2c8e0-111">Meaning</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="2c8e0-112"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="2c8e0-112"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="2c8e0-113">Ativar o acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-113">Activate tracking.</span></span><br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="2c8e0-114"><dt>**FOR**</dt></span><span class="sxs-lookup"><span data-stu-id="2c8e0-114"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="2c8e0-115">Desativar o acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-115">Deactivate tracking.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2c8e0-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c8e0-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c8e0-117">Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que identifica a ferramenta à qual essa mensagem se aplica.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-117">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that identifies the tool to which this message applies.</span></span> <span data-ttu-id="2c8e0-118">Os membros de **HWND** e **UID** identificam a ferramenta e o membro **cbSize** especifica o tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-118">The **hwnd** and **uId** members identify the tool, and the **cbSize** member specifies the size of the structure.</span></span> <span data-ttu-id="2c8e0-119">Todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-119">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c8e0-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c8e0-120">Return value</span></span>

<span data-ttu-id="2c8e0-121">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="2c8e0-121">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c8e0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c8e0-122">Requirements</span></span>



| <span data-ttu-id="2c8e0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c8e0-123">Requirement</span></span> | <span data-ttu-id="2c8e0-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2c8e0-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8e0-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c8e0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2c8e0-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c8e0-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c8e0-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c8e0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2c8e0-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c8e0-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c8e0-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c8e0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c8e0-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c8e0-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c8e0-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c8e0-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c8e0-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="2c8e0-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2c8e0-133">**TTM \_ TRACKPOSITION**</span><span class="sxs-lookup"><span data-stu-id="2c8e0-133">**TTM\_TRACKPOSITION**</span></span>](ttm-trackposition.md)
</dt> <dt>

<span data-ttu-id="2c8e0-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="2c8e0-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2c8e0-135">Usando controles de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="2c8e0-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 





