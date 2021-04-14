---
title: Tipo simples de nonEmptyStringType
description: Define os valores usados para uma cadeia de caracteres não vazia de texto.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- tipo simples não vazio Agendador de Tarefas
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369741"
---
# <a name="nonemptystringtype-simple-type"></a>Tipo simples de nonEmptyStringType

Define os valores usados para uma cadeia de caracteres não vazia de texto.

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O tipo simples **Nonemptytype** define o valor a seguir.



| Valor | Descrição                                            |
|-------|--------------------------------------------------------|
| 1     | A cadeia de caracteres contém pelo menos um caractere.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





