---
title: Mensagem de MCM_SETCOLOR (commctrl. h)
description: Define a cor de uma determinada parte de um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a \_ macro setColor calendário mensal.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- Controles de MCM_SETCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476aafd8356359cf6b4313f4b945253af6b493c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086325"
---
# <a name="mcm_setcolor-message"></a><span data-ttu-id="8ccef-105">MCM \_ mensagem SETcolor</span><span class="sxs-lookup"><span data-stu-id="8ccef-105">MCM\_SETCOLOR message</span></span>

<span data-ttu-id="8ccef-106">Define a cor de uma determinada parte de um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="8ccef-106">Sets the color for a given portion of a month calendar control.</span></span> <span data-ttu-id="8ccef-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setColor calendário mensal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) .</span><span class="sxs-lookup"><span data-stu-id="8ccef-107">You can send this message explicitly or by using the [**MonthCal\_SetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ccef-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ccef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ccef-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ccef-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ccef-110">Valor do tipo **int** especificando qual cor de calendário de mês definir.</span><span class="sxs-lookup"><span data-stu-id="8ccef-110">Value of type **int** specifying which month calendar color to set.</span></span> <span data-ttu-id="8ccef-111">Este valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="8ccef-111">This value can be one of the following:</span></span>



| <span data-ttu-id="8ccef-112">Valor</span><span class="sxs-lookup"><span data-stu-id="8ccef-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="8ccef-113">Significado</span><span class="sxs-lookup"><span data-stu-id="8ccef-113">Meaning</span></span>                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="8ccef-114"><dt>**MCSC \_ plano de fundo**</dt></span><span class="sxs-lookup"><span data-stu-id="8ccef-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="8ccef-115">Defina a cor do plano de fundo exibida entre meses.</span><span class="sxs-lookup"><span data-stu-id="8ccef-115">Set the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="8ccef-116"><dt>**MCSC \_ MONTHBK**</dt></span><span class="sxs-lookup"><span data-stu-id="8ccef-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="8ccef-117">Defina a cor do plano de fundo exibida no mês.</span><span class="sxs-lookup"><span data-stu-id="8ccef-117">Set the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="8ccef-118"><dt>**\_texto MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="8ccef-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="8ccef-119">Defina a cor usada para exibir o texto em um mês.</span><span class="sxs-lookup"><span data-stu-id="8ccef-119">Set the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="8ccef-120"><dt>**MCSC \_ TITLEBK**</dt></span><span class="sxs-lookup"><span data-stu-id="8ccef-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="8ccef-121">Defina a cor do plano de fundo exibida no título do calendário.</span><span class="sxs-lookup"><span data-stu-id="8ccef-121">Set the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="8ccef-122"><dt>**MCSC \_ TITLETEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="8ccef-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="8ccef-123">Defina a cor usada para exibir texto dentro do título do calendário.</span><span class="sxs-lookup"><span data-stu-id="8ccef-123">Set the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="8ccef-124"><dt>**MCSC \_ TRAILINGTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="8ccef-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="8ccef-125">Defina a cor usada para exibir o dia do cabeçalho e o texto do dia final.</span><span class="sxs-lookup"><span data-stu-id="8ccef-125">Set the color used to display header day and trailing day text.</span></span> <span data-ttu-id="8ccef-126">Os dias de cabeçalho e à direita são os dias dos meses anteriores e seguintes que aparecem no calendário do mês atual.</span><span class="sxs-lookup"><span data-stu-id="8ccef-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ccef-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ccef-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ccef-128">Valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a cor que será definida para a área especificada do calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="8ccef-128">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the color that will be set for the specified area of the month calendar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ccef-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ccef-129">Return value</span></span>

<span data-ttu-id="8ccef-130">Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a configuração de cor anterior para a parte especificada do controle de calendário mensal se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8ccef-130">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="8ccef-131">Caso contrário, o retorno será-1.</span><span class="sxs-lookup"><span data-stu-id="8ccef-131">Otherwise, the return is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ccef-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ccef-132">Remarks</span></span>

<span data-ttu-id="8ccef-133">Se os estilos visuais estiverem ativos, essa mensagem não terá efeito, exceto quando *wParam* for MCSC \_ background.</span><span class="sxs-lookup"><span data-stu-id="8ccef-133">If visual styles are active, this message has no effect except when *wParam* is MCSC\_BACKGROUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ccef-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ccef-134">Requirements</span></span>



| <span data-ttu-id="8ccef-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ccef-135">Requirement</span></span> | <span data-ttu-id="8ccef-136">Valor</span><span class="sxs-lookup"><span data-stu-id="8ccef-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ccef-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ccef-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8ccef-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ccef-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ccef-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ccef-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8ccef-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8ccef-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ccef-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ccef-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ccef-142"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ccef-142"><dt>Commctrl.h</dt></span></span> </dl> |



 

