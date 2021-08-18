---
title: Método Playlist.insertItem
description: O método insertItem insere um item de mídia na playlist no local especificado.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- Método insertItem Windows Media Player
- Método insertItem Windows Media Player , classe Playlist
- Classe de playlist Windows Media Player , método insertItem
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
ms.openlocfilehash: 7a71d9ceb39b29c1627ea7596166c39b3dc2f6c76faf45e5ffb54bea14154ac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995696"
---
# <a name="playlistinsertitem-method"></a>Método Playlist.insertItem

O **método insertItem** insere um item de mídia na playlist no local especificado.

## <a name="syntax"></a>Sintaxe


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ Em\]
</dt> <dd>

**Número** (**longo**) que contém o índice no qual adicionar o item.

</dd> <dt>

*item* \[ Em\]
</dt> <dd>

**Objeto de** mídia a ser inserido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Todos os itens após o item inserido terão seus números de índice aumentados em um.

Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Playlist.removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





