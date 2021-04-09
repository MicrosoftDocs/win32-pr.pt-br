---
title: Elemento ID (networkSettingsType)
description: Contém um valor de GUID que identifica um perfil de rede.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Elemento de ID Agendador de Tarefas
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d14865d50e9c3418e3ef65cdbeaea747a98a4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086452"
---
# <a name="id-networksettingstype-element"></a>Elemento ID (networkSettingsType)

Contém um valor de GUID que identifica um perfil de rede.

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

O elemento **ID** é definido pelo tipo complexo [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                            | Derivado de                                                                       | Descrição                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingstype)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contém as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede. O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) é definido como **true**.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade ID de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).

Para o desenvolvimento de scripts, consulte [**NetworkSettings.ID**](networksettings-id.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





