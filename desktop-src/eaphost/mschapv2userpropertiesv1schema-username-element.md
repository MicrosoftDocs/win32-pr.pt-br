---
title: Elemento username (CHAP)
description: Saiba mais sobre o elemento username, que identifica o usuário que está sendo autenticado. Consulte um exemplo de sintaxe e exiba recursos adicionais disponíveis.
ms.assetid: 3dd12864-5e0a-492c-a2c3-28118d21a0f2
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
ms.openlocfilehash: 29065a59e150d2a4295e91b41862250d58e017b5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917678"
---
# <a name="username-element-chap"></a>Elemento username (CHAP)

O elemento **username** identifica o usuário que está sendo autenticado.

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="remarks"></a>Comentários

Se o elemento **username** não estiver presente, o nome de usuário será obtido do Winlogon. Esse elemento é opcional.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





