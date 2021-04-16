---
title: Estilos de controle de calendário mensal (CommCtrl. h)
description: As constantes de estilo a seguir são usadas ao criar controles de calendário de mês.
ms.assetid: 8d9b2239-fd13-4579-81a2-0385fd318e83
topic_type:
- apiref
api_name:
- MCS_DAYSTATE
- MCS_MULTISELECT
- MCS_WEEKNUMBERS
- MCS_NOTODAYCIRCLE
- MCS_NOTODAY
- MCS_NOTRAILINGDATES
- MCS_SHORTDAYSOFWEEK
- MCS_NOSELCHANGEONNAV
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ccef4a3cc8e16851c0676b8b0dce8c53cfdd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751150"
---
# <a name="month-calendar-control-styles"></a><span data-ttu-id="5c732-103">Estilos de controle de calendário mensal</span><span class="sxs-lookup"><span data-stu-id="5c732-103">Month Calendar Control Styles</span></span>

<span data-ttu-id="5c732-104">As constantes de estilo a seguir são usadas ao criar controles de calendário de mês.</span><span class="sxs-lookup"><span data-stu-id="5c732-104">The following style constants are used when creating month calendar controls.</span></span>



| <span data-ttu-id="5c732-105">Constante</span><span class="sxs-lookup"><span data-stu-id="5c732-105">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="5c732-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c732-106">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <span data-ttu-id="5c732-107"><dt>**MCS \_ DAYSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="5c732-107"><dt>**MCS\_DAYSTATE**</dt></span></span> </dl>                         | <span data-ttu-id="5c732-108">[Versão 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="5c732-108">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="5c732-109">O calendário mensal envia notificações [MCN \_ GETDAYSTATE](mcn-getdaystate.md) para solicitar informações sobre quais dias devem ser exibidos em negrito.</span><span class="sxs-lookup"><span data-stu-id="5c732-109">The month calendar sends [MCN\_GETDAYSTATE](mcn-getdaystate.md) notifications to request information about which days should be displayed in bold.</span></span><br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <span data-ttu-id="5c732-110"><dt>**multiseleção MCS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c732-110"><dt>**MCS\_MULTISELECT**</dt></span></span> </dl>                | <span data-ttu-id="5c732-111">[Versão 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="5c732-111">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="5c732-112">O calendário mensal permite que o usuário selecione um intervalo de datas dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="5c732-112">The month calendar enables the user to select a range of dates within the control.</span></span> <span data-ttu-id="5c732-113">Por padrão, o intervalo máximo é de uma semana.</span><span class="sxs-lookup"><span data-stu-id="5c732-113">By default, the maximum range is one week.</span></span> <span data-ttu-id="5c732-114">Você pode alterar o intervalo máximo que pode ser selecionado usando a mensagem [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) .</span><span class="sxs-lookup"><span data-stu-id="5c732-114">You can change the maximum range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span> <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <span data-ttu-id="5c732-115"><dt>**MCS \_ WEEKNUMBERS**</dt></span><span class="sxs-lookup"><span data-stu-id="5c732-115"><dt>**MCS\_WEEKNUMBERS**</dt></span></span> </dl>                | <span data-ttu-id="5c732-116">[Versão 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="5c732-116">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="5c732-117">O controle de calendário mensal exibe os números das semanas (1-52) à esquerda de cada linha de dias.</span><span class="sxs-lookup"><span data-stu-id="5c732-117">The month calendar control displays week numbers (1-52) to the left of each row of days.</span></span> <span data-ttu-id="5c732-118">A semana 1 é definida como a primeira semana que contém pelo menos quatro dias.</span><span class="sxs-lookup"><span data-stu-id="5c732-118">Week 1 is defined as the first week that contains at least four days.</span></span> <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <span data-ttu-id="5c732-119"><dt>**MCS \_ NOTODAYCIRCLE**</dt></span><span class="sxs-lookup"><span data-stu-id="5c732-119"><dt>**MCS\_NOTODAYCIRCLE**</dt></span></span> </dl>          | <span data-ttu-id="5c732-120">[Versão 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="5c732-120">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="5c732-121">O controle de calendário mensal não circula a data "hoje".</span><span class="sxs-lookup"><span data-stu-id="5c732-121">The month calendar control does not circle the "today" date.</span></span> <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <span data-ttu-id="5c732-122"><dt>**MCS \_ NOhoje**</dt></span><span class="sxs-lookup"><span data-stu-id="5c732-122"><dt>**MCS\_NOTODAY**</dt></span></span> </dl>                            | <span data-ttu-id="5c732-123">[Versão 4,70](common-control-versions.md). O controle de calendário mensal não exibe a data "hoje" na parte inferior do controle.</span><span class="sxs-lookup"><span data-stu-id="5c732-123">[Version 4.70](common-control-versions.md).The month calendar control does not display the "today" date at the bottom of the control.</span></span> <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <span data-ttu-id="5c732-124"><dt>**MCS \_ NOTRAILINGDATES**</dt></span><span class="sxs-lookup"><span data-stu-id="5c732-124"><dt>**MCS\_NOTRAILINGDATES**</dt></span></span> </dl>    | <span data-ttu-id="5c732-125">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="5c732-125">**Windows Vista.**</span></span> <span data-ttu-id="5c732-126">As datas dos meses anteriores e posteriores não são exibidas no calendário do mês atual.</span><span class="sxs-lookup"><span data-stu-id="5c732-126">Dates from the previous and next months are not displayed in the current month's calendar.</span></span><br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <span data-ttu-id="5c732-127"><dt>**MCS \_ SHORTDAYSOFWEEK**</dt></span><span class="sxs-lookup"><span data-stu-id="5c732-127"><dt>**MCS\_SHORTDAYSOFWEEK**</dt></span></span> </dl>    | <span data-ttu-id="5c732-128">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="5c732-128">**Windows Vista.**</span></span> <span data-ttu-id="5c732-129">Nomes de dia curto são exibidos no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="5c732-129">Short day names are displayed in the header.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <span data-ttu-id="5c732-130"><dt>**MCS \_ NOSELCHANGEONNAV**</dt></span><span class="sxs-lookup"><span data-stu-id="5c732-130"><dt>**MCS\_NOSELCHANGEONNAV**</dt></span></span> </dl> | <span data-ttu-id="5c732-131">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="5c732-131">**Windows Vista.**</span></span> <span data-ttu-id="5c732-132">A seleção não é alterada quando o usuário navega em próximo ou anterior no calendário.</span><span class="sxs-lookup"><span data-stu-id="5c732-132">The selection is not changed when the user navigates next or previous in the calendar.</span></span> <span data-ttu-id="5c732-133">Isso permite que o usuário selecione um intervalo maior que o que está visível.</span><span class="sxs-lookup"><span data-stu-id="5c732-133">This allows the user to select a range larger than is visible.</span></span><br/>                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="5c732-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c732-134">Requirements</span></span>



| <span data-ttu-id="5c732-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c732-135">Requirement</span></span> | <span data-ttu-id="5c732-136">Valor</span><span class="sxs-lookup"><span data-stu-id="5c732-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c732-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c732-137">Header</span></span><br/> | <dl> <span data-ttu-id="5c732-138"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c732-138"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





