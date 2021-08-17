---
description: Define um tipo de cadeia de caracteres para o perfil de Banda Larga Móvel.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: tipo simples nameType (Banda Larga Móvel)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: 9b07bfb62e23b0c82ef69bc924147675caad10d61258a5c49edc906c4b6bf2a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881400"
---
# <a name="nametype-simple-type-mobile-broadband"></a>tipo simples nameType (Banda Larga Móvel)

O **tipo simples nameType** define um tipo de cadeia de caracteres para o perfil de Banda Larga Móvel. Essa cadeia de caracteres tem pelo menos um caractere de comprimento e, no máximo, 255 caracteres.

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
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



 

 




