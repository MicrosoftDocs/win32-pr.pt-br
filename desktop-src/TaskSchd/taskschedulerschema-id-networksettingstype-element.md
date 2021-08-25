---
title: Elemento ID (networkSettingsType)
description: Contém um valor guid que identifica um perfil de rede.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Elemento Id Agendador de Tarefas
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06196710b9db9d39d45a24b78bccabf479ef210a97f3cea1fd19286b76f2fc42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125836"
---
# <a name="id-networksettingstype-element"></a>Elemento ID (networkSettingsType)

Contém um valor guid que identifica um perfil de rede.

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

O **elemento Id** é definido pelo [**tipo complexo networkSettingsType.**](taskschedulerschema-networksettingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                            | Derivado de                                                                       | Descrição                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contém as configurações que o serviço Agendador de Tarefas usa para obter um perfil de rede. O Agendador de Tarefas serviço verifica a disponibilidade dessa rede quando o [**elemento RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está definido como **True.**<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**Propriedade de ID de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).

Para desenvolvimento de script, [**consulte NetworkSettings.Id**](networksettings-id.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





