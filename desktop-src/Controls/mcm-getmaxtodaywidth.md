---
title: Mensagem de MCM_GETMAXTODAYWIDTH (commctrl. h)
description: Recupera a largura máxima de \ 0034; hoje \ 0034; Cadeia de caracteres em um controle de calendário mensal. Isso inclui o texto do rótulo e o texto de data. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetMaxTodayWidth.
ms.assetid: bb55c24e-ba04-4a57-97b0-ff04d77e1d43
keywords:
- Controles de MCM_GETMAXTODAYWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETMAXTODAYWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b4c188e994a1dcc5a8fbd80ae3f1b06894bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644729"
---
# <a name="mcm_getmaxtodaywidth-message"></a><span data-ttu-id="36648-106">\_Mensagem MCM GETMAXTODAYWIDTH</span><span class="sxs-lookup"><span data-stu-id="36648-106">MCM\_GETMAXTODAYWIDTH message</span></span>

<span data-ttu-id="36648-107">Recupera a largura máxima da cadeia de caracteres "hoje" em um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="36648-107">Retrieves the maximum width of the "today" string in a month calendar control.</span></span> <span data-ttu-id="36648-108">Isso inclui o texto do rótulo e o texto de data.</span><span class="sxs-lookup"><span data-stu-id="36648-108">This includes the label text and the date text.</span></span> <span data-ttu-id="36648-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) .</span><span class="sxs-lookup"><span data-stu-id="36648-109">You can send this message explicitly or by using the [**MonthCal\_GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="36648-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36648-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36648-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36648-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="36648-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="36648-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="36648-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36648-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="36648-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="36648-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36648-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36648-115">Return value</span></span>

<span data-ttu-id="36648-116">Retorna a largura da cadeia de caracteres "Today", em pixels.</span><span class="sxs-lookup"><span data-stu-id="36648-116">Returns the width of the "today" string, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="36648-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36648-117">Requirements</span></span>



| <span data-ttu-id="36648-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="36648-118">Requirement</span></span> | <span data-ttu-id="36648-119">Valor</span><span class="sxs-lookup"><span data-stu-id="36648-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36648-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36648-120">Minimum supported client</span></span><br/> | <span data-ttu-id="36648-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36648-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36648-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36648-122">Minimum supported server</span></span><br/> | <span data-ttu-id="36648-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="36648-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36648-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36648-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="36648-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="36648-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





