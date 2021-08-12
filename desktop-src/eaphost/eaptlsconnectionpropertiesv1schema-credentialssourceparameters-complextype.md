---
title: Tipo complexo CredentialsSourceParameters
description: Define o elemento necessário para especificar a origem do certificado a ser usado com uma autenticação EAP-TLS.
ms.assetid: 1482694e-3025-4231-8154-4be0301fe5ce
keywords:
- CredentialsSourceParameters tipo complexo EAPHost
topic_type:
- apiref
api_name:
- CredentialsSourceParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 881cd4225c0e7e2f557ad7206176224a0b3929cdac7398b29f30382506f816ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274003"
---
# <a name="credentialssourceparameters-complex-type"></a>Tipo complexo CredentialsSourceParameters

O **tipo complexo CredentialsSourceParameters** define o elemento necessário para especificar a origem do certificado a ser usado com uma autenticação EAP-TLS.

Há uma opção entre o elemento [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) ou [**o elemento CertificateStore.**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)

``` syntax
<xs:complexType name="CredentialsSourceParameters">
    <xs:choice>
        <xs:element name="SmartCard"
            type="emptyString"
         />
        <xs:element name="CertificateStore"
            type="CertSelection"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                             | Type                                                                                  | Descrição                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | Indica que o EAP-TLS deve ler o certificado da Minha Loja do usuário ou do computador que está sendo autenticado. <br/> |
| [**Smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [**emptyString**](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | Indica que o EAP-TLS deve ler o certificado do Cartão Inteligente. <br/>                                          |



## <a name="remarks"></a>Comentários

Os [**elementos CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) [**e SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) não podem ser usados simultaneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Tipos complexos de esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





