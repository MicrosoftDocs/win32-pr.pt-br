---
title: Elemento username (TLS)
description: Saiba mais sobre o elemento username. Esse elemento captura o nome de usuário a ser enviado na resposta EAP-Identity.
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Elemento username EAPHost
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
ms.openlocfilehash: 6748ac8c352540d2288cf3bf3c790004d832ba47961fbc7b9e8211fa712ccb6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720115"
---
# <a name="username-element-tls"></a>Elemento username (TLS)

O elemento **username** captura o nome de usuário a ser enviado na resposta EAP-Identity.

Se o elemento **username** estiver ausente, o EAP-TLS usará o nome no certificado referido no elemento [**usercert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a>Requisitos



| Função | Versões mínimas do sistema operacional com suporte |
|------|-------------------------------|
| Cliente<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





