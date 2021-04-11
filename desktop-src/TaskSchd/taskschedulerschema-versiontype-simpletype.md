---
title: Tipo simples versiontype
description: Define um padrão que especifica uma versão de uma tarefa.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- tipo simples de versiontype Agendador de Tarefas
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df7010c6ecba29ad0ade80ce403018dd626d01cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294781"
---
# <a name="versiontype-simple-type"></a>Tipo simples versiontype

Define um padrão que especifica uma versão de uma tarefa.

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O tipo simples **versiontype** é uma **cadeia de caracteres** que é restrita pelo seguinte padrão:

-   `\d+(\.\d+){1,3}`

    Um duplo seguido de um, dois ou três duplos. Por exemplo, 1,2 ou 1.2.3.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





