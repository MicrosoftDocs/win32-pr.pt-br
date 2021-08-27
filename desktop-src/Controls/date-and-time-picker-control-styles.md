---
title: Estilos de controle do seletor de data e hora (CommCtrl. h)
description: Os estilos de janela listados aqui são específicos dos controles de seletor de data e hora.
ms.assetid: d3b95521-75ef-4cca-b801-94c6f749aa47
topic_type:
- apiref
api_name:
- DTS_APPCANPARSE
- DTS_LONGDATEFORMAT
- DTS_RIGHTALIGN
- DTS_SHOWNONE
- DTS_SHORTDATEFORMAT
- DTS_SHORTDATECENTURYFORMAT
- DTS_TIMEFORMAT
- DTS_UPDOWN
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f9740e0de413649b67cc8231d31425d212d2571dbc9a1b703f9f95c35e4981
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085756"
---
# <a name="date-and-time-picker-control-styles"></a>Estilos de controle do seletor de data e hora

Os estilos de janela listados aqui são específicos dos controles de seletor de data e hora.



| Constante                                                                                                                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DTS_APPCANPARSE"></span><span id="dts_appcanparse"></span><dl> <dt>**\_APPCANPARSE Dts**</dt> </dl>                                  | Permite que o proprietário analise a entrada do usuário e execute a ação necessária. Ele permite que os usuários editem dentro da área do cliente do controle quando eles pressionam a tecla F2. O controle envia os códigos de notificação [DTN \_ userstring](dtn-userstring.md) quando os usuários são concluídos.<br/>                                                                                                                                                                                                                                                                    |
| <span id="DTS_LONGDATEFORMAT"></span><span id="dts_longdateformat"></span><dl> <dt>**\_LONGDATEFORMAT Dts**</dt> </dl>                         | Exibe a data em formato longo. A cadeia de caracteres de formato padrão para esse estilo é definida pela localidade \_ SLONGDATEFORMAT, que produz uma saída como "sexta-feira, 19 de abril de 1996". Quando esse estilo é usado, o botão suspenso não exibe um ícone.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="DTS_RIGHTALIGN"></span><span id="dts_rightalign"></span><dl> <dt>**\_RIGHTALIGN Dts**</dt> </dl>                                     | O calendário do mês suspenso será alinhado à direita com o controle em vez de alinhado à esquerda, que é o padrão. <br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHOWNONE"></span><span id="dts_shownone"></span><dl> <dt>**DTS não \_ None**</dt> </dl>                                           | É possível que não haja nenhuma data atualmente selecionada no controle. Com esse estilo, o controle exibe uma caixa de seleção que é selecionada automaticamente sempre que uma data é escolhida ou inserida. Se a caixa de seleção for desmarcada subsequentemente, o aplicativo não poderá recuperar a data do controle porque, em essência, o controle não terá nenhuma data. O estado da caixa de seleção pode ser definido com a mensagem [**DTM \_ SetSystemTime**](dtm-setsystemtime.md) ou consultado com a mensagem [**DTM \_ GetSystemTime**](dtm-getsystemtime.md) .<br/> |
| <span id="DTS_SHORTDATEFORMAT"></span><span id="dts_shortdateformat"></span><dl> <dt>**\_SHORTDATEFORMAT Dts**</dt> </dl>                      | Exibe a data em formato curto. A cadeia de caracteres de formato padrão para esse estilo é definida pela localidade \_ SSHORTDATE, que produz uma saída como "4/19/96".<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHORTDATECENTURYFORMAT"></span><span id="dts_shortdatecenturyformat"></span><dl> <dt>**\_SHORTDATECENTURYFORMAT Dts**</dt> </dl> | **Versão 5,80.** Semelhante ao estilo **DTS \_ SHORTDATEFORMAT** , exceto que year é um campo de quatro dígitos. A cadeia de caracteres de formato padrão para esse estilo se baseia na localidade \_ SSHORTDATE. A saída é semelhante a: "4/19/1996".<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="DTS_TIMEFORMAT"></span><span id="dts_timeformat"></span><dl> <dt>**\_formato de timeforma Dts**</dt> </dl>                                     | Exibe a hora. A cadeia de caracteres de formato padrão para esse estilo é definida pela localidade \_ STIMEFORMAT, que produz uma saída como "5:31:42 PM".<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="DTS_UPDOWN"></span><span id="dts_updown"></span><dl> <dt>**Updown DTS \_**</dt> </dl>                                                 | Coloca um controle acima à direita do controle DTP para modificar os valores de data e hora. Esse estilo pode ser usado no lugar do calendário do mês suspenso, que é o estilo padrão.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Comentários

Os \_ estilos DTS XXXFORMAT que definem o formato de exibição não podem ser combinados. Se nenhum dos estilos de formato for adequado, use uma [**mensagem \_ SetFormat DTM**](dtm-setformat.md) para definir um formato personalizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





