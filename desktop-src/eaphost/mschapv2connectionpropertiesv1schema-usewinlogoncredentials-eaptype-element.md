---
title: Elemento UseWinLogonCredentials (EapType)
description: Saiba mais sobre o elemento UseWinLogonCredentials (EapType). Esse elemento controla o uso de credenciais Winlogin.
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
ms.openlocfilehash: f17520d4eaee64d3dd9809ecb465ca8e39690fc4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641867"
---
# <a name="usewinlogoncredentials-eaptype-element"></a>Elemento UseWinLogonCredentials (EapType)

O elemento **UseWinLogonCredentials (EapType)** controla o uso das credenciais Winlogin.

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

O elemento **UseWinLogonCredentials** é definido pelo elemento [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Comentários

Se for TRUE, o EAP MS-CHAPv2 obterá as credenciais do Winlogon. Se for FALSE, o EAP MS-CHAPv2 obterá as credenciais do usuário. O elemento **UseWinLogonCredentials (EapType)** é opcional.

## <a name="requirements"></a>Requisitos



| Função | Versões mínimas do sistema operacional com suporte |
|------|-------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

 

 





