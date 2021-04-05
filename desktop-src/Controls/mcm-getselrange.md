---
title: Mensagem de MCM_GETSELRANGE (commctrl. h)
description: Recupera informações de data que representam os limites superior e inferior do intervalo de datas selecionado no momento pelo usuário. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetSelRange.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- Controles de MCM_GETSELRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0d2f922b013a3eab525228bda4f5b99f33e70d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918272"
---
# <a name="mcm_getselrange-message"></a><span data-ttu-id="c51a3-105">\_Mensagem MCM GETSELRANGE</span><span class="sxs-lookup"><span data-stu-id="c51a3-105">MCM\_GETSELRANGE message</span></span>

<span data-ttu-id="c51a3-106">Recupera informações de data que representam os limites superior e inferior do intervalo de datas selecionado no momento pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c51a3-106">Retrieves date information that represents the upper and lower limits of the date range currently selected by the user.</span></span> <span data-ttu-id="c51a3-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) .</span><span class="sxs-lookup"><span data-stu-id="c51a3-107">You can send this message explicitly or by using the [**MonthCal\_GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c51a3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c51a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c51a3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c51a3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c51a3-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c51a3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c51a3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c51a3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c51a3-112">Ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que receberá os limites inferior e superior da seleção do usuário.</span><span class="sxs-lookup"><span data-stu-id="c51a3-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the user's selection.</span></span> <span data-ttu-id="c51a3-113">Os limites inferior e superior são colocados em *lprgSysTimeArray* \[ 0 \] e *lprgSysTimeArray* \[ 1 \] , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c51a3-113">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="c51a3-114">Esse parâmetro deve ser um endereço válido e não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c51a3-114">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c51a3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c51a3-115">Return value</span></span>

<span data-ttu-id="c51a3-116">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="c51a3-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="c51a3-117">**MCM \_ GETSELRANGE** falhará se for aplicado a um controle de calendário de mês que não usa o estilo de [**\_ multiseleção MCS**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="c51a3-117">**MCM\_GETSELRANGE** will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="c51a3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c51a3-118">Requirements</span></span>



| <span data-ttu-id="c51a3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c51a3-119">Requirement</span></span> | <span data-ttu-id="c51a3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c51a3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c51a3-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c51a3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c51a3-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c51a3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c51a3-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c51a3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c51a3-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c51a3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c51a3-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c51a3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c51a3-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c51a3-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c51a3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c51a3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c51a3-128">Vezes no controle de calendário mensal</span><span class="sxs-lookup"><span data-stu-id="c51a3-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

