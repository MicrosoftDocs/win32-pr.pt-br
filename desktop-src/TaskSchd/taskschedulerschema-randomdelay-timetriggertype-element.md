---
title: Elemento RandomDelay (timeTriggerType)
description: Contém o tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. | Elemento RandomDelay (timeTriggerType)
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
keywords:
- Elemento RandomDelay Agendador de Tarefas
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c4c9fde8a0f88ed7e87b5a0d3ccc252f141f6b677f535adf853ef0aca9499b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611499"
---
# <a name="randomdelay-timetriggertype-element"></a>Elemento RandomDelay (timeTriggerType)

Contém o tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, em que nY é o número de anos, nM é o número de meses, nD é o número de dias, 'T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

O elemento é definido pelo tipo [**complexo timeTriggerType.**](taskschedulerschema-timetriggertype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                    | Derivado de                                                               | Descrição                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**TimeTrigger (triggerGroup)**](taskschedulerschema-timetrigger-triggergroup-element.md) | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**Propriedade RandomDelay de ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).

Para desenvolvimento de scripts, [**consulte TimeTrigger.RandomDelay**](timetrigger-randomdelay.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





