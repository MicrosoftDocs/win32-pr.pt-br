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
ms.openlocfilehash: 5665b385c3264ff9d36e79ad671c8f9e8377d4bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828699"
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

O elemento **SSIDConfig** é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                    | Type                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | Contém o SSID de uma LAN sem fio em formato hexadecimal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**nomes**](wlan-profileschema-name-ssid-element.md)                       |                                                                   | Contém o nome (diferencia maiúsculas de minúsculas) do SSID de uma LAN sem fio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**sem difusão**](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [booleano](/dotnet/api/system.boolean) | Indica se a rede transmite seu SSID.<br/> Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como ESS, esse valor poderá ser **true** ou **false**. O valor padrão será **true** se esse elemento estiver ausente.<br/> Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como IBSS, esse valor deverá ser **false**.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/> |
| [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | Contém um SSID para uma LAN sem fio.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** No máximo um elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) pode aparecer em um perfil.<br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **SSIDConfig** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                |
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

 

 
