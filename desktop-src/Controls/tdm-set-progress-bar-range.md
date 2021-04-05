---
title: Mensagem de TDM_SET_PROGRESS_BAR_RANGE (commctrl. h)
description: Define os valores mínimo e máximo para a barra de progresso em uma caixa de diálogo de tarefa.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- Controles de TDM_SET_PROGRESS_BAR_RANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17ebb6caa2c33282dccbb117980fc970cd45477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824804"
---
# <a name="tdm_set_progress_bar_range-message"></a><span data-ttu-id="8c9cd-104">\_Mensagem de \_ intervalo da barra de progresso do conjunto TDM \_ \_</span><span class="sxs-lookup"><span data-stu-id="8c9cd-104">TDM\_SET\_PROGRESS\_BAR\_RANGE message</span></span>

<span data-ttu-id="8c9cd-105">Define os valores mínimo e máximo para a barra de progresso em uma caixa de diálogo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="8c9cd-105">Sets the minimum and maximum values for the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c9cd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c9cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c9cd-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c9cd-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c9cd-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8c9cd-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8c9cd-109">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c9cd-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c9cd-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o valor mínimo.</span><span class="sxs-lookup"><span data-stu-id="8c9cd-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum value.</span></span> <span data-ttu-id="8c9cd-111">Por padrão, o valor mínimo é zero.</span><span class="sxs-lookup"><span data-stu-id="8c9cd-111">By default, the minimum value is zero.</span></span> <span data-ttu-id="8c9cd-112">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o valor máximo.</span><span class="sxs-lookup"><span data-stu-id="8c9cd-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum value.</span></span> <span data-ttu-id="8c9cd-113">Por padrão, o valor máximo é 100.</span><span class="sxs-lookup"><span data-stu-id="8c9cd-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c9cd-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c9cd-114">Return value</span></span>

<span data-ttu-id="8c9cd-115">Retorna os valores mínimo e máximo anteriores, se bem-sucedido, ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="8c9cd-115">Returns the previous minimum and maximum values, if successful, or zero otherwise.</span></span> <span data-ttu-id="8c9cd-116">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o valor mínimo e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém o valor máximo.</span><span class="sxs-lookup"><span data-stu-id="8c9cd-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c9cd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c9cd-117">Requirements</span></span>



| <span data-ttu-id="8c9cd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c9cd-118">Requirement</span></span> | <span data-ttu-id="8c9cd-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8c9cd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c9cd-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c9cd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8c9cd-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c9cd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c9cd-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c9cd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8c9cd-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c9cd-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c9cd-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c9cd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c9cd-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c9cd-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

