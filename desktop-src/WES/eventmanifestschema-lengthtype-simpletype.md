---
title: Tipo simples LengthType
description: Define um tipo de comprimento usado para especificar o número de bytes ou caracteres em um item de dados de comprimento variável, como dados binários ou uma cadeia de caracteres ANSI ou Unicode.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- Tipo simples LengthType EventLog
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9ded861e3e46cd5e4fc6c069d95bba9f0ab3457559bf319aef41cdf906e193b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997856"
---
# <a name="lengthtype-simple-type"></a>Tipo simples LengthType

Define um tipo de comprimento usado para especificar o número de bytes ou caracteres em um item de dados de comprimento variável, como dados binários ou uma cadeia de caracteres ANSI ou Unicode. O valor pode ser especificado como um valor xs:unsignedShort ou como uma cadeia de caracteres que faz referência ao nome do nó de item de dados que contém o valor curto sem assinatura.

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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





