---
title: tipo simples pathType
description: Define o número mínimo e máximo de caracteres para uma cadeia de caracteres que define um caminho de arquivo.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- tipo simples pathType Agendador de Tarefas
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 289e91b3d7139001bfab22c81bfb0f9e9871033f6296286373c5bde18fdc366d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758375"
---
# <a name="pathtype-simple-type"></a>tipo simples pathType

Define o número mínimo e máximo de caracteres para uma cadeia de caracteres que define um caminho de arquivo. O caminho não pode ser uma cadeia de caracteres vazia e deve ter menos de 260 caracteres.

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





