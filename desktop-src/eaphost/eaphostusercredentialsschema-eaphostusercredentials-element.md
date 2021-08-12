---
title: Elemento EapHostUserCredentials
description: Contém o elemento EapMethod e as credenciais ou o elemento CredentialsBlob.
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- Elemento EapHostUserCredentials EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a18922ef19bd828067ddb0153aa7c6369ecfeebd0446f5a6481f91fa64ca21b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274416"
---
# <a name="eaphostusercredentials-element"></a>Elemento EapHostUserCredentials

O elemento **EapHostUserCredentials** contém o elemento [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) e [**as credenciais**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) ou o elemento [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) .

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
                    type="hexBinary"
                 />
            </xs:choice>
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



| Elemento                                                                                                | Type                                                                                                                | Descrição                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Fornecidas**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [**BaseEapMethodUserCredentials**](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | É usado quando a configuração do método está no formato de texto XML em vez de em um BLOB binário.<br/>   |
| [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | hexBinary                                                                                                           | É usado quando a configuração do método é um BLOB binário em vez de no formato de texto XML.<br/> |
| [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)                                                  | Identifica o método que está sendo referenciado. <br/>                                             |



## <a name="remarks"></a>Comentários

As [**credenciais**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) e os elementos [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) não podem ser usados simultaneamente.

Há um ponto de extensão para outros namespaces.

O elemento **ProcessContents** permite aprimoramentos futuros no esquema. O elemento **ProcessContents** é opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaphostusercredentials](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





