---
description: Define um tipo para o elemento SubscriberID do perfil de Banda Larga Móvel.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: Tipo simples subscriberIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: aac83be84ae313f572d82e6b4c9a2afb14beeb7e15c531eaae7efd67bcc90464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881360"
---
# <a name="subscriberidtype-simple-type"></a>Tipo simples subscriberIdType

O **tipo simples subscriberIdType** define um tipo para o [**elemento SubscriberID**](schema-subscriberid-mbnprofile-element.md) do perfil de Banda Larga Móvel. Esse tipo é uma coleção de um ou mais caracteres.

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos UWP da área \| de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



 

 




