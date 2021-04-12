---
title: Mensagem de MCM_GETCURRENTVIEW (commctrl. h)
description: Obtém a exibição atual do calendário. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetCurrentView.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- Controles de MCM_GETCURRENTVIEW de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebbd6a2b33043294b64b8b65308520b52dbe449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455738"
---
# <a name="mcm_getcurrentview-message"></a><span data-ttu-id="5129e-105">\_Mensagem MCM GETCURRENTVIEW</span><span class="sxs-lookup"><span data-stu-id="5129e-105">MCM\_GETCURRENTVIEW message</span></span>

<span data-ttu-id="5129e-106">Obtém a exibição atual do calendário.</span><span class="sxs-lookup"><span data-stu-id="5129e-106">Gets the current view of the calendar.</span></span> <span data-ttu-id="5129e-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="5129e-107">You can send this message explicitly or by using the [**MonthCal\_GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5129e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5129e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5129e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5129e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5129e-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5129e-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5129e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5129e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5129e-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5129e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5129e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5129e-113">Return value</span></span>

<span data-ttu-id="5129e-114">Exibição atual.</span><span class="sxs-lookup"><span data-stu-id="5129e-114">Current view.</span></span> <span data-ttu-id="5129e-115">Um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5129e-115">One of the following values.</span></span>



| <span data-ttu-id="5129e-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5129e-116">Return code</span></span>                                                                                  | <span data-ttu-id="5129e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="5129e-117">Description</span></span>              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="5129e-118"><dt>**MCMV \_ mês**</dt></span><span class="sxs-lookup"><span data-stu-id="5129e-118"><dt>**MCMV\_MONTH**</dt></span></span> </dl>   | <span data-ttu-id="5129e-119">Exibição mensal.</span><span class="sxs-lookup"><span data-stu-id="5129e-119">Monthly view.</span></span><br/> |
| <dl> <span data-ttu-id="5129e-120"><dt>**MCMV \_ ano**</dt></span><span class="sxs-lookup"><span data-stu-id="5129e-120"><dt>**MCMV\_YEAR**</dt></span></span> </dl>    | <span data-ttu-id="5129e-121">Exibição anual.</span><span class="sxs-lookup"><span data-stu-id="5129e-121">Annual view.</span></span><br/>  |
| <dl> <span data-ttu-id="5129e-122"><dt>**década de MCMV \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5129e-122"><dt>**MCMV\_DECADE**</dt></span></span> </dl>  | <span data-ttu-id="5129e-123">Exibição da década.</span><span class="sxs-lookup"><span data-stu-id="5129e-123">Decade view.</span></span><br/>  |
| <dl> <span data-ttu-id="5129e-124"><dt>**\_século MCMV**</dt></span><span class="sxs-lookup"><span data-stu-id="5129e-124"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="5129e-125">Exibição do século.</span><span class="sxs-lookup"><span data-stu-id="5129e-125">Century view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5129e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5129e-126">Requirements</span></span>



| <span data-ttu-id="5129e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5129e-127">Requirement</span></span> | <span data-ttu-id="5129e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5129e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5129e-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5129e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5129e-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5129e-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5129e-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5129e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5129e-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5129e-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5129e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5129e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5129e-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5129e-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





