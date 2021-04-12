---
title: Elemento RandomDelay (calendarTriggerType)
description: Contém o tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. | Elemento RandomDelay (calendarTriggerType)
ms.assetid: 497fab4e-ad63-43e6-a086-2d77b43662d9
keywords:
- Agendador de Tarefas do elemento RandomDelay
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d71149bfeceeb6c17cafa27f56bb15bb184ead06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298325"
---
# <a name="randomdelay-calendartriggertype-element"></a>Elemento RandomDelay (calendarTriggerType)

Contém o tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

O elemento **RandomDelay** é definido pelo tipo complexo [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                            | Derivado de                                                                       | Descrição                                                                                 |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**CalendarTrigger (The Trigger)**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





