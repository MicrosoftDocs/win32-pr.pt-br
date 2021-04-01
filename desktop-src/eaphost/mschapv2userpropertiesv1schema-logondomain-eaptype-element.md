---
title: Elemento LogonDomain (EapType)
description: Saiba mais sobre o elemento LogonDomain (EapType). Esse elemento identifica o domínio do usuário ou computador que está sendo autenticado.
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- Elemento LogonDomain EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008352"
---
# <a name="logondomain-eaptype-element"></a>Elemento LogonDomain (EapType)

O elemento **LogonDomain (EapType)** identifica o domínio do usuário ou computador que está sendo autenticado.

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

O elemento **LogonDomain** é definido pelo elemento [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Comentários

Se o elemento **LogonDomain (EapType)** não estiver presente, o domínio do Winlogon será usado. Esse elemento é opcional.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





