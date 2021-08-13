---
description: Define um tipo de cadeia de caracteres para o elemento ProviderName no perfil de Banda Larga Móvel.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: tipo simples providerNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: e0a1a0c999eebe8d4ac9922564a28f3b8abce90397fbbda3556bf7726c7355cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744381"
---
# <a name="providernametype-simple-type"></a>tipo simples providerNameType

O **tipo simples providerNameType** define um tipo de cadeia de caracteres para o [**elemento ProviderName**](schema-providername-providertype-element.md) no perfil de Banda Larga Móvel. Essa cadeia de caracteres tem pelo menos um caractere de comprimento e, no máximo, 20 caracteres.

``` syntax
<xs:simpleType name="providerNameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="20"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows aplicativos UWP de 7 \[ \| áreas de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



 

 




