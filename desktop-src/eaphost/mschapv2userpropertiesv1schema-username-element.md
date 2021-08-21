---
title: Elemento Username (CHAP)
description: Saiba mais sobre o elemento Username, que identifica o usuário que está sendo autenticado. Consulte um exemplo de sintaxe e ex veja os recursos disponíveis adicionais.
ms.assetid: 3dd12864-5e0a-492c-a2c3-28118d21a0f2
keywords:
- Elemento Username EAPHost
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
ms.openlocfilehash: d9ad861388ba8e15bb0df924610e6df1f833968794101cb1b04ccc47fb5ae541
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086150"
---
# <a name="username-element-chap"></a>Elemento Username (CHAP)

O **elemento Username** identifica o usuário que está sendo autenticado.

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="remarks"></a>Comentários

Se o **elemento Username** não estiver presente, o nome de usuário será obtido do winlogon. Esse elemento é opcional.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





