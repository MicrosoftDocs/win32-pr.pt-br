---
description: Especifica o par de autenticação e criptografia a ser usado para este perfil.
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: Elemento authEncryption (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754205"
---
# <a name="authencryption-security-element"></a>Elemento authEncryption (segurança)

O elemento authEncryption (segurança) especifica o par de autenticação e criptografia a ser usado para esse perfil.

``` syntax
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
```

O elemento é definido pelo elemento [**Security**](wlan-profileschema-security-msm-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                            | Type                                                              | Descrição                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Authentication**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Especifica o método de autenticação que deve ser usado para se conectar à LAN sem fio.<br/> |
| [**encripta**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Define a criptografia de dados a ser usada para se conectar à LAN sem fio.<br/>                       |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [booleano](/dotnet/api/system.boolean) | Indica se 802.1 X é usado.<br/>                                                     |



## <a name="remarks"></a>Comentários

O elemento [**fipsmode**](wlan-profileschema-fipsmode-authencryption-element.md) pode ser inserido como um filho do elemento **authEncryption** .

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **authEncryption** , consulte [amostras de perfil sem fio](wireless-profile-samples.md). Para exibir um perfil de exemplo que usa o elemento [**fipsmode**](wlan-profileschema-fipsmode-authencryption-element.md) , consulte [exemplo de perfil FIPS](fips-profile-sample.md).

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

[**segurança**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**segurança (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
