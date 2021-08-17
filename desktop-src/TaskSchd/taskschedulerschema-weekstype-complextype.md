---
title: Tipo de Weekly Complex
description: Define o elemento filho e as informações de sequenciamento para o elemento Week.
ms.assetid: c9e8814c-b8f9-426d-943d-ca3efa5d914b
keywords:
- tipo complexo de weektype Agendador de Tarefas
topic_type:
- apiref
api_name:
- weeksType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 876d798acdf1f8684fc4f2cecac8e77bceb73dddd0036f2117d4bb55a77a71ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757983"
---
# <a name="weekstype-complex-type"></a>Tipo de Weekly Complex

Define o elemento filho e as informações de sequenciamento para o elemento [**Week**](taskschedulerschema-week-weekstype-element.md) .

``` syntax
<xs:complexType name="weeksType">
    <xs:sequence>
        <xs:element name="Week"
            type="weekType"
            minOccurs="0"
            maxOccurs="5"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                    | Type                                                        | Descrição                                             |
|------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------|
| [**Semana**](taskschedulerschema-week-weekstype-element.md) | [**weektype**](taskschedulerschema-weektype-simpletype.md) | Especifica a semana em que a tarefa é executada.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





