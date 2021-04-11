---
title: Tipo complexo PeapExtensionsType (Propriedades de conexão)
description: Saiba mais sobre o tipo complexo PeapExtensionsType. Esse tipo permite aprimoramentos futuros no esquema.
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
keywords:
- PeapExtensionsType tipo complexo EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bf7e22a013bbd7a931b61b55ae0013bb42f4e41
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294510"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a>Tipo complexo PeapExtensionsType (Propriedades de conexão)

O tipo complexo **PeapExtensionsType** permite aprimoramentos futuros no esquema.

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Comentários

O tipo complexo **PeapExtensionsType** é opcional.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





