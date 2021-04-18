---
description: Contém várias configurações de MSM (módulo específico de mídia).
ms.assetid: 31f98af8-a577-4f6a-9a0a-b182b5a89cc3
title: Elemento MSM (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: b2e1ffdc5ad27524d3d2fc5b37b3a060a90c7575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759672"
---
# <a name="msm-wlanprofile-element"></a>Elemento MSM (WLANProfile)

O elemento MSM (WLANProfile) contém várias configurações do módulo de mídia específica (MSM).

``` syntax
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
```

O elemento é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                            | Type                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Especifica o par de autenticação e criptografia a ser usado para este perfil.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Authentication**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Especifica o par de autenticação e criptografia a ser usado para este perfil.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**conectividade**](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | Contém várias configurações de conectividade. Esse elemento é opcional.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**encripta**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Define a criptografia de dados a ser usada para se conectar à LAN sem fio.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Especifica qual índice de chave deve ser usado para criptografar o tráfego sem fio. Isso só é usado quando KeyType está definido como networkKey.<br/>                                                                                                                                                                                                                                                                                          |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [cadeia de caracteres](/dotnet/api/system.string)   | Contém a chave de rede ou frase secreta.<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Tipo de chave.<br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | Especifica o padrão de LAN sem fio 802,11 usado na LAN sem fio. O valor "n" só tem suporte no Windows Vista com SP1 e em versões posteriores do sistema operacional.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                        |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Indica se o cache PMK será usado. Esse elemento é válido somente para redes definidas por WPA2.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                                                                                 |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Especifica o número de entradas no cache OMK no cliente. Esse elemento é válido somente para redes definidas por WPA2 com o modo PMKCache definido como habilitado. Se o modo PMKCache estiver habilitado e esse elemento estiver ausente, o tamanho do cache será padronizado para 128 entradas.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                   |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Indica o período de tempo, em minutos, que um cache de PMK será mantido. Esse elemento é válido somente para redes definidas por WPA2 com o modo PMKCache definido como habilitado.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                                                                                                                  |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Determina se a pré-autenticação será usada pelo cliente. A pré-autenticação habilita o roaming rápido seguro de WPA2. Esse elemento é válido somente para redes definidas por WPA2 com o modo PMKCache definido como habilitado. Se o modo PMKCache estiver habilitado e esse elemento estiver ausente, o valor padrão será desabilitado.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/> |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Indica o número de tentativas ao se autenticar em APs vizinhos. Esse elemento é válido somente para redes definidas por WPA2 com o modo PMKCache definido como habilitado. Se o modo PMKCache estiver habilitado e esse elemento estiver ausente, o número de tentativas padrão será 3.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.<br/>                                      |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)                | [booleano](/dotnet/api/system.boolean) | Indica se a chave está criptografada.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento deve ter um valor de FALSE.<br/>                                                                                                                                                                                                                                                 |
| [**segurança**](wlan-profileschema-security-msm-element.md)                        |                                                                   | Contém várias configurações de segurança. Esse elemento é opcional.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Contém as informações de chave compartilhada. Esse elemento só será necessário se as chaves WEP ou PSK forem necessárias para o par de autenticação e criptografia.<br/>                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [booleano](/dotnet/api/system.boolean) | Indica se 802.1 X é usado. Esse sinalizador é opcional.<br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Comentários

O elemento [**fipsmode**](wlan-profileschema-fipsmode-authencryption-element.md) pode ser inserido como um filho do elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) . O elemento [**Onex**](onexschema-onex-element.md) pode ser inserido como um filho do elemento [**Security (MSM)**](wlan-profileschema-security-msm-element.md) .

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **msm** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Exemplos de perfil sem fio](wireless-profile-samples.md)
</dt> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
