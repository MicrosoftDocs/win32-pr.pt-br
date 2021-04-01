---
title: Tipo complexo networkSettingsType
description: Define os elementos que fornecem as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- Agendador de Tarefas tipo complexo networkSettingsType
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918663"
---
# <a name="networksettingstype-complex-type"></a>Tipo complexo networkSettingsType

Define os elementos que fornecem as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede.

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
| [**Sessão**](taskschedulerschema-id-networksettingstype-element.md)     | [**guidtype**](taskschedulerschema-guidtype-simpletype.md) | Especifica um valor de GUID que identifica um perfil de rede. <br/>                       |
| [**Nome**](taskschedulerschema-name-networksettingstype-element.md) | não vazio                                              | Especifica o nome de um perfil de rede. O nome é usado para fins de exibição. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





