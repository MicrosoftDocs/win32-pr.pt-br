---
title: Tipo complexo timetriggertype
description: Define o tipo base para o elemento timetrigger.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- tipo complexo de timetriggertype Agendador de Tarefas
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c03ede1b87f3969d12256df16c0b05c109391876a12c256190966c8befc7f2fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355744"
---
# <a name="timetriggertype-complex-type"></a>Tipo complexo timetriggertype

Define o tipo base para o elemento [**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                        | Type     | Descrição                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RandomDelay**](taskschedulerschema-randomdelay-timetriggertype-element.md) | duration | Especifica o tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. O formato dessa cadeia de caracteres é `P<days>DT<hours>H<minutes>M<seconds>S` (por exemplo, P2DT5S é um atraso de 2 dias, 5 segundos). <br/> |



## <a name="remarks"></a>Comentários

Observe que esse elemento não adiciona nenhum elemento filho àqueles definidos pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





