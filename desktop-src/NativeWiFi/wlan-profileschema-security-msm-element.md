---
description: Contém várias configurações de segurança.
ms.assetid: 1d912fb1-8fb4-4761-8991-5a50ffb0399e
title: Elemento security (MSM) (LAN_policy) (WLAN)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c885f330538177cddca40c47cf6a5ad910030c6c5f4c3429ca7bd92c3b437b20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912686"
---
# <a name="security-msm-element-lan_policy-for-wlan"></a>Elemento Security (MSM) (LAN_policy) para WLAN

O elemento de segurança (MSM) contém várias configurações de segurança.

``` syntax
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
```

O elemento é definido pelo [**elemento MSM.**](wlan-profileschema-msm-wlanprofile-element.md)

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                            | Type                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Especifica o par de autenticação e criptografia a ser usado para esse perfil.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Autenticação**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Especifica o par de autenticação e criptografia a ser usado para esse perfil.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Criptografia**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Define a criptografia de dados a ser usada para se conectar à LAN sem fio.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Especifica qual índice de chave deve ser usado para criptografar o tráfego sem fio. Isso só é usado quando keyType é definido como networkKey.<br/>                                                                                                                                                                                                                                                                                          |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [cadeia de caracteres](/dotnet/api/system.string)   | Contém a chave de rede ou a frase-senha.<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**Keytype**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Tipo de chave.<br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Indica se o cache PMK será usado. Esse elemento é válido somente para redes definidas pelo WPA2.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para esse elemento.<br/>                                                                                                                                                                                                 |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Especifica o número de entradas no cache do OMK no cliente. Esse elemento é válido somente para redes definidas pelo WPA2 com o modo PMKCache definido como habilitado. Se o modo PMKCache estiver habilitado e esse elemento estiver ausente, o tamanho do cache será padrão para 128 entradas.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para esse elemento.<br/>                                   |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Indica o período de tempo, em minutos, que um cache PMK será mantido. Esse elemento é válido somente para redes definidas pelo WPA2 com o modo PMKCache definido como habilitado.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para esse elemento.<br/>                                                                                                                                  |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Determina se a pré-autenticação será usada pelo cliente. A pré-autenticação habilita o roaming rápido seguro do WPA2. Esse elemento é válido somente para redes definidas pelo WPA2 com o modo PMKCache definido como habilitado. Se o modo PMKCache estiver habilitado e esse elemento estiver ausente, o valor padrão será desabilitado.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para esse elemento.<br/> |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Indica o número de tentativas ao pré-autenticar para APs vizinhos. Esse elemento é válido somente para redes definidas pelo WPA2 com o modo PMKCache definido como habilitado. Se o modo PMKCache estiver habilitado e esse elemento estiver ausente, o número de tentativas será padrão como 3.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para esse elemento.<br/>                                      |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)                | [booleano](/dotnet/api/system.boolean) | Indica se a chave está criptografada.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento deve ter um valor **false.**<br/>                                                                                                                                                                                                                                             |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Contém as informações de chave compartilhada. Esse elemento só será necessário se as chaves WEP ou PSK são necessárias para o par de autenticação e criptografia.<br/>                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [booleano](/dotnet/api/system.boolean) | Indica se 802.1X é usado. Esse sinalizador é opcional.<br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Comentários

O [**elemento FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) pode ser inserido como um filho do [**elemento authEncryption.**](wlan-profileschema-authencryption-security-element.md) O [**elemento OneX**](onexschema-onex-element.md) pode ser inserido como um filho do **elemento de segurança (MSM).**

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **de** segurança, consulte [Exemplos de perfil sem fio](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, Windows XP somente com aplicativos da área de trabalho SP3 \[\]<br/> |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Exemplos de perfil sem fio](wireless-profile-samples.md)
</dt> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**Msm**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**MSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 
