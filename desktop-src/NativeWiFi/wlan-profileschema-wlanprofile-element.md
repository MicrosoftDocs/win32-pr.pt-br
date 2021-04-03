---
description: Contém um perfil de LAN sem fio.
ms.assetid: bc97cb49-3891-4a4a-aab4-895cd9ce6908
title: Elemento WLANProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 227d912128bf3f656fca7aecbaf0fe0640659465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837197"
---
# <a name="wlanprofile-element"></a>Elemento WLANProfile

O elemento **WLANProfile** contém um perfil de LAN sem fio. Esse é o elemento raiz exclusivo para um perfil sem fio.

O namespace de destino para o elemento WLANProfile é `https://www.microsoft.com/networking/WLAN/profile/v1` .

``` syntax
<xs:element name="WLANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
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
            <xs:element name="connectionType">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="IBSS"
                         />
                        <xs:enumeration
                            value="ESS"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="connectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="manual"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="autoSwitch"
                type="boolean"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
            <xs:element name="MSM"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="connectivity"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="phyType"
                                        minOccurs="0"
                                        maxOccurs="4"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="a"
                                                 />
                                                <xs:enumeration
                                                    value="b"
                                                 />
                                                <xs:enumeration
                                                    value="g"
                                                 />
                                                <xs:enumeration
                                                    value="n"
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
                        <xs:element name="security"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="authEncryption">
                                        <xs:complexType>
                                            <xs:sequence>
                                                <xs:element name="authentication">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="open"
                                                             />
                                                            <xs:enumeration
                                                                value="shared"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA"
                                                             />
                                                            <xs:enumeration
                                                                value="WPAPSK"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA2"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA2PSK"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="encryption">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="none"
                                                             />
                                                            <xs:enumeration
                                                                value="WEP"
                                                             />
                                                            <xs:enumeration
                                                                value="TKIP"
                                                             />
                                                            <xs:enumeration
                                                                value="AES"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="useOneX"
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
                                    <xs:element name="sharedKey"
                                        minOccurs="0"
                                    >
                                        <xs:complexType>
                                            <xs:sequence>
                                                <xs:element name="keyType">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="networkKey"
                                                             />
                                                            <xs:enumeration
                                                                value="passPhrase"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="protected"
                                                    type="boolean"
                                                 />
                                                <xs:element name="keyMaterial"
                                                    type="string"
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
                                    <xs:element name="keyIndex"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="0"
                                                 />
                                                <xs:maxInclusive
                                                    value="3"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheMode"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="disabled"
                                                 />
                                                <xs:enumeration
                                                    value="enabled"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheTTL"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="5"
                                                 />
                                                <xs:maxInclusive
                                                    value="1400"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheSize"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="1"
                                                 />
                                                <xs:maxInclusive
                                                    value="255"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="preAuthMode"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="disabled"
                                                 />
                                                <xs:enumeration
                                                    value="enabled"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="preAuthThrottle"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="1"
                                                 />
                                                <xs:maxInclusive
                                                    value="16"
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
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="IHV"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUIHeader">
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="OUI">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:length
                                                    value="3"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="type">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:length
                                                    value="1"
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
                        <xs:element name="connectivity"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:any
                                        processContents="lax"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="security"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:any
                                        processContents="lax"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="useMSOneX"
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

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                            | Type                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Especifica o par de autenticação e criptografia a ser usado para este perfil.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Authentication**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Especifica o método de autenticação a ser usado para se conectar à LAN sem fio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**autocomutação**](wlan-profileschema-autoswitch-wlanprofile-element.md)            | [booleano](/dotnet/api/system.boolean) | Determina o comportamento de roaming de uma rede conectada automaticamente quando uma rede preferencial está no intervalo. Esse elemento é opcional e não tem nenhum efeito em uma rede conectada manualmente.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md)    |                                                                   | Indica se a conexão com a LAN sem fio deve ser automática ("automática") ou iniciada ("manual") pelo usuário. Esse elemento é opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md)    |                                                                   | Indica se a rede é infraestrutura ("ESS") ou ad-hoc ("IBSS").<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**conectividade**](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | Contém várias configurações de conectividade. Esse elemento é opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**conectividade**](wlan-profileschema-connectivity-ihv-element.md)                |                                                                   | Contém configurações de conectividade relacionadas a IHV.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**encripta**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Define a criptografia de dados a ser usada para se conectar à LAN sem fio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**hex**](wlan-profileschema-hex-ssid-element.md)                                 |                                                                   | Contém o SSID de uma LAN sem fio em formato hexadecimal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)                          |                                                                   | Contém configurações opcional do fornecedor de hardware independente (IHV).<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Especifica qual índice de chave deve ser usado para criptografar o tráfego sem fio. Isso só é usado quando [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) está definido como "networkKey".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [cadeia de caracteres](/dotnet/api/system.string)   | Contém a chave de rede ou frase secreta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Tipo de chave.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**MSM**](wlan-profileschema-msm-wlanprofile-element.md)                          |                                                                   | Contém várias configurações de MSM. Esse elemento é opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**nomes**](wlan-profileschema-name-wlanprofile-element.md)                        | [**nometype**](wlan-profileschema-nametype-simpletype.md)        | Nome do perfil de WLAN.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**nomes**](wlan-profileschema-name-ssid-element.md)                               |                                                                   | Contém o SSID de uma LAN sem fio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**sem difusão**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)         | [booleano](/dotnet/api/system.boolean) | Indica se a rede transmite seu SSID.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**OUI**](wlan-profileschema-oui-ouiheader-element.md)                            |                                                                   | Contém um hexBinary de 3 bytes que identifica o IHV.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)                      |                                                                   | Identifica o IHV.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | Especifica o padrão de LAN sem fio 802,11 usado na LAN sem fio. O valor "n" só tem suporte no Windows Vista com SP1 e em versões posteriores do sistema operacional.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Indica se o cache PMK será usado. Esse elemento é válido somente para redes definidas por WPA2.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Especifica o número de entradas no cache PMK no cliente. Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado". Se **PMKCacheMode** estiver habilitado e esse elemento estiver ausente, o tamanho do cache será padronizado para 128 entradas.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Indica o período de tempo, em minutos, que um cache de PMK será mantido. Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado".<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Determina se a pré-autenticação será usada pelo cliente. A pré-autenticação habilita o roaming rápido seguro de WPA2. Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado". Se **PMKCacheMode** estiver habilitado e esse elemento estiver ausente, o valor padrão será desabilitado.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                         |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Indica o número de tentativas ao se autenticar em APs vizinhos. Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado". Se **PMKCacheMode** estiver habilitado e esse elemento estiver ausente, o número de tentativas padrão será 3.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)                | [booleano](/dotnet/api/system.boolean) | Indica se a chave está criptografada.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento deve ter um valor de **false**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**segurança**](wlan-profileschema-security-msm-element.md)                        |                                                                   | Contém várias configurações de segurança. Esse elemento é opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**segurança**](wlan-profileschema-security-ihv-element.md)                        |                                                                   | Contém configurações de segurança específicas de IHV. As configurações de segurança da Microsoft e as configurações de segurança de IHV são mutuamente exclusivas. Se os dois conjuntos de configurações de segurança estiverem presentes no mesmo perfil, o perfil será inválido.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Contém as informações de chave compartilhada. Esse elemento só será necessário se as chaves WEP ou PSK forem necessárias para o par de autenticação e criptografia.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)                         |                                                                   | Especifica o SSID de uma LAN sem fio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)            |                                                                   | Contém um ou mais SSIDs juntamente com outras configurações comuns. <br/> Um perfil pode ter vários elementos [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) e cada elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) pode ter vários elementos [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) . No entanto, o Windows apenas considera o primeiro elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) em um elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** No máximo um elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) pode aparecer em um perfil.<br/> |
| [**Escreva**](wlan-profileschema-type-ouiheader-element.md)                          |                                                                   | Contém um **hexBinary** de 1 byte que é usado para diferenciar NICs pelo mesmo IHV.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)                      | [booleano](/dotnet/api/system.boolean) | Especifica a origem das configurações de segurança 802.1 X usadas por um componente de segurança do IHV. Quando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) é verdadeiro, os componentes de segurança de IHV usam configurações 802.1 x definidas pela Microsoft. Quando **useMSOneX** é false, os componentes de segurança de IHV usam configurações 802.1 x fornecidas pelo fornecedor. Por padrão, **useMSOneX** é false. Esse elemento é opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [booleano](/dotnet/api/system.boolean) | Indica se 802.1 X é usado. Esse sinalizador é opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Comentários

A maioria dos elementos filho do elemento WLANProfile está no `https://www.microsoft.com/networking/WLAN/profile/v1` namespace. Há duas exceções: o elemento [**fipsmode**](wlan-profileschema-fipsmode-authencryption-element.md) está no `https://www.microsoft.com/networking/WLAN/profile/v2` namespace e o elemento [**Onex**](onexschema-onex-element.md) está no `https://www.microsoft.com/networking/OneX/v1` namespace.

O elemento [**fipsmode**](wlan-profileschema-fipsmode-authencryption-element.md) pode ser inserido como um filho do elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) . O elemento [**Onex**](onexschema-onex-element.md) pode ser inserido como um filho do elemento [**Security (MSM)**](wlan-profileschema-security-msm-element.md) .

Para exibir a lista de elementos filho em uma estrutura do tipo árvore, consulte [ \_ elementos do esquema do perfil WLAN](wlan-profileschema-elements.md).

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo, consulte [amostras de perfil sem fio](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Exemplos de perfil sem fio](wireless-profile-samples.md)
</dt> </dl>

 

 
