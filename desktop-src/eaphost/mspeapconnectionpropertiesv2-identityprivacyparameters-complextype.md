---
title: Tipo complexo IdentityPrivacyParameters
description: Contém informações sobre o uso de identidade anônima durante a autenticação PEAP.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8360065e2ce124531bec63637e2b6560cfc32f54
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104084291"
---
# <a name="identityprivacyparameters-complex-type"></a>Tipo complexo IdentityPrivacyParameters

O tipo complexo **IdentityPrivacyParameters** contém informações sobre o uso de identidade anônima durante a autenticação PEAP.


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| Elemento                                                                                                               | Type    | Descrição                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | booleano | Indica se a identidade verdadeira de um usuário ou uma identidade anônima é enviada.                                                                                                                                                                                                                                                                           |
| [**AnonymousUserName**](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | string  | contém uma identidade anônima usada no lugar da identificação verdadeira de um usuário. Ele é enviado durante a 1ª fase da autenticação PEAP quando a **identidade** é enviada como texto sem formatação. O uso de identidade anônima é determinado pelo elemento [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) . |



 

## <a name="remarks"></a>Comentários

O elemento IdentityPrivacyParameters é opcional.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Tipos complexos mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




