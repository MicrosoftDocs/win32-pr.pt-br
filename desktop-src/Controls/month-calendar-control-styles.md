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
# <a name="month-calendar-control-styles"></a>Estilos de controle de calendário mensal

As constantes de estilo a seguir são usadas ao criar controles de calendário de mês.



| Constante                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <dt>**MCS \_ DAYSTATE**</dt> </dl>                         | [Versão 4,70](common-control-versions.md). O calendário mensal envia notificações [MCN \_ GETDAYSTATE](mcn-getdaystate.md) para solicitar informações sobre quais dias devem ser exibidos em negrito.<br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <dt>**multiseleção MCS \_**</dt> </dl>                | [Versão 4,70](common-control-versions.md). O calendário mensal permite que o usuário selecione um intervalo de datas dentro do controle. Por padrão, o intervalo máximo é de uma semana. Você pode alterar o intervalo máximo que pode ser selecionado usando a mensagem [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) . <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <dt>**MCS \_ WEEKNUMBERS**</dt> </dl>                | [Versão 4,70](common-control-versions.md). O controle de calendário mensal exibe os números das semanas (1-52) à esquerda de cada linha de dias. A semana 1 é definida como a primeira semana que contém pelo menos quatro dias. <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <dt>**MCS \_ NOTODAYCIRCLE**</dt> </dl>          | [Versão 4,70](common-control-versions.md). O controle de calendário mensal não circula a data "hoje". <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <dt>**MCS \_ NOhoje**</dt> </dl>                            | [Versão 4,70](common-control-versions.md). O controle de calendário mensal não exibe a data "hoje" na parte inferior do controle. <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <dt>**MCS \_ NOTRAILINGDATES**</dt> </dl>    | **Windows Vista.** As datas dos meses anteriores e posteriores não são exibidas no calendário do mês atual.<br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <dt>**MCS \_ SHORTDAYSOFWEEK**</dt> </dl>    | **Windows Vista.** Nomes de dia curto são exibidos no cabeçalho.<br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <dt>**MCS \_ NOSELCHANGEONNAV**</dt> </dl> | **Windows Vista.** A seleção não é alterada quando o usuário navega em próximo ou anterior no calendário. Isso permite que o usuário selecione um intervalo maior que o que está visível.<br/>                                                                                                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





