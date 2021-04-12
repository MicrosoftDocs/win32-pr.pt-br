---
title: Mensagem de PBM_SETSTATE (commctrl. h)
description: Define o estado da barra de progresso.
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- Controles de PBM_SETSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c91e94bcc909957264eff776e56d3580b2c36ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455543"
---
# <a name="pbm_setstate-message"></a><span data-ttu-id="7a089-104">Mensagem do estado do PBM \_</span><span class="sxs-lookup"><span data-stu-id="7a089-104">PBM\_SETSTATE message</span></span>

<span data-ttu-id="7a089-105">Define o estado da barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="7a089-105">Sets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a089-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a089-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a089-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a089-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a089-108">Estado da barra de progresso que está sendo definida.</span><span class="sxs-lookup"><span data-stu-id="7a089-108">State of the progress bar that is being set.</span></span> <span data-ttu-id="7a089-109">Um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7a089-109">One of the following values.</span></span>



| <span data-ttu-id="7a089-110">Valor</span><span class="sxs-lookup"><span data-stu-id="7a089-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="7a089-111">Significado</span><span class="sxs-lookup"><span data-stu-id="7a089-111">Meaning</span></span>                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="7a089-112"><dt>**PBST \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="7a089-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="7a089-113">Em andamento.</span><span class="sxs-lookup"><span data-stu-id="7a089-113">In progress.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="7a089-114"><dt>**erro de PBST \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7a089-114"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="7a089-115">Erro.</span><span class="sxs-lookup"><span data-stu-id="7a089-115">Error.</span></span><br/>       |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="7a089-116"><dt>**PBST em \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="7a089-116"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="7a089-117">Em pausa.</span><span class="sxs-lookup"><span data-stu-id="7a089-117">Paused.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="7a089-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a089-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7a089-119">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7a089-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a089-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a089-120">Return value</span></span>

<span data-ttu-id="7a089-121">Retorna o estado anterior.</span><span class="sxs-lookup"><span data-stu-id="7a089-121">Returns the previous state.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a089-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a089-122">Requirements</span></span>



| <span data-ttu-id="7a089-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a089-123">Requirement</span></span> | <span data-ttu-id="7a089-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7a089-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a089-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a089-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7a089-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a089-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a089-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a089-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7a089-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a089-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a089-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a089-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a089-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a089-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





