---
description: Define um tipo de cadeia de caracteres para o perfil de banda larga móvel.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: tipo simples nametype (banda larga móvel)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: d8c6032e17eaf2d067dc23030a7a6279bd41eafa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755282"
---
# <a name="nametype-simple-type-mobile-broadband"></a>tipo simples nametype (banda larga móvel)

O tipo simples **nametype** define um tipo de cadeia de caracteres para o perfil de banda larga móvel. Essa cadeia de caracteres tem pelo menos um caractere e, no máximo, 255 caracteres de comprimento.

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



 

 




