---
title: Mensagem de PBM_SETRANGE32 (commctrl. h)
description: Define os valores mínimo e máximo de uma barra de progresso para valores de 32 bits e redesenha a barra para refletir o novo intervalo.
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- Controles de PBM_SETRANGE32 de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55fcf91c794ec9ae3880d67f8df947f87fec413d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644907"
---
# <a name="pbm_setrange32-message"></a><span data-ttu-id="56237-104">Mensagem do SETRANGE32 do PBM \_</span><span class="sxs-lookup"><span data-stu-id="56237-104">PBM\_SETRANGE32 message</span></span>

<span data-ttu-id="56237-105">Define os valores mínimo e máximo de uma barra de progresso para valores de 32 bits e redesenha a barra para refletir o novo intervalo.</span><span class="sxs-lookup"><span data-stu-id="56237-105">Sets the minimum and maximum values for a progress bar to 32-bit values, and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="56237-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56237-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56237-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56237-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56237-108">Valor de intervalo mínimo.</span><span class="sxs-lookup"><span data-stu-id="56237-108">Minimum range value.</span></span> <span data-ttu-id="56237-109">Por padrão, o valor mínimo é zero.</span><span class="sxs-lookup"><span data-stu-id="56237-109">By default, the minimum value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="56237-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56237-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56237-111">Valor de intervalo máximo.</span><span class="sxs-lookup"><span data-stu-id="56237-111">Maximum range value.</span></span> <span data-ttu-id="56237-112">Esse valor deve ser maior que *wParam*.</span><span class="sxs-lookup"><span data-stu-id="56237-112">This value must be greater than *wParam*.</span></span> <span data-ttu-id="56237-113">Por padrão, o valor máximo é 100.</span><span class="sxs-lookup"><span data-stu-id="56237-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56237-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56237-114">Return value</span></span>

<span data-ttu-id="56237-115">Retorna um valor **DWORD** que contém o limite baixo de 16 bits anterior em seu [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e o limite superior de 16 bits anterior em seu [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="56237-115">Returns a **DWORD** value that holds the previous 16-bit low limit in its [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous 16-bit high limit in its [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="56237-116">Se os intervalos anteriores eram valores de 32 bits, o valor de retorno consiste em **LOWORD** s de ambos os limites de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="56237-116">If the previous ranges were 32-bit values, the return value consists of the **LOWORD** s of both 32-bit limits.</span></span>

## <a name="remarks"></a><span data-ttu-id="56237-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="56237-117">Remarks</span></span>

<span data-ttu-id="56237-118">Para recuperar os valores inteiros de 32 bits altos e baixos, use a mensagem do [**PBM \_ GetRange**](pbm-getrange.md) .</span><span class="sxs-lookup"><span data-stu-id="56237-118">To retrieve the entire high and low 32-bit values, use the [**PBM\_GETRANGE**](pbm-getrange.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="56237-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56237-119">Requirements</span></span>



| <span data-ttu-id="56237-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="56237-120">Requirement</span></span> | <span data-ttu-id="56237-121">Valor</span><span class="sxs-lookup"><span data-stu-id="56237-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56237-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56237-122">Minimum supported client</span></span><br/> | <span data-ttu-id="56237-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56237-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56237-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56237-124">Minimum supported server</span></span><br/> | <span data-ttu-id="56237-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56237-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56237-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56237-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="56237-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56237-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

