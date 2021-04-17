---
title: Elemento Name (networkSettingsType)
description: Contém o nome de um perfil de rede. O nome é usado para fins de exibição.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Elemento Name Agendador de Tarefas
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed877b731b64ee8f2d807067b59399decc0eefe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499472"
---
# <a name="name-networksettingstype-element"></a>Elemento Name (networkSettingsType)

Contém o nome de um perfil de rede. O nome é usado para fins de exibição.

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

O elemento **Name** é definido pelo tipo complexo [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                            | Derivado de                                                                       | Descrição                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingstype)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contém as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede. O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) é definido como **true**.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade Name de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).

Para o desenvolvimento de scripts, consulte [**NetworkSettings.Name**](networksettings-name.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





