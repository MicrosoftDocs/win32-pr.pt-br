---
title: Método PlaylistArray. Item
description: O método item recupera a lista de reprodução no índice fornecido.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- método de item Windows Media Player
- método de item Windows Media Player, classe PlaylistArray
- Classe PlaylistArray do Windows Media Player, método de item
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6144f6e1cfda93be32060e8206a96b0da7568d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771650"
---
# <a name="playlistarrayitem-method"></a>Método PlaylistArray. Item

O método **Item** recupera a lista de reprodução no índice fornecido.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) que contém o índice da lista de reprodução a ser recuperada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto **playlist** .

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





