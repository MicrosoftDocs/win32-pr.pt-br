---
title: Elemento AnonymousUserName (IdentityPrivacyParameters)
description: Contém uma identidade anônima usada no lugar da identificação verdadeira de um usuário. Ele é enviado durante a 1ª fase da autenticação PEAP quando a identidade é enviada como texto sem formatação.
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- Elemento AnonymousUserName EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369759"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a>Elemento AnonymousUserName (IdentityPrivacyParameters)

O elemento **AnonymousUserName (IdentityPrivacyParameters)** contém uma identidade anônima usada no lugar da identificação verdadeira de um usuário. Ele é enviado durante a 1ª fase da autenticação PEAP quando a **identidade** é enviada como texto sem formatação.

O uso de identidade anônima é determinado pelo elemento [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

O elemento **AnonymousUserName** é definido pelo [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .

## <a name="remarks"></a>Comentários

O elemento **AnonymousUserName** é opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Elementos do esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





