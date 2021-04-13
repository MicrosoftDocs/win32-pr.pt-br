---
title: Mensagem de MCM_SETDAYSTATE (commctrl. h)
description: Define os Estados de dia para todos os meses que estão visíveis no momento dentro de um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetDayState.
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- Controles de MCM_SETDAYSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6174cc7d8d97d424d599671740530dd8014cc998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455893"
---
# <a name="mcm_setdaystate-message"></a><span data-ttu-id="69d55-105">\_Mensagem MCM SETDAYSTATE</span><span class="sxs-lookup"><span data-stu-id="69d55-105">MCM\_SETDAYSTATE message</span></span>

<span data-ttu-id="69d55-106">Define os Estados de dia para todos os meses que estão visíveis no momento dentro de um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="69d55-106">Sets the day states for all months that are currently visible within a month calendar control.</span></span> <span data-ttu-id="69d55-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) .</span><span class="sxs-lookup"><span data-stu-id="69d55-107">You can send this message explicitly or by using the [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="69d55-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69d55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69d55-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69d55-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69d55-110">Valor indicando quantos elementos estão na matriz para a qual *lParam* aponta.</span><span class="sxs-lookup"><span data-stu-id="69d55-110">Value indicating how many elements are in the array that *lParam* points to.</span></span>

</dd> <dt>

<span data-ttu-id="69d55-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69d55-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69d55-112">Ponteiro para uma matriz de valores [**MONTHDAYSTATE**](monthdaystate.md) que definem como o controle de calendário mensal será desenhado todos os dias em sua exibição.</span><span class="sxs-lookup"><span data-stu-id="69d55-112">Pointer to an array of [**MONTHDAYSTATE**](monthdaystate.md) values that define how the month calendar control will draw each day in its display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69d55-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69d55-113">Return value</span></span>

<span data-ttu-id="69d55-114">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="69d55-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="69d55-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="69d55-115">Remarks</span></span>

<span data-ttu-id="69d55-116">Um aplicativo pode definir explicitamente as informações de estado do dia enviando essa mensagem, mas o estado não será mantido quando uma parte diferente do calendário for rolada para a exibição.</span><span class="sxs-lookup"><span data-stu-id="69d55-116">An application can explicitly set day state information by sending this message, but the state will not persist when a different part of the calendar is scrolled into view.</span></span> <span data-ttu-id="69d55-117">As informações de estado de dia geralmente são definidas em resposta ao código de notificação [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , que é enviado sempre que o controle precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="69d55-117">Day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed.</span></span>

<span data-ttu-id="69d55-118">A matriz em *lParam* deve conter quantos elementos forem retornados pelo valor retornado pela macro a seguir:</span><span class="sxs-lookup"><span data-stu-id="69d55-118">The array at *lParam* must contain as many elements as the value returned by the following macro:</span></span>

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

<span data-ttu-id="69d55-119">Tenha em mente que a matriz em *lParam* deve conter valores [**MONTHDAYSTATE**](monthdaystate.md) que correspondam a todos os meses atualmente na exibição do controle, em ordem cronológica.</span><span class="sxs-lookup"><span data-stu-id="69d55-119">Keep in mind that the array at *lParam* must contain [**MONTHDAYSTATE**](monthdaystate.md) values that correspond with all months currently in the control's display, in chronological order.</span></span> <span data-ttu-id="69d55-120">Isso inclui os dois meses que podem ser exibidos parcialmente antes do primeiro mês e após o último mês.</span><span class="sxs-lookup"><span data-stu-id="69d55-120">This includes the two months that may be partially displayed before the first month and after the last month.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d55-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69d55-121">Requirements</span></span>



| <span data-ttu-id="69d55-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="69d55-122">Requirement</span></span> | <span data-ttu-id="69d55-123">Valor</span><span class="sxs-lookup"><span data-stu-id="69d55-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69d55-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d55-124">Minimum supported client</span></span><br/> | <span data-ttu-id="69d55-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69d55-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69d55-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d55-126">Minimum supported server</span></span><br/> | <span data-ttu-id="69d55-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="69d55-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69d55-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69d55-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="69d55-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="69d55-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69d55-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="69d55-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d55-131">Usando controles de calendário de mês</span><span class="sxs-lookup"><span data-stu-id="69d55-131">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 





