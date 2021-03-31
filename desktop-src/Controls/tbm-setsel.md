---
title: Mensagem de TBM_SETSEL (commctrl. h)
description: Define as posições inicial e final para o intervalo de seleção disponível em um TrackBar.
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- Controles de TBM_SETSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edebc6b6dcf3b0b93e3047a39aac74c34d121bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644250"
---
# <a name="tbm_setsel-message"></a><span data-ttu-id="e14dc-104">\_Mensagem tbm SETSEL</span><span class="sxs-lookup"><span data-stu-id="e14dc-104">TBM\_SETSEL message</span></span>

<span data-ttu-id="e14dc-105">Define as posições inicial e final para o intervalo de seleção disponível em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="e14dc-105">Sets the starting and ending positions for the available selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="e14dc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e14dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e14dc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e14dc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e14dc-108">Sinalizador de redesenho.</span><span class="sxs-lookup"><span data-stu-id="e14dc-108">Redraw flag.</span></span> <span data-ttu-id="e14dc-109">Se esse parâmetro for **true**, a mensagem redesenhará o TrackBar depois que o intervalo de seleção for definido.</span><span class="sxs-lookup"><span data-stu-id="e14dc-109">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="e14dc-110">Se esse parâmetro for **false**, a mensagem definirá o intervalo de seleção, mas não redesenhará o TrackBar.</span><span class="sxs-lookup"><span data-stu-id="e14dc-110">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="e14dc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e14dc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e14dc-112">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a posição lógica inicial para o intervalo de seleção e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição lógica final.</span><span class="sxs-lookup"><span data-stu-id="e14dc-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the starting logical position for the selection range, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the ending logical position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e14dc-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e14dc-113">Return value</span></span>

<span data-ttu-id="e14dc-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e14dc-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e14dc-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e14dc-115">Remarks</span></span>

<span data-ttu-id="e14dc-116">Essa mensagem será ignorada se o TrackBar não tiver o [**estilo \_ ENABLESELRANGE TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e14dc-116">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

<span data-ttu-id="e14dc-117">**Tbm \_ SETSEL** permite restringir o ponteiro a apenas uma parte do intervalo disponível para a barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="e14dc-117">**TBM\_SETSEL** allows you to restrict the pointer to only a portion of the range available to the progress bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="e14dc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e14dc-118">Requirements</span></span>



| <span data-ttu-id="e14dc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e14dc-119">Requirement</span></span> | <span data-ttu-id="e14dc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e14dc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e14dc-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e14dc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e14dc-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e14dc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e14dc-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e14dc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e14dc-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e14dc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e14dc-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e14dc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e14dc-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e14dc-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e14dc-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e14dc-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e14dc-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="e14dc-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e14dc-129">**TBM \_ GETSELEND**</span><span class="sxs-lookup"><span data-stu-id="e14dc-129">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="e14dc-130">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="e14dc-130">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="e14dc-131">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="e14dc-131">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="e14dc-132">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="e14dc-132">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

