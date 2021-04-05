---
title: Elemento Delay (bootTriggerType)
description: Especifica a quantidade de tempo entre quando o sistema é inicializado e quando a tarefa é iniciada.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
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
ms.openlocfilehash: 1ab28da8e9c739d3deff52572fe6a5d37f862119
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919186"
---
# <a name="delay-boottriggertype-element"></a>Elemento Delay (bootTriggerType)

Especifica a quantidade de tempo entre quando o sistema é inicializado e quando a tarefa é iniciada. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

O elemento **Delay** é definido pelo tipo complexo [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                     | Derivado de                                                               | Descrição                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de script, o atraso do gatilho de evento é especificado pela propriedade [**BootTrigger. Delay**](boottrigger-delay.md) .

Para desenvolvimento em C++, o atraso do gatilho de evento é especificado pela propriedade [**IBootTrigger::D epetição**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





