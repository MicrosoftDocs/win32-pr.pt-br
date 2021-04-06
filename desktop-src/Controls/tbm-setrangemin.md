---
title: Mensagem de TBM_SETRANGEMIN (commctrl. h)
description: Define a posição lógica mínima para o controle deslizante em um TrackBar.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- Controles de TBM_SETRANGEMIN de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34c2e70aa6247cb970e576c915bdcd28cd18d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917982"
---
# <a name="tbm_setrangemin-message"></a><span data-ttu-id="6cd82-104">\_Mensagem tbm SETRANGEMIN</span><span class="sxs-lookup"><span data-stu-id="6cd82-104">TBM\_SETRANGEMIN message</span></span>

<span data-ttu-id="6cd82-105">Define a posição lógica mínima para o controle deslizante em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6cd82-105">Sets the minimum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cd82-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cd82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cd82-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cd82-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cd82-108">Sinalizador de redesenho.</span><span class="sxs-lookup"><span data-stu-id="6cd82-108">Redraw flag.</span></span> <span data-ttu-id="6cd82-109">Se esse parâmetro for **true**, a mensagem redesenhará o TrackBar depois que o intervalo for definido.</span><span class="sxs-lookup"><span data-stu-id="6cd82-109">If this parameter is **TRUE**, the message redraws the trackbar after the range is set.</span></span> <span data-ttu-id="6cd82-110">Se esse parâmetro for **false**, a mensagem definirá o intervalo, mas não redesenhará o TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6cd82-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="6cd82-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cd82-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cd82-112">Posição mínima do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="6cd82-112">Minimum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cd82-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6cd82-113">Return value</span></span>

<span data-ttu-id="6cd82-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="6cd82-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cd82-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cd82-115">Remarks</span></span>

<span data-ttu-id="6cd82-116">Se a posição do controle deslizante atual for menor que o novo mínimo, a mensagem **tbm \_ SETRANGEMIN** definirá a posição do controle deslizante como o novo valor mínimo.</span><span class="sxs-lookup"><span data-stu-id="6cd82-116">If the current slider position is less than the new minimum, the **TBM\_SETRANGEMIN** message sets the slider position to the new minimum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd82-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cd82-117">Requirements</span></span>



| <span data-ttu-id="6cd82-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cd82-118">Requirement</span></span> | <span data-ttu-id="6cd82-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6cd82-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd82-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cd82-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6cd82-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6cd82-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cd82-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cd82-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6cd82-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6cd82-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cd82-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6cd82-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cd82-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cd82-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cd82-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cd82-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6cd82-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6cd82-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6cd82-128">**\_SETRANGE tbm**</span><span class="sxs-lookup"><span data-stu-id="6cd82-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="6cd82-129">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="6cd82-129">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





