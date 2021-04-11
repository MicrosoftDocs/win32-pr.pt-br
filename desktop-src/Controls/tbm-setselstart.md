---
title: Mensagem de TBM_SETSELSTART (commctrl. h)
description: Define a posição lógica inicial do intervalo de seleção atual em um TrackBar. Essa mensagem será ignorada se o TrackBar não tiver o \_ estilo ENABLESELRANGE TBS.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- Controles de TBM_SETSELSTART de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445cb97c73f8e6483b5d4dd76bc3ccf64322e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008847"
---
# <a name="tbm_setselstart-message"></a><span data-ttu-id="a8e5d-105">\_Mensagem tbm SETSELSTART</span><span class="sxs-lookup"><span data-stu-id="a8e5d-105">TBM\_SETSELSTART message</span></span>

<span data-ttu-id="a8e5d-106">Define a posição lógica inicial do intervalo de seleção atual em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a8e5d-106">Sets the starting logical position of the current selection range in a trackbar.</span></span> <span data-ttu-id="a8e5d-107">Essa mensagem será ignorada se o TrackBar não tiver o [**estilo \_ ENABLESELRANGE TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a8e5d-107">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8e5d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8e5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8e5d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8e5d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8e5d-110">Sinalizador de redesenho.</span><span class="sxs-lookup"><span data-stu-id="a8e5d-110">Redraw flag.</span></span> <span data-ttu-id="a8e5d-111">Se esse parâmetro for **true**, a mensagem redesenhará o TrackBar depois que o intervalo de seleção for definido.</span><span class="sxs-lookup"><span data-stu-id="a8e5d-111">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="a8e5d-112">Se esse parâmetro for **false**, a mensagem definirá o intervalo de seleção, mas não redesenhará o TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a8e5d-112">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="a8e5d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8e5d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8e5d-114">Posição inicial do intervalo de seleção.</span><span class="sxs-lookup"><span data-stu-id="a8e5d-114">Starting position of the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8e5d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8e5d-115">Return value</span></span>

<span data-ttu-id="a8e5d-116">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a8e5d-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8e5d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8e5d-117">Requirements</span></span>



| <span data-ttu-id="a8e5d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8e5d-118">Requirement</span></span> | <span data-ttu-id="a8e5d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a8e5d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e5d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8e5d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e5d-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8e5d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8e5d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8e5d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e5d-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8e5d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8e5d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8e5d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8e5d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8e5d-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8e5d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8e5d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8e5d-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a8e5d-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a8e5d-128">**TBM \_ GETSELEND**</span><span class="sxs-lookup"><span data-stu-id="a8e5d-128">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="a8e5d-129">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="a8e5d-129">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="a8e5d-130">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="a8e5d-130">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="a8e5d-131">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="a8e5d-131">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> </dl>

 

 





