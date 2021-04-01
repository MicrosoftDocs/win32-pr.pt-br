---
description: Define um tipo de cadeia de caracteres para o elemento ICONFilePath no perfil de banda larga móvel.
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: Tipo simples de iconFileType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: 168c2709f8b3049270711e286a35fbbd11e1ffef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090303"
---
# <a name="iconfiletype-simple-type"></a>Tipo simples de iconFileType

O tipo simples **iconFileType** define um tipo de cadeia de caracteres para o elemento [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) no perfil de banda larga móvel. Essa cadeia de caracteres tem pelo menos um caractere e, no máximo, 1024 caracteres de comprimento.

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



 

 




