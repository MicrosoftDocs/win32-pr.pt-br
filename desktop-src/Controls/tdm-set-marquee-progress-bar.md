---
title: Mensagem de TDM_SET_MARQUEE_PROGRESS_BAR (commctrl. h)
description: Indica se a barra de progresso hospedada de uma caixa de diálogo de tarefa deve ser exibida no modo de letreiro.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- Controles de TDM_SET_MARQUEE_PROGRESS_BAR de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a9384826b89d07c6564dc511d4909058871ca3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086319"
---
# <a name="tdm_set_marquee_progress_bar-message"></a><span data-ttu-id="9914d-104">\_Mensagem da \_ barra de \_ progresso do letreiro de conjunto de TDM \_</span><span class="sxs-lookup"><span data-stu-id="9914d-104">TDM\_SET\_MARQUEE\_PROGRESS\_BAR message</span></span>

<span data-ttu-id="9914d-105">Indica se a barra de progresso hospedada de uma caixa de diálogo de tarefa deve ser exibida no modo de letreiro.</span><span class="sxs-lookup"><span data-stu-id="9914d-105">Indicates whether the hosted progress bar of a task dialog should be displayed in marquee mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="9914d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9914d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9914d-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9914d-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9914d-108">Um **bool** que indica se a barra de progresso deve ser mostrada no modo de letreiro.</span><span class="sxs-lookup"><span data-stu-id="9914d-108">A **BOOL** that indicates whether the progress bar should be shown in marquee mode.</span></span> <span data-ttu-id="9914d-109">Um valor **true** ativa o modo de letreiro e um valor de **false** desativa o modo de letreiro.</span><span class="sxs-lookup"><span data-stu-id="9914d-109">A value of **TRUE** turns on marquee mode, and a value of **FALSE** turns off marquee mode.</span></span>

</dd> <dt>

<span data-ttu-id="9914d-110">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9914d-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9914d-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9914d-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9914d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9914d-112">Return value</span></span>

<span data-ttu-id="9914d-113">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="9914d-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="9914d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9914d-114">Remarks</span></span>

<span data-ttu-id="9914d-115">Para obter informações sobre o modo de letreiro, consulte [controle de barra de progresso](progress-bar-control.md).</span><span class="sxs-lookup"><span data-stu-id="9914d-115">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9914d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9914d-116">Requirements</span></span>



| <span data-ttu-id="9914d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9914d-117">Requirement</span></span> | <span data-ttu-id="9914d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9914d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9914d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9914d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9914d-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9914d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9914d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9914d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9914d-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9914d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9914d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9914d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9914d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9914d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





