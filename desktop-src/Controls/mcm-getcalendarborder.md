---
title: Mensagem de MCM_GETCALENDARBORDER (commctrl. h)
description: Obtém o tamanho da borda, em pixels. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetCurrentView.
ms.assetid: 68366ee1-7511-46a5-aab0-a42fb80c265f
keywords:
- Controles de MCM_GETCALENDARBORDER de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581eeb5c060f725d3f884f4c19d7d3da3023c63a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499546"
---
# <a name="mcm_getcalendarborder-message"></a><span data-ttu-id="72ff5-105">\_Mensagem MCM GETCALENDARBORDER</span><span class="sxs-lookup"><span data-stu-id="72ff5-105">MCM\_GETCALENDARBORDER message</span></span>

<span data-ttu-id="72ff5-106">Obtém o tamanho da borda, em pixels.</span><span class="sxs-lookup"><span data-stu-id="72ff5-106">Gets the size of the border, in pixels.</span></span> <span data-ttu-id="72ff5-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="72ff5-107">You can send this message explicitly or by using the [**MonthCal\_GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="72ff5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72ff5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72ff5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72ff5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72ff5-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="72ff5-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="72ff5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72ff5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72ff5-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="72ff5-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72ff5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72ff5-113">Return value</span></span>

<span data-ttu-id="72ff5-114">Tamanho da borda, em pixels.</span><span class="sxs-lookup"><span data-stu-id="72ff5-114">Border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="72ff5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72ff5-115">Requirements</span></span>



| <span data-ttu-id="72ff5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="72ff5-116">Requirement</span></span> | <span data-ttu-id="72ff5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="72ff5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72ff5-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72ff5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="72ff5-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72ff5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72ff5-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72ff5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="72ff5-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="72ff5-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72ff5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72ff5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="72ff5-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="72ff5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





