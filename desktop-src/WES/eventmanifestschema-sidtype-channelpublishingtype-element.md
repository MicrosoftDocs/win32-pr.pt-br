---
title: Elemento sidType (ChannelPublishingType)
description: Determina se um SID (identificador de segurança) do principal deve ser incluído em cada evento gravado no canal.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- EventLog do elemento sidType
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41653a1fbda3400b74ca5302deb8075ae891e69f22ca0f0e88b6ec4dbb58dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589147"
---
# <a name="sidtype-channelpublishingtype-element"></a>Elemento sidType (ChannelPublishingType)

Determina se um SID (identificador de segurança) do principal deve ser incluído em cada evento gravado no canal.

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento **sidType** é definido pelo tipo complexo [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**publicando (channelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





