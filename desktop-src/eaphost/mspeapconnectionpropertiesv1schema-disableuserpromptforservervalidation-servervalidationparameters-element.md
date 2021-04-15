---
title: Elemento DisableUserPromptForServerValidation (PEAP)
description: Saiba mais sobre o elemento DisableUserPromptForServerValidation (ServerValidationParameters). Indica se o usuário deve ser solicitado a fazer a validação do servidor. | Elemento DisableUserPromptForServerValidation (PEAP)
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
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
ms.openlocfilehash: 168ce6e371495901f2ed93fb69b605a807bc363c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105747431"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a>Elemento DisableUserPromptForServerValidation (ServerValidationParameters) (PEAP)

O elemento **DisableUserPromptForServerValidation (ServerValidationParameters)** indica se o usuário deve ser solicitado para a validação do servidor.

Se **DisableUserPromptForServerValidation** for true, o EAP-TLS executará a validação do servidor sem a entrada do usuário; se a validação falhar, o EAP-TLS falhará na autenticação. Se **DisableUserPromptForServerValidation** for false, o usuário será solicitado a fornecer um certificado ou nome de servidor validado ou AC (autoridade de certificação) raiz.

O elemento **DisableUserPromptForServerValidation** é opcional.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

O elemento **DisableUserPromptForServerValidation** é definido pelo tipo complexo [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

 

 





