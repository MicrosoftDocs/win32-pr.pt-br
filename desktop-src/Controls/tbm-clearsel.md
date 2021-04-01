---
title: Mensagem de TBM_CLEARSEL (commctrl. h)
description: Limpa o intervalo de seleção atual em um TrackBar.
ms.assetid: ccf69fb7-d616-4a7a-8c7c-7a82827758b1
keywords:
- Controles de TBM_CLEARSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_CLEARSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d2474f3978dc80b2611bd6b454c45e515ee159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824841"
---
# <a name="tbm_clearsel-message"></a><span data-ttu-id="aa42a-104">\_Mensagem tbm CLEARSEL</span><span class="sxs-lookup"><span data-stu-id="aa42a-104">TBM\_CLEARSEL message</span></span>

<span data-ttu-id="aa42a-105">Limpa o intervalo de seleção atual em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="aa42a-105">Clears the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa42a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa42a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa42a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa42a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa42a-108">Sinalizador de redesenho.</span><span class="sxs-lookup"><span data-stu-id="aa42a-108">Redraw flag.</span></span> <span data-ttu-id="aa42a-109">Se esse parâmetro for **true**, o TrackBar será redesenhado depois que a seleção for desmarcada.</span><span class="sxs-lookup"><span data-stu-id="aa42a-109">If this parameter is **TRUE**, the trackbar is redrawn after the selection is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="aa42a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa42a-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="aa42a-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="aa42a-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa42a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa42a-112">Return value</span></span>

<span data-ttu-id="aa42a-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="aa42a-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa42a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa42a-114">Remarks</span></span>

<span data-ttu-id="aa42a-115">Um TrackBar pode ter um intervalo de seleção somente se você especificou o estilo de [**\_ ENABLESELRANGE TBS**](trackbar-control-styles.md) quando o criou.</span><span class="sxs-lookup"><span data-stu-id="aa42a-115">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa42a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa42a-116">Requirements</span></span>



| <span data-ttu-id="aa42a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa42a-117">Requirement</span></span> | <span data-ttu-id="aa42a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="aa42a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa42a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa42a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aa42a-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa42a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa42a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa42a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aa42a-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa42a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa42a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa42a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa42a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa42a-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa42a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa42a-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa42a-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="aa42a-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aa42a-127">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="aa42a-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="aa42a-128">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="aa42a-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="aa42a-129">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="aa42a-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





