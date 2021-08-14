---
title: tipo complexo networkSettingsType
description: Define os elementos que fornecem as configurações que o serviço Agendador de Tarefas usa para obter um perfil de rede.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- tipo complexo networkSettingsType Agendador de Tarefas
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9969e4e3827d926d8c295d4e1a3ce7b77550804eb4995a267a920a16871837f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758466"
---
# <a name="networksettingstype-complex-type"></a>tipo complexo networkSettingsType

Define os elementos que fornecem as configurações que o serviço Agendador de Tarefas usa para obter um perfil de rede.

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                              | Type                                                        | Descrição                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**Id**](taskschedulerschema-id-networksettingstype-element.md)     | [**guidType**](taskschedulerschema-guidtype-simpletype.md) | Especifica um valor guid que identifica um perfil de rede. <br/>                       |
| [**Nome**](taskschedulerschema-name-networksettingstype-element.md) | nonEmptyString                                              | Especifica o nome de um perfil de rede. O nome é usado para fins de exibição. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





