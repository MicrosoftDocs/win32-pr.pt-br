---
title: Elemento ExecutionTimeLimit (settingsType)
description: Tempo permitido para concluir a tarefa.
ms.assetid: c42d0f42-4571-44ab-90b1-948fd7ea991b
keywords:
- Elemento ExecutionTimeLimit Agendador de Tarefas
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f6519495cc16cdff6a30c65f75468bd676ca1f2750faedb5c632972c1affb996
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356412"
---
# <a name="executiontimelimit-settingstype-element"></a>Elemento ExecutionTimeLimit (settingsType)

Tempo permitido para concluir a tarefa. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, em que nY é o número de anos, nM é o número de meses, nD é o número de dias, 'T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> . Um valor de PT0S permitirá que a tarefa seja executado indefinidamente.

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
    minOccurs="0"
 />
```

O **elemento ExecutionTimeLimit** é definido pelo tipo complexo [**settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**Propriedade ExecutionTimeLimit de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).

Para desenvolvimento de scripts, [**consulteTaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





