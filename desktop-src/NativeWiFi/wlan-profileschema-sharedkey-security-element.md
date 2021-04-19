---
description: Contém informações de chave compartilhada.
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: Elemento sharedKey (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sharedKey
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfd138044e4849e5b0a42ab396561331bea9a338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754322"
---
# <a name="sharedkey-security-element"></a>Elemento sharedKey (segurança)

O elemento sharedKey (Security) contém informações de chave compartilhadas. Esse elemento só será necessário se as chaves WEP ou PSK forem necessárias para o par de autenticação e criptografia.

``` syntax
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
```

O elemento é definido pelo elemento [**Security**](wlan-profileschema-security-msm-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                 | Type                                                              | Descrição                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md) | [cadeia de caracteres](/dotnet/api/system.string)   | Contém a chave de rede ou frase secreta.<br/>                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | Tipo de chave.<br/>                                                                                                                                                      |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)     | [booleano](/dotnet/api/system.boolean) | Indica se a chave está criptografada.<br/> **Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento deve ter um valor de FALSE.<br/> |



## <a name="remarks"></a>Comentários

Para o Windows Vista e o Windows Server 2008, os dados associados ao elemento **sharedKey** são criptografados antes de serem salvos no repositório de perfis.

Para o Windows XP com SP3 e a API de LAN sem fio para Windows XP com SP2, os dados não são criptografados.

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **sharedKey** , consulte exemplo de [perfil sem difusão](non-broadcast-profile-sample.md), [exemplo de perfil WPA-Pessoal](wpa-personal-profile-sample.md)e [exemplo de perfil WPA2-Pessoal](wpa2-personal-profile-sample.md).

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

[**segurança**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**segurança (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
