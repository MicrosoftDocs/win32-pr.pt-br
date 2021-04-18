---
title: Mensagem de MCM_GETFIRSTDAYOFWEEK (commctrl. h)
description: Recupera o primeiro dia da semana para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ getFirstDayOfWeek.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- Controles de MCM_GETFIRSTDAYOFWEEK de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b625e470e13c111b0274bfef422963e48c9cc7c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755428"
---
# <a name="mcm_getfirstdayofweek-message"></a><span data-ttu-id="1b30d-105">\_Mensagem MCM GETfirstdayofweek</span><span class="sxs-lookup"><span data-stu-id="1b30d-105">MCM\_GETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="1b30d-106">Recupera o primeiro dia da semana para um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="1b30d-106">Retrieves the first day of the week for a month calendar control.</span></span> <span data-ttu-id="1b30d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ getFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) .</span><span class="sxs-lookup"><span data-stu-id="1b30d-107">You can send this message explicitly or by using the [**MonthCal\_GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b30d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b30d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b30d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b30d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1b30d-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1b30d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1b30d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b30d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1b30d-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1b30d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b30d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b30d-113">Return value</span></span>

<span data-ttu-id="1b30d-114">Retorna um valor **DWORD** que contém dois valores.</span><span class="sxs-lookup"><span data-stu-id="1b30d-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="1b30d-115">A palavra alta é um valor **bool** que é diferente de zero se o primeiro dia da semana for definido como algo diferente de \_ IFIRSTDAYOFWEEK de localidade, caso contrário, zero.</span><span class="sxs-lookup"><span data-stu-id="1b30d-115">The high word is a **BOOL** value that is nonzero if the first day of the week is set to something other than LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="1b30d-116">A palavra inferior é um valor inteiro que representa o primeiro dia da semana, em que 0 é segunda-feira, 1 é terça-feira e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="1b30d-116">The low word is an INT value that represents the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b30d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b30d-117">Requirements</span></span>



| <span data-ttu-id="1b30d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b30d-118">Requirement</span></span> | <span data-ttu-id="1b30d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1b30d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b30d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b30d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1b30d-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b30d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b30d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b30d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1b30d-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b30d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b30d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b30d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b30d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b30d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





