---
title: Elemento clocktype (ChannelPublishingType)
description: A resolução de relógio a ser usada ao registrar em log o carimbo de data/hora para cada evento.
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- Log do elemento EventLogtype
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b85537ec209f39da87e74db6881abdf60e488b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369301"
---
# <a name="clocktype-channelpublishingtype-element"></a>Elemento clocktype (ChannelPublishingType)

A resolução de relógio a ser usada ao registrar em log o carimbo de data/hora para cada evento.

``` syntax
<xs:element name="clockType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="SystemTime"
             />
            <xs:enumeration
                value="QPC"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento **clocktype** é definido pelo tipo complexo [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .

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

 

 





