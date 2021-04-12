---
title: Elemento NetworkSettings (settingstype)
description: Contém as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede. O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento RunOnlyIfNetworkAvailable é definido como true.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- Agendador de Tarefas do elemento NetworkSettings
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7861d91cbc2647d241bc41753efbebcc346759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455395"
---
# <a name="networksettings-settingstype-element"></a>Elemento NetworkSettings (settingstype)

Contém as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede. O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) é definido como **true**.

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

O elemento **NetworkSettings** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                      | Derivado de                                                         | Descrição                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Configurações (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade NetworkSettings de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).

Para desenvolvimento de script, consulte [**TaskSettings. NetworkSettings**](tasksettings-networksettings.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





