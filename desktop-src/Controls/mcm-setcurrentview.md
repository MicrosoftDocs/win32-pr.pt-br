---
title: Mensagem de MCM_SETCURRENTVIEW (commctrl. h)
description: Define a exibição atual do calendário. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetCurrentView.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- Controles de MCM_SETCURRENTVIEW de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d383c984932c19805f452cb39841c2edf36809b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919085"
---
# <a name="mcm_setcurrentview-message"></a><span data-ttu-id="3ce03-105">\_Mensagem MCM SETCURRENTVIEW</span><span class="sxs-lookup"><span data-stu-id="3ce03-105">MCM\_SETCURRENTVIEW message</span></span>

<span data-ttu-id="3ce03-106">Define a exibição atual do calendário.</span><span class="sxs-lookup"><span data-stu-id="3ce03-106">Sets the current view of the calendar.</span></span> <span data-ttu-id="3ce03-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="3ce03-107">You can send this message explicitly or by using the [**MonthCal\_SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ce03-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ce03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce03-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ce03-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ce03-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3ce03-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3ce03-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ce03-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ce03-112">Nova exibição.</span><span class="sxs-lookup"><span data-stu-id="3ce03-112">New view.</span></span> <span data-ttu-id="3ce03-113">Uma das constantes a seguir.</span><span class="sxs-lookup"><span data-stu-id="3ce03-113">One of the following constants.</span></span>



| <span data-ttu-id="3ce03-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3ce03-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="3ce03-115">Significado</span><span class="sxs-lookup"><span data-stu-id="3ce03-115">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <span data-ttu-id="3ce03-116"><dt>**MCMV \_ mês**</dt></span><span class="sxs-lookup"><span data-stu-id="3ce03-116"><dt>**MCMV\_MONTH**</dt></span></span> </dl>       | <span data-ttu-id="3ce03-117">Exibição mensal.</span><span class="sxs-lookup"><span data-stu-id="3ce03-117">Monthly view.</span></span><br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <span data-ttu-id="3ce03-118"><dt>**MCMV \_ ano**</dt></span><span class="sxs-lookup"><span data-stu-id="3ce03-118"><dt>**MCMV\_YEAR**</dt></span></span> </dl>          | <span data-ttu-id="3ce03-119">Exibição anual.</span><span class="sxs-lookup"><span data-stu-id="3ce03-119">Annual view.</span></span><br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <span data-ttu-id="3ce03-120"><dt>**década de MCMV \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3ce03-120"><dt>**MCMV\_DECADE**</dt></span></span> </dl>    | <span data-ttu-id="3ce03-121">Exibição da década.</span><span class="sxs-lookup"><span data-stu-id="3ce03-121">Decade view.</span></span><br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <span data-ttu-id="3ce03-122"><dt>**\_século MCMV**</dt></span><span class="sxs-lookup"><span data-stu-id="3ce03-122"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="3ce03-123">Exibição do século.</span><span class="sxs-lookup"><span data-stu-id="3ce03-123">Century view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ce03-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ce03-124">Return value</span></span>

<span data-ttu-id="3ce03-125">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="3ce03-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ce03-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ce03-126">Requirements</span></span>



| <span data-ttu-id="3ce03-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ce03-127">Requirement</span></span> | <span data-ttu-id="3ce03-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3ce03-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce03-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ce03-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce03-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ce03-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ce03-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ce03-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce03-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ce03-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ce03-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ce03-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ce03-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ce03-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





