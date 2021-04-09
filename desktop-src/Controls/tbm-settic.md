---
title: Mensagem de TBM_SETTIC (commctrl. h)
description: Define uma marca de escala em um TrackBar na posição lógica especificada.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- Controles de TBM_SETTIC de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085334"
---
# <a name="tbm_settic-message"></a><span data-ttu-id="5e2b8-104">Mensagem de TBM de Conguração \_</span><span class="sxs-lookup"><span data-stu-id="5e2b8-104">TBM\_SETTIC message</span></span>

<span data-ttu-id="5e2b8-105">Define uma marca de escala em um TrackBar na posição lógica especificada.</span><span class="sxs-lookup"><span data-stu-id="5e2b8-105">Sets a tick mark in a trackbar at the specified logical position.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e2b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e2b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e2b8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e2b8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5e2b8-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5e2b8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5e2b8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e2b8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e2b8-110">Posição da marca de escala.</span><span class="sxs-lookup"><span data-stu-id="5e2b8-110">Position of the tick mark.</span></span> <span data-ttu-id="5e2b8-111">Esse parâmetro pode ser qualquer um dos valores inteiros no intervalo de TrackBar de mínimo para o máximo de posições do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="5e2b8-111">This parameter can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e2b8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e2b8-112">Return value</span></span>

<span data-ttu-id="5e2b8-113">Retornará **true** se a marca de escala estiver definida ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="5e2b8-113">Returns **TRUE** if the tick mark is set, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e2b8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e2b8-114">Remarks</span></span>

<span data-ttu-id="5e2b8-115">Um TrackBar cria suas próprias primeiras e últimas marcas de escala.</span><span class="sxs-lookup"><span data-stu-id="5e2b8-115">A trackbar creates its own first and last tick marks.</span></span> <span data-ttu-id="5e2b8-116">Não use essa mensagem para definir a primeira e a última marca de escala.</span><span class="sxs-lookup"><span data-stu-id="5e2b8-116">Do not use this message to set the first and last tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e2b8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e2b8-117">Requirements</span></span>



| <span data-ttu-id="5e2b8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e2b8-118">Requirement</span></span> | <span data-ttu-id="5e2b8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5e2b8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e2b8-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e2b8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5e2b8-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e2b8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e2b8-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e2b8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5e2b8-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5e2b8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e2b8-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e2b8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e2b8-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e2b8-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e2b8-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e2b8-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e2b8-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="5e2b8-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5e2b8-128">**TBM \_ GETPTICS**</span><span class="sxs-lookup"><span data-stu-id="5e2b8-128">**TBM\_GETPTICS**</span></span>](tbm-getptics.md)
</dt> <dt>

[<span data-ttu-id="5e2b8-129">**TBM \_ GETTIC**</span><span class="sxs-lookup"><span data-stu-id="5e2b8-129">**TBM\_GETTIC**</span></span>](tbm-gettic.md)
</dt> </dl>

 

 





