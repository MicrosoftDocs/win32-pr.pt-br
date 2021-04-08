---
title: Mensagem de DTM_CLOSEMONTHCAL (commctrl. h)
description: Fecha um controle do seletor de data e hora (DTP). Envie essa mensagem explicitamente ou usando a macro DateTime \_ CloseMonthCal.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- Controles de DTM_CLOSEMONTHCAL de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd79f33576490196bf29fd51316f8ce3daf4ad4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008946"
---
# <a name="dtm_closemonthcal-message"></a><span data-ttu-id="fdef9-105">\_Mensagem DTM CLOSEMONTHCAL</span><span class="sxs-lookup"><span data-stu-id="fdef9-105">DTM\_CLOSEMONTHCAL message</span></span>

<span data-ttu-id="fdef9-106">Fecha um controle do seletor de data e hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="fdef9-106">Closes a date and time picker (DTP) control.</span></span> <span data-ttu-id="fdef9-107">Envie essa mensagem explicitamente ou usando a macro [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .</span><span class="sxs-lookup"><span data-stu-id="fdef9-107">Send this message explicitly or by using the [**DateTime\_CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fdef9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdef9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdef9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fdef9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdef9-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fdef9-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fdef9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fdef9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fdef9-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fdef9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdef9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fdef9-113">Return value</span></span>

<span data-ttu-id="fdef9-114">Retorna zero.</span><span class="sxs-lookup"><span data-stu-id="fdef9-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdef9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdef9-115">Remarks</span></span>

<span data-ttu-id="fdef9-116">Destrói o controle e envia uma notificação [DTN \_ closeup](dtn-closeup.md) de que o controle está fechando, ao contrário do controle, é aberto (descartando como na notificação [ \_ suspensa DTN](dtn-dropdown.md) ) para o pai do controle.</span><span class="sxs-lookup"><span data-stu-id="fdef9-116">Destroys the control and sends a [DTN\_CLOSEUP](dtn-closeup.md) notification that the control is closing as opposed to the control is opening (dropping-down as in the [DTN\_DROPDOWN](dtn-dropdown.md) notification) to the control's parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdef9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdef9-117">Requirements</span></span>



| <span data-ttu-id="fdef9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdef9-118">Requirement</span></span> | <span data-ttu-id="fdef9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fdef9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdef9-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdef9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fdef9-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fdef9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fdef9-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdef9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fdef9-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fdef9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fdef9-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fdef9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdef9-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdef9-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdef9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdef9-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="fdef9-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="fdef9-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fdef9-128">\_lista suspensa DTN</span><span class="sxs-lookup"><span data-stu-id="fdef9-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="fdef9-129">DTN \_ closeup</span><span class="sxs-lookup"><span data-stu-id="fdef9-129">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> </dl>

 

 





