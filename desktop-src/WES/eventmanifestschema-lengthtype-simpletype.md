---
title: Tipo simples de lengthtype
description: Define um tipo de comprimento que é usado para especificar o número de bytes ou caracteres em um item de dados de comprimento variável, como dados binários ou uma cadeia de caracteres ANSI ou Unicode.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- LogType de tipo simples de comprimento
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295889"
---
# <a name="lengthtype-simple-type"></a>Tipo simples de lengthtype

Define um tipo de comprimento que é usado para especificar o número de bytes ou caracteres em um item de dados de comprimento variável, como dados binários ou uma cadeia de caracteres ANSI ou Unicode. O valor pode ser especificado como um valor xs: unsignedShort ou como uma cadeia de caracteres que faz referência ao nome do nó de item de dados que contém o valor curto sem sinal.

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





