---
title: Mensagem de MCM_HITTEST (commctrl. h)
description: Determina qual parte de um controle de calendário mensal está em um determinado ponto na tela. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ HitTest.
ms.assetid: 51e74b07-4ed7-488d-ad5d-116f046577fc
keywords:
- controles de Windows de mensagem de MCM_HITTEST
topic_type:
- apiref
api_name:
- MCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab43ae76a2e747ff019a5bafa32870a208851a143ad94dd0679e894366c3592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697186"
---
# <a name="mcm_hittest-message"></a>\_Mensagem MCM HITTEST

Determina qual parte de um controle de calendário mensal está em um determinado ponto na tela. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_hittest) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) . Ao enviar a mensagem, o membro **cbSize** deve ser definido como o tamanho da estrutura **MCHITTESTINFO** e o **pt** deve ser definido como o ponto que você deseja testar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Define valores em membros do



| Código de retorno                                                                                           | Descrição                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**calendário do MCHT \_**</dt> </dl>         | O ponto determinado estava dentro do calendário.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**MCHT \_ CALENDARBK**</dt> </dl>       | O ponto determinado estava no plano de fundo do calendário.<br/>                                                                                                                                                                                                              |
| <dl> <dt>**MCHT \_ CALENDARDATE**</dt> </dl>     | O ponto determinado estava em uma determinada data dentro do calendário. A estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) em *lParam->St* é definida como a data no ponto determinado.<br/>                                                                                    |
| <dl> <dt>**MCHT \_ CALENDARDATENEXT**</dt> </dl> | O ponto determinado estava acima de uma data do mês seguinte (parcialmente exibido no final do mês exibido no momento). Se o usuário clicar aqui, o calendário mensal rolará sua exibição para o próximo mês ou conjunto de meses.<br/>                                 |
| <dl> <dt>**MCHT \_ CALENDARDATEPREV**</dt> </dl> | O ponto determinado estava acima de uma data do mês anterior (parcialmente exibido no final do mês exibido no momento). Se o usuário clicar aqui, o calendário mensal rolará sua exibição para o mês anterior ou para o conjunto de meses.<br/>                         |
| <dl> <dt>**MCHT \_ CALENDARDAY**</dt> </dl>      | O ponto determinado foi uma abreviação de dia ("sexta-feira", por exemplo). A estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) em *lParam->St* é definida como a data correspondente na linha superior.<br/>                                                                      |
| <dl> <dt>**MCHT \_ CALENDARWEEKNUM**</dt> </dl>  | O ponto determinado foi um número de semana (apenas em estilo [**MCS \_ WEEKNUMBERS**](month-calendar-control-styles.md) ). A estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) em *lParam->St* é definida como a data correspondente na coluna mais à esquerda.<br/> |
| <dl> <dt>**MCHT \_ próximo**</dt> </dl>             | O ponto determinado está em uma área que fará com que o calendário mensal role sua exibição para o próximo mês ou conjunto de meses. Esse sinalizador é usado para modificar outros sinalizadores de teste de clique.<br/>                                                                                   |
| <dl> <dt>**MCHT em qualquer \_ lugar**</dt> </dl>          | O ponto determinado não estava no controle de calendário mensal ou estava em uma parte inativa do controle.<br/>                                                                                                                                                        |
| <dl> <dt>**MCHT \_ anterior**</dt> </dl>             | O ponto determinado está em uma área que fará com que o calendário mensal role sua exibição para o mês anterior ou para o conjunto de meses. Esse sinalizador é usado para modificar outros sinalizadores de teste de clique.<br/>                                                                               |
| <dl> <dt>**título do MCHT \_**</dt> </dl>            | O ponto determinado estava acima do título de um mês.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**MCHT \_ TITLEBK**</dt> </dl>          | O ponto determinado foi sobre o plano de fundo do título de um mês.<br/>                                                                                                                                                                                                    |
| <dl> <dt>**MCHT \_ TITLEBTNNEXT**</dt> </dl>     | O ponto determinado estava sobre o botão no canto superior direito do controle. Se o usuário clicar aqui, o calendário mensal rolará sua exibição para o próximo mês ou conjunto de meses. <br/>                                                                           |
| <dl> <dt>**MCHT \_ TITLEBTNPREV**</dt> </dl>     | O ponto determinado estava sobre o botão no canto superior esquerdo do controle. Se o usuário clicar aqui, o calendário mensal rolará sua exibição para o mês anterior ou para o conjunto de meses. <br/>                                                                        |
| <dl> <dt>**MCHT \_ TITLEMONTH**</dt> </dl>       | O ponto determinado estava na barra de título de um mês, em um nome de mês.<br/>                                                                                                                                                                                                 |
| <dl> <dt>**MCHT \_ TITLEYEAR**</dt> </dl>        | O ponto determinado estava na barra de título de um mês, ao longo do valor year.<br/>                                                                                                                                                                                               |
| <dl> <dt>**MCHT \_ TODAYLINK**</dt> </dl>        | O ponto determinado estava no link "hoje" na parte inferior do controle de calendário mensal.<br/> O membro **uHit** da estrutura [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) em *lParam* será igual ao valor de retorno. <br/>                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

