---
title: Mensagem de MCM_SETTODAY (commctrl. h)
description: Define o \ 0034; hoje \ 0034; seleção de um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ sethoje.
ms.assetid: fcd4d33d-e661-4e02-8d19-666d80e1a070
keywords:
- Controles de MCM_SETTODAY de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b725e5f61e3c08170a323b063616434acb857e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645228"
---
# <a name="mcm_settoday-message"></a><span data-ttu-id="61b2d-105">MCM \_ mensagem de hoje</span><span class="sxs-lookup"><span data-stu-id="61b2d-105">MCM\_SETTODAY message</span></span>

<span data-ttu-id="61b2d-106">Define a seleção "hoje" para um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="61b2d-106">Sets the "today" selection for a month calendar control.</span></span> <span data-ttu-id="61b2d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ sethoje**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) .</span><span class="sxs-lookup"><span data-stu-id="61b2d-107">You can send this message explicitly or by using the [**MonthCal\_SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="61b2d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61b2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61b2d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61b2d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="61b2d-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="61b2d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="61b2d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61b2d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61b2d-112">Ponteiro para uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contém a data a ser definida como a seleção "hoje" para o controle.</span><span class="sxs-lookup"><span data-stu-id="61b2d-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the "today" selection for the control.</span></span> <span data-ttu-id="61b2d-113">Se esse parâmetro for definido como **NULL**, o controle retornará à configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="61b2d-113">If this parameter is set to **NULL**, the control returns to the default setting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61b2d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61b2d-114">Return value</span></span>

<span data-ttu-id="61b2d-115">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="61b2d-115">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="61b2d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="61b2d-116">Remarks</span></span>

<span data-ttu-id="61b2d-117">Se a seleção "hoje" for definida como qualquer data diferente do padrão, as seguintes condições se aplicarão:</span><span class="sxs-lookup"><span data-stu-id="61b2d-117">If the "today" selection is set to any date other than the default, the following conditions apply:</span></span>

-   <span data-ttu-id="61b2d-118">O controle não atualizará automaticamente a seleção "hoje" quando o tempo passar a meia-noite do dia atual.</span><span class="sxs-lookup"><span data-stu-id="61b2d-118">The control will not automatically update the "today" selection when the time passes midnight for the current day.</span></span>
-   <span data-ttu-id="61b2d-119">O controle não atualizará automaticamente sua exibição com base nas alterações de localidade.</span><span class="sxs-lookup"><span data-stu-id="61b2d-119">The control will not automatically update its display based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="61b2d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61b2d-120">Requirements</span></span>



| <span data-ttu-id="61b2d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="61b2d-121">Requirement</span></span> | <span data-ttu-id="61b2d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="61b2d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61b2d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61b2d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="61b2d-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61b2d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61b2d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61b2d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="61b2d-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="61b2d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61b2d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61b2d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="61b2d-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61b2d-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61b2d-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="61b2d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b2d-130">Vezes no controle de calendário mensal</span><span class="sxs-lookup"><span data-stu-id="61b2d-130">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

