---
title: tipo complexo restartType
description: Define os elementos filho e as informações de sequência para o elemento RestartOnFailure.
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- tipo complexo restartType Agendador de Tarefas
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 996debc2c8e3d7d00ca7b42facde582f918d72736426ed326691461d800f8562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516473"
---
# <a name="restarttype-complex-type"></a>tipo complexo restartType

Define os elementos filho e as informações de sequência para o [elemento RestartOnFailure.](taskschedulerschema-restartonfailure-settingstype-element.md)

``` syntax
<xs:complexType name="restartType">
    <xs:all>
        <xs:element name="Interval">
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                    <xs:maxInclusive
                        value="P31D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Count">
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                              | Type | Descrição                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [**Contagem**](taskschedulerschema-count-restarttype-element.md)       |      | Número de tentativas de reiniciar a tarefa.<br/> |
| [**Intervalo**](taskschedulerschema-interval-restarttype-element.md) |      | Por quanto tempo tentar iniciar a tarefa.<br/>      |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas complexos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





