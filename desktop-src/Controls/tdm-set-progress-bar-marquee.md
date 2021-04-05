---
title: Mensagem de TDM_SET_PROGRESS_BAR_MARQUEE (commctrl. h)
description: Inicia e interrompe a exibição de letreiro da barra de progresso em uma caixa de diálogo de tarefa e define a velocidade do letreiro.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- Controles de TDM_SET_PROGRESS_BAR_MARQUEE de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f73d3d4308d2e3f963c015b6e36f385902bea6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009704"
---
# <a name="tdm_set_progress_bar_marquee-message"></a><span data-ttu-id="8a900-104">\_Mensagem de \_ letreiro da barra de progresso \_ \_ do TDM Set</span><span class="sxs-lookup"><span data-stu-id="8a900-104">TDM\_SET\_PROGRESS\_BAR\_MARQUEE message</span></span>

<span data-ttu-id="8a900-105">Inicia e interrompe a exibição de letreiro da barra de progresso em uma caixa de diálogo de tarefa e define a velocidade do letreiro.</span><span class="sxs-lookup"><span data-stu-id="8a900-105">Starts and stops the marquee display of the progress bar in a task dialog, and sets the speed of the marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a900-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a900-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a900-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a900-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a900-108">Um **bool** que indica se a exibição do letreiror deve ser ativada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="8a900-108">A **BOOL** that indicates whether to turn the marquee display on or off.</span></span> <span data-ttu-id="8a900-109">Use **true** para ativar a exibição do letreiro ou **false** para desativá-la.</span><span class="sxs-lookup"><span data-stu-id="8a900-109">Use **TRUE** to turn on the marquee display, or **FALSE** to turn it off.</span></span>

</dd> <dt>

<span data-ttu-id="8a900-110">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a900-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a900-111">Um **uint** que especifica o tempo, em milissegundos, entre as atualizações de animação do letreiro digital.</span><span class="sxs-lookup"><span data-stu-id="8a900-111">A **UINT** that specifies the time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="8a900-112">Se esse parâmetro for zero, a animação do letreiro digital será atualizada a cada 30 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="8a900-112">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a900-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a900-113">Return value</span></span>

<span data-ttu-id="8a900-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="8a900-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a900-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a900-115">Remarks</span></span>

<span data-ttu-id="8a900-116">Para obter informações sobre o modo de letreiro, consulte [controle de barra de progresso](progress-bar-control.md).</span><span class="sxs-lookup"><span data-stu-id="8a900-116">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a900-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a900-117">Requirements</span></span>



| <span data-ttu-id="8a900-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a900-118">Requirement</span></span> | <span data-ttu-id="8a900-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8a900-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a900-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a900-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8a900-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a900-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8a900-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a900-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8a900-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a900-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a900-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a900-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a900-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a900-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





