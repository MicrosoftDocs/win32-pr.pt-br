---
title: EFFECTs. allowAll
description: O atributo allowAll especifica ou recupera um valor que indica se todas as visualizações que estão no registro devem ser incluídas.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- EFFECTs. allowAll Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7a87aa8336e3961b31716c8d6bbfaa6aee71374a0f3c6e17b644a47136df550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996837"
---
# <a name="effectsallowall"></a>EFFECTs. allowAll

O atributo **allowAll** especifica ou recupera um valor que indica se todas as visualizações que estão no registro devem ser incluídas.

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                                                         |
|-------|---------------------------------------------------------------------|
| true  | Padrão. Permite o ciclo de todas as visualizações no sistema do usuário. |
| false | Limita o ciclo às visualizações que aparecem dentro das marcas de **efeitos** . |



 

## <a name="remarks"></a>Comentários

Se esse atributo for definido como false, somente as visualizações que aparecem dentro de marcas de **efeitos** podem ser alternadas usando Previous/avançar. Se estiver definido como true, todas as visualizações registradas no sistema do usuário poderão ser alternadas pelo. Se ele for definido como true e você especificar quaisquer visualizações dentro de marcas de **efeitos** , os atributos especificados nessas marcas serão aplicados a todas as visualizações no sistema do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EFFECTs**](effects-element.md)
</dt> </dl>

 

 





