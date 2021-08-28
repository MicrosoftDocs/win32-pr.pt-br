---
title: Tipo complexo requiredPrivilegesType
description: Define os elementos filho e as informações de sequenciamento para o elemento RequiredPrivileges (requiredPrivilegesType).
ms.assetid: ae96282a-d167-47ea-9d37-2d682f746d23
keywords:
- Agendador de Tarefas tipo complexo requiredPrivilegesType
topic_type:
- apiref
api_name:
- requiredPrivilegesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d79b75a4d4bb44aded7367fd4acfd758887815bba6fc6fcfd965f9123ac58c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658786"
---
# <a name="requiredprivilegestype-complex-type"></a>Tipo complexo requiredPrivilegesType

Define os elementos filho e as informações de sequenciamento para o elemento [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) .

``` syntax
<xs:complexType name="requiredPrivilegesType">
    <xs:all>
        <xs:element name="Privilege"
            type="privilegeType"
            minOccurs="1"
            maxOccurs="64"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                           | Type                                                                  | Descrição                                                |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| [**Privilege**](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [**privilégiotype**](taskschedulerschema-privilegetype-simpletype.md) | Especifica os privilégios necessários da tarefa. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos complexos de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





