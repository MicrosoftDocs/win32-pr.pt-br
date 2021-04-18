---
title: Método playlist. moveItem
description: O método moveItem altera o local de um item na lista de reprodução.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- método moveItem Windows Media Player
- método moveItem Windows Media Player, classe playlist
- Classe playlist Windows Media Player, método moveItem
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812180"
---
# <a name="playlistmoveitem-method"></a>Método playlist. moveItem

O método **moveItem** altera o local de um item na lista de reprodução.

## <a name="syntax"></a>Sintaxe


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*oldIndex* \[ no\]
</dt> <dd>

**Número** (**longo**) que contém o índice antigo.

</dd> <dt>

*NewIndex* \[ no\]
</dt> <dd>

**Número** (**longo**) que contém o novo índice.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

As listas de reprodução armazenadas na biblioteca podem ser alteradas fora do seu controle. Certifique-se de monitorar e lidar com todos os eventos relacionados à playlist apropriados para que a ordem dos itens na lista de reprodução não mude inesperadamente.

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

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





