---
title: Mensagem de DTM_SETRANGE (commctrl. h)
description: Define os tempos mínimos e máximos de sistema permitidos para um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetRange de DateTime.
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- Controles de DTM_SETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70578e7d468c6a0e54d1373af2d46e680afbbe5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644914"
---
# <a name="dtm_setrange-message"></a><span data-ttu-id="70661-105">\_Mensagem SETRANGE DTM</span><span class="sxs-lookup"><span data-stu-id="70661-105">DTM\_SETRANGE message</span></span>

<span data-ttu-id="70661-106">Define os tempos mínimos e máximos de sistema permitidos para um controle do seletor de data e hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="70661-106">Sets the minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="70661-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetRange de DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) .</span><span class="sxs-lookup"><span data-stu-id="70661-107">You can send this message explicitly or use the [**DateTime\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="70661-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70661-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70661-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70661-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70661-110">Um valor que especifica quais valores de intervalo são válidos.</span><span class="sxs-lookup"><span data-stu-id="70661-110">A value specifying which range values are valid.</span></span> <span data-ttu-id="70661-111">Esse parâmetro pode ser uma combinação dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="70661-111">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="70661-112">Valor</span><span class="sxs-lookup"><span data-stu-id="70661-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="70661-113">Significado</span><span class="sxs-lookup"><span data-stu-id="70661-113">Meaning</span></span>                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="70661-114"><dt>**GDTR \_ mín.**</dt></span><span class="sxs-lookup"><span data-stu-id="70661-114"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="70661-115">O primeiro elemento na matriz de estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) é válido e será usado para definir a hora mínima permitida do sistema.</span><span class="sxs-lookup"><span data-stu-id="70661-115">The first element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the minimum allowable system time.</span></span><br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="70661-116"><dt>**GDTR \_ Max**</dt></span><span class="sxs-lookup"><span data-stu-id="70661-116"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="70661-117">O segundo elemento na matriz de estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) é válido e será usado para definir a hora máxima permitida do sistema.</span><span class="sxs-lookup"><span data-stu-id="70661-117">The second element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the maximum allowable system time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="70661-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70661-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70661-119">Um ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="70661-119">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span> <span data-ttu-id="70661-120">O primeiro elemento da matriz **SYSTEMTIME** contém o tempo mínimo permitido.</span><span class="sxs-lookup"><span data-stu-id="70661-120">The first element of the **SYSTEMTIME** array contains the minimum allowable time.</span></span> <span data-ttu-id="70661-121">O segundo elemento da matriz **SYSTEMTIME** contém o tempo máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="70661-121">The second element of the **SYSTEMTIME** array contains the maximum allowable time.</span></span> <span data-ttu-id="70661-122">Não é necessário preencher um elemento de matriz que não esteja especificado no parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="70661-122">It is not necessary to fill an array element that is not specified in the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70661-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70661-123">Return value</span></span>

<span data-ttu-id="70661-124">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="70661-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="70661-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="70661-125">Remarks</span></span>

<span data-ttu-id="70661-126">O seletor de data e hora exibe apenas datas/horários que se enquadram no intervalo especificado, impedindo que o usuário selecione uma data e hora que esteja fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="70661-126">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="70661-127">Se a mensagem [**DTM \_ SetSystemTime**](dtm-setsystemtime.md) especificar uma data e hora que esteja fora do intervalo, ela falhará.</span><span class="sxs-lookup"><span data-stu-id="70661-127">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="70661-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70661-128">Requirements</span></span>



| <span data-ttu-id="70661-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="70661-129">Requirement</span></span> | <span data-ttu-id="70661-130">Valor</span><span class="sxs-lookup"><span data-stu-id="70661-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70661-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70661-131">Minimum supported client</span></span><br/> | <span data-ttu-id="70661-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70661-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70661-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70661-133">Minimum supported server</span></span><br/> | <span data-ttu-id="70661-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="70661-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70661-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70661-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="70661-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="70661-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

