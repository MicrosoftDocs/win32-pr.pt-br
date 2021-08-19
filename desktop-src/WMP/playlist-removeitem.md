---
title: Método playlist. removeItem
description: O método removeItem remove o item especificado da lista de reprodução.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- método removeItem Windows Media Player
- método removeItem Windows Media Player, classe Playlist
- classe Playlist Windows Media Player, método removeItem
topic_type:
- apiref
api_name:
- Playlist.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8a55fb45fa7ea8d172d76321d7c907fbedfd3f868448f1ad63e220ff8e69f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336587"
---
# <a name="playlistremoveitem-method"></a>Método playlist. removeItem

O método **RemoveItem** remove o item especificado da lista de reprodução.

## <a name="syntax"></a>Sintaxe


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Item* \[ de no\]
</dt> <dd>

Objeto de **mídia** a ser removido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o item removido for a faixa em execução no momento (*Player*.**currentMedia**), a reprodução é interrompida e o próximo item na playlist se torna o atual. Se não houver nenhum item seguinte, o item anterior será usado, ou se não houver outros itens, então o *Player*. **currentMedia** é definido como **NULL**.

Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> <dt>

[**Playlist. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Lista de reprodução. Item**](playlist-item.md)
</dt> <dt>

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





