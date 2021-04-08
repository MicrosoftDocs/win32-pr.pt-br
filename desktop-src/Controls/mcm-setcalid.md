---
title: Mensagem de MCM_SETCALID (commctrl. h)
description: Define a ID do calendário para o controle de calendário fornecido. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetCALID.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- Controles de MCM_SETCALID de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a661a685062fe737a1927c3a6ab455e8499c6ca9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009001"
---
# <a name="mcm_setcalid-message"></a><span data-ttu-id="54434-105">\_Mensagem MCM SETCALID</span><span class="sxs-lookup"><span data-stu-id="54434-105">MCM\_SETCALID message</span></span>

<span data-ttu-id="54434-106">Define a ID do calendário para o controle de calendário fornecido.</span><span class="sxs-lookup"><span data-stu-id="54434-106">Sets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="54434-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) .</span><span class="sxs-lookup"><span data-stu-id="54434-107">You can send this message explicitly or by using the [**MonthCal\_SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="54434-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54434-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54434-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54434-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54434-110">A ID do calendário.</span><span class="sxs-lookup"><span data-stu-id="54434-110">The calendar ID.</span></span> <span data-ttu-id="54434-111">Uma das constantes de [identificadores de calendário](/windows/desktop/Intl/calendar-identifiers) .</span><span class="sxs-lookup"><span data-stu-id="54434-111">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

</dd> <dt>

<span data-ttu-id="54434-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54434-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54434-113">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="54434-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54434-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="54434-114">Return value</span></span>

<span data-ttu-id="54434-115">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="54434-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="54434-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54434-116">Requirements</span></span>



| <span data-ttu-id="54434-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="54434-117">Requirement</span></span> | <span data-ttu-id="54434-118">Valor</span><span class="sxs-lookup"><span data-stu-id="54434-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54434-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54434-119">Minimum supported client</span></span><br/> | <span data-ttu-id="54434-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54434-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54434-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54434-121">Minimum supported server</span></span><br/> | <span data-ttu-id="54434-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54434-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54434-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54434-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="54434-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="54434-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

