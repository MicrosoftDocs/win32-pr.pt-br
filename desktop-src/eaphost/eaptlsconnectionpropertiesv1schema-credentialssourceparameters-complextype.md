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
ms.openlocfilehash: 912faa4a388d9a57225991959625a978ca0921f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085952"
---
# <a name="credentialssourceparameters-complex-type"></a>Tipo complexo CredentialsSourceParameters

O tipo complexo **CredentialsSourceParameters** define o elemento necessário para especificar a origem do certificado a ser usado com uma autenticação EAP-TLS.

Há uma opção entre o elemento [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) ou o elemento [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) .

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
| [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | Indica que o EAP-TLS deve ler o certificado do meu repositório do usuário ou do computador que está sendo autenticado. <br/> |
| [**Smart**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [**emptyString**](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | Indica que o EAP-TLS deve ler o certificado do cartão inteligente. <br/>                                          |



## <a name="remarks"></a>Comentários

Os elementos [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) e [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) não podem ser usados simultaneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Tipos complexos de esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





