---
title: Mensagem de UDM_SETRANGE (commctrl. h)
description: Define as posições mínima e máxima (intervalo) para um controle de cima para baixo.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- Controles de UDM_SETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb32a72ca8ca5182e87e2c0346cbc44ab25300e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009547"
---
# <a name="udm_setrange-message"></a><span data-ttu-id="77fb9-104">Mensagem do UDM \_ SETRANGE</span><span class="sxs-lookup"><span data-stu-id="77fb9-104">UDM\_SETRANGE message</span></span>

<span data-ttu-id="77fb9-105">Define as posições mínima e máxima (intervalo) para um controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="77fb9-105">Sets the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="77fb9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77fb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77fb9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77fb9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="77fb9-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="77fb9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="77fb9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77fb9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77fb9-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **curto** que especifica a posição máxima para o controle de cima para baixo e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é um **curto** que especifica a posição mínima.</span><span class="sxs-lookup"><span data-stu-id="77fb9-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **short** that specifies the maximum position for the up-down control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **short** that specifies the minimum position.</span></span> <span data-ttu-id="77fb9-111">Nenhuma posição pode ser maior que o \_ valor de maxVal UD ou menor que o \_ valor de minVal UD.</span><span class="sxs-lookup"><span data-stu-id="77fb9-111">Neither position can be greater than the UD\_MAXVAL value or less than the UD\_MINVAL value.</span></span> <span data-ttu-id="77fb9-112">Além disso, a diferença entre as duas posições não pode exceder UD \_ maxVal.</span><span class="sxs-lookup"><span data-stu-id="77fb9-112">In addition, the difference between the two positions cannot exceed UD\_MAXVAL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77fb9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77fb9-113">Return value</span></span>

<span data-ttu-id="77fb9-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="77fb9-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77fb9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="77fb9-115">Remarks</span></span>

<span data-ttu-id="77fb9-116">A posição máxima pode ser menor que a posição mínima.</span><span class="sxs-lookup"><span data-stu-id="77fb9-116">The maximum position can be less than the minimum position.</span></span> <span data-ttu-id="77fb9-117">Clicar no botão de seta para cima move a posição atual para mais perto da posição máxima e, ao clicar no botão de seta para baixo, move-se para a posição mínima.</span><span class="sxs-lookup"><span data-stu-id="77fb9-117">Clicking the up arrow button moves the current position closer to the maximum position, and clicking the down arrow button moves toward the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="77fb9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77fb9-118">Requirements</span></span>



| <span data-ttu-id="77fb9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="77fb9-119">Requirement</span></span> | <span data-ttu-id="77fb9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="77fb9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77fb9-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77fb9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="77fb9-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77fb9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77fb9-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77fb9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="77fb9-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77fb9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77fb9-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77fb9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="77fb9-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77fb9-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77fb9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="77fb9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77fb9-128">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="77fb9-128">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="77fb9-129">**SETRANGE de UDM \_**</span><span class="sxs-lookup"><span data-stu-id="77fb9-129">**UDM\_SETRANGE**</span></span>](udm-setrange.md)
</dt> </dl>

 

