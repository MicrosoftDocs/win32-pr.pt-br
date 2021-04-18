---
title: Método Query. beginNextGroup
description: O método beginNextGroup inicia um novo grupo de condição. | Método Query. beginNextGroup
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- método beginNextGroup Windows Media Player
- método beginNextGroup Windows Media Player, classe de consulta
- Classe de consulta Windows Media Player, método beginNextGroup
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
ms.openlocfilehash: 46c043b9a0ea506e054877b4d8122304ced75e28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814084"
---
# <a name="querybeginnextgroup-method"></a>Método Query. beginNextGroup

O método **beginNextGroup** inicia um novo grupo de condição.

## <a name="syntax"></a>Sintaxe


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

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

 

 





