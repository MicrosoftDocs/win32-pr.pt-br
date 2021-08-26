---
title: Tipo complexo namedValue
description: Define um nome associado a um valor em um par nome-valor.
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- tipo complexo namedValue Agendador de Tarefas
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f0f92b89114dfedfbfdbc61d476aff99332191317c1f67b2163eb9416ef3a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080416"
---
# <a name="namedvalue-complex-type"></a>Tipo complexo namedValue

Define um nome associado a um valor em um par nome-valor.

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nome | Tipo                                                                    | Descrição                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| name | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica o nome associado a um valor em um par nome-valor. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





