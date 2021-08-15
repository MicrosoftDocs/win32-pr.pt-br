---
title: Tipo complexo bootTriggerType
description: Define o elemento filho e as informações de sequenciamento para o elemento BootTrigger.
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- Agendador de Tarefas tipo complexo bootTriggerType
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc0b04bfaf08ecee87d02a2b410fd1df2fbbe584d5649a5e9fe2ea2e5efacebd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131855"
---
# <a name="boottriggertype-complex-type"></a>Tipo complexo bootTriggerType

Define o elemento filho e as informações de sequenciamento para o elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="bootTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
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



| Elemento                                                            | Type     | Descrição                                                                                 |
|--------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------|
| [**Atrasar**](taskschedulerschema-delay-boottriggertype-element.md) | duration | Quantidade de tempo entre quando o sistema é inicializado e quando o gatilho é acionado. <br/> |



## <a name="remarks"></a>Comentários

Além do elemento filho definido aqui, o elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) também usa elementos filho definidos pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





