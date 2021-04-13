---
description: Define um tipo de cadeia de caracteres para o elemento ProviderName no perfil de banda larga móvel.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: Tipo simples de providerNametype
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: df61473358a9ed4453bc28f1b5c7974082e515bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501645"
---
# <a name="providernametype-simple-type"></a>Tipo simples de providerNametype

O tipo simples **providernametype** define um tipo de cadeia de caracteres para o elemento [**ProviderName**](schema-providername-providertype-element.md) no perfil de banda larga móvel. Essa cadeia de caracteres tem pelo menos um caractere de comprimento e no máximo 20 caracteres.

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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



 

 




