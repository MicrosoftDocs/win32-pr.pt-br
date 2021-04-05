---
title: Mensagem de DTM_GETMCSTYLE (commctrl. h)
description: Obtém o estilo de um controle do seletor de data e hora (DTP). Envie essa mensagem explicitamente ou usando a macro DateTime \_ GetMonthCalStyle.
ms.assetid: 8983898f-e23a-4247-838c-56364f695429
keywords:
- Controles de DTM_GETMCSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_GETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cae82d271d0e9aece54046527dfa3bedcef657f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918813"
---
# <a name="dtm_getmcstyle-message"></a><span data-ttu-id="95fac-105">\_Mensagem DTM GETMCSTYLE</span><span class="sxs-lookup"><span data-stu-id="95fac-105">DTM\_GETMCSTYLE message</span></span>

<span data-ttu-id="95fac-106">Obtém o estilo de um controle do seletor de data e hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="95fac-106">Gets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="95fac-107">Envie essa mensagem explicitamente ou usando a macro [**DateTime \_ GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) .</span><span class="sxs-lookup"><span data-stu-id="95fac-107">Send this message explicitly or by using the [**DateTime\_GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="95fac-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95fac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95fac-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95fac-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95fac-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="95fac-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="95fac-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95fac-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="95fac-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="95fac-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95fac-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95fac-113">Return value</span></span>

<span data-ttu-id="95fac-114">Retorna o valor do estilo do controle.</span><span class="sxs-lookup"><span data-stu-id="95fac-114">Returns the style value of the control.</span></span> <span data-ttu-id="95fac-115">Para obter mais informações, consulte [estilos de controle de calendário mensal](month-calendar-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="95fac-115">For more information see [Month Calendar Control Styles](month-calendar-control-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95fac-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95fac-116">Requirements</span></span>



| <span data-ttu-id="95fac-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="95fac-117">Requirement</span></span> | <span data-ttu-id="95fac-118">Valor</span><span class="sxs-lookup"><span data-stu-id="95fac-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95fac-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95fac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95fac-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95fac-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95fac-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95fac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95fac-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="95fac-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95fac-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95fac-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95fac-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="95fac-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





