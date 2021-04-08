---
description: Define o tipo que define valores válidos para o atributo Type do leitor de diário de elementos de conteúdo \[ \] .
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Tipo simples de ContentTypetype
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 55297be38dfd75f9ca11bfb6213cd99d52d2a7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011174"
---
# <a name="contenttypetype-simple-type"></a>Tipo simples de ContentTypetype

Define o tipo que define valores válidos para o atributo *Type* do [leitor \[ \] de diário de elementos de conteúdo](content-element--journal-reader.md).

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O tipo simples **contenttypetype** é uma cadeia de caracteres que é restrita pelo seguinte padrão:

-   `Normal|Inert`

## <a name="remarks"></a>Comentários

Os valores válidos são "normal" e "Inert".

Se o tipo for "Inert", o conteúdo contido será uma página de diário que é o "plano de fundo" somente leitura/não editável para o documento. Isso ocorre quando um documento é criado usando o driver de impressora do gravador de notas do diário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                     |



 

 




