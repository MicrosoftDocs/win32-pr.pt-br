---
title: Tipo simples PathType
description: Define o número mínimo e máximo de caracteres para uma cadeia de caracteres que define um caminho de arquivo.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- tipo simples de PathType Agendador de Tarefas
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780105"
---
# <a name="pathtype-simple-type"></a>Tipo simples PathType

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





