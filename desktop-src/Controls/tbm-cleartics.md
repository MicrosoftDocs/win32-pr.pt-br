---
title: Mensagem de TBM_CLEARTICS (commctrl. h)
description: Remove as marcas de escala atuais de um TrackBar. Essa mensagem não remove a primeira e a última marca de escala, que são criadas automaticamente pelo TrackBar.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- Controles de TBM_CLEARTICS de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1ecb4f9f931c976b2542a1f263fc069f1eca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454881"
---
# <a name="tbm_cleartics-message"></a><span data-ttu-id="991bc-105">\_Mensagem tbm CLEARTICS</span><span class="sxs-lookup"><span data-stu-id="991bc-105">TBM\_CLEARTICS message</span></span>

<span data-ttu-id="991bc-106">Remove as marcas de escala atuais de um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="991bc-106">Removes the current tick marks from a trackbar.</span></span> <span data-ttu-id="991bc-107">Essa mensagem não remove a primeira e a última marca de escala, que são criadas automaticamente pelo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="991bc-107">This message does not remove the first and last tick marks, which are created automatically by the trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="991bc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="991bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="991bc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="991bc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="991bc-110">Sinalizador de redesenho.</span><span class="sxs-lookup"><span data-stu-id="991bc-110">Redraw flag.</span></span> <span data-ttu-id="991bc-111">Se esse parâmetro for **true**, o TrackBar será redesenhado depois que as marcas de escala forem limpas.</span><span class="sxs-lookup"><span data-stu-id="991bc-111">If this parameter is **TRUE**, the trackbar is redrawn after the tick marks are cleared.</span></span> <span data-ttu-id="991bc-112">Se esse parâmetro for **false**, a mensagem limpará as marcas de escala, mas não redesenhará o TrackBar.</span><span class="sxs-lookup"><span data-stu-id="991bc-112">If this parameter is **FALSE**, the message clears the tick marks but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="991bc-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="991bc-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="991bc-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="991bc-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="991bc-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="991bc-115">Return value</span></span>

<span data-ttu-id="991bc-116">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="991bc-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="991bc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="991bc-117">Requirements</span></span>



| <span data-ttu-id="991bc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="991bc-118">Requirement</span></span> | <span data-ttu-id="991bc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="991bc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="991bc-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="991bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="991bc-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="991bc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="991bc-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="991bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="991bc-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="991bc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="991bc-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="991bc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="991bc-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="991bc-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





