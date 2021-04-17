---
description: Estende o esquema de perfil WLAN v1 para dar suporte a redes hotspot 2,0.
ms.assetid: DE30DBCB-80B9-43D0-8DE1-56BBA99DBF31
title: Elemento Hotspot2 (WLANProfile)
ms.topic: reference
ms.date: 10/08/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- Hotspot2
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0e372c1025a74dfb304cacdb0f3a4cf18bcdbabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784174"
---
# <a name="hotspot2-wlanprofile-element"></a>Elemento Hotspot2 (WLANProfile)

Estende o esquema de perfil WLAN v1 para dar suporte a redes hotspot 2,0. O HotSpot 2,0 permite a conexão automática a serviços de Wi-Fi públicos usando credenciais existentes e associação em redes de provedor de serviços. Os provedores de serviço especificam como as conexões são feitas usando os novos elementos de esquema para descrever quais redes usar e como se autenticar neles.

``` syntax
<xs:element name="Hotspot2">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="DomainName"
                minOccurs="0"
             />
            <xs:element name="NAIRealm"
                minOccurs="0"
             />
            <xs:element name="Network3GPP"
                minOccurs="0"
             />
            <xs:element name="RoamingConsortium"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

O elemento é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementos filho

| Elemento | Type | Descrição |
|-|-|-|
| [**DomainName**](wlan-profileschema-hotspot2-domainname-element.md) | | O nome de domínio do provedor de rede inicial do dispositivo, identificando o operador da rede. |
| [**NAIRealm**](wlan-profileschema-hotspot2-nairealm-element.md) | | Uma lista de identificadores de territórios da NAI (identificador de acesso à rede). As entradas nessa lista geralmente são do formulário user@domain . |
| [**Network3GPP**](wlan-profileschema-hotspot2-network3gpp-element.md) | | Uma lista de IDs de rede móvel pública (PLMN). |
| [**RoamingConsortium**](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | Uma lista de OUI (identificadores exclusivos da organização) atribuídos pelo IEEE.  |

## <a name="examples"></a>Exemplos

```xml
<Hotspot2>
  <DomainName>contoso.com</DomainName>
  <NAIRealm>
    <name>test1@contoso.com</name>
    <name>test2@contoso.com</name>
  </NAIRealm>
  <Network3GPP>
    <PLMNID>12345</PLMNID>
    <PLMNID>123456</PLMNID>
  </Network3GPP>
  <RoamingConsortium>
    <OUI>00AABB</OUI>
    <OUI>001122</OUI>
  </RoamingConsortium>
</Hotspot2>
```
