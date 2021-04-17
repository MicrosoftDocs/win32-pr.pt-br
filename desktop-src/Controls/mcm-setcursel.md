---
title: Mensagem de MCM_SETCURSEL (commctrl. h)
description: Define a data atualmente selecionada para um controle de calendário mensal. Se a data especificada não estiver na exibição, o controle atualizará a exibição para colocá-la no modo de exibição. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setcurseal calendário mensal.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- Controles de MCM_SETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cceff48fbc4ffdb7446277d506c369e1bd89c92b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755657"
---
# <a name="mcm_setcursel-message"></a><span data-ttu-id="9dde0-106">\_Mensagem MCM SETcurseal</span><span class="sxs-lookup"><span data-stu-id="9dde0-106">MCM\_SETCURSEL message</span></span>

<span data-ttu-id="9dde0-107">Define a data atualmente selecionada para um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="9dde0-107">Sets the currently selected date for a month calendar control.</span></span> <span data-ttu-id="9dde0-108">Se a data especificada não estiver na exibição, o controle atualizará a exibição para colocá-la no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="9dde0-108">If the specified date is not in view, the control updates the display to bring it into view.</span></span> <span data-ttu-id="9dde0-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setcurseal calendário mensal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="9dde0-109">You can send this message explicitly or by using the [**MonthCal\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9dde0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9dde0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dde0-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9dde0-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9dde0-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9dde0-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9dde0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9dde0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9dde0-114">Ponteiro para uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contém a data a ser definida como a seleção atual.</span><span class="sxs-lookup"><span data-stu-id="9dde0-114">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the current selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dde0-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9dde0-115">Return value</span></span>

<span data-ttu-id="9dde0-116">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="9dde0-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="9dde0-117">Essa mensagem falhará se for aplicada a um controle de calendário de mês que usa o estilo de [**\_ multiseleção MCS**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9dde0-117">This message will fail if applied to a month calendar control that uses the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dde0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dde0-118">Requirements</span></span>



| <span data-ttu-id="9dde0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dde0-119">Requirement</span></span> | <span data-ttu-id="9dde0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9dde0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9dde0-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9dde0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9dde0-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9dde0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9dde0-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9dde0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9dde0-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9dde0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9dde0-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9dde0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dde0-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dde0-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dde0-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9dde0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dde0-128">Vezes no controle de calendário mensal</span><span class="sxs-lookup"><span data-stu-id="9dde0-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

