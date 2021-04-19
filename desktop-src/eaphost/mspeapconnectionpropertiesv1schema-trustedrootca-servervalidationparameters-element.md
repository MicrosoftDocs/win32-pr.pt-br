---
title: Elemento TrustedRootCA (ServerValidationParameters) (v1)
description: Captura a impressão em miniatura das CAs (autoridades de certificação) raiz confiáveis do cliente. | Elemento TrustedRootCA (ServerValidationParameters)
ms.assetid: f0485dcc-8610-4c5b-b4db-6f2a77057489
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
ms.openlocfilehash: 17e1b81e080d48ac8fae4f082c3cf4b46bac858e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389076"
---
# <a name="trustedrootca-servervalidationparameters-element"></a>Elemento TrustedRootCA (ServerValidationParameters)

O elemento de elemento **TrustedRootCA (ServerValidationParameters)** captura a impressão digital das CAS (autoridades de certificação) raiz confiáveis do cliente.

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

O elemento **TrustedRootCA** é definido pelo tipo complexo [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

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

[**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Possíveis elementos pai imediatos na instância de esquema**
</dt> <dt>

[**ServerValidation (EapType)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos do esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





