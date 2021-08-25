---
title: Tipo complexo logonTriggerType
description: Define os elementos filho e as informações de sequenciamento para o elemento LogonTrigger.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- Agendador de Tarefas tipo complexo logonTriggerType
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85cbbeaa5d911b1ef9677c79980167a66cdf410c7aa63597b02b007795dfbd81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991206"
---
# <a name="logontriggertype-complex-type"></a>Tipo complexo logonTriggerType

Define os elementos filho e as informações de sequenciamento para o elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                               | Type                                                                    | Descrição                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Atrasar**](taskschedulerschema-delay-logontriggertype-element.md)   | duration                                                                | Quantidade de tempo entre quando o usuário faz logon e quando a tarefa é iniciada.<br/>         |
| [**ID**](taskschedulerschema-userid-logontriggertype-element.md) | [**não vazio**](taskschedulerschema-nonemptystring-simpletype.md) | Identificador do usuário. A tarefa é iniciada quando esse usuário faz logon no computador.<br/> |



## <a name="remarks"></a>Comentários

Além dos elementos filho definidos aqui, o elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) também usa elementos filho definidos pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos complexos de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





