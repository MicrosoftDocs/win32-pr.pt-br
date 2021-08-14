---
title: Elemento Name (networkSettingsType)
description: Contém o nome de um perfil de rede. O nome é usado para fins de exibição.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Nome do elemento Agendador de Tarefas
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41b92c7e63a820c2a2a34378b041bec3a49f432b52887a732c3f3bfd360b10f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758496"
---
# <a name="name-networksettingstype-element"></a>Elemento Name (networkSettingsType)

Contém o nome de um perfil de rede. O nome é usado para fins de exibição.

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

O **elemento Name** é definido pelo tipo complexo [**networkSettingsType.**](taskschedulerschema-networksettingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                            | Derivado de                                                                       | Descrição                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contém as configurações que o serviço Agendador de Tarefas usa para obter um perfil de rede. O Agendador de Tarefas serviço verifica a disponibilidade dessa rede quando o [**elemento RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está definido como **True.**<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**Propriedade name de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).

Para desenvolvimento de scripts, [**consulte NetworkSettings.Name**](networksettings-name.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





