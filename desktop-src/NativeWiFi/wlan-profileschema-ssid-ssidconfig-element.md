---
description: Contém um SSID para uma LAN sem fio.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: Elemento SSID (SSIDConfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 644a4afbd10fbfff870007befda964fc9babd593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828845"
---
# <a name="ssid-ssidconfig-element"></a>Elemento SSID (SSIDConfig)

O elemento SSID (SSIDConfig) contém um SSID para uma LAN sem fio.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** No máximo um elemento **SSID** pode aparecer em um perfil.

``` syntax
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
```

O elemento **SSID** é definido pelo elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                              | Type | Descrição                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)   |      | Contém o SSID de uma LAN sem fio em formato hexadecimal.<br/> |
| [**nomes**](wlan-profileschema-name-ssid-element.md) |      | Contém o SSID para uma LAN sem fio.<br/>                      |



## <a name="remarks"></a>Comentários

Embora os elementos [**hex**](wlan-profileschema-hex-ssid-element.md) e [**Name**](wlan-profileschema-name-ssid-element.md) sejam opcionais, pelo menos um elemento **hex** ou [**Name**](wlan-profileschema-name-ssid-element.md) deve aparecer como um filho do elemento **SSID** .

Quando as informações de perfil são convertidas em um SSID, o elemento [**hex**](wlan-profileschema-hex-ssid-element.md) é convertido para o SSID (se presente) e o elemento [**Name**](wlan-profileschema-name-ssid-element.md) é ignorado. Se o elemento **hex** não estiver presente, o elemento [**Name**](wlan-profileschema-name-ssid-element.md) será convertido em um SSID usando a conversão de Unicode em ASCII.

Quando um SSID é armazenado em um perfil, o elemento [**hex**](wlan-profileschema-hex-ssid-element.md) sempre é gerado. O elemento [**Name**](wlan-profileschema-name-ssid-element.md) só será gerado se a conversão de ASCII para Unicode do SSID e a geração do perfil XML forem bem-sucedidas. Algumas informações do SSID original podem ser perdidas quando são convertidas em um [**nome**](wlan-profileschema-name-ssid-element.md).

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **SSID** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).

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

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




