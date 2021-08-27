---
title: Tipo simples runLevelType
description: Define os valores possíveis para o elemento RunLevel (principalType).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- Tipo simples runLevelType Agendador de Tarefas
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ce534008ce0138293a773e4f5fa4a5270a2d4b27aad54dd062eafe286ab8ba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991066"
---
# <a name="runleveltype-simple-type"></a>Tipo simples runLevelType

Define os valores possíveis para o [**elemento RunLevel (principalType).**](taskschedulerschema-runlevel-principaltype-element.md)

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O **tipo simples runLevelType** define os valores a seguir.



| Valor            | Descrição                                               |
|------------------|-----------------------------------------------------------|
| LeastPrivilege   | As tarefas são executadas com os privilégios mínimos (LUA).<br/> |
| HighestAvailable | As tarefas são executadas com os privilégios mais altos.<br/>     |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





