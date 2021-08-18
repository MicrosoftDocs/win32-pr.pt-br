---
title: Elemento DifferentUsername (EapType)
description: Saiba mais sobre o elemento DifferentUsername (EapType). Esse elemento determina qual nome de usuário EAP-TLS deve ser usado.
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- Elemento DifferentUsername EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2980a55e76d238578822cfc8db54a9b6c324e21d4a8f0481ab9bc91e050fb008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984086"
---
# <a name="differentusername-eaptype-element"></a>Elemento DifferentUsername (EapType)

O **elemento DifferentUsername (EapType)** determina qual nome de usuário EAP-TLS deve ser usado.

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

O **elemento DifferentUsername** é definido pelo [**elemento EapType.**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)

## <a name="remarks"></a>Comentários

Se o **elemento DifferentUserName** for TRUE, o EAP-TLS deverá usar um nome de usuário diferente do nome que aparece no certificado. Se o **elemento DifferentUserName** for FALSE, o EAP-TLS usará o nome de usuário que aparece no certificado.

O **elemento DifferentUserName** é opcional.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





