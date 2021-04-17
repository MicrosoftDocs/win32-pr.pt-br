---
title: Mensagem de TCM_ADJUSTRECT (commctrl. h)
description: Calcula a área de exibição de um controle guia, dado um retângulo de janela, ou calcula o retângulo da janela que corresponderia a uma área de exibição especificada. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ AdjustRect.
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- Controles de TCM_ADJUSTRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c1612a4f6c2fc436f858807fca59112c376a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749304"
---
# <a name="tcm_adjustrect-message"></a><span data-ttu-id="8036d-105">\_Mensagem ADJUSTRECT de TCM</span><span class="sxs-lookup"><span data-stu-id="8036d-105">TCM\_ADJUSTRECT message</span></span>

<span data-ttu-id="8036d-106">Calcula a área de exibição de um controle guia, dado um retângulo de janela, ou calcula o retângulo da janela que corresponderia a uma área de exibição especificada.</span><span class="sxs-lookup"><span data-stu-id="8036d-106">Calculates a tab control's display area given a window rectangle, or calculates the window rectangle that would correspond to a specified display area.</span></span> <span data-ttu-id="8036d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) .</span><span class="sxs-lookup"><span data-stu-id="8036d-107">You can send this message explicitly or by using the [**TabCtrl\_AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8036d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8036d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8036d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8036d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8036d-110">Operação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="8036d-110">Operation to perform.</span></span> <span data-ttu-id="8036d-111">Se esse parâmetro for **true**, *lParam* especificará um retângulo de exibição e receberá o retângulo de janela correspondente.</span><span class="sxs-lookup"><span data-stu-id="8036d-111">If this parameter is **TRUE**, *lParam* specifies a display rectangle and receives the corresponding window rectangle.</span></span> <span data-ttu-id="8036d-112">Se esse parâmetro for **false**, *lParam* especificará um retângulo de janela e receberá a área de exibição correspondente.</span><span class="sxs-lookup"><span data-stu-id="8036d-112">If this parameter is **FALSE**, *lParam* specifies a window rectangle and receives the corresponding display area.</span></span>

</dd> <dt>

<span data-ttu-id="8036d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8036d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8036d-114">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica o retângulo fornecido e recebe o retângulo calculado.</span><span class="sxs-lookup"><span data-stu-id="8036d-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the given rectangle and receives the calculated rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8036d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8036d-115">Return value</span></span>

<span data-ttu-id="8036d-116">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="8036d-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8036d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8036d-117">Remarks</span></span>

<span data-ttu-id="8036d-118">Essa mensagem se aplica somente a controles de guia que estão na parte superior.</span><span class="sxs-lookup"><span data-stu-id="8036d-118">This message applies only to tab controls that are at the top.</span></span> <span data-ttu-id="8036d-119">Ele não se aplica a controles de guia que estão nos lados ou na parte inferior.</span><span class="sxs-lookup"><span data-stu-id="8036d-119">It does not apply to tab controls that are on the sides or bottom.</span></span>

## <a name="requirements"></a><span data-ttu-id="8036d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8036d-120">Requirements</span></span>



| <span data-ttu-id="8036d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8036d-121">Requirement</span></span> | <span data-ttu-id="8036d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8036d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8036d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8036d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8036d-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8036d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8036d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8036d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8036d-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8036d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8036d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8036d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8036d-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8036d-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

