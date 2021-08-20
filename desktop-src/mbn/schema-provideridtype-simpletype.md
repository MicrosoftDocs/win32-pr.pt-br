---
description: Define um tipo para o elemento ProviderID do perfil de banda larga móvel.
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: Tipo simples de providerIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: 545629755174d74170c54e6ce85eabe9a82f13709cf83e3029d05949cb8aadcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065890"
---
# <a name="provideridtype-simple-type"></a>Tipo simples de providerIdType

O tipo simples **providerIdType** define um tipo para o elemento [**ProviderID**](schema-providerid-providertype-element.md) do perfil de banda larga móvel. Esse tipo é uma coleção de dígitos com pelo menos um dígito e, no máximo, seis dígitos.

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O tipo simples **providerIdType** é um token que é restrito pelo seguinte padrão:

-   `\d{1,6}`

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



 

 




