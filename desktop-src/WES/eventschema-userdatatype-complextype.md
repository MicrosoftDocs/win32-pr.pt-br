---
title: Tipo complexo UserDataType
description: Define um fragmento XML que especifica o layout dos dados do evento.
ms.assetid: 25147ace-cc36-43cc-ad85-6a1714f43dbe
keywords:
- Log de eventos do tipo complexo UserDataType
topic_type:
- apiref
api_name:
- UserDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747f2e30f6b2588cdfd6a9f0dd50187b73817996bd3725a571283a7929c91b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904186"
---
# <a name="userdatatype-complex-type"></a>Tipo complexo UserDataType

Define um fragmento XML que especifica o layout dos dados do evento.

``` syntax
<xs:complexType name="UserDataType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





