---
title: Mensagem de MCM_SETRANGE (commctrl. h)
description: Define as datas mínimas e máximas permitidas para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetRange calendário mensal.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- Controles de MCM_SETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380e599da8cd4a054c02135bc64f57f29d2c81d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762751"
---
# <a name="mcm_setrange-message"></a><span data-ttu-id="f0180-105">\_Mensagem SETRANGE MCM</span><span class="sxs-lookup"><span data-stu-id="f0180-105">MCM\_SETRANGE message</span></span>

<span data-ttu-id="f0180-106">Define as datas mínimas e máximas permitidas para um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="f0180-106">Sets the minimum and maximum allowable dates for a month calendar control.</span></span> <span data-ttu-id="f0180-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetRange calendário mensal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) .</span><span class="sxs-lookup"><span data-stu-id="f0180-107">You can send this message explicitly or by using the [**MonthCal\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0180-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0180-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0180-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0180-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0180-110">Valores de sinalizador que especificam quais limites de data estão sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="f0180-110">Flag values that specify which date limits are being set.</span></span> <span data-ttu-id="f0180-111">Esse valor deve ser um ou ambos os seguintes:</span><span class="sxs-lookup"><span data-stu-id="f0180-111">This value must be one or both of the following:</span></span>



| <span data-ttu-id="f0180-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f0180-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="f0180-113">Significado</span><span class="sxs-lookup"><span data-stu-id="f0180-113">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="f0180-114"><dt>**GDTR \_ Max**</dt></span><span class="sxs-lookup"><span data-stu-id="f0180-114"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="f0180-115">A data máxima permitida está sendo definida.</span><span class="sxs-lookup"><span data-stu-id="f0180-115">The maximum allowable date is being set.</span></span> <span data-ttu-id="f0180-116">A estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) em *lpSysTimeArray* \[ 1 \] deve conter informações de data.</span><span class="sxs-lookup"><span data-stu-id="f0180-116">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[1\] must contain date information.</span></span> <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="f0180-117"><dt>**GDTR \_ mín.**</dt></span><span class="sxs-lookup"><span data-stu-id="f0180-117"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="f0180-118">A data mínima permitida está sendo definida.</span><span class="sxs-lookup"><span data-stu-id="f0180-118">The minimum allowable date is being set.</span></span> <span data-ttu-id="f0180-119">A estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) em *lpSysTimeArray* \[ 0 \] deve conter informações de data.</span><span class="sxs-lookup"><span data-stu-id="f0180-119">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[0\] must contain date information.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="f0180-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0180-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0180-121">Ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contêm os limites de data.</span><span class="sxs-lookup"><span data-stu-id="f0180-121">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain the date limits.</span></span> <span data-ttu-id="f0180-122">O limite máximo deve estar em *lpSysTimeArray* \[ 1 \] se GDTR \_ Max for especificado e *lpSysTimeArray* \[ 0 \] deve conter o limite mínimo se GDTR \_ min for especificado.</span><span class="sxs-lookup"><span data-stu-id="f0180-122">The maximum limit must be in *lpSysTimeArray*\[1\] if GDTR\_MAX is specified, and *lpSysTimeArray*\[0\] must contain the minimum limit if GDTR\_MIN is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0180-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0180-123">Return value</span></span>

<span data-ttu-id="f0180-124">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="f0180-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0180-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0180-125">Requirements</span></span>



| <span data-ttu-id="f0180-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0180-126">Requirement</span></span> | <span data-ttu-id="f0180-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f0180-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0180-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0180-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f0180-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0180-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0180-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0180-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f0180-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f0180-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0180-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0180-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0180-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0180-133"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0180-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0180-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0180-135">Vezes no controle de calendário mensal</span><span class="sxs-lookup"><span data-stu-id="f0180-135">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

