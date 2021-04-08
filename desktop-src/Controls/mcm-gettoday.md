---
title: Mensagem de MCM_GETTODAY (commctrl. h)
description: Recupera as informações de data da data especificada como \ 0034; hoje \ 0034; para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ gethoje.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- Controles de MCM_GETTODAY de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21538af3c573b3d972b7f16bfe024e0d36211644
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918520"
---
# <a name="mcm_gettoday-message"></a><span data-ttu-id="77858-105">Mensagem do MCM \_ GEThoje</span><span class="sxs-lookup"><span data-stu-id="77858-105">MCM\_GETTODAY message</span></span>

<span data-ttu-id="77858-106">Recupera as informações de data da data especificada como "hoje" para um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="77858-106">Retrieves the date information for the date specified as "today" for a month calendar control.</span></span> <span data-ttu-id="77858-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ gethoje**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) .</span><span class="sxs-lookup"><span data-stu-id="77858-107">You can send this message explicitly or by using the [**MonthCal\_GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="77858-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77858-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77858-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77858-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="77858-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="77858-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="77858-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77858-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77858-112">Ponteiro para uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que receberá as informações de data.</span><span class="sxs-lookup"><span data-stu-id="77858-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the date information.</span></span> <span data-ttu-id="77858-113">Esse parâmetro deve ser um endereço válido e não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="77858-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77858-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77858-114">Return value</span></span>

<span data-ttu-id="77858-115">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="77858-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="77858-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77858-116">Requirements</span></span>



| <span data-ttu-id="77858-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="77858-117">Requirement</span></span> | <span data-ttu-id="77858-118">Valor</span><span class="sxs-lookup"><span data-stu-id="77858-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77858-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77858-119">Minimum supported client</span></span><br/> | <span data-ttu-id="77858-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77858-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77858-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77858-121">Minimum supported server</span></span><br/> | <span data-ttu-id="77858-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77858-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77858-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77858-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="77858-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77858-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77858-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="77858-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77858-126">Vezes no controle de calendário mensal</span><span class="sxs-lookup"><span data-stu-id="77858-126">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

