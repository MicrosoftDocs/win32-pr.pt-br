---
description: Define um tipo para o elemento SimIccID do perfil de banda larga móvel.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: Tipo simples de simIccIDType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750721"
---
# <a name="simiccidtype-simple-type"></a>Tipo simples de simIccIDType

O tipo simples **simIccIDType** define um tipo para o elemento [**SimIccID**](schema-simiccid-mbnprofile-element.md) do perfil de banda larga móvel. Esse tipo é uma coleção de dígitos e/ou letras maiúsculas e minúsculas, pelo menos um caractere de comprimento e no máximo 20 caracteres.

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

O tipo simples **simIccIDType** é um token que é restrito pelo seguinte padrão:

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



 

 




