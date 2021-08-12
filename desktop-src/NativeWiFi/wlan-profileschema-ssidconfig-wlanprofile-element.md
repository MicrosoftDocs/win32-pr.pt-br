---
description: Contém um ou mais SSIDs para LANs sem fio.
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: Elemento SSIDConfig (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSIDConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6df6edc3affa551d62473b616562257cd422fcc4a4021ea7e4ef05ba3c8af9dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619034"
---
# <a name="ssidconfig-wlanprofile-element"></a>Elemento SSIDConfig (WLANProfile)

O elemento SSIDConfig (WLANProfile) contém um ou mais SSIDs para LANs sem fio.

``` syntax
<xs:element name="SSIDConfig"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="SSID"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="hex"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="name"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="nonBroadcast"
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

O **elemento SSIDConfig** é definido pelo [**elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                    | Type                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Hex**](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | Contém o SSID de uma LAN sem fio em formato hexadecimal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**name**](wlan-profileschema-name-ssid-element.md)                       |                                                                   | Contém o nome (sensível a minúsculas) do SSID de uma LAN sem fio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**nonBroadcast**](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [booleano](/dotnet/api/system.boolean) | Indica se a rede transmite seu SSID.<br/> Se [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como ESS, esse valor poderá ser **TRUE** ou **FALSE.** O valor padrão será **TRUE** se esse elemento estiver ausente.<br/> Se [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como IBSS, esse valor deverá ser **FALSE.**<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para esse elemento.<br/> |
| [**Ssid**](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | Contém um SSID para uma LAN sem fio.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** No máximo um [**elemento SSID**](wlan-profileschema-ssid-ssidconfig-element.md) pode aparecer em um perfil.<br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o **elemento SSIDConfig,** consulte [Exemplos de perfil sem fio](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, Windows XP somente com aplicativos da área de trabalho SP3 \[\]<br/> |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
