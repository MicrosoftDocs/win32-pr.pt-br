---
title: Mensagem de MCM_GETRANGE (commctrl. h)
description: Recupera as datas mínimas e máximas permitidas definidas para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetRange calendário mensal.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- Controles de MCM_GETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c757c046b88479072eb0771ecbf3f7fb79cdb31b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824765"
---
# <a name="mcm_getrange-message"></a><span data-ttu-id="b5324-105">MCM \_ mensagem GETrange</span><span class="sxs-lookup"><span data-stu-id="b5324-105">MCM\_GETRANGE message</span></span>

<span data-ttu-id="b5324-106">Recupera as datas mínimas e máximas permitidas definidas para um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="b5324-106">Retrieves the minimum and maximum allowable dates set for a month calendar control.</span></span> <span data-ttu-id="b5324-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetRange calendário mensal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) .</span><span class="sxs-lookup"><span data-stu-id="b5324-107">You can send this message explicitly or by using the [**MonthCal\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5324-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5324-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5324-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5324-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b5324-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b5324-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b5324-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5324-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5324-112">Ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que receberá as informações de limite de data.</span><span class="sxs-lookup"><span data-stu-id="b5324-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the date limit information.</span></span> <span data-ttu-id="b5324-113">O limite mínimo é definido em *lprgSysTimeArray* \[ 0 \] e *lprgSysTimeArray* \[ 1 \] recebe o limite máximo.</span><span class="sxs-lookup"><span data-stu-id="b5324-113">The minimum limit is set in *lprgSysTimeArray*\[0\], and *lprgSysTimeArray*\[1\] receives the maximum limit.</span></span> <span data-ttu-id="b5324-114">Se qualquer elemento for definido como todos os zeros, nenhum limite correspondente será definido para o controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="b5324-114">If either element is set to all zeros, then no corresponding limit is set for the month calendar control.</span></span> <span data-ttu-id="b5324-115">Esse parâmetro deve ser um endereço válido e não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b5324-115">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5324-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5324-116">Return value</span></span>

<span data-ttu-id="b5324-117">Retorna um **DWORD** que pode ser zero (nenhum limite é definido) ou uma combinação dos seguintes valores que especificam informações de limite:</span><span class="sxs-lookup"><span data-stu-id="b5324-117">Returns a **DWORD** that can be zero (no limits are set) or a combination of the following values that specify limit information:</span></span>



| <span data-ttu-id="b5324-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b5324-118">Return code</span></span>                                                                              | <span data-ttu-id="b5324-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5324-119">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5324-120"><dt>**GDTR \_ Max**</dt></span><span class="sxs-lookup"><span data-stu-id="b5324-120"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="b5324-121">Um limite máximo é definido para o controle; *lprgSysTimeArray* \[ 0 \] é válido e contém as informações de data aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="b5324-121">A maximum limit is set for the control; *lprgSysTimeArray*\[0\] is valid and contains the applicable date information.</span></span> <br/> |
| <dl> <span data-ttu-id="b5324-122"><dt>**GDTR \_ mín.**</dt></span><span class="sxs-lookup"><span data-stu-id="b5324-122"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="b5324-123">Um limite mínimo é definido para o controle; *lprgSysTimeArray* \[ 1 \] é válido e contém as informações de data aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="b5324-123">A minimum limit is set for the control; *lprgSysTimeArray*\[1\] is valid and contains the applicable date information.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="b5324-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5324-124">Requirements</span></span>



| <span data-ttu-id="b5324-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5324-125">Requirement</span></span> | <span data-ttu-id="b5324-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b5324-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5324-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5324-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b5324-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5324-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5324-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5324-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b5324-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b5324-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5324-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5324-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5324-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5324-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5324-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5324-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5324-134">Vezes no controle de calendário mensal</span><span class="sxs-lookup"><span data-stu-id="b5324-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

