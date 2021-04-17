---
title: Método StringCollection. getItemInfo
description: O método getItemInfo recupera a cadeia de caracteres correspondente ao índice e nome do item StringCollection especificado.
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- método getItemInfo Windows Media Player
- método getItemInfo Windows Media Player, classe StringCollection
- Classe StringCollection Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- StringCollection.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9552dcebbc7d565ebc797c62ac3bc00ee109fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812233"
---
# <a name="stringcollectiongetiteminfo-method"></a>Método StringCollection. getItemInfo

O método **getItemInfo** recupera a cadeia de caracteres correspondente ao índice e nome do item **StringCollection** especificado.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) especificando o índice de base zero do item **StringCollection** do qual obter o atributo.

</dd> <dt>

*nome* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do atributo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma **cadeia de caracteres** que representa o valor do atributo especificado. Para atributos cujo valor subjacente é **booliano**, ele retorna a cadeia de caracteres "true" ou "false".

## <a name="remarks"></a>Comentários

Para recuperar atributos com vários valores e atributos com valores complexos, use o método **getItemInfoByType** .

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**StringCollection. getItemInfoByType**](stringcollection-getiteminfobytype.md)
</dt> <dt>

[**Objeto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





