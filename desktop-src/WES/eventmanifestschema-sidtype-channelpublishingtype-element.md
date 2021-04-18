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
ms.openlocfilehash: 5d65e1ade4ded95b070b45de9462f6aee2c60ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784934"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**publicando (channelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





