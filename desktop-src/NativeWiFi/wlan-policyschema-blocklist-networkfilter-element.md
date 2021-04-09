---
description: Especifica a lista de redes LAN sem fio às quais um computador não deve se conectar.
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: Elemento blocklist (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- blockList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e852286d00d93904bd185fef6c2f3444bb5987f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920660"
---
# <a name="blocklist-networkfilter-element"></a>Elemento blocklist (networkFilter)

O elemento blocklist (networkFilter) especifica a lista de redes LAN sem fio às quais um computador não deve se conectar.

``` syntax
<xs:element name="blockList">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="network"
                type="networkItemType"
                maxOccurs="unbounded"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

O elemento **blocklist** é definido pelo elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                        | Type                                                                     | Descrição                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [**rede**](wlan-policyschema-network-blocklist-element.md) | [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) | A rede bloqueada. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




