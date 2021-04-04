---
title: Mensagem de MCM_SETSELRANGE (commctrl. h)
description: Define a seleção de um controle de calendário de mês para um determinado intervalo de datas. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetSelRange.
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- Controles de MCM_SETSELRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad28966ab67a5e7c0d27dd8fc9c367ec30e4cd7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008929"
---
# <a name="mcm_setselrange-message"></a><span data-ttu-id="d04f5-105">\_Mensagem MCM SETSELRANGE</span><span class="sxs-lookup"><span data-stu-id="d04f5-105">MCM\_SETSELRANGE message</span></span>

<span data-ttu-id="d04f5-106">Define a seleção de um controle de calendário de mês para um determinado intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="d04f5-106">Sets the selection for a month calendar control to a given date range.</span></span> <span data-ttu-id="d04f5-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) .</span><span class="sxs-lookup"><span data-stu-id="d04f5-107">You can send this message explicitly or by using the [**MonthCal\_SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d04f5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d04f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d04f5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d04f5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d04f5-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d04f5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d04f5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d04f5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d04f5-112">Ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contêm informações de data que representam os limites de seleção.</span><span class="sxs-lookup"><span data-stu-id="d04f5-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain date information representing the selection limits.</span></span> <span data-ttu-id="d04f5-113">A primeira data selecionada deve ser especificada em *lpSysTimeArray* \[ 0 \] , e a última data selecionada deve ser especificada em *lpSysTimeArray* \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="d04f5-113">The first selected date must be specified in *lpSysTimeArray*\[0\], and the last selected date must be specified in *lpSysTimeArray*\[1\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d04f5-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d04f5-114">Return value</span></span>

<span data-ttu-id="d04f5-115">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="d04f5-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="d04f5-116">Esta mensagem falhará se for aplicada a um controle de calendário de mês que não usa o estilo de [**\_ multiseleção MCS**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d04f5-116">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d04f5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d04f5-117">Requirements</span></span>



| <span data-ttu-id="d04f5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d04f5-118">Requirement</span></span> | <span data-ttu-id="d04f5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d04f5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d04f5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d04f5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d04f5-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d04f5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d04f5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d04f5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d04f5-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d04f5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d04f5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d04f5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d04f5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d04f5-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d04f5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d04f5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d04f5-127">Vezes no controle de calendário mensal</span><span class="sxs-lookup"><span data-stu-id="d04f5-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

