---
title: Mensagem de MCM_GETCALID (commctrl. h)
description: Obtém a ID do calendário para o controle de calendário fornecido. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetCALID.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- Controles de MCM_GETCALID de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb4a780d5107a7761d7dcac9b27a7cb01f3de744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085675"
---
# <a name="mcm_getcalid-message"></a><span data-ttu-id="5686c-105">\_Mensagem MCM GETCALID</span><span class="sxs-lookup"><span data-stu-id="5686c-105">MCM\_GETCALID message</span></span>

<span data-ttu-id="5686c-106">Obtém a ID do calendário para o controle de calendário fornecido.</span><span class="sxs-lookup"><span data-stu-id="5686c-106">Gets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="5686c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) .</span><span class="sxs-lookup"><span data-stu-id="5686c-107">You can send this message explicitly or by using the [**MonthCal\_GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5686c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5686c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5686c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5686c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5686c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5686c-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5686c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5686c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5686c-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5686c-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5686c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5686c-113">Return value</span></span>

<span data-ttu-id="5686c-114">ID do calendário atual.</span><span class="sxs-lookup"><span data-stu-id="5686c-114">ID of the current calendar.</span></span> <span data-ttu-id="5686c-115">Uma das constantes de [identificadores de calendário](/windows/desktop/Intl/calendar-identifiers) .</span><span class="sxs-lookup"><span data-stu-id="5686c-115">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="5686c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5686c-116">Requirements</span></span>



| <span data-ttu-id="5686c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5686c-117">Requirement</span></span> | <span data-ttu-id="5686c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5686c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5686c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5686c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5686c-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5686c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5686c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5686c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5686c-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5686c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5686c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5686c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5686c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5686c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

