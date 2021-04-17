---
description: Define a lista de redes permitidas e negadas para computadores.
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: Elemento networkFilter (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkFilter
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d78a23ba1a456f1ad45745fcc25580c27de148c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782966"
---
# <a name="networkfilter-wlanpolicy-element"></a>Elemento networkFilter (WLANPolicy)

O elemento networkFilter (WLANPolicy) define a lista de redes permitidas e negadas para computadores.

``` syntax
<xs:element name="networkFilter">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="allowList"
                minOccurs="0"
            >
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
            <xs:element name="blockList"
                minOccurs="0"
            >
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
            <xs:element name="denyAllIBSS"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="denyAllESS"
                type="boolean"
                minOccurs="0"
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

O elemento **networkFilter** é definido pelo elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                    | Type                                                                     | Descrição                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**Lista**](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | A lista de redes LAN sem fio às quais qualquer computador deve ter permissão para se conectar. <br/> |
| [**Bloqueios**](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | A lista de redes LAN sem fio às quais um computador não deve se conectar.<br/>              |
| [**denyAllESS**](wlan-policyschema-denyalless-networkfilter-element.md)   | booleano                                                                  | Especifica se o acesso a todas as redes de infraestrutura está bloqueado. <br/>                     |
| [**denyAllIBSS**](wlan-policyschema-denyallibss-networkfilter-element.md) | booleano                                                                  | Especifica se o acesso a todas as redes ad hoc está bloqueado. <br/>                             |
| [**rede**](wlan-policyschema-network-allowlist-element.md)             | [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) | Uma rede permitida. <br/>                                                                |
| [**rede**](wlan-policyschema-network-blocklist-element.md)             | [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) | Uma rede bloqueada. <br/>                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




