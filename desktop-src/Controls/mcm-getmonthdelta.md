---
title: Mensagem de MCM_GETMONTHDELTA (commctrl. h)
description: Recupera a taxa de rolagem para um controle de calendário mensal. A taxa de rolagem é o número de meses que o controle move sua exibição quando o usuário clica em um botão de rolagem. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetMonthDelta.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- Controles de MCM_GETMONTHDELTA de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01eaa40b930e6317cc2be6b674f0cea58115ae40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086549"
---
# <a name="mcm_getmonthdelta-message"></a><span data-ttu-id="e8035-106">\_Mensagem MCM GETMONTHDELTA</span><span class="sxs-lookup"><span data-stu-id="e8035-106">MCM\_GETMONTHDELTA message</span></span>

<span data-ttu-id="e8035-107">Recupera a taxa de rolagem para um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="e8035-107">Retrieves the scroll rate for a month calendar control.</span></span> <span data-ttu-id="e8035-108">A taxa de rolagem é o número de meses que o controle move sua exibição quando o usuário clica em um botão de rolagem.</span><span class="sxs-lookup"><span data-stu-id="e8035-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="e8035-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) .</span><span class="sxs-lookup"><span data-stu-id="e8035-109">You can send this message explicitly or by using the [**MonthCal\_GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8035-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8035-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8035-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8035-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e8035-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e8035-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e8035-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8035-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e8035-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e8035-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8035-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8035-115">Return value</span></span>

<span data-ttu-id="e8035-116">Se o Delta de mês tiver sido definido anteriormente usando a mensagem [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) , retornará um valor int que representa a taxa de rolagem atual do calendário do mês.</span><span class="sxs-lookup"><span data-stu-id="e8035-116">If the month delta was previously set using the [**MCM\_SETMONTHDELTA**](mcm-setmonthdelta.md) message, returns an INT value that represents the month calendar's current scroll rate.</span></span> <span data-ttu-id="e8035-117">Se o Delta de mês não tiver sido definido anteriormente usando a mensagem **MCM \_ SETMONTHDELTA** ou se o Delta de mês tiver sido redefinido para o padrão, retornará um valor int que representa o número atual de meses visíveis.</span><span class="sxs-lookup"><span data-stu-id="e8035-117">If the month delta was not previously set using the **MCM\_SETMONTHDELTA** message, or the month delta was reset to the default, returns an INT value that represents the current number of months visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8035-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8035-118">Requirements</span></span>



| <span data-ttu-id="e8035-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8035-119">Requirement</span></span> | <span data-ttu-id="e8035-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e8035-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8035-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8035-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e8035-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8035-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8035-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8035-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e8035-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8035-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8035-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8035-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8035-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8035-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





