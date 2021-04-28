---
title: Mensagem de TBM_SETPOS (commctrl. h)
description: TBM_SETPOS mensagem – define a posição lógica atual do controle deslizante em um TrackBar.
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- Controles de TBM_SETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f10e05a677119f18489d0eb9eebc4528d3ad115
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085864"
---
# <a name="tbm_setpos-message"></a><span data-ttu-id="3d7f8-104">\_Mensagem tbm SETPOS</span><span class="sxs-lookup"><span data-stu-id="3d7f8-104">TBM\_SETPOS message</span></span>

<span data-ttu-id="3d7f8-105">Define a posição lógica atual do controle deslizante em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="3d7f8-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3d7f8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d7f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d7f8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d7f8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d7f8-108">Sinalizador de redesenho.</span><span class="sxs-lookup"><span data-stu-id="3d7f8-108">Redraw flag.</span></span> <span data-ttu-id="3d7f8-109">Se esse parâmetro for **true**, a mensagem redesenhará o controle com o controle deslizante na posição fornecida pelo *lParam*.</span><span class="sxs-lookup"><span data-stu-id="3d7f8-109">If this parameter is **TRUE**, the message redraws the control with the slider at the position given by *lParam*.</span></span> <span data-ttu-id="3d7f8-110">Se esse parâmetro for **false**, a mensagem não redesenhará o controle deslizante na nova posição.</span><span class="sxs-lookup"><span data-stu-id="3d7f8-110">If this parameter is **FALSE**, the message does not redraw the slider at the new position.</span></span> <span data-ttu-id="3d7f8-111">Observe que a mensagem define o valor da posição do controle deslizante (como retornado pela mensagem [**tbm \_ GETPOS**](tbm-getpos.md) ), independentemente do parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="3d7f8-111">Note that the message sets the value of the slider position (as returned by the [**TBM\_GETPOS**](tbm-getpos.md) message) regardless of the *wParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3d7f8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d7f8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d7f8-113">Nova posição lógica do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="3d7f8-113">New logical position of the slider.</span></span> <span data-ttu-id="3d7f8-114">As posições lógicas válidas são os valores inteiros no intervalo de TrackBar de mínimo para o máximo de posições do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="3d7f8-114">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="3d7f8-115">Se esse valor estiver fora do intervalo máximo e mínimo do controle, a posição será definida como o valor máximo ou mínimo.</span><span class="sxs-lookup"><span data-stu-id="3d7f8-115">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d7f8-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3d7f8-116">Return value</span></span>

<span data-ttu-id="3d7f8-117">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="3d7f8-117">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d7f8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d7f8-118">Requirements</span></span>



| <span data-ttu-id="3d7f8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d7f8-119">Requirement</span></span> | <span data-ttu-id="3d7f8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3d7f8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d7f8-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d7f8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3d7f8-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d7f8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d7f8-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d7f8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3d7f8-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3d7f8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d7f8-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3d7f8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d7f8-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d7f8-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





