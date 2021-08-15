---
title: Elemento NetworkSettings (settingsType)
description: Contém as configurações que o serviço Agendador de Tarefas usa para obter um perfil de rede. O Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento RunOnlyIfNetworkAvailable está definido como True.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- Elemento NetworkSettings Agendador de Tarefas
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b81e1ff2a9f03646d124f5fd2d3aae27f18069f4b32631f9f8d9e66a193ac3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758476"
---
# <a name="networksettings-settingstype-element"></a>Elemento NetworkSettings (settingsType)

Contém as configurações que o serviço Agendador de Tarefas usa para obter um perfil de rede. O Agendador de Tarefas serviço verifica a disponibilidade dessa rede quando o [**elemento RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está definido como **True.**

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

O **elemento NetworkSettings** é definido pelo tipo complexo [**settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                      | Derivado de                                                         | Descrição                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Configurações (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**Propriedade NetworkSettings de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).

Para desenvolvimento de scripts, [**consulte TaskSettings.NetworkSettings**](tasksettings-networksettings.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





