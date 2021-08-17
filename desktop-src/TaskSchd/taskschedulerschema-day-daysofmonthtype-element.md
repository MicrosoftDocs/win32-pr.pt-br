---
title: Elemento Day (daysOfMonthType)
description: Especifica um dia do mês durante o qual a tarefa é executada.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Agendador de Tarefas de elemento Day
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c238ee5bd873c33f3acd2207ba9ad31869b151924dd20f082669b782d207c59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857949"
---
# <a name="day-daysofmonthtype-element"></a>Elemento Day (daysOfMonthType)

Especifica um dia do mês durante o qual a tarefa é executada.

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

O elemento **Day** é definido pelo tipo complexo [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                            | Derivado de                                                               | Descrição                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Especifica os dias do mês durante os quais a tarefa é executada.<br/> |



## <a name="examples"></a>Exemplos

O XML a seguir define a parte de dias de um calendário mensal que executa a tarefa no 1º e no 15º dia do mês.


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





