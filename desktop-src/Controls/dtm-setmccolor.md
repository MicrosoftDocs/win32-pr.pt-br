---
title: Mensagem de DTM_SETMCCOLOR (commctrl. h)
description: Define a cor de uma determinada parte do calendário mensal dentro de um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a \_ macro DateTime SetMonthCalColor.
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- Controles de DTM_SETMCCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_SETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e496abb4dd28b040dd4a8035073ffa32a3f3847
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644915"
---
# <a name="dtm_setmccolor-message"></a><span data-ttu-id="2e2d9-105">\_Mensagem DTM SETMCCOLOR</span><span class="sxs-lookup"><span data-stu-id="2e2d9-105">DTM\_SETMCCOLOR message</span></span>

<span data-ttu-id="2e2d9-106">Define a cor de uma determinada parte do calendário mensal dentro de um controle do seletor de data e hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="2e2d9-106">Sets the color for a given portion of the month calendar within a date and time picker (DTP) control.</span></span> <span data-ttu-id="2e2d9-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) .</span><span class="sxs-lookup"><span data-stu-id="2e2d9-107">You can send this message explicitly or use the [**DateTime\_SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e2d9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e2d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e2d9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e2d9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e2d9-110">Um valor do tipo **int** especificando qual cor de calendário de mês definir.</span><span class="sxs-lookup"><span data-stu-id="2e2d9-110">A value of type **int** specifying which month calendar color to set.</span></span> <span data-ttu-id="2e2d9-111">Este valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="2e2d9-111">This value can be one of the following:</span></span>



| <span data-ttu-id="2e2d9-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2e2d9-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="2e2d9-113">Significado</span><span class="sxs-lookup"><span data-stu-id="2e2d9-113">Meaning</span></span>                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="2e2d9-114"><dt>**MCSC \_ plano de fundo**</dt></span><span class="sxs-lookup"><span data-stu-id="2e2d9-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="2e2d9-115">Defina a cor do plano de fundo exibida entre meses.</span><span class="sxs-lookup"><span data-stu-id="2e2d9-115">Set the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="2e2d9-116"><dt>**MCSC \_ MONTHBK**</dt></span><span class="sxs-lookup"><span data-stu-id="2e2d9-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="2e2d9-117">Defina a cor do plano de fundo exibida no mês.</span><span class="sxs-lookup"><span data-stu-id="2e2d9-117">Set the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="2e2d9-118"><dt>**\_texto MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="2e2d9-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="2e2d9-119">Defina a cor usada para exibir o texto em um mês.</span><span class="sxs-lookup"><span data-stu-id="2e2d9-119">Set the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="2e2d9-120"><dt>**MCSC \_ TITLEBK**</dt></span><span class="sxs-lookup"><span data-stu-id="2e2d9-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="2e2d9-121">Defina a cor do plano de fundo exibida no título do calendário.</span><span class="sxs-lookup"><span data-stu-id="2e2d9-121">Set the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="2e2d9-122"><dt>**MCSC \_ TITLETEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="2e2d9-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="2e2d9-123">Defina a cor usada para exibir texto dentro do título do calendário.</span><span class="sxs-lookup"><span data-stu-id="2e2d9-123">Set the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="2e2d9-124"><dt>**MCSC \_ TRAILINGTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="2e2d9-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="2e2d9-125">Defina a cor usada para exibir o dia do cabeçalho e o texto do dia final.</span><span class="sxs-lookup"><span data-stu-id="2e2d9-125">Set the color used to display header day and trailing day text.</span></span> <span data-ttu-id="2e2d9-126">Os dias de cabeçalho e à direita são os dias dos meses anteriores e seguintes que aparecem no calendário do mês atual.</span><span class="sxs-lookup"><span data-stu-id="2e2d9-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2e2d9-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e2d9-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e2d9-128">Um valor de **COLORREF** que representa a cor que será definida para a área especificada do calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="2e2d9-128">A **COLORREF** value representing the color that will be set for the specified area of the month calendar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e2d9-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e2d9-129">Return value</span></span>

<span data-ttu-id="2e2d9-130">Retorna um valor **COLORREF** que representa a configuração de cor anterior para a parte especificada do controle de calendário mensal se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2e2d9-130">Returns a **COLORREF** value that represents the previous color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="2e2d9-131">Caso contrário, a mensagem retornará-1.</span><span class="sxs-lookup"><span data-stu-id="2e2d9-131">Otherwise, the message returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e2d9-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e2d9-132">Remarks</span></span>

<span data-ttu-id="2e2d9-133">Quando os estilos visuais são habilitados, essa mensagem não tem nenhum efeito, exceto quando *wParam* é MCSC \_ plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="2e2d9-133">When visual styles are enabled, this message has no effect except when *wParam* is MCSC\_BACKGROUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e2d9-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e2d9-134">Requirements</span></span>



| <span data-ttu-id="2e2d9-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e2d9-135">Requirement</span></span> | <span data-ttu-id="2e2d9-136">Valor</span><span class="sxs-lookup"><span data-stu-id="2e2d9-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2d9-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e2d9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2e2d9-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e2d9-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e2d9-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e2d9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2e2d9-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e2d9-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e2d9-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e2d9-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e2d9-142"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e2d9-142"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





