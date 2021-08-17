---
title: Elemento NetworkProfileName (settingsType)
description: Contém o nome de um perfil de rede. O Agendador de Tarefas serviço verifica a disponibilidade dessa rede quando o elemento RunOnlyIfNetworkAvailable está definido como True. O nome é usado para fins de exibição.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- Elemento NetworkProfileName Agendador de Tarefas
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 464c8b8f23dfeed6ea7c3412c3eeec07f20e5a8a7fcea662b4a16dfac7cb3fb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758486"
---
# <a name="networkprofilename-settingstype-element"></a>Elemento NetworkProfileName (settingsType)

Contém o nome de um perfil de rede. O Agendador de Tarefas serviço verifica a disponibilidade dessa rede quando o [**elemento RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está definido como **True.** O nome é usado para fins de exibição.

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

O **elemento NetworkProfileName** é definido pelo tipo complexo [**settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                      | Derivado de                                                         | Descrição                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Configurações (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





