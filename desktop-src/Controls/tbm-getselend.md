---
title: Mensagem de TBM_GETSELEND (commctrl. h)
description: Recupera a posição final do intervalo de seleção atual em um TrackBar.
ms.assetid: e365dd4d-eb49-4107-b6d4-cdb558d27fdb
keywords:
- Controles de TBM_GETSELEND de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 486d66d3e7fc2dd4d23b89cb5e9406fa81b34638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455175"
---
# <a name="tbm_getselend-message"></a><span data-ttu-id="aa4ce-104">\_Mensagem tbm GETSELEND</span><span class="sxs-lookup"><span data-stu-id="aa4ce-104">TBM\_GETSELEND message</span></span>

<span data-ttu-id="aa4ce-105">Recupera a posição final do intervalo de seleção atual em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-105">Retrieves the ending position of the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa4ce-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa4ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa4ce-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa4ce-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="aa4ce-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="aa4ce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa4ce-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="aa4ce-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa4ce-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa4ce-111">Return value</span></span>

<span data-ttu-id="aa4ce-112">Retorna um valor de 32 bits que especifica a posição final do intervalo de seleção atual.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-112">Returns a 32-bit value that specifies the ending position of the current selection range.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa4ce-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa4ce-113">Remarks</span></span>

<span data-ttu-id="aa4ce-114">Um TrackBar pode ter um intervalo de seleção somente se você especificou o estilo de [**\_ ENABLESELRANGE TBS**](trackbar-control-styles.md) quando o criou.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-114">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa4ce-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa4ce-115">Requirements</span></span>



| <span data-ttu-id="aa4ce-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa4ce-116">Requirement</span></span> | <span data-ttu-id="aa4ce-117">Valor</span><span class="sxs-lookup"><span data-stu-id="aa4ce-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4ce-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa4ce-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aa4ce-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa4ce-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa4ce-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa4ce-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aa4ce-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa4ce-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa4ce-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa4ce-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa4ce-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa4ce-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa4ce-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa4ce-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa4ce-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aa4ce-126">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-126">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="aa4ce-127">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="aa4ce-128">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="aa4ce-129">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





