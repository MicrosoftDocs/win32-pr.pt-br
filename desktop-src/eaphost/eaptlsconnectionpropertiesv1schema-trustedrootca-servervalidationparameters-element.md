---
title: Elemento TrustedRootCA (ServerValidationParameters) – Conexão
description: Captura a impressão digital de autoridades de certificação raiz (CAs) que são confiáveis para o cliente. | Elemento TrustedRootCA (ServerValidationParameters)
ms.assetid: 81e3b6ca-6360-42dc-bfd3-298e81e66c1a
keywords:
- Elemento TrustedRootCA EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c8f5b129f2db80bc46b24d1a935eea9294d423b205268ec0885869613d44a8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904468"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a>Elemento TrustedRootCA (ServerValidationParameters) para propriedades de conexão

O **elemento TrustedRootCA (ServerValidationParameters)** captura a impressão digital das autoridades de certificação raiz (CAs) que são confiáveis pelo cliente.

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

O **elemento TrustedRootCA** é definido pelo [**tipo complexo ServerValidationParameters.**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)

## <a name="remarks"></a>Comentários

A impressão digital é uma cadeia de caracteres hexadecimal que contém o hash SHA-1 do certificado. O **elemento TrustedRootCA** é opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Possíveis elementos pai imediatos na instância de esquema**
</dt> <dt>

[**ServerValidation (EapType)**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





