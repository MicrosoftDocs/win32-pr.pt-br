---
description: Define um tipo para o elemento subscriberid do perfil de banda larga móvel.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: Tipo simples de subscriberIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: c3c776bbd721bbb03b4f5549f87d48248a35206b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010467"
---
# <a name="subscriberidtype-simple-type"></a>Tipo simples de subscriberIdType

O tipo simples **subscriberIdType** define um tipo para o elemento [**subscriberid**](schema-subscriberid-mbnprofile-element.md) do perfil de banda larga móvel. Esse tipo é uma coleção de um ou mais caracteres.

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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



 

 




