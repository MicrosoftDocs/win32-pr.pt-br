---
title: MCN_SELCHANGE código de notificação (commctrl. h)
description: Enviado por um controle de calendário mensal quando a data ou o intervalo de datas selecionado atualmente é alterado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- MCN_SELCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffa328ca0173afd3a577f6cf14e0204cd5c0f7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009000"
---
# <a name="mcn_selchange-notification-code"></a><span data-ttu-id="66b10-105">Código de notificação do MCN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="66b10-105">MCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="66b10-106">Enviado por um controle de calendário mensal quando a data ou o intervalo de datas selecionado atualmente é alterado.</span><span class="sxs-lookup"><span data-stu-id="66b10-106">Sent by a month calendar control when the currently selected date or range of dates changes.</span></span> <span data-ttu-id="66b10-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="66b10-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="66b10-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66b10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66b10-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66b10-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66b10-110">Ponteiro para uma estrutura [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) que contém informações sobre o intervalo de datas selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="66b10-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66b10-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66b10-111">Return value</span></span>

<span data-ttu-id="66b10-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="66b10-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66b10-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="66b10-113">Remarks</span></span>

<span data-ttu-id="66b10-114">Por exemplo, o controle envia MCN \_ SELCHANGE quando o usuário altera explicitamente a seleção dentro do mês atual ou quando a seleção é implicitamente alterada em resposta à navegação do mês seguinte/anterior.</span><span class="sxs-lookup"><span data-stu-id="66b10-114">For example, the control sends MCN\_SELCHANGE when the user explicitly changes the selection within the current month or when the selection is implicitly changed in response to next/previous month navigation.</span></span> <span data-ttu-id="66b10-115">Esse código de notificação também é enviado pelo sistema em intervalos regulares para que o controle possa responder às alterações de data.</span><span class="sxs-lookup"><span data-stu-id="66b10-115">This notification code is also sent by the system at regular intervals so that the control can respond to date changes.</span></span>

<span data-ttu-id="66b10-116">Esse código de notificação é semelhante a [MCN \_ Select](mcn-select.md), mas é enviado em resposta a qualquer alteração de seleção.</span><span class="sxs-lookup"><span data-stu-id="66b10-116">This notification code is similar to [MCN\_SELECT](mcn-select.md), but it is sent in response to any selection change.</span></span> <span data-ttu-id="66b10-117">MCN \_ Select é enviado somente para uma seleção de data explícita.</span><span class="sxs-lookup"><span data-stu-id="66b10-117">MCN\_SELECT is sent only for an explicit date selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="66b10-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66b10-118">Requirements</span></span>



| <span data-ttu-id="66b10-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="66b10-119">Requirement</span></span> | <span data-ttu-id="66b10-120">Valor</span><span class="sxs-lookup"><span data-stu-id="66b10-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66b10-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66b10-121">Minimum supported client</span></span><br/> | <span data-ttu-id="66b10-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66b10-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66b10-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66b10-123">Minimum supported server</span></span><br/> | <span data-ttu-id="66b10-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="66b10-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66b10-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66b10-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="66b10-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66b10-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





