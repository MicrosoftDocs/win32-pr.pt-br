---
title: Mensagem de PBM_SETRANGE (commctrl. h)
description: Define os valores mínimo e máximo para uma barra de progresso e redesenha a barra para refletir o novo intervalo.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- Controles de PBM_SETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e588170c80378082eab7e419e9425e716b8caf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824586"
---
# <a name="pbm_setrange-message"></a><span data-ttu-id="3e6ee-104">\_Mensagem SETRANGE do PBM</span><span class="sxs-lookup"><span data-stu-id="3e6ee-104">PBM\_SETRANGE message</span></span>

<span data-ttu-id="3e6ee-105">Define os valores mínimo e máximo para uma barra de progresso e redesenha a barra para refletir o novo intervalo.</span><span class="sxs-lookup"><span data-stu-id="3e6ee-105">Sets the minimum and maximum values for a progress bar and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e6ee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e6ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e6ee-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e6ee-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e6ee-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3e6ee-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3e6ee-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e6ee-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e6ee-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o valor de intervalo mínimo e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o valor de intervalo máximo.</span><span class="sxs-lookup"><span data-stu-id="3e6ee-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum range value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum range value.</span></span> <span data-ttu-id="3e6ee-111">O valor mínimo do intervalo não deve ser negativo.</span><span class="sxs-lookup"><span data-stu-id="3e6ee-111">The minimum range value must not be negative.</span></span> <span data-ttu-id="3e6ee-112">Por padrão, o valor mínimo é zero.</span><span class="sxs-lookup"><span data-stu-id="3e6ee-112">By default, the minimum value is zero.</span></span> <span data-ttu-id="3e6ee-113">O valor máximo do intervalo deve ser maior que o valor mínimo do intervalo.</span><span class="sxs-lookup"><span data-stu-id="3e6ee-113">The maximum range value must be greater than the minimum range value.</span></span> <span data-ttu-id="3e6ee-114">Por padrão, o valor de intervalo máximo é 100.</span><span class="sxs-lookup"><span data-stu-id="3e6ee-114">By default, the maximum range value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e6ee-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e6ee-115">Return value</span></span>

<span data-ttu-id="3e6ee-116">Retorna os valores do intervalo anterior, se for bem-sucedido, ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3e6ee-116">Returns the previous range values if successful, or zero otherwise.</span></span> <span data-ttu-id="3e6ee-117">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o valor mínimo anterior e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o valor máximo anterior.</span><span class="sxs-lookup"><span data-stu-id="3e6ee-117">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the previous minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the previous maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e6ee-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e6ee-118">Remarks</span></span>

<span data-ttu-id="3e6ee-119">Se você não definir os valores de intervalo, o sistema definirá o valor mínimo como 0 e o valor máximo como 100.</span><span class="sxs-lookup"><span data-stu-id="3e6ee-119">If you do not set the range values, the system sets the minimum value to 0 and the maximum value to 100.</span></span> <span data-ttu-id="3e6ee-120">Como essa mensagem expressa o intervalo como um inteiro sem sinal de 16 bits, ele pode se estender de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="3e6ee-120">Because this message expresses the range as a 16-bit unsigned integer, it can extend from 0 to 65,535.</span></span> <span data-ttu-id="3e6ee-121">O valor mínimo no intervalo pode ser de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="3e6ee-121">The minimum value in the range can be from 0 to 65,535.</span></span> <span data-ttu-id="3e6ee-122">Da mesma forma, o valor máximo pode ser de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="3e6ee-122">Likewise, the maximum value can be from 0 to 65,535.</span></span>

<span data-ttu-id="3e6ee-123">Para definir um intervalo maior, chame o [**PBM \_ SETRANGE32**](pbm-setrange32.md).</span><span class="sxs-lookup"><span data-stu-id="3e6ee-123">To set a larger range, call [**PBM\_SETRANGE32**](pbm-setrange32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e6ee-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e6ee-124">Requirements</span></span>



| <span data-ttu-id="3e6ee-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e6ee-125">Requirement</span></span> | <span data-ttu-id="3e6ee-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3e6ee-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e6ee-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e6ee-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3e6ee-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e6ee-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e6ee-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e6ee-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3e6ee-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3e6ee-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e6ee-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e6ee-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e6ee-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e6ee-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e6ee-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e6ee-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="3e6ee-134">**Referência**</span><span class="sxs-lookup"><span data-stu-id="3e6ee-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3e6ee-135">**GetRange do PBM \_**</span><span class="sxs-lookup"><span data-stu-id="3e6ee-135">**PBM\_GETRANGE**</span></span>](pbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="3e6ee-136">**SETRANGE32 do PBM \_**</span><span class="sxs-lookup"><span data-stu-id="3e6ee-136">**PBM\_SETRANGE32**</span></span>](pbm-setrange32.md)
</dt> </dl>

 

