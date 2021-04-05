---
title: Mensagem de MCM_GETCALENDARCOUNT (commctrl. h)
description: Obtém o número de calendários atualmente exibidos no controle de calendário. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetCalendarCount.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- Controles de MCM_GETCALENDARCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a3be9e9bcc5db8c1aab32cacbcc2ded82727af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085931"
---
# <a name="mcm_getcalendarcount-message"></a><span data-ttu-id="e8928-105">\_Mensagem MCM GETCALENDARCOUNT</span><span class="sxs-lookup"><span data-stu-id="e8928-105">MCM\_GETCALENDARCOUNT message</span></span>

<span data-ttu-id="e8928-106">Obtém o número de calendários atualmente exibidos no controle de calendário.</span><span class="sxs-lookup"><span data-stu-id="e8928-106">Gets the number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="e8928-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) .</span><span class="sxs-lookup"><span data-stu-id="e8928-107">You can send this message explicitly or by using the [**MonthCal\_GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8928-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8928-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8928-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8928-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8928-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e8928-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e8928-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8928-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8928-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e8928-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8928-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8928-113">Return value</span></span>

<span data-ttu-id="e8928-114">Número de calendários atualmente exibidos no controle de calendário.</span><span class="sxs-lookup"><span data-stu-id="e8928-114">Number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="e8928-115">O número máximo de calendários permitidos é 12.</span><span class="sxs-lookup"><span data-stu-id="e8928-115">The maximum number of allowed calendars is 12.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8928-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8928-116">Requirements</span></span>



| <span data-ttu-id="e8928-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8928-117">Requirement</span></span> | <span data-ttu-id="e8928-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e8928-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8928-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8928-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e8928-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8928-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8928-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8928-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e8928-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e8928-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8928-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8928-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8928-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8928-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





