---
title: Mensagem de TBM_SETRANGE (commctrl. h)
description: Define o intervalo de posições lógicas mínimas e máximas para o controle deslizante em um TrackBar.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- Controles de TBM_SETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d870df628b06031374260c679f792f0b7218a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009119"
---
# <a name="tbm_setrange-message"></a><span data-ttu-id="1bfe5-104">\_Mensagem SETRANGE tbm</span><span class="sxs-lookup"><span data-stu-id="1bfe5-104">TBM\_SETRANGE message</span></span>

<span data-ttu-id="1bfe5-105">Define o intervalo de posições lógicas mínimas e máximas para o controle deslizante em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="1bfe5-105">Sets the range of minimum and maximum logical positions for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1bfe5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1bfe5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bfe5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1bfe5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bfe5-108">Sinalizador de redesenho.</span><span class="sxs-lookup"><span data-stu-id="1bfe5-108">Redraw flag.</span></span> <span data-ttu-id="1bfe5-109">Se esse parâmetro for **true**, o TrackBar será redesenhado depois que o intervalo for definido.</span><span class="sxs-lookup"><span data-stu-id="1bfe5-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="1bfe5-110">Se esse parâmetro for **false**, a mensagem definirá o intervalo, mas não redesenhará o TrackBar.</span><span class="sxs-lookup"><span data-stu-id="1bfe5-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="1bfe5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1bfe5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bfe5-112">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a posição mínima para o controle deslizante e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição máxima.</span><span class="sxs-lookup"><span data-stu-id="1bfe5-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum position for the slider, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bfe5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1bfe5-113">Return value</span></span>

<span data-ttu-id="1bfe5-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1bfe5-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bfe5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bfe5-115">Remarks</span></span>

<span data-ttu-id="1bfe5-116">Se a posição do controle deslizante atual estiver fora do novo intervalo, a mensagem **\_ SETRANGE tbm** definirá a posição do controle deslizante como o novo valor máximo ou mínimo.</span><span class="sxs-lookup"><span data-stu-id="1bfe5-116">If the current slider position is outside the new range, the **TBM\_SETRANGE** message sets the slider position to the new maximum or minimum value.</span></span>

<span data-ttu-id="1bfe5-117">Como essa mensagem usa valores inteiros sem sinal de 2 16 bits, o intervalo máximo que essa mensagem pode especificar é de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="1bfe5-117">Because this message takes two 16-bit unsigned integer values, the maximum range that this message can specify is from 0 to 65,535.</span></span> <span data-ttu-id="1bfe5-118">Para especificar valores de intervalo maiores, use as mensagens [**tbm \_ SETRANGEMIN**](tbm-setrangemin.md) e [**tbm \_ SETRANGEMAX**](tbm-setrangemax.md) .</span><span class="sxs-lookup"><span data-stu-id="1bfe5-118">To specify larger range values, use the [**TBM\_SETRANGEMIN**](tbm-setrangemin.md) and [**TBM\_SETRANGEMAX**](tbm-setrangemax.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bfe5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bfe5-119">Requirements</span></span>



| <span data-ttu-id="1bfe5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bfe5-120">Requirement</span></span> | <span data-ttu-id="1bfe5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1bfe5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfe5-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bfe5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1bfe5-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1bfe5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1bfe5-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bfe5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1bfe5-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1bfe5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1bfe5-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1bfe5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bfe5-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bfe5-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bfe5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bfe5-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="1bfe5-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="1bfe5-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1bfe5-130">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="1bfe5-130">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> <dt>

[<span data-ttu-id="1bfe5-131">**TBM \_ SETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="1bfe5-131">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 

