---
title: Mensagem de TBM_SETRANGEMAX (commctrl. h)
description: Define a posição lógica máxima para o controle deslizante em um TrackBar.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- Controles de TBM_SETRANGEMAX de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43997725e2fa88db3f9d4dc2fec1d51255cbb0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454619"
---
# <a name="tbm_setrangemax-message"></a><span data-ttu-id="bea1c-104">\_Mensagem tbm SETRANGEMAX</span><span class="sxs-lookup"><span data-stu-id="bea1c-104">TBM\_SETRANGEMAX message</span></span>

<span data-ttu-id="bea1c-105">Define a posição lógica máxima para o controle deslizante em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bea1c-105">Sets the maximum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="bea1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bea1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bea1c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bea1c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bea1c-108">Sinalizador de redesenho.</span><span class="sxs-lookup"><span data-stu-id="bea1c-108">Redraw flag.</span></span> <span data-ttu-id="bea1c-109">Se esse parâmetro for **true**, o TrackBar será redesenhado depois que o intervalo for definido.</span><span class="sxs-lookup"><span data-stu-id="bea1c-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="bea1c-110">Se esse parâmetro for **false**, a mensagem definirá o intervalo, mas não redesenhará o TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bea1c-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="bea1c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bea1c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bea1c-112">Posição máxima do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="bea1c-112">Maximum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bea1c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bea1c-113">Return value</span></span>

<span data-ttu-id="bea1c-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="bea1c-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bea1c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="bea1c-115">Remarks</span></span>

<span data-ttu-id="bea1c-116">Se a posição do controle deslizante atual for maior que o novo máximo, a mensagem **tbm \_ SETRANGEMAX** definirá a posição do controle deslizante como o novo valor máximo.</span><span class="sxs-lookup"><span data-stu-id="bea1c-116">If the current slider position is greater than the new maximum, the **TBM\_SETRANGEMAX** message sets the slider position to the new maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bea1c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bea1c-117">Requirements</span></span>



| <span data-ttu-id="bea1c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bea1c-118">Requirement</span></span> | <span data-ttu-id="bea1c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bea1c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bea1c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bea1c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bea1c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bea1c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bea1c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bea1c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bea1c-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bea1c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bea1c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bea1c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bea1c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bea1c-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bea1c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="bea1c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="bea1c-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="bea1c-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bea1c-128">**\_SETRANGE tbm**</span><span class="sxs-lookup"><span data-stu-id="bea1c-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="bea1c-129">**TBM \_ SETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="bea1c-129">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 

 





