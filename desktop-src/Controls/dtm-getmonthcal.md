---
title: Mensagem de DTM_GETMONTHCAL (commctrl. h)
description: Obtém o identificador de um controle de calendário do mês filho do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a \_ macro DateTime GetMonthCal.
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- Controles de DTM_GETMONTHCAL de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_GETMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99609ed3a437990889066da9a3424ef147c3d6b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918812"
---
# <a name="dtm_getmonthcal-message"></a><span data-ttu-id="bb750-105">\_Mensagem DTM GETMONTHCAL</span><span class="sxs-lookup"><span data-stu-id="bb750-105">DTM\_GETMONTHCAL message</span></span>

<span data-ttu-id="bb750-106">Obtém o identificador de um controle de calendário do mês filho do seletor de data e hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="bb750-106">Gets the handle to a date and time picker's (DTP) child month calendar control.</span></span> <span data-ttu-id="bb750-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) .</span><span class="sxs-lookup"><span data-stu-id="bb750-107">You can send this message explicitly or use the [**DateTime\_GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb750-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb750-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb750-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb750-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bb750-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bb750-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bb750-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb750-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bb750-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bb750-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb750-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb750-113">Return value</span></span>

<span data-ttu-id="bb750-114">Retorna o identificador para o controle de calendário do mês filho de um controle DTP, se for bem-sucedido, caso contrário, será **nulo** .</span><span class="sxs-lookup"><span data-stu-id="bb750-114">Returns the handle to a DTP control's child month calendar control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb750-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb750-115">Remarks</span></span>

<span data-ttu-id="bb750-116">Os controles DTP criam um controle de calendário de mês filho quando o usuário clica na seta suspensa[( \_ notificação suspensa DTN](dtn-dropdown.md) ).</span><span class="sxs-lookup"><span data-stu-id="bb750-116">DTP controls create a child month calendar control when the user clicks the drop-down arrow ([DTN\_DROPDOWN](dtn-dropdown.md) notification).</span></span> <span data-ttu-id="bb750-117">Quando o calendário mensal não é mais necessário, ele é destruído (uma notificação [DTN \_ closeup](dtn-closeup.md) é enviada na destruição).</span><span class="sxs-lookup"><span data-stu-id="bb750-117">When the month calendar is no longer needed, it is destroyed (a [DTN\_CLOSEUP](dtn-closeup.md) notification is sent on destruction).</span></span> <span data-ttu-id="bb750-118">Portanto, seu aplicativo não deve depender de um identificador estático para o calendário de mês filho do controle DTP.</span><span class="sxs-lookup"><span data-stu-id="bb750-118">So your application must not rely on a static handle to the DTP control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb750-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb750-119">Requirements</span></span>



| <span data-ttu-id="bb750-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb750-120">Requirement</span></span> | <span data-ttu-id="bb750-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bb750-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb750-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb750-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bb750-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb750-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb750-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb750-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bb750-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb750-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb750-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb750-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb750-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb750-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb750-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb750-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb750-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="bb750-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bb750-130">DTN \_ closeup</span><span class="sxs-lookup"><span data-stu-id="bb750-130">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="bb750-131">\_lista suspensa DTN</span><span class="sxs-lookup"><span data-stu-id="bb750-131">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> </dl>

 

 





