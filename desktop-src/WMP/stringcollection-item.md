---
title: Método StringCollection. Item
description: O método item recupera a cadeia de caracteres no índice especificado.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- método de item Windows Media Player
- método de item Windows Media Player, classe StringCollection
- Classe StringCollection Windows Media Player, método item
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4244ad194ff3426dab81baddc0b7188214e0360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780335"
---
# <a name="stringcollectionitem-method"></a>Método StringCollection. Item

O método **Item** recupera a cadeia de caracteres no índice especificado.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) que contém o índice.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma **cadeia de caracteres**.

## <a name="remarks"></a>Comentários

O objeto **StringCollection** é usado para recuperar o conjunto de valores disponíveis para um atributo. Por exemplo, a *mediacollection*. o método **getAttributeStringCollection** pode ser usado para recuperar um objeto **StringCollection** que representa todos os valores do atributo gênero dentro do tipo de mídia de áudio. A propriedade **Item** pode então ser usada para iterar por todos os valores possíveis para o atributo gênero.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Mediacollection. getAttributeStringCollection**](mediacollection-getattributestringcollection.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**Objeto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





