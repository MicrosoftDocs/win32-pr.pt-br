---
title: Mensagem de MCM_SETFIRSTDAYOFWEEK (commctrl. h)
description: Define o primeiro dia da semana para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ setFirstDayOfWeek.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- Controles de MCM_SETFIRSTDAYOFWEEK de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32452c9043bbd7c3bbcf96f9dc32e67714eacce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756425"
---
# <a name="mcm_setfirstdayofweek-message"></a><span data-ttu-id="19f85-105">\_Mensagem MCM SETfirstdayofweek</span><span class="sxs-lookup"><span data-stu-id="19f85-105">MCM\_SETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="19f85-106">Define o primeiro dia da semana para um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="19f85-106">Sets the first day of the week for a month calendar control.</span></span> <span data-ttu-id="19f85-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ setFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) .</span><span class="sxs-lookup"><span data-stu-id="19f85-107">You can send this message explicitly or by using the [**MonthCal\_SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="19f85-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19f85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19f85-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19f85-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="19f85-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="19f85-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="19f85-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19f85-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19f85-112">Valor do tipo **int** que representa qual dia deve ser definido como o primeiro dia da semana, em que 0 é segunda-feira, 1 é terça-feira e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="19f85-112">Value of type **int** representing which day is to be set as the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19f85-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19f85-113">Return value</span></span>

<span data-ttu-id="19f85-114">Retorna um valor **DWORD** que contém dois valores.</span><span class="sxs-lookup"><span data-stu-id="19f85-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="19f85-115">A palavra alta é um valor **bool** que será diferente de zero se o primeiro dia da semana anterior não for igual a IFIRSTDAYOFWEEK de localidade \_ nem nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="19f85-115">The high word is a **BOOL** value that is nonzero if the previous first day of the week did not equal LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="19f85-116">A palavra inferior é um valor inteiro que representa o primeiro dia da semana anterior.</span><span class="sxs-lookup"><span data-stu-id="19f85-116">The low word is an INT value that represents the previous first day of the week.</span></span>

## <a name="remarks"></a><span data-ttu-id="19f85-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="19f85-117">Remarks</span></span>

<span data-ttu-id="19f85-118">Se o primeiro dia da semana for definido como algo diferente do padrão (localidade \_ IFIRSTDAYOFWEEK), o controle não atualizará automaticamente as alterações do primeiro dia da semana com base nas alterações de localidade.</span><span class="sxs-lookup"><span data-stu-id="19f85-118">If the first day of the week is set to anything other than the default (LOCALE\_IFIRSTDAYOFWEEK), the control will not automatically update first-day-of-the-week changes based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="19f85-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19f85-119">Requirements</span></span>



| <span data-ttu-id="19f85-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="19f85-120">Requirement</span></span> | <span data-ttu-id="19f85-121">Valor</span><span class="sxs-lookup"><span data-stu-id="19f85-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19f85-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19f85-122">Minimum supported client</span></span><br/> | <span data-ttu-id="19f85-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19f85-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19f85-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19f85-124">Minimum supported server</span></span><br/> | <span data-ttu-id="19f85-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19f85-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19f85-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19f85-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="19f85-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="19f85-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





