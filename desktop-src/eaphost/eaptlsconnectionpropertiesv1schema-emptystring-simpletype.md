---
title: Tipo simples emptyobject
description: Saiba mais sobre o tipo simples emptyobject, que não está em uso. Consulte requisitos e exiba recursos adicionais disponíveis.
ms.assetid: e561b8d5-8683-41a1-bd72-73b1a767b6cf
keywords:
- tipo simples emptytype EAPHost
topic_type:
- apiref
api_name:
- emptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 756c8976c8b989cf77be921491770fcff9ea62d5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008387"
---
# <a name="emptystring-simple-type"></a>Tipo simples emptyobject

O tipo simples **emptyobject** não está em uso.

``` syntax
<xs:simpleType name="emptyString">
    <xs:restriction
        base="string"
    >
        <xs:maxLength
            value="0"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|-------------------------------------|------------------------------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Tipos simples de esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-simple-types.md)
</dt> </dl>

 

 





