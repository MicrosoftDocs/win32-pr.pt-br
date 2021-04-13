---
title: Mensagem de DTM_GETMCCOLOR (commctrl. h)
description: Obtém a cor de uma determinada parte do calendário mensal dentro de um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a \_ macro DateTime GetMonthCalColor.
ms.assetid: 892e8c23-f0d0-4fd6-98ed-39592c4d316f
keywords:
- Controles de DTM_GETMCCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_GETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690c461c5bccbd050fb3d698d1a41c6d1e513944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456059"
---
# <a name="dtm_getmccolor-message"></a><span data-ttu-id="d7a5e-105">\_Mensagem DTM GETMCCOLOR</span><span class="sxs-lookup"><span data-stu-id="d7a5e-105">DTM\_GETMCCOLOR message</span></span>

<span data-ttu-id="d7a5e-106">Obtém a cor de uma determinada parte do calendário mensal dentro de um controle do seletor de data e hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="d7a5e-106">Gets the color for a given portion of the month calendar within a date and time picker (DTP) control.</span></span> <span data-ttu-id="d7a5e-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) .</span><span class="sxs-lookup"><span data-stu-id="d7a5e-107">You can send this message explicitly or use the [**DateTime\_GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7a5e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7a5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7a5e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7a5e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7a5e-110">Um valor do tipo **int** que especifica qual cor de calendário de mês deve ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-110">A value of type **int** specifying which month calendar color to retrieve.</span></span> <span data-ttu-id="d7a5e-111">Este valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d7a5e-111">This value can be one of the following:</span></span>



| <span data-ttu-id="d7a5e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d7a5e-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="d7a5e-113">Significado</span><span class="sxs-lookup"><span data-stu-id="d7a5e-113">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="d7a5e-114"><dt>**MCSC \_ plano de fundo**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a5e-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="d7a5e-115">Recupere a cor de plano de fundo exibida entre meses.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-115">Retrieve the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="d7a5e-116"><dt>**MCSC \_ MONTHBK**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a5e-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="d7a5e-117">Recupere a cor do plano de fundo exibida no mês.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-117">Retrieve the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="d7a5e-118"><dt>**\_texto MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a5e-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="d7a5e-119">Recupere a cor usada para exibir o texto em um mês.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-119">Retrieve the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="d7a5e-120"><dt>**MCSC \_ TITLEBK**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a5e-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="d7a5e-121">Recupere a cor do plano de fundo exibida no título do calendário.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-121">Retrieve the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="d7a5e-122"><dt>**MCSC \_ TITLETEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a5e-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="d7a5e-123">Recupere a cor usada para exibir texto dentro do título do calendário.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-123">Retrieve the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="d7a5e-124"><dt>**MCSC \_ TRAILINGTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a5e-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="d7a5e-125">Recupere a cor usada para exibir o dia do cabeçalho e o texto do dia final.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-125">Retrieve the color used to display header day and trailing day text.</span></span> <span data-ttu-id="d7a5e-126">Os dias de cabeçalho e à direita são os dias dos meses anteriores e seguintes que aparecem no calendário do mês atual.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d7a5e-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7a5e-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d7a5e-128">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7a5e-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7a5e-129">Return value</span></span>

<span data-ttu-id="d7a5e-130">Retorna um valor **COLORREF** que representa a configuração de cor para a parte especificada do controle de calendário mensal se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-130">Returns a **COLORREF** value that represents the color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="d7a5e-131">A mensagem retornará-1 se não for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-131">The message returns -1 if unsuccessful.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7a5e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7a5e-132">Requirements</span></span>



| <span data-ttu-id="d7a5e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7a5e-133">Requirement</span></span> | <span data-ttu-id="d7a5e-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d7a5e-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a5e-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7a5e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a5e-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7a5e-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7a5e-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7a5e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a5e-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7a5e-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7a5e-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7a5e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7a5e-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a5e-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





