---
title: Elemento UseWinLogonCredentials (EapType)
description: Saiba mais sobre o elemento UseWinLogonCredentials (EapType). Esse elemento controla o uso de credenciais winlogin.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- Elemento UseWinLogonCredentials EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2a407c505139562a155e5aa9d7ed57fed5d15077cf5d035ea8bb7bbe0e177363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086187"
---
# <a name="usewinlogoncredentials-eaptype-element"></a>Elemento UseWinLogonCredentials (EapType)

O **elemento UseWinLogonCredentials (EapType)** controla o uso das credenciais do winlogin.

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

O **elemento UseWinLogonCredentials** é definido pelo [**elemento EapType.**](mschapv2connectionpropertiesv1schema-eaptype-element.md)

## <a name="remarks"></a>Comentários

Se TRUE, o EAP MS-CHAPv2 obtém credenciais do winlogon. Se FALSE, o EAP MS-CHAPv2 obtém credenciais do usuário. O **elemento UseWinLogonCredentials (EapType)** é opcional.

## <a name="requirements"></a>Requisitos



| Função | Versões mínimas do sistema operacional com suporte |
|------|-------------------------------|
| Cliente<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





