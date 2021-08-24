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
ms.openlocfilehash: 1fff0738b8497bd52bee02a04402c77e959e2689c66e47519be20c95a58d56a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684376"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



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

 

 




