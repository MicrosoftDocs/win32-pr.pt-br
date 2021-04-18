---
title: Método playlist. insertItem
description: O método insertItem insere um item de mídia na lista de reprodução no local especificado.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- método insertItem Windows Media Player
- método insertItem Windows Media Player, classe playlist
- Classe playlist Windows Media Player, método insertItem
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a456b7a359d59958ce7693cc48c16eabba435621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813649"
---
# <a name="playlistinsertitem-method"></a>Método playlist. insertItem

O método **insertItem** insere um item de mídia na lista de reprodução no local especificado.

## <a name="syntax"></a>Sintaxe


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) que contém o índice no qual adicionar o item.

</dd> <dt>

*Item* \[ de no\]
</dt> <dd>

Objeto de **mídia** a ser inserido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Todos os itens após o item inserido terão seus números de índice aumentados em um.

Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> <dt>

[**Lista de reprodução. Item**](playlist-item.md)
</dt> <dt>

[**Playlist. removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





