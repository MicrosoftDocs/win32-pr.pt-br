---
title: Mensagem de MCM_GETCURSEL (commctrl. h)
description: Recupera a data atualmente selecionada. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Getcurseal calendário mensal.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- Controles de MCM_GETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dece95c65e900119c7043c0d5eda22bf473e6c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455426"
---
# <a name="mcm_getcursel-message"></a><span data-ttu-id="0bb67-105">\_Mensagem GETcurseal MCM</span><span class="sxs-lookup"><span data-stu-id="0bb67-105">MCM\_GETCURSEL message</span></span>

<span data-ttu-id="0bb67-106">Recupera a data atualmente selecionada.</span><span class="sxs-lookup"><span data-stu-id="0bb67-106">Retrieves the currently selected date.</span></span> <span data-ttu-id="0bb67-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ getcurseal calendário mensal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="0bb67-107">You can send this message explicitly or by using the [**MonthCal\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0bb67-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bb67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bb67-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0bb67-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0bb67-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0bb67-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0bb67-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0bb67-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bb67-112">Ponteiro para uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que receberá as informações de data atualmente selecionadas.</span><span class="sxs-lookup"><span data-stu-id="0bb67-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the currently selected date information.</span></span> <span data-ttu-id="0bb67-113">Esse parâmetro deve ser um endereço válido e não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0bb67-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bb67-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0bb67-114">Return value</span></span>

<span data-ttu-id="0bb67-115">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="0bb67-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="0bb67-116">Esta mensagem sempre falhará quando aplicada aos controles de calendário de mês definidos como o estilo de [**\_ multiseleção MCS**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0bb67-116">This message will always fail when applied to month calendar controls set to the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb67-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bb67-117">Requirements</span></span>



| <span data-ttu-id="0bb67-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bb67-118">Requirement</span></span> | <span data-ttu-id="0bb67-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0bb67-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb67-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bb67-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0bb67-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0bb67-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0bb67-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bb67-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0bb67-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0bb67-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0bb67-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0bb67-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bb67-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bb67-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bb67-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bb67-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bb67-127">Vezes no controle de calendário mensal</span><span class="sxs-lookup"><span data-stu-id="0bb67-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

