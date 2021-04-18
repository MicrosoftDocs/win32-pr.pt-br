---
title: Mensagem de TTM_GETDELAYTIME (commctrl. h)
description: Recupera as durações inicial, pop-up e Reexibir atualmente definidas para um controle ToolTip.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- Controles de TTM_GETDELAYTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_GETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff8c75f078465646333cae1f519049733a0c9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748851"
---
# <a name="ttm_getdelaytime-message"></a><span data-ttu-id="12643-104">\_Mensagem GETdelaytime TTM</span><span class="sxs-lookup"><span data-stu-id="12643-104">TTM\_GETDELAYTIME message</span></span>

<span data-ttu-id="12643-105">Recupera as durações inicial, pop-up e Reexibir atualmente definidas para um controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="12643-105">Retrieves the initial, pop-up, and reshow durations currently set for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="12643-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12643-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12643-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12643-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12643-108">Sinalizador que especifica qual valor de duração será recuperado.</span><span class="sxs-lookup"><span data-stu-id="12643-108">Flag that specifies which duration value will be retrieved.</span></span> <span data-ttu-id="12643-109">Esse parâmetro pode ter um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="12643-109">This parameter can have one of the following values:</span></span>



| <span data-ttu-id="12643-110">Valor</span><span class="sxs-lookup"><span data-stu-id="12643-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="12643-111">Significado</span><span class="sxs-lookup"><span data-stu-id="12643-111">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="12643-112"><dt>**TTDT \_ AUTOPOP**</dt></span><span class="sxs-lookup"><span data-stu-id="12643-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl> | <span data-ttu-id="12643-113">Recupere a quantidade de tempo que a janela de dica de ferramenta permanece visível se o ponteiro é estático dentro do retângulo delimitador de uma ferramenta.</span><span class="sxs-lookup"><span data-stu-id="12643-113">Retrieve the amount of time the tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span><br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="12643-114"><dt>**TTDT \_ inicial**</dt></span><span class="sxs-lookup"><span data-stu-id="12643-114"><dt>**TTDT\_INITIAL**</dt></span></span> </dl> | <span data-ttu-id="12643-115">Recupere a quantidade de tempo que o ponteiro deve permanecer fixo dentro do retângulo delimitador de uma ferramenta antes que a janela de dica de ferramentas seja exibida.</span><span class="sxs-lookup"><span data-stu-id="12643-115">Retrieve the amount of time the pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span><br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="12643-116"><dt>**remostrar TTDT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12643-116"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>    | <span data-ttu-id="12643-117">Recupere a quantidade de tempo que leva para que janelas de dica de ferramenta subsequentes apareçam à medida que o ponteiro se move de uma das ferramentas para outra.</span><span class="sxs-lookup"><span data-stu-id="12643-117">Retrieve the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="12643-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12643-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="12643-119">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="12643-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12643-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12643-120">Return value</span></span>

<span data-ttu-id="12643-121">Retorna e valor INT com a duração especificada em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="12643-121">Returns and INT value with the specified duration in milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="12643-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12643-122">Requirements</span></span>



| <span data-ttu-id="12643-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="12643-123">Requirement</span></span> | <span data-ttu-id="12643-124">Valor</span><span class="sxs-lookup"><span data-stu-id="12643-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12643-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12643-125">Minimum supported client</span></span><br/> | <span data-ttu-id="12643-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12643-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12643-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12643-127">Minimum supported server</span></span><br/> | <span data-ttu-id="12643-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="12643-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12643-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12643-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="12643-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="12643-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12643-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="12643-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12643-132">**TTM \_ SETatrasartime**</span><span class="sxs-lookup"><span data-stu-id="12643-132">**TTM\_SETDELAYTIME**</span></span>](ttm-setdelaytime.md)
</dt> </dl>

 

 





