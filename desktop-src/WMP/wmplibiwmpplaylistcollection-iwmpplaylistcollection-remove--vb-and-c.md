---
title: Método de remoção de IWMPPlaylistCollection
description: O método remove remove uma lista de reprodução da biblioteca. | Método de remoção de IWMPPlaylistCollection
ms.assetid: 40c8ee1d-13fa-40d9-9532-4dc8383c4eb3
keywords:
- remover método Windows Media Player
- método de remoção do Windows Media Player, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection Windows Media Player, remover método
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99fbaa2f60c769599bd6173b8e38f4d99e9f42d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812291"
---
# <a name="iwmpplaylistcollectionremove-method"></a>Método IWMPPlaylistCollection:: Remove

O método **Remove** remove uma lista de reprodução da biblioteca.

## <a name="syntax"></a>Sintaxe


```CSharp
public void remove(
  IWMPPlaylist pItem
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPPlaylist _
)
Implements IWMPPlaylistCollection.remove
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pItem* \[ no\]
</dt> <dd>

Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução que será removida por este método.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





