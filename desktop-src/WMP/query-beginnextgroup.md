---
title: Método Query. beginNextGroup
description: O método beginNextGroup inicia um novo grupo de condição. | Método Query. beginNextGroup
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- Windows Media Player do método beginNextGroup
- Windows Media Player do método beginNextGroup, classe de consulta
- classe de consulta Windows Media Player, método beginNextGroup
topic_type:
- apiref
api_name:
- Query.beginNextGroup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d12f8e37c32b83afb3e518deda09643033c7f396d8c52a2898893a01dc930d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861846"
---
# <a name="querybeginnextgroup-method"></a>Método Query. beginNextGroup

O método **beginNextGroup** inicia um novo grupo de condição.

## <a name="syntax"></a>Sintaxe


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Iniciar um novo grupo de condição implica que você concluiu o grupo de condições atual. O novo grupo de condição sempre é concatenado ao grupo de condições anterior usando ou lógica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Mediacollection. createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**Mediacollection. getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Mediacollection. getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Objeto de consulta**](query-object.md)
</dt> <dt>

[**Consulta. addcondition**](query-addcondition.md)
</dt> </dl>

 

 





