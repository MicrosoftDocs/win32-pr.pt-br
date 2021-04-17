---
title: Mensagem de MCM_GETMONTHRANGE (commctrl. h)
description: Recupera informações de data (usando estruturas SYSTEMTIME) que representam os limites altos e baixos da exibição de um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetMonthRange.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- Controles de MCM_GETMONTHRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022ca7e05cc0c69cd32f6ad92531420cdaed7c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753963"
---
# <a name="mcm_getmonthrange-message"></a><span data-ttu-id="bef79-105">\_Mensagem MCM GETMONTHRANGE</span><span class="sxs-lookup"><span data-stu-id="bef79-105">MCM\_GETMONTHRANGE message</span></span>

<span data-ttu-id="bef79-106">Recupera informações de data (usando estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) ) que representam os limites altos e baixos da exibição de um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="bef79-106">Retrieves date information (using [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures) that represents the high and low limits of a month calendar control's display.</span></span> <span data-ttu-id="bef79-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) .</span><span class="sxs-lookup"><span data-stu-id="bef79-107">You can send this message explicitly or by using the [**MonthCal\_GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bef79-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bef79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bef79-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bef79-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bef79-110">Valor que especifica o escopo dos limites de intervalo a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="bef79-110">Value specifying the scope of the range limits to be retrieved.</span></span> <span data-ttu-id="bef79-111">Esse valor deve ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="bef79-111">This value must be one of the following:</span></span>



| <span data-ttu-id="bef79-112">Valor</span><span class="sxs-lookup"><span data-stu-id="bef79-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="bef79-113">Significado</span><span class="sxs-lookup"><span data-stu-id="bef79-113">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <span data-ttu-id="bef79-114"><dt>**GMR \_ DAYSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="bef79-114"><dt>**GMR\_DAYSTATE**</dt></span></span> </dl> | <span data-ttu-id="bef79-115">Incluir meses anteriores e posteriores do intervalo visível que são exibidos apenas parcialmente.</span><span class="sxs-lookup"><span data-stu-id="bef79-115">Include preceding and trailing months of visible range that are only partially displayed.</span></span> <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <span data-ttu-id="bef79-116"><dt>**GMR \_ visível**</dt></span><span class="sxs-lookup"><span data-stu-id="bef79-116"><dt>**GMR\_VISIBLE**</dt></span></span> </dl>    | <span data-ttu-id="bef79-117">Inclua somente os meses que são totalmente exibidos.</span><span class="sxs-lookup"><span data-stu-id="bef79-117">Include only those months that are entirely displayed.</span></span> <br/>                                    |



 

</dd> <dt>

<span data-ttu-id="bef79-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bef79-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bef79-119">Ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que receberá os limites inferior e superior do escopo especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="bef79-119">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the scope specified by *wParam*.</span></span> <span data-ttu-id="bef79-120">Os limites inferior e superior são colocados em *lprgSysTimeArray* \[ 0 \] e *lprgSysTimeArray* \[ 1 \] , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bef79-120">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="bef79-121">Esse parâmetro deve ser um endereço válido e não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bef79-121">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bef79-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bef79-122">Return value</span></span>

<span data-ttu-id="bef79-123">Retorna um valor INT que representa o intervalo, em meses, estendido pelos dois limites retornados em *lParam*.</span><span class="sxs-lookup"><span data-stu-id="bef79-123">Returns an INT value that represents the range, in months, spanned by the two limits returned at *lParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="bef79-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bef79-124">Requirements</span></span>



| <span data-ttu-id="bef79-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bef79-125">Requirement</span></span> | <span data-ttu-id="bef79-126">Valor</span><span class="sxs-lookup"><span data-stu-id="bef79-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bef79-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bef79-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bef79-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bef79-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bef79-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bef79-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bef79-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bef79-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bef79-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bef79-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bef79-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bef79-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bef79-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="bef79-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bef79-134">Vezes no controle de calendário mensal</span><span class="sxs-lookup"><span data-stu-id="bef79-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

