---
title: Mensagem de TBM_SETSELEND (commctrl. h)
description: Define a posição lógica final do intervalo de seleção atual em um TrackBar. Essa mensagem será ignorada se o TrackBar não tiver o \_ estilo ENABLESELRANGE TBS.
ms.assetid: 1feec14c-1607-49d5-a147-af2443f82dc1
keywords:
- Controles de TBM_SETSELEND de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146446df4daf8e8ac7c0f3499149ba0f46940880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085154"
---
# <a name="tbm_setselend-message"></a><span data-ttu-id="b8aaf-105">\_Mensagem tbm SETSELEND</span><span class="sxs-lookup"><span data-stu-id="b8aaf-105">TBM\_SETSELEND message</span></span>

<span data-ttu-id="b8aaf-106">Define a posição lógica final do intervalo de seleção atual em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-106">Sets the ending logical position of the current selection range in a trackbar.</span></span> <span data-ttu-id="b8aaf-107">Essa mensagem será ignorada se o TrackBar não tiver o [**estilo \_ ENABLESELRANGE TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b8aaf-107">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8aaf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8aaf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8aaf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8aaf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8aaf-110">Sinalizador de redesenho.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-110">Redraw flag.</span></span> <span data-ttu-id="b8aaf-111">Se esse parâmetro for **true**, a mensagem redesenhará o TrackBar depois que o intervalo de seleção for definido.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-111">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="b8aaf-112">Se esse parâmetro for **false**, a mensagem definirá o intervalo de seleção, mas não redesenhará o TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-112">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="b8aaf-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8aaf-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8aaf-114">Posição lógica final do intervalo de seleção.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-114">Ending logical position of the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8aaf-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8aaf-115">Return value</span></span>

<span data-ttu-id="b8aaf-116">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8aaf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8aaf-117">Requirements</span></span>



| <span data-ttu-id="b8aaf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8aaf-118">Requirement</span></span> | <span data-ttu-id="b8aaf-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b8aaf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8aaf-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8aaf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b8aaf-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8aaf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8aaf-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8aaf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b8aaf-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8aaf-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8aaf-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8aaf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8aaf-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8aaf-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8aaf-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8aaf-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b8aaf-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b8aaf-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b8aaf-128">**TBM \_ GETSELEND**</span><span class="sxs-lookup"><span data-stu-id="b8aaf-128">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="b8aaf-129">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="b8aaf-129">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="b8aaf-130">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="b8aaf-130">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="b8aaf-131">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="b8aaf-131">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





