---
title: Elemento Delay (logonTriggerType)
description: Quantidade de tempo entre quando o usuário faz logo on e quando a tarefa é iniciada.
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
keywords:
- Elemento Delay Agendador de Tarefas
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1bd18652630ad14f9b888db6a810d8da1eb42a18fb9d2caa6726414aa9054702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357124"
---
# <a name="delay-logontriggertype-element"></a>Elemento Delay (logonTriggerType)

Quantidade de tempo entre quando o usuário faz logo on e quando a tarefa é iniciada. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, em que nY é o número de anos, nM é o número de meses, nD é o número de dias, 'T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

O **elemento Delay** é definido pelo tipo complexo [**logonTriggerType.**](taskschedulerschema-logontriggertype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                       | Derivado de                                                                 | Descrição                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando um usuário faz login.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, o atraso do gatilho de logon é especificado usando a [**propriedade LogonTrigger.Delay.**](logontrigger-delay.md)

Para desenvolvimento em C++, o identificador de usuário para o gatilho de logon é especificado usando a [**propriedade ILogonTrigger::D elay.**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





