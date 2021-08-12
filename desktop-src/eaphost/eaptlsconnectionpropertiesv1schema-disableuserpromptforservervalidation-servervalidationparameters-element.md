---
title: DisableUserPromptForServerValidation (ServerValidationParameters)
description: Saiba mais sobre o elemento DisableUserPromptForServerValidation (ServerValidationParameters). Indica se o usuário deve ser solicitado a fazer a validação do servidor. | DisableUserPromptForServerValidation (ServerValidationParameters)
ms.assetid: d1c2f334-286b-4aac-b723-806b90fc7b1f
keywords:
- Elemento DisableUserPromptForServerValidation EAPHost
topic_type:
- apiref
api_name:
- DisableUserPromptForServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37f412f9c6200e7d2a54d624d0a77b4df5316ea7edd0ab75b69f92c753abbcff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273714"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-tls"></a>Elemento DisableUserPromptForServerValidation (ServerValidationParameters) (TLS)

O elemento **DisableUserPromptForServerValidation (ServerValidationParameters)** indica se o usuário deve ser solicitado para a validação do servidor.

Se **DisableUserPromptForServerValidation** for true, o EAP-TLS executará a validação do servidor sem a entrada do usuário; se a validação falhar, o EAP-TLS falhará na autenticação. Se **DisableUserPromptForServerValidation** for false, o usuário será solicitado a fornecer um certificado ou nome de servidor validado ou AC (autoridade de certificação) raiz.

O elemento **DisableUserPromptForServerValidation** é opcional.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

O elemento **DisableUserPromptForServerValidation** é definido pelo tipo complexo [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



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

 

 





