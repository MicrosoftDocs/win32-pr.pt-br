---
title: Elemento TrustedRootCA (ServerValidationParameters)-conexão
description: Captura a impressão em miniatura das CAs (autoridades de certificação) raiz confiáveis do cliente. | Elemento TrustedRootCA (ServerValidationParameters)
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
ms.openlocfilehash: e6f91816ba90300a76545a7a22cea6d037b4e897
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105772921"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a>Elemento TrustedRootCA (ServerValidationParameters) para propriedades de conexão

O elemento **TrustedRootCA (ServerValidationParameters)** captura a impressão digital das CAS (autoridades de certificação) raiz confiáveis do cliente.

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

O elemento **TrustedRootCA** é definido pelo tipo complexo [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="remarks"></a>Comentários

O Thumb Print é uma cadeia de caracteres hexadecimal que contém o hash SHA-1 do certificado. O elemento **TrustedRootCA** é opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

[Elementos do esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





