---
description: Define um tipo para o elemento SimIccID do perfil de Banda Larga Móvel.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: Tipo simples simIccIDType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 33a984875e1e6840787d81dc53c8fc13ead54a0328f6610d75c30075066c13c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035754"
---
# <a name="simiccidtype-simple-type"></a>Tipo simples simIccIDType

O **tipo simples simIccIDType** define um tipo para o [**elemento SimIccID**](schema-simiccid-mbnprofile-element.md) do perfil de Banda Larga Móvel. Esse tipo é uma coleção de dígitos e/ou letras maiúsculas e inferiores, pelo menos um caractere longo e, no máximo, 20 caracteres.

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O **tipo simples simIccIDType** é um token restrito pelo seguinte padrão:

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos UWP da área \| de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



 

 




