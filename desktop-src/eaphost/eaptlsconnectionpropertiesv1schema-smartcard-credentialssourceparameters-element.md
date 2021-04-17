---
title: Elemento SmartCard (CredentialsSourceParameters)
description: Indica que o EAP-TLS deve ler o certificado do cartão inteligente.
ms.assetid: 0755b0bf-520a-4ae6-a8fc-2f69ae12b066
keywords:
- Elemento SmartCard EAPHost
topic_type:
- apiref
api_name:
- SmartCard
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14581a06064a242a0f66e763e0b848d7d74bce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105790364"
---
# <a name="smartcard-credentialssourceparameters-element"></a>Elemento SmartCard (CredentialsSourceParameters)

O elemento **SmartCard (CredentialsSourceParameters)** indica que o EAP-TLS deve ler o certificado do cartão inteligente.

``` syntax
<xs:element name="SmartCard"
    type="emptyString"
 />
```

O elemento **SmartCard** é definido pelo tipo complexo [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .

## <a name="remarks"></a>Comentários

Os elementos [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) e **SmartCard** não podem ser usados simultaneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**CredentialName (EapType)**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos do esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





