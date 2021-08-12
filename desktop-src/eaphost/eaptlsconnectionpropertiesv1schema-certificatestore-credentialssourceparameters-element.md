---
title: Elemento CertificateStore (CredentialsSourceParameters)
description: Indica que o EAP-TLS deve ler o certificado da Minha Loja do usuário ou do computador que está sendo autenticado.
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- Elemento CertificateStore EAPHost
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fb3d2b5c9d50ea8b63c513e4fd9e7297afe236c5ccd16711d9bf4371e76a8d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274288"
---
# <a name="certificatestore-credentialssourceparameters-element"></a>Elemento CertificateStore (CredentialsSourceParameters)

O **elemento CertificateStore (CredentialsSourceParameters)** indica que o EAP-TLS deve ler o certificado do My Store do usuário ou o computador que está sendo autenticado.

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

O **elemento CertificateStore** é definido pelo tipo complexo [**CredentialsSourceParameters.**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)

## <a name="remarks"></a>Comentários

Os **elementos CertificateStore** [**e SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) não podem ser usados simultaneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**CredentialsSource (EapType)**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





